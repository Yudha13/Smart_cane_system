# Initial Bill of Materials

**Status:** Candidate categories only. No exact model or price is approved.

| Subsystem | Candidate | Selection/verification required | Status |
|---|---|---|---|
| Field compute | Raspberry Pi 4B (RAM variant TBD) | Confirm board, workload, supply and thermal limits | ASSUMPTION |
| Storage | USB 3 SSD, 256 GB starting assumption | Endurance, power, retention and capacity sizing | ASSUMPTION |
| Gateway | SX1302 multi-channel concentrator/HAT or external gateway | Exact SKU, Pi compatibility, software, RF region, antenna | NEEDS VERIFICATION |
| Weather interface | Isolated USB-RS485 adapter | Isolation, driver, terminal and surge details | RECOMMENDED |
| Uplink | 4G LTE modem/router | Carrier bands, SIM/APN, antenna, Linux support, peak current | NEEDS VERIFICATION |
| Timekeeping | RTC module | Model, backup cell, driver, drift | NEEDS VERIFICATION |
| Power | Regulated PSU and UPS | Measured peak load and required hold-up time | NEEDS VERIFICATION |
| Enclosure/cooling | Active cooling and weatherproof enclosure | Heat, condensation, UV, ingress and service access | NEEDS VERIFICATION |
| Soil node MCU | ESP32 family board/module | Exact variant, sleep current, antenna and certification | NEEDS VERIFICATION |
| Soil radio | SX1262-based module candidate | Regional configuration, RF layout, interface documentation | RECOMMENDED |
| Soil probes | Moisture, temperature, pH, EC | Accuracy, soil suitability, output interface, calibration | BLOCKER |
| Weather sensors | Temperature/RH, rain, wind, solar, pressure | Models, mounting, interface, accuracy and calibration | BLOCKER |
| Node power | Battery and optional solar | Sampling interval, link budget, autonomy and load profile | NEEDS VERIFICATION |

Do not add prices without exact SKU, supplier, currency, location, and quote date. Do not order from this preliminary list.
