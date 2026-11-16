# Risk Register

| ID | Risk | Mitigation / evidence needed | Status |
|---|---|---|---|
| R-001 | Incorrect Indonesian LoRaWAN regional plan | Verify current Indonesian RF rules before configuration | BLOCKER |
| R-002 | Network server depends on WAN | Decide local/hybrid topology and prove outage operation | BLOCKER |
| R-003 | Incompatible concentrator, Pi and gateway software | Exact SKU/interface/driver/OS compatibility test | OPEN |
| R-004 | Sensor signal mismatches host interface | Datasheet-based conditioning/isolation and bench test | OPEN |
| R-005 | Soil-probe calibration drift | Sensor selection, calibration and reference checks | OPEN |
| R-006 | Power interruption or corruption | UPS sizing, durable writes, recovery and backup tests | OPEN |
| R-007 | Storage wear/capacity | Workload sizing, endurance, monitoring and retention | OPEN |
| R-008 | Duplicate/reordered sync events | Transactional outbox, idempotency and fault injection | OPEN |
| R-009 | Exposed database or leaked credentials | Network isolation, TLS, secrets, firewall and access review | OPEN |
| R-010 | Enclosure, condensation, lightning or surge | Environmental design, grounding, protection and field tests | OPEN |
