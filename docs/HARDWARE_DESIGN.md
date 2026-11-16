# Hardware Design

**Status:** Requirements and interface strategy only. No wiring is approved.

Verify exact manufacturer/model/revision, supply range, current draw, logic levels, pinout, connector, environmental rating, and primary documentation before giving model-specific instructions. Design power, grounding, surge protection, isolation, shielding, cable, and enclosure for field exposure.

- Raspberry Pi has no native ADC. Analog sensors require an external ADC and signal conditioning.
- Do not connect 5 V signals to 3.3 V-only GPIO without a verified interface.
- RS485/Modbus: verify register map, baud/parity, termination, biasing, isolation, topology, and surge protection.
- Pulse sensors: determine voltage/current, maximum frequency, filtering, and protected input design.
- I2C: keep wiring short and controlled unless extension is engineered.
- ESP32 node: account for radio, antenna, sensor connectors, ADC front ends, battery measurement, charging, low-power modes, corrosion, cable length, calibration, and enclosure.

Initial Pi, SSD, SX1302, RS485, LTE, RTC, UPS, cooling, and enclosure assumptions are not compatibility proof. No pin allocation, wire size, fuse, battery capacity, or protection component is final until parts and loads are known.
