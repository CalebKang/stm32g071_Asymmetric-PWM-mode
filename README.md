# stm32g071_Asymmetric-PWM-mode

1. OC1PE, OC3PE Enable

TIM1->CCMR1 = TIM1->CCMR1 | 0x08; // OC1PE = 1로 셋팅
TIM1->CCMR2 = TIM1->CCMR2 | 0x08; // OC3PE = 1로 셋팅

2. Asymmetric PWM은Up-counting, Down-counting 때 두개의 CCR로 Phase shift하는 모드로 Counter mode = Center aligned
 
3. Asymmetric PWM에서 Asymmetric PWM1과 Asymmetric PWM2의 차이점.

  1) Asymmetric PWM1 : 
    Upcounting 일 경우 Counter < CCR 일 경우 Active 그 외는 Inactive.
    Donwncounting 일 경우 Counter > CCR 일 경우 Inactive 그 외는 Active.

  2) Asymmetric PWM2 : 
    Upcounting 일 경우 Counter < CCR 일 경우 Inactive 그 외는 Active.
    Donwncounting 일 경우 Counter > CCR 일 경우 Active 그 외는 Inactive.


