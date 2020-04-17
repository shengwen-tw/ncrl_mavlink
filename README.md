# NCRL MAVLink

A MAVLink dialect extended by NCRL (Networked Control Robotics Lab)

## Instruction for generating C header files

```
git clone https://github.com/ArduPilot/pymavlink.git

python ./pymavlink/tools/mavgen.py --lang=C --wire-protocol=2.0 --output=generated/include/mavlink/v2.0 message_definitions/ncrl.xml
```

## Extended messages

**polynomial_trajectory_write**

  * uint8_t target_system
  * uint8_t target_component
  * uint8_t list_size

**polynomial_trajectory_cmd**

  * uint8_t target_system
  * uint8_t target_component
  * uint8_t cmd

**polynomial_trajectory_ack**

  * uint8_t target_system
  * uint8_t target_component
  * uint8_t ack_val

**polynomial_trajectory_item**

  * uint8_t target_system
  * uint8_t target_component
  * float[8] x_coeff
  * float[8] y_coeff
  * float[8] z_coeff
  * float[8] yaw_coeff

## Extended enums

**polynomial_trajectory_cmd_types**

trajectory_following_start: 0

trajectory_following_stop: 1

**polynomial_trajectory_ack_values**

trajectory_ack_ok: 0

trajectory_ack_error: 1
