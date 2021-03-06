# 수동 모드(고정 날개)

<!-- this requires review -->

[<img src="../../assets/site/difficulty_hard.png" title="Hard to fly" width="30px" />](../getting_started/flight_modes.md#key_difficulty)&nbsp;[<img src="../../assets/site/remote_control.svg" title="Manual/Remote control required" width="30px" />](../getting_started/flight_modes.md#key_manual)&nbsp;

* Manual mode(수동 모드) *은 RC 스틱 입력을 출력 믹서에 직접 전송하여 완전한 수동 제어를 제공합니다

:::tip
This is the hardest mode to fly, because nothing is stabilized. Unlike [Acro Mode](../flight_modes/acro_fw.md) if the RP stick is centered the vehicle will not automatically stop rotating around the axis; the pilot actually has to move the stick to apply force in the other direction.
:::

:::note
This is the only mode that overrides the FMU (commands are sent via the safety coprocessor). It provides a safety mechanism that allows full control of throttle, elevator, ailerons and rudder via RC in the event of an FMU firmware malfunction.
:::

## Technical Description

RC mode where stick input is sent directly to the output mixer (for "fully" manual control).

This is the only mode that overrides the FMU (commands are sent via the safety coprocessor). It provides a safety mechanism that allows full control of throttle, elevator, ailerons and rudder via RC in the event of an FMU firmware malfunction.

## Parameters

| Parameter                                                                                       | Description                                                                                                                              |
| ----------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| <span id="FW_MAN_P_SC"></span>[FW_MAN_P_SC](../advanced_config/parameter_reference.md#FW_MAN_P_SC) | 수동 피치 스케일. 전체 수동 모드에서 원하는 피치 액추에이터 명령에 적용되는 스케일 팩터. This parameter allows to adjust the throws of the control surfaces. 기본값: 1.0 표준.     |
| <span id="FW_MAN_R_SC"></span>[FW_MAN_R_SC](../advanced_config/parameter_reference.md#FW_MAN_R_SC) | 수동 롤 스케일. 전체 수동 모드에서 원하는 롤 액추에이터 명령에 적용되는 스케일 팩터. This parameter allows to adjust the throws of the control surfaces. Default: 1.0 norm. |
| <span id="FW_MAN_Y_SC"></span>[FW_MAN_Y_SC](../advanced_config/parameter_reference.md#FW_MAN_Y_SC) | 수동 요 스케일. 전체 수동 모드에서 원하는 요 액츄에이터 명령에 적용되는 스케일 계수. This parameter allows to adjust the throws of the control surfaces. Default: 1.0 norm. |