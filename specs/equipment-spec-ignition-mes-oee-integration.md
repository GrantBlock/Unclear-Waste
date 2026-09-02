# Equipment Specification — Ignition MES / OEE Integration Readiness

Use this as an RFQ/spec boilerplate section for new or retrofit equipment that must integrate
with an Inductive Automation Ignition platform for MES and OEE (Overall Equipment
Effectiveness) reporting. Attach it to a machine RFQ or hand it to a vendor as a checklist.

## 1. Connectivity

- Controller/PLC must expose an Ethernet port with one of the following:
  - Native OPC UA server, **or**
  - A protocol natively supported by Ignition's drivers: EtherNet/IP (Allen-Bradley CIP),
    S7comm (Siemens), or Modbus TCP/RTU as a fallback for simpler controllers.
- Static IP address or a reserved DHCP lease on the plant automation network/VLAN. Serial-only
  interfaces (RS-232/RS-485) are not acceptable unless paired with a serial-to-Ethernet gateway
  supplied as part of the machine package.
- If the machine's onboard controller cannot host OPC UA (e.g., relay logic, legacy PLC,
  or a vendor-locked controller with no open protocol), the equipment must include an
  on-machine edge device (Ignition Edge, industrial PC, or protocol gateway) that:
  - Bridges the machine's native I/O/protocol to OPC UA or a Ignition-supported driver.
  - Supports store-and-forward buffering so a temporary network outage does not lose
    production/downtime data.

## 2. Signals and Tags Required for OEE (Availability × Performance × Quality)

| Factor | Required Tag/Signal | Notes |
|---|---|---|
| Availability | Run/Idle state | Discrete bit or state code indicating the machine is actively cycling vs. stopped |
| Availability | Fault/alarm code | Discrete **reason code**, not just a generic fault bit — feeds Ignition's Downtime/OEE module reason tracking |
| Performance | Cycle-complete / part-count pulse | From an encoder, photoeye, or PLC-generated pulse; must not be missed at max machine speed |
| Performance | Ideal cycle time | Fixed spec value or a live tag if it varies by product/recipe |
| Quality | Good count | Total accepted parts |
| Quality | Reject/scrap count or quality-gate signal | Total rejected parts, or a pass/fail gate signal per part |

## 3. MES-Specific Data

- Current product/recipe/work-order ID tag, if work orders must be tracked against a
  specific job or SKU.
- Operator ID/badge input, if labor tracking or operator attribution is in scope.
- Changeover/setup state signal, if changeover time is tracked separately from unplanned downtime.

## 4. Timing and Data Rate

- PLC clock synced via NTP (or accepts an NTP source) to avoid timestamp drift against the
  Ignition Gateway and historian.
- Tag update rate fast enough to avoid missed counts — sub-second to 1-second scan/update
  rate is typical for count and state tags.

## 5. Security

- OPC UA endpoint must support authentication (username/password or certificate-based)
  if required by plant security policy. Anonymous/unsecured endpoints should be disabled
  in production.

## 6. Vendor Documentation Deliverables

The equipment vendor must supply, prior to acceptance:

- A complete I/O list.
- A documented tag/point list mapping each required signal (Section 2 and 3) to its
  protocol address or OPC UA node ID.
- Communication driver/protocol documentation (firmware version, supported drivers,
  licensing requirements for OPC UA if applicable).
- A network drawing showing how the machine connects to the plant network (IP scheme,
  switch/port, any gateway or edge device).

This documentation set — not the choice of protocol alone — is what determines actual
integration cost and timeline, so it should be requested and reviewed as part of the
quote, not left until commissioning.
