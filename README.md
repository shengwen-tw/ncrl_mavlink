# NCRL MAVLink

A MAVLink dialect extended by NCRL (Networked Control Robotics Lab)

## Instruction for generating C header files

```
git clone https://github.com/ArduPilot/pymavlink.git

python ./pymavlink/tools/mavgen.py --lang=C --wire-protocol=2.0 --output=generated/include/mavlink/v2.0 message_definitions/ncrl.xml
```

## Extended messages

1. polynomial_trajectory_write

2. polynomial_trajectory_cmd

3. polynomial_trajectory_ack

4. polynomial_trajectory_item

## Extended enums

**POLYNOMIAL_TRAJECTORY_CMD_TYPES**

TRAJECTORY_FOLLOWING_START: 0

TRAJECTORY_FOLLOWING_STOP: 1

**POLYNOMIAL_TRAJECTORY_ACK_VALUES**

TRAJECTORY_ACK_OK: 0

TRAJECTORY_ACK_ERROR: 1

