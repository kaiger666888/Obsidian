# Irq

## 模块描述

Configuration of the Irq module.

## 容器列表

### 1. IrqGeneral

**描述**: Interrupt Module global settings and module specific settings are present in this container

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqOsekEnable
  长名称: ''
  描述: Parameter to identify the use of OS. This controls the available configuration options for
      Interrupt Category.
  默认值: false
  最小值: ''
  最大值: ''
```

### 2. IrqGPT120Config

**描述**: This container contains the GPT120 module interrupt nodes configuration parameters.

该容器没有参数。

### 3. IrqGPT120CatConfig

**描述**: This container contains parameters to configure the interrupt category of all SRN supported by
GPT120 module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_GPT120CIRQ_Cat
  长名称: ''
  描述: The interrupt category setting of GPT120_CIRQ SRN.                             Depending upon
      the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: Irq_GPT120T2_Cat
  长名称: ''
  描述: The interrupt category setting of GPT120_T2 SRN.                             Depending upon
      the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: Irq_GPT120T3_Cat
  长名称: ''
  描述: The interrupt category setting of GPT120_T3 SRN.                             Depending upon
      the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: Irq_GPT120T4_Cat
  长名称: ''
  描述: The interrupt category setting of GPT120_T4 SRN.                             Depending upon
      the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: Irq_GPT120T5_Cat
  长名称: ''
  描述: The interrupt category setting of GPT120_T5 SRN.                             Depending upon
      the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: Irq_GPT120T6_Cat
  长名称: ''
  描述: The interrupt category setting of GPT120_T6 SRN.                             Depending upon
      the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 4. IrqGPT120PrioConfig

**描述**: This container contains the parameter to configure the priority of all the SRN supported by GPT120
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_GPT120CIRQ_Prio
  长名称: ''
  描述: The interrupt priority setting of GPT120_CIRQ of GPT120 Module.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: Irq_GPT120T2_Prio
  长名称: ''
  描述: The interrupt priority setting of GPT120_T2 of GPT120 Module.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: Irq_GPT120T3_Prio
  长名称: ''
  描述: The interrupt priority setting of GPT120_T3 of GPT120 Module.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: Irq_GPT120T4_Prio
  长名称: ''
  描述: The interrupt priority setting of GPT120_T4 of GPT120 Module.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: Irq_GPT120T5_Prio
  长名称: ''
  描述: The interrupt priority setting of GPT120_T5 of GPT120 Module.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: Irq_GPT120T6_Prio
  长名称: ''
  描述: The interrupt priority setting of GPT120_T6 of GPT120 Module.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 5. IrqGPT120TosConfig

**描述**: This container contains the parameter to configure the type of service providers of all SRN
supported by GPT120 module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_GPT120CIRQ_Tos
  长名称: ''
  描述: The interrupt type of service provider setting of GPT120_CIRQ of GPT120 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: Irq_GPT120T2_Tos
  长名称: ''
  描述: The interrupt type of service provider setting of GPT120_T2 of GPT120 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: Irq_GPT120T3_Tos
  长名称: ''
  描述: The interrupt type of service provider setting of GPT120_T2 of GPT120 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: Irq_GPT120T4_Tos
  长名称: ''
  描述: The interrupt type of service provider setting of GPT120_T2 of GPT120 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: Irq_GPT120T5_Tos
  长名称: ''
  描述: The interrupt type of service provider setting of GPT120_T2 of GPT120 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: Irq_GPT120T6_Tos
  长名称: ''
  描述: The interrupt type of service provider setting of GPT120_T2 of GPT120 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 6. IrqQSPIConfig

**描述**: This container contains the QSPI module interrupt nodes configuration parameters.

该容器没有参数。

### 7. IrqQspiCatConfig

**描述**: This container contains parameters to configure the interrupt category of all SRN supported by QSPI
module.

该容器没有参数。

### 8. IrqQspiTxCatConfig

**描述**: This container contains the parameter to configure the category of all the Transmit SRN supported by
Qspi module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqQspi0TxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNTx of Qspi0 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqQspi1TxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNTx of Qspi1 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqQspi2TxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNTx of Qspi2 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqQspi3TxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNTx of Qspi3 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: IrqQspi4TxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNTx of Qspi4 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: IrqQspi5TxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNTx of Qspi5 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 9. IrqQspiRxCatConfig

**描述**: This container contains the parameter to configure the category of all the Receive SRN supported by
Qspi module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqQspi0RxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNRx of Qspi0 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqQspi1RxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNRx of Qspi1 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqQspi2RxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNRx of Qspi2 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqQspi3RxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNRx of Qspi3 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: IrqQspi4RxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNRx of Qspi4 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: IrqQspi5RxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNRx of Qspi5 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 10. IrqQspiErrCatConfig

**描述**: This container contains the parameter to configure the category of all the Error SRN supported by
Qspi module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqQspi0ErrCat
  长名称: ''
  描述: |
    The interrupt category setting of SRN Err of Qspi0 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqQspi1ErrCat
  长名称: ''
  描述: |
    The interrupt category setting of SRN Err of Qspi1 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqQspi2ErrCat
  长名称: ''
  描述: |
    The interrupt category setting of SRN Err of Qspi2 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqQspi3ErrCat
  长名称: ''
  描述: |
    The interrupt category setting of SRN Err of Qspi3 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: IrqQspi4ErrCat
  长名称: ''
  描述: |
    The interrupt category setting of SRN Err of Qspi4 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: IrqQspi5ErrCat
  长名称: ''
  描述: |
    The interrupt category setting of SRN Err of Qspi5 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 11. IrqQspiPTCatConfig

**描述**: This container contains the parameter to configure the category of all the Phase Transition SRN
supported by Qspi module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqQspi0PTCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNPT of Qspi0 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqQspi1PTCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNPT of Qspi1 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqQspi2PTCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNPT of Qspi2 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqQspi3PTCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNPT of Qspi3 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: IrqQspi4PTCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNPT of Qspi4 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: IrqQspi5PTCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNPT of Qspi5 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 12. IrqQspiHCCatConfig

**描述**: This container contains the parameter to configure the category of all the Half Cycle SRN supported
by Qspi module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqQspi2HCCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNHC of Qspi2 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqQspi3HCCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNHC of Qspi3 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 13. IrqQspiUDCatConfig

**描述**: This container contains the parameter to configure the category of all the User Defined SRN
supported by Qspi module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqQspi0UDCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNU of Qspi0 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqQspi1UDCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNU of Qspi1 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqQspi2UDCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNU of Qspi2 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqQspi3UDCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNU of Qspi3 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: IrqQspi4UDCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNU of Qspi4 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: IrqQspi5UDCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNU of Qspi5 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 14. IrqQspiPrioConfig

**描述**: This container contains the parameter to configure the priority of all the SRN supported by Qspi
module.

该容器没有参数。

### 15. IrqQspiTxPrioConfig

**描述**: This container contains the parameter to configure the priority of all the Transmit SRN supported by
Qspi module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqQspi0TxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNTx of Qspi0.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqQspi1TxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNTx of Qspi1.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: IrqQspi2TxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNTx of Qspi2.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: IrqQspi3TxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNTx of Qspi3.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: IrqQspi4TxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNTx of Qspi4.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: IrqQspi5TxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNTx of Qspi5.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 16. IrqQspiRxPrioConfig

**描述**: This container contains the parameter to configure the priority of all the Receive SRN supported by
Qspi module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqQspi0RxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNRx of AscLin0.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqQspi1RxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNRx of AscLin1.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: IrqQspi2RxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNRx of AscLin2.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: IrqQspi3RxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNRx of AscLin3.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: IrqQspi4RxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNRx of AscLin4.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: IrqQspi5RxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNRx of AscLin5.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 17. IrqQspiErrPrioConfig

**描述**: This container contains the parameter to configure the priority of all the Error SRN supported by
Qspi module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqQspi0ErrPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN Error of Qspi0.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqQspi1ErrPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN Error of Qspi1.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: IrqQspi2ErrPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN Error of Qspi2.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: IrqQspi3ErrPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN Error of Qspi3.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: IrqQspi4ErrPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN Error of Qspi4.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: IrqQspi5ErrPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN Error of Qspi5.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 18. IrqQspiPTPrioConfig

**描述**: This container contains the parameter to configure the priority of all the Phase Transmission SRN
supported by Qspi module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqQspi0PTPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNPT of Qspi0.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqQspi1PTPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNPT of Qspi1.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: IrqQspi2PTPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNPT of Qspi2.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: IrqQspi3PTPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNPT of Qspi3.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: IrqQspi4PTPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNPT of Qspi4.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: IrqQspi5PTPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNPT of Qspi5.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 19. IrqQspiHCPrioConfig

**描述**: This container contains the parameter to configure the priority of all the Half Cycle SRN supported
by Qspi module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqQspi2HCPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNHC of Qspi2.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqQspi3HCPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNHC of Qspi3.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 20. IrqQspiUDPrioConfig

**描述**: This container contains the parameter to configure the priority of all the User Defined SRN
supported by Qspi module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqQspi0UDPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNUD of Qspi0.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqQspi1UDPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNUD of Qspi1.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: IrqQspi2UDPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNUD of Qspi2.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: IrqQspi3UDPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNUD of Qspi3.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: IrqQspi4UDPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNUD of Qspi4.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: IrqQspi5UDPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNUD of Qspi5.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 21. IrqQspiTosConfig

**描述**: This container contains the Qspi interrupt configuration parameters.

该容器没有参数。

### 22. IrqQspiTxTosConfig

**描述**: This container contains the parameter to configure the Type of service of all the Transmit SRN
supported by Qspi module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqQspi0TxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNTx of Qspi0 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqQspi1TxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNTx of Qspi1 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqQspi2TxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNTx of Qspi2 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqQspi3TxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNTx of Qspi3 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: IrqQspi4TxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNTx of Qspi4 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: IrqQspi5TxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNTx of Qspi5 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 23. IrqQspiRxTosConfig

**描述**: This container contains the parameter to configure the Type of service of all the Transmit SRN
supported by Qspi module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqQspi0RxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNRx of Qspi0 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqQspi1RxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNRx of Qspi1 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqQspi2RxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNRx of Qspi2 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqQspi3RxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNRx of Qspi3 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: IrqQspi4RxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNRx of Qspi4 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: IrqQspi5RxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNRx of Qspi5 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 24. IrqQspiErrTosConfig

**描述**: This container contains the parameter to configure the Type of service of all the Transmit SRN
supported by Qspi module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqQspi0ErrTos
  长名称: ''
  描述: The interrupt type of service setting of SRN Err of Qspi0 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqQspi1ErrTos
  长名称: ''
  描述: The interrupt type of service setting of SRN Err of Qspi1 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqQspi2ErrTos
  长名称: ''
  描述: The interrupt type of service setting of SRN Err of Qspi2 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqQspi3ErrTos
  长名称: ''
  描述: The interrupt type of service setting of SRN Err of Qspi3 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: IrqQspi4ErrTos
  长名称: ''
  描述: The interrupt type of service setting of SRN Err of Qspi4 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: IrqQspi5ErrTos
  长名称: ''
  描述: The interrupt type of service setting of SRN Err of Qspi5 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 25. IrqQspiPTTosConfig

**描述**: This container contains the parameter to configure the Type of service of all the Transmit SRN
supported by Qspi module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqQspi0PTTos
  长名称: ''
  描述: The intPTupt type of service setting of SRNPT of Qspi0 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqQspi1PTTos
  长名称: ''
  描述: The intPTupt type of service setting of SRNPT of Qspi1 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqQspi2PTTos
  长名称: ''
  描述: The intPTupt type of service setting of SRNPT of Qspi2 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqQspi3PTTos
  长名称: ''
  描述: The intPTupt type of service setting of SRNPT of Qspi3 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: IrqQspi4PTTos
  长名称: ''
  描述: The intPTupt type of service setting of SRNPT of Qspi4 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: IrqQspi5PTTos
  长名称: ''
  描述: The intPTupt type of service setting of SRNPT of Qspi5 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 26. IrqQspiHCTosConfig

**描述**: This container contains the parameter to configure the Type of service of all the Transmit SRN
supported by Qspi module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqQspi2HCTos
  长名称: ''
  描述: The intHCuHC type of service setting of SRNHC of Qspi2 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqQspi3HCTos
  长名称: ''
  描述: The intHCuHC type of service setting of SRNHC of Qspi3 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 27. IrqQspiUDTosConfig

**描述**: This container contains the parameter to configure the Type of service of all the Transmit SRN
supported by Qspi module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqQspi0UDTos
  长名称: ''
  描述: The intUDuUD type of service setting of SRNUD of Qspi0 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqQspi1UDTos
  长名称: ''
  描述: The intUDuUD type of service setting of SRNUD of Qspi1 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqQspi2UDTos
  长名称: ''
  描述: The intUDuUD type of service setting of SRNUD of Qspi2 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqQspi3UDTos
  长名称: ''
  描述: The intUDuUD type of service setting of SRNUD of Qspi3 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: IrqQspi4UDTos
  长名称: ''
  描述: The intUDuUD type of service setting of SRNUD of Qspi4 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: IrqQspi5UDTos
  长名称: ''
  描述: The intUDuUD type of service setting of SRNUD of Qspi5 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 28. IrqDmaConfig

**描述**: This container contains the Dma interrupt configuration parameters.

该容器没有参数。

### 29. IrqDmaCatConfig

**描述**: This container contains the parameter to configure the category of all the SRN supported by Dma
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqDmaErr0SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Error Service Reuest.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqDmaErr1SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Error Service Reuest.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqDmaErr2SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Error Service Reuest.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqDmaErr3SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Error Service Reuest.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: IrqDmaCh0SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 0 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: IrqDmaCh1SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 1 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: IrqDmaCh2SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 2 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: IrqDmaCh3SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 3 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: IrqDmaCh4SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 4 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: IrqDmaCh5SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 5 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: IrqDmaCh6SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 6 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: IrqDmaCh7SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 7 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: IrqDmaCh8SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 8 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: IrqDmaCh9SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 9 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: IrqDmaCh10SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 10 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: IrqDmaCh11SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 11 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 17
  名称: IrqDmaCh12SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 12 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 18
  名称: IrqDmaCh13SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 13 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 19
  名称: IrqDmaCh14SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 14 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 20
  名称: IrqDmaCh15SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 15 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 21
  名称: IrqDmaCh16SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA   Channel 16 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 22
  名称: IrqDmaCh17SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA   Channel 17 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 23
  名称: IrqDmaCh18SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA   Channel 18 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 24
  名称: IrqDmaCh19SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA   Channel 19 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 25
  名称: IrqDmaCh20SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA   Channel 20 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 26
  名称: IrqDmaCh21SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA   Channel 21 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 27
  名称: IrqDmaCh22SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA   Channel 22 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 28
  名称: IrqDmaCh23SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA   Channel 23 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 29
  名称: IrqDmaCh24SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA   Channel 24 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 30
  名称: IrqDmaCh25SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA   Channel 25 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 31
  名称: IrqDmaCh26SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA   Channel 26 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 32
  名称: IrqDmaCh27SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA   Channel 27 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 33
  名称: IrqDmaCh28SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA   Channel 28 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 34
  名称: IrqDmaCh29SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA   Channel 29 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 35
  名称: IrqDmaCh30SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA   Channel 30 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 36
  名称: IrqDmaCh31SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA   Channel 31 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 37
  名称: IrqDmaCh32SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA   Channel 32 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 38
  名称: IrqDmaCh33SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA   Channel 33 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 39
  名称: IrqDmaCh34SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA   Channel 34 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 40
  名称: IrqDmaCh35SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA   Channel 35 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 41
  名称: IrqDmaCh36SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA   Channel 36 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 42
  名称: IrqDmaCh37SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA   Channel 37 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 43
  名称: IrqDmaCh38SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA   Channel 38 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 44
  名称: IrqDmaCh39SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA   Channel 39 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 45
  名称: IrqDmaCh40SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA   Channel 40 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 46
  名称: IrqDmaCh41SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA   Channel 41 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 47
  名称: IrqDmaCh42SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA   Channel 42 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 48
  名称: IrqDmaCh43SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA   Channel 43 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 49
  名称: IrqDmaCh44SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA   Channel 44 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 50
  名称: IrqDmaCh45SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA   Channel 45 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 51
  名称: IrqDmaCh46SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA   Channel 46 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 52
  名称: IrqDmaCh47SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA   Channel 47 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 53
  名称: IrqDmaCh48SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA   Channel 48 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 54
  名称: IrqDmaCh49SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA   Channel 49 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 55
  名称: IrqDmaCh50SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA   Channel 50 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 56
  名称: IrqDmaCh51SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 51 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 57
  名称: IrqDmaCh52SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 52 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 58
  名称: IrqDmaCh53SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 53 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 59
  名称: IrqDmaCh54SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 54 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 60
  名称: IrqDmaCh55SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA   Channel 55 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 61
  名称: IrqDmaCh56SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 56 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 62
  名称: IrqDmaCh57SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 57 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 63
  名称: IrqDmaCh58SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 58 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 64
  名称: IrqDmaCh59SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 59 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 65
  名称: IrqDmaCh60SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 60 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 66
  名称: IrqDmaCh61SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 61 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 67
  名称: IrqDmaCh62SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 62 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 68
  名称: IrqDmaCh63SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 63 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 69
  名称: IrqDmaCh64SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 64 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 70
  名称: IrqDmaCh65SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 65 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 71
  名称: IrqDmaCh66SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 66 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 72
  名称: IrqDmaCh67SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 67 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 73
  名称: IrqDmaCh68SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 68 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 74
  名称: IrqDmaCh69SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 69 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 75
  名称: IrqDmaCh70SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 70 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 76
  名称: IrqDmaCh71SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 71 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 77
  名称: IrqDmaCh72SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 72 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 78
  名称: IrqDmaCh73SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 73 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 79
  名称: IrqDmaCh74SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 74 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 80
  名称: IrqDmaCh75SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 75 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 81
  名称: IrqDmaCh76SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 76 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 82
  名称: IrqDmaCh77SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 77 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 83
  名称: IrqDmaCh78SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 78 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 84
  名称: IrqDmaCh79SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 79 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 85
  名称: IrqDmaCh80SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 80 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 86
  名称: IrqDmaCh81SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 81 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 87
  名称: IrqDmaCh82SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 82 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 88
  名称: IrqDmaCh83SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 83 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 89
  名称: IrqDmaCh84SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 84 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 90
  名称: IrqDmaCh85SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 85 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 91
  名称: IrqDmaCh86SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 86 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 92
  名称: IrqDmaCh87SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 87 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 93
  名称: IrqDmaCh88SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 88 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 94
  名称: IrqDmaCh89SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 89 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 95
  名称: IrqDmaCh90SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 90 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 96
  名称: IrqDmaCh91SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 91 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 97
  名称: IrqDmaCh92SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 92 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 98
  名称: IrqDmaCh93SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 93 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 99
  名称: IrqDmaCh94SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 94 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 100
  名称: IrqDmaCh95SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 95 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 101
  名称: IrqDmaCh96SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 96 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 102
  名称: IrqDmaCh97SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 97 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 103
  名称: IrqDmaCh98SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 98 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 104
  名称: IrqDmaCh99SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 99 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 105
  名称: IrqDmaCh100SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 100 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 106
  名称: IrqDmaCh101SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 101 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 107
  名称: IrqDmaCh102SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 102 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 108
  名称: IrqDmaCh103SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 103 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 109
  名称: IrqDmaCh104SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 104 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 110
  名称: IrqDmaCh105SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 105 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 111
  名称: IrqDmaCh106SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 106 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 112
  名称: IrqDmaCh107SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 107 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 113
  名称: IrqDmaCh108SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 108 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 114
  名称: IrqDmaCh109SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 109 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 115
  名称: IrqDmaCh110SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 110 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 116
  名称: IrqDmaCh111SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 111 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 117
  名称: IrqDmaCh112SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 112 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 118
  名称: IrqDmaCh113SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 113 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 119
  名称: IrqDmaCh114SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 114 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 120
  名称: IrqDmaCh115SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 115 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 121
  名称: IrqDmaCh116SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 116 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 122
  名称: IrqDmaCh117SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 117 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 123
  名称: IrqDmaCh118SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 118 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 124
  名称: IrqDmaCh119SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 119 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 125
  名称: IrqDmaCh120SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 120 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 126
  名称: IrqDmaCh121SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 121 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 127
  名称: IrqDmaCh122SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 122 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 128
  名称: IrqDmaCh123SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 123 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 129
  名称: IrqDmaCh124SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 124 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 130
  名称: IrqDmaCh125SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 125 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 131
  名称: IrqDmaCh126SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 126 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 132
  名称: IrqDmaCh127SRCat
  长名称: ''
  描述: |
    The interrupt category setting of DMA Channel 127 Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 30. IrqDmaPrioConfig

**描述**: This container contains the parameter to configure the priority of all the SRN supported by Dma
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqDmaErr0SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Error Service Reuest.The SRN number indicates the SRN
      configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqDmaErr1SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Error Service Reuest.The SRN number indicates the SRN
      configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: IrqDmaErr2SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Error Service Reuest.The SRN number indicates the SRN
      configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: IrqDmaErr3SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Error Service Reuest.The SRN number indicates the SRN
      configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: IrqDmaCh0SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 0 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: IrqDmaCh1SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 1 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: IrqDmaCh2SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 2 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 8
  名称: IrqDmaCh3SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 3 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 9
  名称: IrqDmaCh4SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 4 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 10
  名称: IrqDmaCh5SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 5 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 11
  名称: IrqDmaCh6SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 6 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 12
  名称: IrqDmaCh7SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 7 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 13
  名称: IrqDmaCh8SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 8 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 14
  名称: IrqDmaCh9SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 9 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 15
  名称: IrqDmaCh10SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 10 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 16
  名称: IrqDmaCh11SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 11 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 17
  名称: IrqDmaCh12SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 12 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 18
  名称: IrqDmaCh13SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 13 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 19
  名称: IrqDmaCh14SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 14 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 20
  名称: IrqDmaCh15SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 15 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 21
  名称: IrqDmaCh16SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 16 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 22
  名称: IrqDmaCh17SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 17 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 23
  名称: IrqDmaCh18SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 18 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 24
  名称: IrqDmaCh19SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 19 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 25
  名称: IrqDmaCh20SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 20 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 26
  名称: IrqDmaCh21SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 21 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 27
  名称: IrqDmaCh22SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 22 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 28
  名称: IrqDmaCh23SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 23 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 29
  名称: IrqDmaCh24SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 24 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 30
  名称: IrqDmaCh25SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 25 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 31
  名称: IrqDmaCh26SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 26 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 32
  名称: IrqDmaCh27SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 27 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 33
  名称: IrqDmaCh28SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 28 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 34
  名称: IrqDmaCh29SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 29 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 35
  名称: IrqDmaCh30SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 30 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 36
  名称: IrqDmaCh31SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 31 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 37
  名称: IrqDmaCh32SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 32 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 38
  名称: IrqDmaCh33SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 33 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 39
  名称: IrqDmaCh34SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 34 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 40
  名称: IrqDmaCh35SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 35 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 41
  名称: IrqDmaCh36SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 36 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 42
  名称: IrqDmaCh37SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 37 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 43
  名称: IrqDmaCh38SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 38 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 44
  名称: IrqDmaCh39SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 39 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 45
  名称: IrqDmaCh40SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 40 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 46
  名称: IrqDmaCh41SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 41 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 47
  名称: IrqDmaCh42SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 42 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 48
  名称: IrqDmaCh43SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 43 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 49
  名称: IrqDmaCh44SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 44 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 50
  名称: IrqDmaCh45SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 45 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 51
  名称: IrqDmaCh46SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 46 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 52
  名称: IrqDmaCh47SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 47 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 53
  名称: IrqDmaCh48SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 48 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 54
  名称: IrqDmaCh49SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 49 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 55
  名称: IrqDmaCh50SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 50 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 56
  名称: IrqDmaCh51SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 51 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 57
  名称: IrqDmaCh52SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 52 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 58
  名称: IrqDmaCh53SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 53 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 59
  名称: IrqDmaCh54SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 54 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 60
  名称: IrqDmaCh55SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 55 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 61
  名称: IrqDmaCh56SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 56 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 62
  名称: IrqDmaCh57SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 57 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 63
  名称: IrqDmaCh58SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 58 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 64
  名称: IrqDmaCh59SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 59 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 65
  名称: IrqDmaCh60SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 60 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 66
  名称: IrqDmaCh61SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 61 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 67
  名称: IrqDmaCh62SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 62 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 68
  名称: IrqDmaCh63SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 63 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 69
  名称: IrqDmaCh64SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 64 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 70
  名称: IrqDmaCh65SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 65 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 71
  名称: IrqDmaCh66SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 66 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 72
  名称: IrqDmaCh67SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 67 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 73
  名称: IrqDmaCh68SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 68 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 74
  名称: IrqDmaCh69SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 69 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 75
  名称: IrqDmaCh70SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 70 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 76
  名称: IrqDmaCh71SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 71 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 77
  名称: IrqDmaCh72SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 72 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 78
  名称: IrqDmaCh73SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 73 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 79
  名称: IrqDmaCh74SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 74 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 80
  名称: IrqDmaCh75SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 75 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 81
  名称: IrqDmaCh76SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 76 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 82
  名称: IrqDmaCh77SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 77 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 83
  名称: IrqDmaCh78SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 78 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 84
  名称: IrqDmaCh79SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 79 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 85
  名称: IrqDmaCh80SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 80 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 86
  名称: IrqDmaCh81SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 81 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 87
  名称: IrqDmaCh82SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 82 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 88
  名称: IrqDmaCh83SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 83 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 89
  名称: IrqDmaCh84SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 84 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 90
  名称: IrqDmaCh85SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 85 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 91
  名称: IrqDmaCh86SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 86 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 92
  名称: IrqDmaCh87SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 87 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 93
  名称: IrqDmaCh88SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 88 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 94
  名称: IrqDmaCh89SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 89 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 95
  名称: IrqDmaCh90SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 90 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 96
  名称: IrqDmaCh91SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 91 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 97
  名称: IrqDmaCh92SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 92 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 98
  名称: IrqDmaCh93SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 93 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 99
  名称: IrqDmaCh94SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 94 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 100
  名称: IrqDmaCh95SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 95 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 101
  名称: IrqDmaCh96SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 96 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 102
  名称: IrqDmaCh97SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 97 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 103
  名称: IrqDmaCh98SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 98 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 104
  名称: IrqDmaCh99SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 99 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 105
  名称: IrqDmaCh100SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 100 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 106
  名称: IrqDmaCh101SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 101 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 107
  名称: IrqDmaCh102SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 102 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 108
  名称: IrqDmaCh103SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 103 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 109
  名称: IrqDmaCh104SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 104 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 110
  名称: IrqDmaCh105SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 105 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 111
  名称: IrqDmaCh106SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 106 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 112
  名称: IrqDmaCh107SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 107 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 113
  名称: IrqDmaCh108SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 108 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 114
  名称: IrqDmaCh109SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 109 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 115
  名称: IrqDmaCh110SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 110 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 116
  名称: IrqDmaCh111SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 111 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 117
  名称: IrqDmaCh112SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 112 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 118
  名称: IrqDmaCh113SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 113 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 119
  名称: IrqDmaCh114SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 114 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 120
  名称: IrqDmaCh115SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 115 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 121
  名称: IrqDmaCh116SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 116 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 122
  名称: IrqDmaCh117SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 117 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 123
  名称: IrqDmaCh118SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 118 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 124
  名称: IrqDmaCh119SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 119 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 125
  名称: IrqDmaCh120SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 120 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 126
  名称: IrqDmaCh121SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 121 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 127
  名称: IrqDmaCh122SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 122 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 128
  名称: IrqDmaCh123SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 123 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 129
  名称: IrqDmaCh124SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 124 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 130
  名称: IrqDmaCh125SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 125 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 131
  名称: IrqDmaCh126SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 126 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 132
  名称: IrqDmaCh127SRPrio
  长名称: ''
  描述: The interrupt priority setting of DMA Channel 127 Service Request.The SRN number indicates the
      SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
```

### 31. IrqDmaTosConfig

**描述**: This container contains the parameter to configure the type of service of all the SRN supported by
Dma module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqDmaErr0SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Error Service Reuest.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqDmaErr1SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Error Service Reuest.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqDmaErr2SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Error Service Reuest.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqDmaErr3SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Error Service Reuest.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: IrqDmaCh0SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 0 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: IrqDmaCh1SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 1 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: IrqDmaCh2SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 2 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: IrqDmaCh3SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 3 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: IrqDmaCh4SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 4 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: IrqDmaCh5SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 5 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: IrqDmaCh6SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 6 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: IrqDmaCh7SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 7 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: IrqDmaCh8SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 8 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: IrqDmaCh9SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 9 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: IrqDmaCh10SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 10 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: IrqDmaCh11SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 11 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 17
  名称: IrqDmaCh12SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 12 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 18
  名称: IrqDmaCh13SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 13 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 19
  名称: IrqDmaCh14SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 14 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 20
  名称: IrqDmaCh15SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 15 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 21
  名称: IrqDmaCh16SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 16 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 22
  名称: IrqDmaCh17SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 17 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 23
  名称: IrqDmaCh18SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 18 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 24
  名称: IrqDmaCh19SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 19 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 25
  名称: IrqDmaCh20SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 20 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 26
  名称: IrqDmaCh21SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 21 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 27
  名称: IrqDmaCh22SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 22 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 28
  名称: IrqDmaCh23SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 23 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 29
  名称: IrqDmaCh24SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 24 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 30
  名称: IrqDmaCh25SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 25 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 31
  名称: IrqDmaCh26SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 26 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 32
  名称: IrqDmaCh27SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 27 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 33
  名称: IrqDmaCh28SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 28 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 34
  名称: IrqDmaCh29SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 29 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 35
  名称: IrqDmaCh30SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 30 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 36
  名称: IrqDmaCh31SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 31 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 37
  名称: IrqDmaCh32SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 32 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 38
  名称: IrqDmaCh33SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 33 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 39
  名称: IrqDmaCh34SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 34 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 40
  名称: IrqDmaCh35SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 35 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 41
  名称: IrqDmaCh36SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 36 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 42
  名称: IrqDmaCh37SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 37 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 43
  名称: IrqDmaCh38SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 38 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 44
  名称: IrqDmaCh39SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 39 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 45
  名称: IrqDmaCh40SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 40 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 46
  名称: IrqDmaCh41SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 41 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 47
  名称: IrqDmaCh42SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 42 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 48
  名称: IrqDmaCh43SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 43 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 49
  名称: IrqDmaCh44SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 44 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 50
  名称: IrqDmaCh45SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 45 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 51
  名称: IrqDmaCh46SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 46 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 52
  名称: IrqDmaCh47SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 47 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 53
  名称: IrqDmaCh48SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 48 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 54
  名称: IrqDmaCh49SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 49 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 55
  名称: IrqDmaCh50SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 50 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 56
  名称: IrqDmaCh51SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 51 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 57
  名称: IrqDmaCh52SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 52 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 58
  名称: IrqDmaCh53SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 53 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 59
  名称: IrqDmaCh54SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 54 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 60
  名称: IrqDmaCh55SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 55 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 61
  名称: IrqDmaCh56SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 56 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 62
  名称: IrqDmaCh57SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 57 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 63
  名称: IrqDmaCh58SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 58 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 64
  名称: IrqDmaCh59SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 59 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 65
  名称: IrqDmaCh60SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 60 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 66
  名称: IrqDmaCh61SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 61 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 67
  名称: IrqDmaCh62SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 62 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 68
  名称: IrqDmaCh63SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 63 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 69
  名称: IrqDmaCh64SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 64 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 70
  名称: IrqDmaCh65SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 65 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 71
  名称: IrqDmaCh66SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 66 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 72
  名称: IrqDmaCh67SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 67 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 73
  名称: IrqDmaCh68SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 68 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 74
  名称: IrqDmaCh69SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 69 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 75
  名称: IrqDmaCh70SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 70 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 76
  名称: IrqDmaCh71SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 71 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 77
  名称: IrqDmaCh72SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 72 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 78
  名称: IrqDmaCh73SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 73 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 79
  名称: IrqDmaCh74SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 74 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 80
  名称: IrqDmaCh75SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 75 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 81
  名称: IrqDmaCh76SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 76 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 82
  名称: IrqDmaCh77SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 77 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 83
  名称: IrqDmaCh78SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 78 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 84
  名称: IrqDmaCh79SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 79 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 85
  名称: IrqDmaCh80SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 80 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 86
  名称: IrqDmaCh81SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 81 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 87
  名称: IrqDmaCh82SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 82 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 88
  名称: IrqDmaCh83SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 83 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 89
  名称: IrqDmaCh84SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 84 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 90
  名称: IrqDmaCh85SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 85 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 91
  名称: IrqDmaCh86SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 86 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 92
  名称: IrqDmaCh87SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 87 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 93
  名称: IrqDmaCh88SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 88 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 94
  名称: IrqDmaCh89SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 89 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 95
  名称: IrqDmaCh90SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 90 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 96
  名称: IrqDmaCh91SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 91 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 97
  名称: IrqDmaCh92SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 92 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 98
  名称: IrqDmaCh93SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 93 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 99
  名称: IrqDmaCh94SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 94 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 100
  名称: IrqDmaCh95SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 95 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 101
  名称: IrqDmaCh96SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 96 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 102
  名称: IrqDmaCh97SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 97 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 103
  名称: IrqDmaCh98SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 98 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 104
  名称: IrqDmaCh99SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 99 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 105
  名称: IrqDmaCh100SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 100 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 106
  名称: IrqDmaCh101SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 101 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 107
  名称: IrqDmaCh102SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 102 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 108
  名称: IrqDmaCh103SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 103 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 109
  名称: IrqDmaCh104SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 104 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 110
  名称: IrqDmaCh105SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 105 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 111
  名称: IrqDmaCh106SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 106 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 112
  名称: IrqDmaCh107SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 107 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 113
  名称: IrqDmaCh108SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 108 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 114
  名称: IrqDmaCh109SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 109 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 115
  名称: IrqDmaCh110SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 110 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 116
  名称: IrqDmaCh111SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 111 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 117
  名称: IrqDmaCh112SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 112 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 118
  名称: IrqDmaCh113SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 113 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 119
  名称: IrqDmaCh114SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 114 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 120
  名称: IrqDmaCh115SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 115 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 121
  名称: IrqDmaCh116SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 116 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 122
  名称: IrqDmaCh117SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 117 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 123
  名称: IrqDmaCh118SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 118 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 124
  名称: IrqDmaCh119SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 119 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 125
  名称: IrqDmaCh120SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 120 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 126
  名称: IrqDmaCh121SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 121 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 127
  名称: IrqDmaCh122SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 122 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 128
  名称: IrqDmaCh123SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 123 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 129
  名称: IrqDmaCh124SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 124 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 130
  名称: IrqDmaCh125SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 125 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 131
  名称: IrqDmaCh126SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 126 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 132
  名称: IrqDmaCh127SRTos
  长名称: ''
  描述: The interrupt type of service setting of DMA Channel 127 Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 32. IrqGPSRGroupConfig

**描述**: This container contains the GPSRGroup interrupt configuration parameters.

该容器没有参数。

### 33. Irq_GPSRGroup0_Config

**描述**: This container contains the General Purpose Service Request Group 0 interrupt configuration
parameters.

该容器没有参数。

### 34. Irq_GPSRGroup0Cat_Config

**描述**: This container contains the parameter to configure the category of all the SRN supported by General
Purpose Service Request Group 0.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_GPSRGroup0SR0_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of General Purpose Service Request Group 0.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: Irq_GPSRGroup0SR1_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of General Purpose Service Request Group 0.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: Irq_GPSRGroup0SR2_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of General Purpose Service Request Group 0.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: Irq_GPSRGroup0SR3_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of General Purpose Service Request Group 0.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: Irq_GPSRGroup0SR4_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of General Purpose Service Request Group 0.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: Irq_GPSRGroup0SR5_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of General Purpose Service Request Group 0.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: Irq_GPSRGroup0SR6_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of General Purpose Service Request Group 0.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: Irq_GPSRGroup0SR7_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of General Purpose Service Request Group 0.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 35. Irq_GPSRGroup0Prio_Config

**描述**: This container contains the parameter to configure the priority of all the SRN supported by General
Purpose Service Request Group 0.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_GPSRGroup0SR0_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN0 of General Purpose Service Request Group 0.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: Irq_GPSRGroup0SR1_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN1 of General Purpose Service Request Group 0.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: Irq_GPSRGroup0SR2_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN2 of General Purpose Service Request Group 0.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: Irq_GPSRGroup0SR3_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of General Purpose Service Request Group 0.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: Irq_GPSRGroup0SR4_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of General Purpose Service Request Group 0.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: Irq_GPSRGroup0SR5_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of General Purpose Service Request Group 0.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: Irq_GPSRGroup0SR6_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of General Purpose Service Request Group 0.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 8
  名称: Irq_GPSRGroup0SR7_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of General Purpose Service Request Group 0.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 36. Irq_GPSRGroup0Tos_Config

**描述**: This container contains the parameter to configure the type of service of all the SRN supported by
General Purpose Service Request Group 0.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_GPSRGroup0SR0_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of General Purpose Service Request Group 0.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: Irq_GPSRGroup0SR1_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of General Purpose Service Request Group 0.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: Irq_GPSRGroup0SR2_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of General Purpose Service Request Group 0.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: Irq_GPSRGroup0SR3_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of General Purpose Service Request Group 0.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: Irq_GPSRGroup0SR4_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of General Purpose Service Request Group 0.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: Irq_GPSRGroup0SR5_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of General Purpose Service Request Group 0.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: Irq_GPSRGroup0SR6_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of General Purpose Service Request Group 0.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: Irq_GPSRGroup0SR7_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of General Purpose Service Request Group 0.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 37. Irq_GPSRGroup1_Config

**描述**: This container contains the General Purpose Service Request Group 1 interrupt configuration
parameters.

该容器没有参数。

### 38. Irq_GPSRGroup1Cat_Config

**描述**: This container contains the parameter to configure the category of all the SRN supported by General
Purpose Service Request Group 1.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_GPSRGroup1SR0_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of General Purpose Service Request Group 1.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: Irq_GPSRGroup1SR1_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of General Purpose Service Request Group 1.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: Irq_GPSRGroup1SR2_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of General Purpose Service Request Group 1.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: Irq_GPSRGroup1SR3_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of General Purpose Service Request Group 1.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: Irq_GPSRGroup1SR4_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of General Purpose Service Request Group 1.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: Irq_GPSRGroup1SR5_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of General Purpose Service Request Group 1.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: Irq_GPSRGroup1SR6_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of General Purpose Service Request Group 1.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: Irq_GPSRGroup1SR7_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of General Purpose Service Request Group 1.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 39. Irq_GPSRGroup1Prio_Config

**描述**: This container contains the parameter to configure the priority of all the SRN supported by General
Purpose Service Request Group 1.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_GPSRGroup1SR0_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN0 of General Purpose Service Request Group 1.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: Irq_GPSRGroup1SR1_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN1 of General Purpose Service Request Group 1.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: Irq_GPSRGroup1SR2_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN2 of General Purpose Service Request Group 1.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: Irq_GPSRGroup1SR3_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of General Purpose Service Request Group 1.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: Irq_GPSRGroup1SR4_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of General Purpose Service Request Group 1.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: Irq_GPSRGroup1SR5_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of General Purpose Service Request Group 1.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: Irq_GPSRGroup1SR6_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of General Purpose Service Request Group 1.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 8
  名称: Irq_GPSRGroup1SR7_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of General Purpose Service Request Group 1.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 40. Irq_GPSRGroup1Tos_Config

**描述**: This container contains the parameter to configure the type of service of all the SRN supported by
General Purpose Service Request Group 1.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_GPSRGroup1SR0_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of General Purpose Service Request Group 1.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: Irq_GPSRGroup1SR1_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of General Purpose Service Request Group 1.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: Irq_GPSRGroup1SR2_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of General Purpose Service Request Group 1.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: Irq_GPSRGroup1SR3_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of General Purpose Service Request Group 1.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: Irq_GPSRGroup1SR4_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of General Purpose Service Request Group 1.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: Irq_GPSRGroup1SR5_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of General Purpose Service Request Group 1.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: Irq_GPSRGroup1SR6_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of General Purpose Service Request Group 1.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: Irq_GPSRGroup1SR7_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of General Purpose Service Request Group 1.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 41. Irq_GPSRGroup2_Config

**描述**: This container contains the General Purpose Service Request Group 2 interrupt configuration
parameters.

该容器没有参数。

### 42. Irq_GPSRGroup2Cat_Config

**描述**: This container contains the parameter to configure the category of all the SRN supported by General
Purpose Service Request Group 2.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_GPSRGroup2SR0_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of General Purpose Service Request Group 2.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: Irq_GPSRGroup2SR1_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of General Purpose Service Request Group 2.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: Irq_GPSRGroup2SR2_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of General Purpose Service Request Group 2.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: Irq_GPSRGroup2SR3_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of General Purpose Service Request Group 2.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: Irq_GPSRGroup2SR4_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of General Purpose Service Request Group 2.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: Irq_GPSRGroup2SR5_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of General Purpose Service Request Group 2.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: Irq_GPSRGroup2SR6_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of General Purpose Service Request Group 2.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: Irq_GPSRGroup2SR7_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of General Purpose Service Request Group 2.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 43. Irq_GPSRGroup2Prio_Config

**描述**: This container contains the parameter to configure the priority of all the SRN supported by General
Purpose Service Request Group 2.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_GPSRGroup2SR0_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN0 of General Purpose Service Request Group 2.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: Irq_GPSRGroup2SR1_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN1 of General Purpose Service Request Group 2.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: Irq_GPSRGroup2SR2_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN2 of General Purpose Service Request Group 2.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: Irq_GPSRGroup2SR3_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of General Purpose Service Request Group 2.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: Irq_GPSRGroup2SR4_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of General Purpose Service Request Group 2.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: Irq_GPSRGroup2SR5_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of General Purpose Service Request Group 2.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: Irq_GPSRGroup2SR6_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of General Purpose Service Request Group 2.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 8
  名称: Irq_GPSRGroup2SR7_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of General Purpose Service Request Group 2.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 44. Irq_GPSRGroup2Tos_Config

**描述**: This container contains the parameter to configure the type of service of all the SRN supported by
General Purpose Service Request Group 2.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_GPSRGroup2SR0_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of General Purpose Service Request Group 2.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: Irq_GPSRGroup2SR1_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of General Purpose Service Request Group 2.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: Irq_GPSRGroup2SR2_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of General Purpose Service Request Group 2.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: Irq_GPSRGroup2SR3_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of General Purpose Service Request Group 2.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: Irq_GPSRGroup2SR4_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of General Purpose Service Request Group 2.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: Irq_GPSRGroup2SR5_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of General Purpose Service Request Group 2.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: Irq_GPSRGroup2SR6_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of General Purpose Service Request Group 2.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: Irq_GPSRGroup2SR7_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of General Purpose Service Request Group 2.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 45. Irq_GPSRGroup3_Config

**描述**: This container contains the General Purpose Service Request Group 3 interrupt configuration
parameters.

该容器没有参数。

### 46. Irq_GPSRGroup3Cat_Config

**描述**: This container contains the parameter to configure the category of all the SRN supported by General
Purpose Service Request Group 3.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_GPSRGroup3SR0_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of General Purpose Service Request Group 3.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: Irq_GPSRGroup3SR1_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of General Purpose Service Request Group 3.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: Irq_GPSRGroup3SR2_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of General Purpose Service Request Group 3.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: Irq_GPSRGroup3SR3_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of General Purpose Service Request Group 3.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: Irq_GPSRGroup3SR4_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of General Purpose Service Request Group 3.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: Irq_GPSRGroup3SR5_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of General Purpose Service Request Group 3.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: Irq_GPSRGroup3SR6_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of General Purpose Service Request Group 3.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: Irq_GPSRGroup3SR7_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of General Purpose Service Request Group 3.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 47. Irq_GPSRGroup3Prio_Config

**描述**: This container contains the parameter to configure the priority of all the SRN supported by General
Purpose Service Request Group 3.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_GPSRGroup3SR0_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN0 of General Purpose Service Request Group 3.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: Irq_GPSRGroup3SR1_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN1 of General Purpose Service Request Group 3.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: Irq_GPSRGroup3SR2_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN2 of General Purpose Service Request Group 3.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: Irq_GPSRGroup3SR3_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of General Purpose Service Request Group 3.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: Irq_GPSRGroup3SR4_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of General Purpose Service Request Group 3.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: Irq_GPSRGroup3SR5_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of General Purpose Service Request Group 3.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: Irq_GPSRGroup3SR6_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of General Purpose Service Request Group 3.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 8
  名称: Irq_GPSRGroup3SR7_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of General Purpose Service Request Group 3.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 48. Irq_GPSRGroup3Tos_Config

**描述**: This container contains the parameter to configure the type of service of all the SRN supported by
General Purpose Service Request Group 3.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_GPSRGroup3SR0_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of General Purpose Service Request Group 3.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: Irq_GPSRGroup3SR1_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of General Purpose Service Request Group 3.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: Irq_GPSRGroup3SR2_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of General Purpose Service Request Group 3.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: Irq_GPSRGroup3SR3_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of General Purpose Service Request Group 3.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: Irq_GPSRGroup3SR4_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of General Purpose Service Request Group 3.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: Irq_GPSRGroup3SR5_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of General Purpose Service Request Group 3.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: Irq_GPSRGroup3SR6_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of General Purpose Service Request Group 3.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: Irq_GPSRGroup3SR7_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of General Purpose Service Request Group 3.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 49. Irq_GPSRGroup4_Config

**描述**: This container contains the General Purpose Service Request Group 4 interrupt configuration
parameters.

该容器没有参数。

### 50. Irq_GPSRGroup4Cat_Config

**描述**: This container contains the parameter to configure the category of all the SRN supported by General
Purpose Service Request Group 4.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_GPSRGroup4SR0_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of General Purpose Service Request Group 4.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: Irq_GPSRGroup4SR1_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of General Purpose Service Request Group 4.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: Irq_GPSRGroup4SR2_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of General Purpose Service Request Group 4.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: Irq_GPSRGroup4SR3_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of General Purpose Service Request Group 4.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: Irq_GPSRGroup4SR4_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of General Purpose Service Request Group 4.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: Irq_GPSRGroup4SR5_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of General Purpose Service Request Group 4.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: Irq_GPSRGroup4SR6_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of General Purpose Service Request Group 4.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: Irq_GPSRGroup4SR7_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of General Purpose Service Request Group 4.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 51. Irq_GPSRGroup4Prio_Config

**描述**: This container contains the parameter to configure the priority of all the SRN supported by General
Purpose Service Request Group 4.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_GPSRGroup4SR0_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN0 of General Purpose Service Request Group 4.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: Irq_GPSRGroup4SR1_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN1 of General Purpose Service Request Group 4.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: Irq_GPSRGroup4SR2_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN2 of General Purpose Service Request Group 4.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: Irq_GPSRGroup4SR3_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of General Purpose Service Request Group 4.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: Irq_GPSRGroup4SR4_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of General Purpose Service Request Group 4.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: Irq_GPSRGroup4SR5_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of General Purpose Service Request Group 4.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: Irq_GPSRGroup4SR6_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of General Purpose Service Request Group 4.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 8
  名称: Irq_GPSRGroup4SR7_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of General Purpose Service Request Group 4.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 52. Irq_GPSRGroup4Tos_Config

**描述**: This container contains the parameter to configure the type of service of all the SRN supported by
General Purpose Service Request Group 4.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_GPSRGroup4SR0_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of General Purpose Service Request Group 4.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: Irq_GPSRGroup4SR1_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of General Purpose Service Request Group 4.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: Irq_GPSRGroup4SR2_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of General Purpose Service Request Group 4.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: Irq_GPSRGroup4SR3_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of General Purpose Service Request Group 4.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: Irq_GPSRGroup4SR4_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of General Purpose Service Request Group 4.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: Irq_GPSRGroup4SR5_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of General Purpose Service Request Group 4.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: Irq_GPSRGroup4SR6_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of General Purpose Service Request Group 4.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: Irq_GPSRGroup4SR7_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of General Purpose Service Request Group 4.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 53. Irq_GPSRGroup5_Config

**描述**: This container contains the General Purpose Service Request Group 5 interrupt configuration
parameters.

该容器没有参数。

### 54. Irq_GPSRGroup5Cat_Config

**描述**: This container contains the parameter to configure the category of all the SRN supported by General
Purpose Service Request Group 5.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_GPSRGroup5SR0_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of General Purpose Service Request Group 5.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: Irq_GPSRGroup5SR1_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of General Purpose Service Request Group 5.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: Irq_GPSRGroup5SR2_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of General Purpose Service Request Group 5.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: Irq_GPSRGroup5SR3_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of General Purpose Service Request Group 5.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: Irq_GPSRGroup5SR4_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of General Purpose Service Request Group 5.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: Irq_GPSRGroup5SR5_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of General Purpose Service Request Group 5.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: Irq_GPSRGroup5SR6_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of General Purpose Service Request Group 5.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: Irq_GPSRGroup5SR7_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of General Purpose Service Request Group 5.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 55. Irq_GPSRGroup5Prio_Config

**描述**: This container contains the parameter to configure the priority of all the SRN supported by General
Purpose Service Request Group 5.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_GPSRGroup5SR0_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN0 of General Purpose Service Request Group 5.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: Irq_GPSRGroup5SR1_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN1 of General Purpose Service Request Group 5.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: Irq_GPSRGroup5SR2_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN2 of General Purpose Service Request Group 5.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: Irq_GPSRGroup5SR3_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of General Purpose Service Request Group 5.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: Irq_GPSRGroup5SR4_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of General Purpose Service Request Group 5.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: Irq_GPSRGroup5SR5_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of General Purpose Service Request Group 5.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: Irq_GPSRGroup5SR6_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of General Purpose Service Request Group 5.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 8
  名称: Irq_GPSRGroup5SR7_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of General Purpose Service Request Group 5.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 56. Irq_GPSRGroup5Tos_Config

**描述**: This container contains the parameter to configure the type of service of all the SRN supported by
General Purpose Service Request Group 5.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_GPSRGroup5SR0_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of General Purpose Service Request Group 5.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: Irq_GPSRGroup5SR1_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of General Purpose Service Request Group 5.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: Irq_GPSRGroup5SR2_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of General Purpose Service Request Group 5.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: Irq_GPSRGroup5SR3_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of General Purpose Service Request Group 5.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: Irq_GPSRGroup5SR4_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of General Purpose Service Request Group 5.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: Irq_GPSRGroup5SR5_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of General Purpose Service Request Group 5.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: Irq_GPSRGroup5SR6_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of General Purpose Service Request Group 5.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: Irq_GPSRGroup5SR7_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of General Purpose Service Request Group 5.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 57. IrqFlexRayConfig

**描述**: This container contains the FlexRay interrupt configuration parameters.

该容器没有参数。

### 58. Irq_FlexRay0_Config

**描述**: This container contains the FlexRay0 interrupt configuration parameters.

该容器没有参数。

### 59. Irq_FlexRay0Cat_Config

**描述**: This container contains the FlexRay0 category configuration parameters.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_FlexRay0INT0_Cat
  长名称: ''
  描述: |
    The interrupt category setting of INT0 of FlexRay0 Module. The SR number indicates the SRN
    configured.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: Irq_FlexRay0INT1_Cat
  长名称: ''
  描述: |
    The interrupt category setting of INT1 of FlexRay0 Module. The SR number indicates the SRN
    configured.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: Irq_FlexRay0TimerInt0_Cat
  长名称: ''
  描述: |
    The interrupt category setting of Timer Interrupt 0 Service request of FlexRay0 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: Irq_FlexRay0TimerInt1_Cat
  长名称: ''
  描述: |
    The interrupt category setting of Timer Interrupt 1 Service request of FlexRay0 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: Irq_FlexRay0NewData0_Cat
  长名称: ''
  描述: |
    The interrupt category setting of New Data 0 Service request of FlexRay0 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: Irq_FlexRay0NewData1_Cat
  长名称: ''
  描述: |
    The interrupt category setting of New Data 1 Service request of FlexRay0 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: Irq_FlexRay0MBSC0_Cat
  长名称: ''
  描述: |
    The interrupt category setting of Message Buffer Status Changed 0 Service Request of FlexRay0
    Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: Irq_FlexRay0MBSC1_Cat
  长名称: ''
  描述: |
    The interrupt category setting of Message Buffer Status Changed 1 Service Request of FlexRay0
    Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: Irq_FlexRay0OBusy_Cat
  长名称: ''
  描述: |
    The interrupt category setting of Output Buffer Busy Service Request of FlexRay0 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: Irq_FlexRay0IBusy_Cat
  长名称: ''
  描述: |
    The interrupt category setting of Input Buffer Busy Service Request of FlexRay0 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 60. Irq_FlexRay0Prio_Config

**描述**: This container contains the FlexRay0 priority configuration parameters.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_FlexRay0INT0_Prio
  长名称: ''
  描述: The interrupt priority setting of INT0 of the FlexRay0.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: Irq_FlexRay0INT1_Prio
  长名称: ''
  描述: The interrupt priority setting of INT1 of the FlexRay0.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: Irq_FlexRay0TimerInt0_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN2 of the FlexRay0.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: Irq_FlexRay0TimerInt1_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of the FlexRay0.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: Irq_FlexRay0NewData0_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN4 of the FlexRay0.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: Irq_FlexRay0NewData1_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN5 of the FlexRay0.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: Irq_FlexRay0MBSC0_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN6 of the FlexRay0.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 8
  名称: Irq_FlexRay0MBSC1_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN7 of the FlexRay0.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 9
  名称: Irq_FlexRay0OBusy_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN8 of the FlexRay0.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 10
  名称: Irq_FlexRay0IBusy_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN9 of the FlexRay0.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 61. Irq_FlexRay0Tos_Config

**描述**: This container contains the FlexRay0 Type of Service configuration parameters.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_FlexRay0INT0_Tos
  长名称: ''
  描述: The interrupt type of service setting of INT0 of FlexRay0 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: Irq_FlexRay0INT1_Tos
  长名称: ''
  描述: The interrupt type of service setting of INT1 of FlexRay0 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: Irq_FlexRay0TimerInt0_Tos
  长名称: ''
  描述: The interrupt type of service setting of Timer Interrupt 0 Service request of FlexRay0 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: Irq_FlexRay0TimerInt1_Tos
  长名称: ''
  描述: The interrupt type of service setting of Timer Interrupt 1 Service request of FlexRay0 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: Irq_FlexRay0NewData0_Tos
  长名称: ''
  描述: The interrupt type of service setting of New Data 0 Service request of FlexRay0 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: Irq_FlexRay0NewData1_Tos
  长名称: ''
  描述: The interrupt type of service setting of New Data 1 Service request of FlexRay0 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: Irq_FlexRay0MBSC0_Tos
  长名称: ''
  描述: The interrupt type of service setting of Message Buffer Status Changed 0 Service request of
      FlexRay0 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: Irq_FlexRay0MBSC1_Tos
  长名称: ''
  描述: The interrupt type of service setting of Message Buffer Status Changed 1 Service request of
      FlexRay0 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: Irq_FlexRay0OBusy_Tos
  长名称: ''
  描述: The interrupt type of service setting of Output Buffer Busy Service request of FlexRay0
      Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: Irq_FlexRay0IBusy_Tos
  长名称: ''
  描述: The interrupt type of service setting of Input Buffer Busy Service request of FlexRay0 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 62. Irq_FlexRay1_Config

**描述**: This container contains the FlexRay0 interrupt configuration parameters.

该容器没有参数。

### 63. Irq_FlexRay1Cat_Config

**描述**: This container contains the FlexRay1 category configuration parameters.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_FlexRay1INT0_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN1 of FlexRay1 Module. The SR number indicates the SRN
    configured.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: Irq_FlexRay1INT1_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN1 of FlexRay1 Module. The SR number indicates the SRN
    configured.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: Irq_FlexRay1TimerInt0_Cat
  长名称: ''
  描述: |
    The interrupt category setting of Timer Interrupt 0 Service request of FlexRay1 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: Irq_FlexRay1TimerInt1_Cat
  长名称: ''
  描述: |
    The interrupt category setting of Timer Interrupt 1 Service request of FlexRay1 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: Irq_FlexRay1NewData0_Cat
  长名称: ''
  描述: |
    The interrupt category setting of New Data 0 Service request of FlexRay1 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: Irq_FlexRay1NewData1_Cat
  长名称: ''
  描述: |
    The interrupt category setting of New Data 1 Service request of FlexRay1 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: Irq_FlexRay1MBSC0_Cat
  长名称: ''
  描述: |
    The interrupt category setting of Message Buffer Status Changed 0 Service Request of FlexRay1
    Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: Irq_FlexRay1MBSC1_Cat
  长名称: ''
  描述: |
    The interrupt category setting of Message Buffer Status Changed 1 Service Request of FlexRay1
    Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: Irq_FlexRay1OBusy_Cat
  长名称: ''
  描述: |
    The interrupt category setting of Output Buffer Busy Service Request of FlexRay1 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: Irq_FlexRay1IBusy_Cat
  长名称: ''
  描述: |
    The interrupt category setting of Input Buffer Busy Service Request of FlexRay1 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 64. Irq_FlexRay1Prio_Config

**描述**: This container contains the FlexRay1 priority configuration parameters.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_FlexRay1INT0_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN0 of the FlexRay1.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: Irq_FlexRay1INT1_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN1 of the FlexRay1.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: Irq_FlexRay1TimerInt0_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN2 of the FlexRay1.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: Irq_FlexRay1TimerInt1_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of the FlexRay1.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: Irq_FlexRay1NewData0_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN4 of the FlexRay1.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: Irq_FlexRay1NewData1_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN5 of the FlexRay1.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: Irq_FlexRay1MBSC0_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN6 of the FlexRay1.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 8
  名称: Irq_FlexRay1MBSC1_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN7 of the FlexRay1.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 9
  名称: Irq_FlexRay1OBusy_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN8 of the FlexRay1.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 10
  名称: Irq_FlexRay1IBusy_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN9 of the FlexRay1.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 65. Irq_FlexRay1Tos_Config

**描述**: This container contains the FlexRay1 Type of Service configuration parameters.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_FlexRay1INT0_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of FlexRay1 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: Irq_FlexRay1INT1_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN1 of FlexRay1 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: Irq_FlexRay1TimerInt0_Tos
  长名称: ''
  描述: The interrupt type of service setting of Timer Interrupt 0 Service request of FlexRay1 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: Irq_FlexRay1TimerInt1_Tos
  长名称: ''
  描述: The interrupt type of service setting of Timer Interrupt 1 Service request of FlexRay1 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: Irq_FlexRay1NewData0_Tos
  长名称: ''
  描述: The interrupt type of service setting of New Data 0 Service request of FlexRay1 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: Irq_FlexRay1NewData1_Tos
  长名称: ''
  描述: The interrupt type of service setting of New Data 1 Service request of FlexRay1 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: Irq_FlexRay1MBSC0_Tos
  长名称: ''
  描述: The interrupt type of service setting of Message Buffer Status Changed 0 Service request of
      FlexRay1 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: Irq_FlexRay1MBSC1_Tos
  长名称: ''
  描述: The interrupt type of service setting of Message Buffer Status Changed 1 Service request of
      FlexRay1 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: Irq_FlexRay1OBusy_Tos
  长名称: ''
  描述: The interrupt type of service setting of Output Buffer Busy Service request of FlexRay1
      Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: Irq_FlexRay1IBusy_Tos
  长名称: ''
  描述: The interrupt type of service setting of Input Buffer Busy Service request of FlexRay1 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 66. IrqScuConfig

**描述**: This container contains the SCU interrupt configuration parameters.

该容器没有参数。

### 67. Irq_ScuCat_Config

**描述**: This container contains the parameter to configure the category of all the SRN supported by SCU
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_ScuEruSR0_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of Scu Eru Module.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: Irq_ScuEruSR1_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN1 of SCU ERU Module.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: Irq_ScuEruSR2_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN2 of SCU ERU Module.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: Irq_ScuEruSR3_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN3 of SCU ERU Module.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 68. Irq_ScuPrio_Config

**描述**: This container contains the parameter to configure the priority of all the SRN supported by SCU
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_ScuEruSR0_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN0 of SCU ERU.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: Irq_ScuEruSR1_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN1 of SCU ERU.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: Irq_ScuEruSR2_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN2 of SCU ERU.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: Irq_ScuEruSR3_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of SCU.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 69. Irq_ScuTos_Config

**描述**: This container contains the parameter to configure the type of service of all the SRN supported by
SCU module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_ScuEruSR0_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of Scu Eru Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: Irq_ScuEruSR1_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN1 of Scu Eru Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: Irq_ScuEruSR2_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN2 of Scu Eru Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: Irq_ScuEruSR3_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN3 of Scu Eru Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 70. IrqCCU6Config

**描述**: This container contains the CCU6 interrupt configuration parameters.

该容器没有参数。

### 71. Irq_CCU60_Config

**描述**: This container contains the CCU60 interrupt configuration parameters.

该容器没有参数。

### 72. Irq_CCU60Cat_Config

**描述**: This container contains the parameter to configure the category of all the SRN supported by CCU60
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_CCU60SR0_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of CCU60 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: Irq_CCU60SR1_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN1 of CCU60 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: Irq_CCU60SR2_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN2 of CCU60 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: Irq_CCU60SR3_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN3 of CCU60 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 73. Irq_CCU60Prio_Config

**描述**: This container contains the parameter to configure the priority of all the SRN supported by CCU60
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_CCU60SR0_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN0 of the CCU60.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: Irq_CCU60SR1_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN1 of the CCU60.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: Irq_CCU60SR2_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN2 of the CCU60.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: Irq_CCU60SR3_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of the CCU60.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 74. Irq_CCU60Tos_Config

**描述**: This container contains the parameter to configure the type of service of all the SRN supported by
CCU60 module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_CCU60SR0_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of CCU60 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: Irq_CCU60SR1_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN1 of CCU60 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: Irq_CCU60SR2_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN2 of CCU60 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: Irq_CCU60SR3_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN3 of CCU60 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 75. Irq_CCU61_Config

**描述**: This container contains the CCU61 interrupt configuration parameters.

该容器没有参数。

### 76. Irq_CCU61Cat_Config

**描述**: This container contains the parameter to configure the category of all the SRN supported by CCU61
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_CCU61SR0_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of CCU61 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: Irq_CCU61SR1_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN1 of CCU61 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: Irq_CCU61SR2_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN2 of CCU61 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: Irq_CCU61SR3_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN3 of CCU61 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 77. Irq_CCU61Prio_Config

**描述**: This container contains the parameter to configure the priority of all the SRN supported by CCU61
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_CCU61SR0_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN0 of the CCU61.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: Irq_CCU61SR1_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN1 of the CCU61.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: Irq_CCU61SR2_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN2 of the CCU61.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: Irq_CCU61SR3_Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of the CCU61.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 78. Irq_CCU61Tos_Config

**描述**: This container contains the parameter to configure the type of service of all the SRN supported by
CCU61 module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_CCU61SR0_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of CCU61 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: Irq_CCU61SR1_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN1 of CCU61 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: Irq_CCU61SR2_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN2 of CCU61 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: Irq_CCU61SR3_Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN3 of CCU61 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 79. IrqGtmConfig

**描述**: This container contains the Gtm interrupt configuration parameters.

该容器没有参数。

### 80. Irq_GtmAEI_Config

**描述**: This container contains the GTMAEI interrupt configuration parameters.

该容器没有参数。

### 81. Irq_GtmAEICat_Config

**描述**: This container contains the parameter to configure the category of all the SRN supported by GTMAEI
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_GtmAEI_Cat
  长名称: ''
  描述: |
    The interrupt category setting of AEI shared service request of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 82. Irq_GtmAEIPrio_Config

**描述**: This container contains the parameter to configure the priority of all the SRN supported by GTMAEI
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_GtmAEI_Prio
  长名称: ''
  描述: |
    The interrupt priority setting of AEI shared service request of GTM.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
```

### 83. Irq_GtmAEITos_Config

**描述**: This container contains the parameter to configure the type of service of all the SRN supported by
GTMAEI module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_GtmAEI_Tos
  长名称: ''
  描述: The interrupt category setting of AEI shared service request of GTM.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 84. Irq_GtmARU_Config

**描述**: This container contains the GTMARU interrupt configuration parameters.

该容器没有参数。

### 85. Irq_GtmARUCat_Config

**描述**: This container contains the parameter to configure the category of all the SRN supported by GTMARU
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_GtmARUSR0_Cat
  长名称: ''
  描述: |
    The interrupt category setting of ARU shared service request 0 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: Irq_GtmARUSR1_Cat
  长名称: ''
  描述: |
    The interrupt category setting of ARU shared service request 1 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: Irq_GtmARUSR2_Cat
  长名称: ''
  描述: |
    The interrupt category setting of ARU shared service request 2 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 86. Irq_GtmARUPrio_Config

**描述**: This container contains the parameter to configure the priority of all the SRN supported by GTMARU
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_GtmARUSR0_Prio
  长名称: ''
  描述: |
    The interrupt priority setting of ARU shared service request 0 of GTM.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: Irq_GtmARUSR1_Prio
  长名称: ''
  描述: |
    The interrupt priority setting of ARU shared service request 1 of GTM.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: Irq_GtmARUSR2_Prio
  长名称: ''
  描述: |
    The interrupt priority setting of ARU shared service request 2 of GTM.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
```

### 87. Irq_GtmARUTos_Config

**描述**: This container contains the parameter to configure the type of service of all the SRN supported by
GTMARU module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_GtmARUSR0_Tos
  长名称: ''
  描述: The interrupt type of service setting of ARU shared service request 0 of GTM.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: Irq_GtmARUSR1_Tos
  长名称: ''
  描述: The interrupt type of service setting of ARU shared service request 1 of GTM.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: Irq_GtmARUSR2_Tos
  长名称: ''
  描述: The interrupt type of service setting of ARU shared service request 2 of GTM.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 88. Irq_GtmBRC_Config

**描述**: This container contains the GTMBRC interrupt configuration parameters.

该容器没有参数。

### 89. Irq_GtmBRCCat_Config

**描述**: This container contains the parameter to configure the category of all the SRN supported by GTMBRC
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_GtmBRC_Cat
  长名称: ''
  描述: |
    The interrupt category setting of BRC shared service request of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 90. Irq_GtmBRCPrio_Config

**描述**: This container contains the parameter to configure the priority of all the SRN supported by GTMBRC
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_GtmBRC_Prio
  长名称: ''
  描述: |
    The interrupt priority setting of BRC shared service request of GTM.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
```

### 91. Irq_GtmBRCTos_Config

**描述**: This container contains the parameter to configure the type of service of all the SRN supported by
GTMBRC module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqGtmBRCTos
  长名称: ''
  描述: The interrupt type of service setting of BRC shared service request of GTM.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 92. Irq_GtmCMP_Config

**描述**: This container contains the GTMCMP interrupt configuration parameters.

该容器没有参数。

### 93. Irq_GtmCMPCat_Config

**描述**: This container contains the parameter to configure the category of all the SRN supported by GTMCMP
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_GtmCMP_Cat
  长名称: ''
  描述: |
    The interrupt category setting of CMP shared service request of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 94. Irq_GtmCMPPrio_Config

**描述**: This container contains the parameter to configure the priority of all the SRN supported by GTMCMP
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_GtmCMP_Prio
  长名称: ''
  描述: |
    The interrupt priority setting of CMP shared service request of GTM.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
```

### 95. Irq_GtmCMPTos_Config

**描述**: This container contains the parameter to configure the type of service of all the SRN supported by
GTMCMP module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_GtmCMP_Tos
  长名称: ''
  描述: The interrupt type of service setting of CMP shared service request of GTM.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 96. Irq_GtmSPE_Config

**描述**: This container contains the GTMSPE interrupt configuration parameters.

该容器没有参数。

### 97. Irq_GtmSPECat_Config

**描述**: This container contains the parameter to configure the category of all the SRN supported by GTMSPE
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_GtmSPE0_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SPE0 shared service request of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: Irq_GtmSPE1_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SPE1 shared service request of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: Irq_GtmSPE2_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SPE2 shared service request of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: Irq_GtmSPE3_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SPE3 shared service request of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: Irq_GtmSPE4_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SPE4 shared service request of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: Irq_GtmSPE5_Cat
  长名称: ''
  描述: |
    The interrupt category setting of SPE5 shared service request of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 98. Irq_GtmSPEPrio_Config

**描述**: This container contains the parameter to configure the priority of all the SRN supported by GTMSPE
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_GtmSPE0_Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SPE0 shared service request of GTM.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: Irq_GtmSPE1_Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SPE1 shared service request of GTM.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: Irq_GtmSPE2_Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SPE2 shared service request of GTM.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: Irq_GtmSPE3_Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SPE3 shared service request of GTM.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: Irq_GtmSPE4_Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SPE4 shared service request of GTM.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: Irq_GtmSPE5_Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SPE5 shared service request of GTM.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
```

### 99. Irq_GtmSPETos_Config

**描述**: This container contains the parameter to configure the type of service of all the SRN supported by
GTMSPE module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_GtmSPE0_Tos
  长名称: ''
  描述: The interrupt type of service setting of SPE0 shared service request of GTM.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: Irq_GtmSPE1_Tos
  长名称: ''
  描述: The interrupt type of service setting of SPE1 shared service request of GTM.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: Irq_GtmSPE2_Tos
  长名称: ''
  描述: The interrupt type of service setting of SPE2 shared service request of GTM.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: Irq_GtmSPE3_Tos
  长名称: ''
  描述: The interrupt type of service setting of SPE3 shared service request of GTM.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: Irq_GtmSPE4_Tos
  长名称: ''
  描述: The interrupt type of service setting of SPE4 shared service request of GTM.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: Irq_GtmSPE5_Tos
  长名称: ''
  描述: The interrupt type of service setting of SPE5 shared service request of GTM.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 100. Irq_GtmPSM0_Config

**描述**: This container contains the GTMPSM0 interrupt configuration parameters.

该容器没有参数。

### 101. Irq_GtmPSM0Cat_Config

**描述**: This container contains the parameter to configure the category of all the SRN supported by GTMPSM0
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_GtmPSM0SR0_Cat
  长名称: ''
  描述: |
    The interrupt category setting of PSM0 shared service request 0 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: Irq_GtmPSM0SR1_Cat
  长名称: ''
  描述: |
    The interrupt category setting of PSM0 shared service request 1 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: Irq_GtmPSM0SR2_Cat
  长名称: ''
  描述: |
    The interrupt category setting of PSM0 shared service request 2 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: Irq_GtmPSM0SR3_Cat
  长名称: ''
  描述: |
    The interrupt category setting of PSM0 shared service request 3 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: Irq_GtmPSM0SR4_Cat
  长名称: ''
  描述: |
    The interrupt category setting of PSM0 shared service request 4 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: Irq_GtmPSM0SR5_Cat
  长名称: ''
  描述: |
    The interrupt category setting of PSM0 shared service request 5 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: Irq_GtmPSM0SR6_Cat
  长名称: ''
  描述: |
    The interrupt category setting of PSM0 shared service request 6 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: Irq_GtmPSM0SR7_Cat
  长名称: ''
  描述: |
    The interrupt category setting of PSM0 shared service request 7 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 102. Irq_GtmPSM0Prio_Config

**描述**: This container contains the parameter to configure the priority of all the SRN supported by GTMPSM0
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqGtmPSM0SR0Prio
  长名称: ''
  描述: |
    The interrupt priority setting of PSM0 shared service request 0 of GTM.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: Irq_GtmPSM0SR1_Prio
  长名称: ''
  描述: |
    The interrupt priority setting of PSM0 shared service request 1 of GTM.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: Irq_GtmPSM0SR2_Prio
  长名称: ''
  描述: |
    The interrupt priority setting of PSM0 shared service request 2 of GTM.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: Irq_GtmPSM0SR3_Prio
  长名称: ''
  描述: |
    The interrupt priority setting of PSM0 shared service request 3 of GTM.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: Irq_GtmPSM0SR4_Prio
  长名称: ''
  描述: |
    The interrupt priority setting of PSM0 shared service request 4 of GTM.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: Irq_GtmPSM0SR5_Prio
  长名称: ''
  描述: |
    The interrupt priority setting of PSM0 shared service request 5 of GTM.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: Irq_GtmPSM0SR6_Prio
  长名称: ''
  描述: |
    The interrupt priority setting of PSM0 shared service request 6 of GTM.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 8
  名称: Irq_GtmPSM0SR7_Prio
  长名称: ''
  描述: |
    The interrupt priority setting of PSM0 shared service request 7 of GTM.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
```

### 103. Irq_GtmPSM0Tos_Config

**描述**: This container contains the parameter to configure the type of service of all the SRN supported by
GTMPSM0 module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqGtmPSM0SR0Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of PSM0 shared service request 0 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: Irq_GtmPSM0SR1_Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of PSM0 shared service request 1 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: Irq_GtmPSM0SR2_Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of PSM0 shared service request 2 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: Irq_GtmPSM0SR3_Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of PSM0 shared service request 3 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: Irq_GtmPSM0SR4_Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of PSM0 shared service request 4 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: Irq_GtmPSM0SR5_Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of PSM0 shared service request 5 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: Irq_GtmPSM0SR6_Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of PSM0 shared service request 6 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: Irq_GtmPSM0SR7_Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of PSM0 shared service request 7 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 104. Irq_GtmPSM1_Config

**描述**: This container contains the GTMPSM0 interrupt configuration parameters.

该容器没有参数。

### 105. Irq_GtmPSM1Cat_Config

**描述**: This container contains the parameter to configure the category of all the SRN supported by GTM PSM1
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_GtmPSM1SR0_Cat
  长名称: ''
  描述: |
    The interrupt category setting of PSM1 shared service request 0 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: Irq_GtmPSM1SR1_Cat
  长名称: ''
  描述: |
    The interrupt category setting of PSM1 shared service request 1 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: Irq_GtmPSM1SR2_Cat
  长名称: ''
  描述: |
    The interrupt category setting of PSM1 shared service request 2 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: Irq_GtmPSM1SR3_Cat
  长名称: ''
  描述: |
    The interrupt category setting of PSM1 shared service request 3 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: Irq_GtmPSM1SR4_Cat
  长名称: ''
  描述: |
    The interrupt category setting of PSM1 shared service request 4 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: Irq_GtmPSM1SR5_Cat
  长名称: ''
  描述: |
    The interrupt category setting of PSM1 shared service request 5 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: Irq_GtmPSM1SR6_Cat
  长名称: ''
  描述: |
    The interrupt category setting of PSM1 shared service request 6 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: Irq_GtmPSM1SR7_Cat
  长名称: ''
  描述: |
    The interrupt category setting of PSM1 shared service request 7 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 106. Irq_GtmPSM1Prio_Config

**描述**: This container contains the parameter to configure the priority of all the SRN supported by GTMPSM1
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqGtmPSM1SR0Prio
  长名称: ''
  描述: |
    The interrupt priority setting of PSM1 shared service request 0 of GTM.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: Irq_GtmPSM1SR1_Prio
  长名称: ''
  描述: |
    The interrupt priority setting of PSM1 shared service request 1 of GTM.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: Irq_GtmPSM1SR2_Prio
  长名称: ''
  描述: |
    The interrupt priority setting of PSM1 shared service request 2 of GTM.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: Irq_GtmPSM1SR3_Prio
  长名称: ''
  描述: |
    The interrupt priority setting of PSM1 shared service request 3 of GTM.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: Irq_GtmPSM1SR4_Prio
  长名称: ''
  描述: |
    The interrupt priority setting of PSM1 shared service request 4 of GTM.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: Irq_GtmPSM1SR5_Prio
  长名称: ''
  描述: |
    The interrupt priority setting of PSM1 shared service request 5 of GTM.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: Irq_GtmPSM1SR6_Prio
  长名称: ''
  描述: |
    The interrupt priority setting of PSM1 shared service request 6 of GTM.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 8
  名称: Irq_GtmPSM1SR7_Prio
  长名称: ''
  描述: |
    The interrupt priority setting of PSM1 shared service request 7 of GTM.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
```

### 107. Irq_GtmPSM1Tos_Config

**描述**: This container contains the parameter to configure the type of service of all the SRN supported by
GTMPSM1 module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqGtmPSM1SR0Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of PSM1 shared service request 0 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: Irq_GtmPSM1SR1_Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of PSM1 shared service request 1 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: Irq_GtmPSM1SR2_Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of PSM1 shared service request 2 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: Irq_GtmPSM1SR3_Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of PSM1 shared service request 3 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: Irq_GtmPSM1SR4_Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of PSM1 shared service request 4 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: Irq_GtmPSM1SR5_Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of PSM1 shared service request 5 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: Irq_GtmPSM1SR6_Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of PSM1 shared service request 6 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: Irq_GtmPSM1SR7_Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of PSM1 shared service request 7 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 108. Irq_GtmPSM2_Config

**描述**: This container contains the GTMPSM2 interrupt configuration parameters.

该容器没有参数。

### 109. Irq_GtmPSM2Cat_Config

**描述**: This container contains the parameter to configure the category of all the SRN supported by GTMPSM2
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_GtmPSM2SR0_Cat
  长名称: ''
  描述: |
    The interrupt category setting of PSM2 shared service request 0 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: Irq_GtmPSM2SR1_Cat
  长名称: ''
  描述: |
    The interrupt category setting of PSM2 shared service request 1 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: Irq_GtmPSM2SR2_Cat
  长名称: ''
  描述: |
    The interrupt category setting of PSM2 shared service request 2 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: Irq_GtmPSM2SR3_Cat
  长名称: ''
  描述: |
    The interrupt category setting of PSM2 shared service request 3 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: Irq_GtmPSM2SR4_Cat
  长名称: ''
  描述: |
    The interrupt category setting of PSM2 shared service request 4 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: Irq_GtmPSM2SR5_Cat
  长名称: ''
  描述: |
    The interrupt category setting of PSM2 shared service request 5 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: Irq_GtmPSM2SR6_Cat
  长名称: ''
  描述: |
    The interrupt category setting of PSM2 shared service request 6 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: Irq_GtmPSM2SR7_Cat
  长名称: ''
  描述: |
    The interrupt category setting of PSM2 shared service request 7 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 110. Irq_GtmPSM2Prio_Config

**描述**: This container contains the parameter to configure the priority of all the SRN supported by GTMPSM2
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqGtmPSM2SR0Prio
  长名称: ''
  描述: |
    The interrupt priority setting of PSM2 shared service request 0 of GTM.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: Irq_GtmPSM2SR1_Prio
  长名称: ''
  描述: |
    The interrupt priority setting of PSM2 shared service request 1 of GTM.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: Irq_GtmPSM2SR2_Prio
  长名称: ''
  描述: |
    The interrupt priority setting of PSM2 shared service request 2 of GTM.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: Irq_GtmPSM2SR3_Prio
  长名称: ''
  描述: |
    The interrupt priority setting of PSM2 shared service request 3 of GTM.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: Irq_GtmPSM2SR4_Prio
  长名称: ''
  描述: |
    The interrupt priority setting of PSM2 shared service request 4 of GTM.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: Irq_GtmPSM2SR5_Prio
  长名称: ''
  描述: |
    The interrupt priority setting of PSM2 shared service request 5 of GTM.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: Irq_GtmPSM2SR6_Prio
  长名称: ''
  描述: |
    The interrupt priority setting of PSM2 shared service request 6 of GTM.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 8
  名称: Irq_GtmPSM2SR7_Prio
  长名称: ''
  描述: |
    The interrupt priority setting of PSM2 shared service request 7 of GTM.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
```

### 111. Irq_GtmPSM2Tos_Config

**描述**: This container contains the parameter to configure the type of service of all the SRN supported by
GTMPSM2 module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqGtmPSM2SR0Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of PSM2 shared service request 0 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: Irq_GtmPSM2SR1_Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of PSM2 shared service request 1 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: Irq_GtmPSM2SR2_Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of PSM2 shared service request 2 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: Irq_GtmPSM2SR3_Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of PSM2 shared service request 3 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: Irq_GtmPSM2SR4_Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of PSM2 shared service request 4 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: Irq_GtmPSM2SR5_Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of PSM2 shared service request 5 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: Irq_GtmPSM2SR6_Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of PSM2 shared service request 6 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: Irq_GtmPSM2SR7_Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of PSM2 shared service request 7 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 112. Irq_GtmDPLL_Config

**描述**: This container contains the GTMDPLL interrupt configuration parameters.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_GtmDPLLSR_Cat
  长名称: ''
  描述: |
    The interrupt category setting of DPLL shared service request  of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: Irq_GtmDPLLSR_Prio
  长名称: ''
  描述: |
    The interrupt priority setting of DPLL shared service request  of GTM.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: Irq_GtmDPLLSR_Tos
  长名称: ''
  描述: The interrupt type of service setting of DPLL shared service request  of GTM.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 113. Irq_GtmERR_Config

**描述**: This container contains the GTMERR interrupt configuration parameters.

该容器没有参数。

### 114. Irq_GtmERRCat_Config

**描述**: This container contains the parameter to configure the category of all the SRN supported by GTMERR
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_GtmERRSR_Cat
  长名称: ''
  描述: |
    The interrupt category setting of ERR shared service request 0 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 115. Irq_GtmERRPrio_Config

**描述**: This container contains the parameter to configure the priority of all the SRN supported by GTMERR
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: Irq_GtmERRSR_Prio
  长名称: ''
  描述: |
    The interrupt priority setting of ERR shared service request 0 of GTM.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
```

### 116. Irq_GtmERRTos_Config

**描述**: This container contains the parameter to configure the type of service of all the SRN supported by
GTMERR module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqGtmERRSRTos
  长名称: ''
  描述: The interrupt type of service setting of ERR shared service request 0 of GTM.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 117. Irq_GtmTIM_Config

**描述**: This container contains the GTM TIM interrupt configuration parameters.

该容器没有参数。

### 118. IrqGtmTIMCatConfig

**描述**: This container contains the parameter to configure the category of all the SRN supported by GTMTIM
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqGtmTIMSR0Cat
  长名称: ''
  描述: |
    The interrupt category setting of TIM shared service request 0 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqGtmTIMSR1Cat
  长名称: ''
  描述: |
    The interrupt category setting of TIM shared service request 1 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqGtmTIMSR2Cat
  长名称: ''
  描述: |
    The interrupt category setting of TIM shared service request 2 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqGtmTIMSR3Cat
  长名称: ''
  描述: |
    The interrupt category setting of TIM shared service request 3 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: IrqGtmTIMSR4Cat
  长名称: ''
  描述: |
    The interrupt category setting of TIM shared service request 4 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: IrqGtmTIMSR5Cat
  长名称: ''
  描述: |
    The interrupt category setting of TIM shared service request 5 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: IrqGtmTIMSR6Cat
  长名称: ''
  描述: |
    The interrupt category setting of TIM shared service request 6 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: IrqGtmTIMSR7Cat
  长名称: ''
  描述: |
    The interrupt category setting of TIM shared service request 7 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 119. IrqGtmTIMPrioConfig

**描述**: This container contains the parameter to configure the priority of all the SRN supported by GTMTIM
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqGtmTIMSR0Prio
  长名称: ''
  描述: |
    The interrupt priority setting of TIM shared service request 0 of GTM.
                                      The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqGtmTIMSR1Prio
  长名称: ''
  描述: |
    The interrupt priority setting of TIM shared service request 1 of GTM.
                                      The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: IrqGtmTIMSR2Prio
  长名称: ''
  描述: |
    The interrupt priority setting of TIM shared service request 2 of GTM.
                                      The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: IrqGtmTIMSR3Prio
  长名称: ''
  描述: |
    The interrupt priority setting of TIM shared service request 3 of GTM.
                                      The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: IrqGtmTIMSR4Prio
  长名称: ''
  描述: |
    The interrupt priority setting of TIM shared service request 4 of GTM.
                                      The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: IrqGtmTIMSR5Prio
  长名称: ''
  描述: |
    The interrupt priority setting of TIM shared service request 5 of GTM.
                                      The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: IrqGtmTIMSR6Prio
  长名称: ''
  描述: |
    The interrupt priority setting of TIM shared service request 6 of GTM.
                                      The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 8
  名称: IrqGtmTIMSR7Prio
  长名称: ''
  描述: |
    The interrupt priority setting of TIM shared service request 7 of GTM.
                                      The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
```

### 120. IrqGtmTIMTosConfig

**描述**: This container contains the parameter to configure the type of service of all the SRN supported by
GTMTIM module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqGtmTIMSR0Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of TIM shared service request 0 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqGtmTIMSR1Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of TIM shared service request 1 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqGtmTIMSR2Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of TIM shared service request 2 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqGtmTIMSR3Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of TIM shared service request 3 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: IrqGtmTIMSR4Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of TIM shared service request 4 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: IrqGtmTIMSR5Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of TIM shared service request 5 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: IrqGtmTIMSR6Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of TIM shared service request 6 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: IrqGtmTIMSR7Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of TIM shared service request 7 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 121. Irq_GtmMCS_Config

**描述**: This container contains the GTM MCS interrupt configuration parameters.

该容器没有参数。

### 122. IrqGtmMCSCatConfig

**描述**: This container contains the parameter to configure the category of all the SRN supported by GTMMCS
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqGtmMCSSR0Cat
  长名称: ''
  描述: |
    The interrupt category setting of MCS shared service request 0 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqGtmMCSSR1Cat
  长名称: ''
  描述: |
    The interrupt category setting of MCS shared service request 1 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqGtmMCSSR2Cat
  长名称: ''
  描述: |
    The interrupt category setting of MCS shared service request 2 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqGtmMCSSR3Cat
  长名称: ''
  描述: |
    The interrupt category setting of MCS shared service request 3 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: IrqGtmMCSSR4Cat
  长名称: ''
  描述: |
    The interrupt category setting of MCS shared service request 4 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: IrqGtmMCSSR5Cat
  长名称: ''
  描述: |
    The interrupt category setting of MCS shared service request 5 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: IrqGtmMCSSR6Cat
  长名称: ''
  描述: |
    The interrupt category setting of MCS shared service request 6 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: IrqGtmMCSSR7Cat
  长名称: ''
  描述: |
    The interrupt category setting of MCS shared service request 7 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 123. IrqGtmMCSPrioConfig

**描述**: This container contains the parameter to configure the priority of all the SRN supported by GTMMCS
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqGtmMCSSR0Prio
  长名称: ''
  描述: |
    The interrupt priority setting of MCS shared service request 0 of GTM.
                                      The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqGtmMCSSR1Prio
  长名称: ''
  描述: |
    The interrupt priority setting of MCS shared service request 1 of GTM.
                                      The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: IrqGtmMCSSR2Prio
  长名称: ''
  描述: |
    The interrupt priority setting of MCS shared service request 2 of GTM.
                                      The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: IrqGtmMCSSR3Prio
  长名称: ''
  描述: |
    The interrupt priority setting of MCS shared service request 3 of GTM.
                                      The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: IrqGtmMCSSR4Prio
  长名称: ''
  描述: |
    The interrupt priority setting of MCS shared service request 4 of GTM.
                                      The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: IrqGtmMCSSR5Prio
  长名称: ''
  描述: |
    The interrupt priority setting of MCS shared service request 5 of GTM.
                                      The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: IrqGtmMCSSR6Prio
  长名称: ''
  描述: |
    The interrupt priority setting of MCS shared service request 6 of GTM.
                                      The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 8
  名称: IrqGtmMCSSR7Prio
  长名称: ''
  描述: |
    The interrupt priority setting of MCS shared service request 7 of GTM.
                                      The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
```

### 124. IrqGtmMCSTosConfig

**描述**: This container contains the parameter to configure the type of service of all the SRN supported by
GTMMCS module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqGtmMCSSR0Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of MCS shared service request 0 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqGtmMCSSR1Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of MCS shared service request 1 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqGtmMCSSR2Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of MCS shared service request 2 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqGtmMCSSR3Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of MCS shared service request 3 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: IrqGtmMCSSR4Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of MCS shared service request 4 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: IrqGtmMCSSR5Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of MCS shared service request 5 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: IrqGtmMCSSR6Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of MCS shared service request 6 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: IrqGtmMCSSR7Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of MCS shared service request 7 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 125. Irq_GtmTOM_Config

**描述**: This container contains the GTMTOM interrupt configuration parameters.

该容器没有参数。

### 126. IrqGtmTOMCatConfig

**描述**: This container contains the parameter to configure the category of all the SRN supported by GTMTOM
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqGtmTOMSR0Cat
  长名称: ''
  描述: |
    The interrupt category setting of TOM shared service request 0 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqGtmTOMSR1Cat
  长名称: ''
  描述: |
    The interrupt category setting of TOM shared service request 1 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqGtmTOMSR2Cat
  长名称: ''
  描述: |
    The interrupt category setting of TOM shared service request 2 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqGtmTOMSR3Cat
  长名称: ''
  描述: |
    The interrupt category setting of TOM shared service request 3 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: IrqGtmTOMSR4Cat
  长名称: ''
  描述: |
    The interrupt category setting of TOM shared service request 4 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: IrqGtmTOMSR5Cat
  长名称: ''
  描述: |
    The interrupt category setting of TOM shared service request 5 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: IrqGtmTOMSR6Cat
  长名称: ''
  描述: |
    The interrupt category setting of TOM shared service request 6 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: IrqGtmTOMSR7Cat
  长名称: ''
  描述: |
    The interrupt category setting of TOM shared service request 7 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 127. IrqGtmTOMPrioConfig

**描述**: This container contains the parameter to configure the priority of all the SRN supported by GTMTOM
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqGtmTOMSR0Prio
  长名称: ''
  描述: |
    The interrupt priority setting of TOM shared service request 0 of GTM.
                                      The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqGtmTOMSR1Prio
  长名称: ''
  描述: |
    The interrupt priority setting of TOM shared service request 1 of GTM.
                                      The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: IrqGtmTOMSR2Prio
  长名称: ''
  描述: |
    The interrupt priority setting of TOM shared service request 2 of GTM.
                                      The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: IrqGtmTOMSR3Prio
  长名称: ''
  描述: |
    The interrupt priority setting of TOM shared service request 3 of GTM.
                                      The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: IrqGtmTOMSR4Prio
  长名称: ''
  描述: |
    The interrupt priority setting of TOM shared service request 4 of GTM.
                                      The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: IrqGtmTOMSR5Prio
  长名称: ''
  描述: |
    The interrupt priority setting of TOM shared service request 5 of GTM.
                                      The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: IrqGtmTOMSR6Prio
  长名称: ''
  描述: |
    The interrupt priority setting of TOM shared service request 6 of GTM.
                                      The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 8
  名称: IrqGtmTOMSR7Prio
  长名称: ''
  描述: |
    The interrupt priority setting of TOM shared service request 7 of GTM.
                                      The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
```

### 128. IrqGtmTOMTosConfig

**描述**: This container contains the parameter to configure the type of service of all the SRN supported by
GTMTOM module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqGtmTOMSR0Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of TOM shared service request 0 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqGtmTOMSR1Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of TOM shared service request 1 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqGtmTOMSR2Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of TOM shared service request 2 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqGtmTOMSR3Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of TOM shared service request 3 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: IrqGtmTOMSR4Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of TOM shared service request 4 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: IrqGtmTOMSR5Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of TOM shared service request 5 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: IrqGtmTOMSR6Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of TOM shared service request 6 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: IrqGtmTOMSR7Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of TOM shared service request 7 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 129. Irq_GtmATOM_Config

**描述**: This container contains the GTMATOM interrupt configuration parameters.

该容器没有参数。

### 130. IrqGtmATOMCatConfig

**描述**: This container contains the parameter to configure the category of all the SRN supported by GTMATOM
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqGtmATOMSR0Cat
  长名称: ''
  描述: |
    The interrupt category setting of ATOM shared service request 0 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqGtmATOMSR1Cat
  长名称: ''
  描述: |
    The interrupt category setting of ATOM shared service request 1 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqGtmATOMSR2Cat
  长名称: ''
  描述: |
    The interrupt category setting of ATOM shared service request 2 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqGtmATOMSR3Cat
  长名称: ''
  描述: |
    The interrupt category setting of ATOM shared service request 3 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 131. IrqGtmATOMPrioConfig

**描述**: This container contains the parameter to configure the priority of all the SRN supported by GTMATOM
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqGtmATOMSR0Prio
  长名称: ''
  描述: |
    The interrupt priority setting of ATOM shared service request 0 of GTM.
                                      The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqGtmATOMSR1Prio
  长名称: ''
  描述: |
    The interrupt priority setting of ATOM shared service request 1 of GTM.
                                      The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: IrqGtmATOMSR2Prio
  长名称: ''
  描述: |
    The interrupt priority setting of ATOM shared service request 2 of GTM.
                                      The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: IrqGtmATOMSR3Prio
  长名称: ''
  描述: |
    The interrupt priority setting of ATOM shared service request 3 of GTM.
                                      The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
```

### 132. IrqGtmATOMTosConfig

**描述**: This container contains the parameter to configure the type of service of all the SRN supported by
GTMATOM module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqGtmATOMSR0Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of ATOM shared service request 0 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqGtmATOMSR1Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of ATOM shared service request 1 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqGtmATOMSR2Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of ATOM shared service request 2 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqGtmATOMSR3Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of ATOM shared service request 3 of GTM.
                                      Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 133. Irq_GtmMCSW_Config

**描述**: This container contains the GTMMCSW interrupt configuration parameters.

该容器没有参数。

### 134. IrqGtmMCSWCatConfig

**描述**: This container contains the parameter to configure the category of all the SRN supported by GTMMCSW
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqGtmMCSW0Cat
  长名称: ''
  描述: |
    The interrupt category setting of MCSW shared service request 0 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqGtmMCSW1Cat
  长名称: ''
  描述: |
    The interrupt category setting of MCSW shared service request 1 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqGtmMCSW2Cat
  长名称: ''
  描述: |
    The interrupt category setting of MCSW shared service request 2 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqGtmMCSW3Cat
  长名称: ''
  描述: |
    The interrupt category setting of MCSW shared service request 3 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: IrqGtmMCSW4Cat
  长名称: ''
  描述: |
    The interrupt category setting of MCSW shared service request 4 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: IrqGtmMCSW5Cat
  长名称: ''
  描述: |
    The interrupt category setting of MCSW shared service request 5 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: IrqGtmMCSW6Cat
  长名称: ''
  描述: |
    The interrupt category setting of MCSW shared service request 6 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: IrqGtmMCSW7Cat
  长名称: ''
  描述: |
    The interrupt category setting of MCSW shared service request 7 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: IrqGtmMCSW8Cat
  长名称: ''
  描述: |
    The interrupt category setting of MCSW shared service request 8 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: IrqGtmMCSW9Cat
  长名称: ''
  描述: |
    The interrupt category setting of MCSW shared service request 9 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 135. IrqGtmMCSWPrioConfig

**描述**: This container contains the parameter to configure the priority of all the SRN supported by GTMMCSW
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqGtmMCSW0Prio
  长名称: ''
  描述: |
    The interrupt priority setting of MCSW shared service request 0 of GTM.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqGtmMCSW1Prio
  长名称: ''
  描述: |
    The interrupt priority setting of MCSW shared service request 1 of GTM.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: IrqGtmMCSW2Prio
  长名称: ''
  描述: |
    The interrupt priority setting of MCSW shared service request 2 of GTM.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: IrqGtmMCSW3Prio
  长名称: ''
  描述: |
    The interrupt priority setting of MCSW shared service request 3 of GTM.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: IrqGtmMCSW4Prio
  长名称: ''
  描述: |
    The interrupt priority setting of MCSW shared service request 4 of GTM.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: IrqGtmMCSW5Prio
  长名称: ''
  描述: |
    The interrupt priority setting of MCSW shared service request 5 of GTM.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: IrqGtmMCSW6Prio
  长名称: ''
  描述: |
    The interrupt priority setting of MCSW shared service request 6 of GTM.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 8
  名称: IrqGtmMCSW7Prio
  长名称: ''
  描述: |
    The interrupt priority setting of MCSW shared service request 7 of GTM.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 9
  名称: IrqGtmMCSW8Prio
  长名称: ''
  描述: |
    The interrupt priority setting of MCSW shared service request 8 of GTM.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 10
  名称: IrqGtmMCSW9Prio
  长名称: ''
  描述: |
    The interrupt priority setting of MCSW shared service request 9 of GTM.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
```

### 136. IrqGtmMCSWTosConfig

**描述**: This container contains the parameter to configure the type of service of all the SRN supported by
GTMMCSW module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqGtmMCSW0Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of MCSW shared service request 0 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqGtmMCSW1Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of MCSW shared service request 1 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqGtmMCSW2Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of MCSW shared service request 2 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqGtmMCSW3Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of MCSW shared service request 3 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: IrqGtmMCSW4Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of MCSW shared service request 4 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: IrqGtmMCSW5Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of MCSW shared service request 5 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: IrqGtmMCSW6Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of MCSW shared service request 6 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: IrqGtmMCSW7Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of MCSW shared service request 7 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: IrqGtmMCSW8Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of MCSW shared service request 8 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: IrqGtmMCSW9Tos
  长名称: ''
  描述: |
    The interrupt type of service setting of MCSW shared service request 9 of GTM.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 137. IrqStmConfig

**描述**: This container contains the Stm interrupt configuration parameters.

该容器没有参数。

### 138. IrqStm0Config

**描述**: This container contains the stm interrupt configuration parameters.

该容器没有参数。

### 139. IrqStm0CatConfig

**描述**: This container contains the parameter to configure the category of all the SRN supported by Stm0
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqStm0SR0Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of Stm0 Module.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqStm0SR1Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN1 of Stm0 Module.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 140. IrqStm0PrioConfig

**描述**: This container contains the parameter to configure the priority of all the SRN supported by Stm0
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqStm0SR0Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN0 of Stm0.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqStm0SR1Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN1 of Stm0.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
```

### 141. IrqStm0TosConfig

**描述**: This container contains the parameter to configure the type of service of all the SRN supported by
Stm0 module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqStm0SR0Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of Stm0 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqStm0SR1Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN1 of Stm0 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 142. IrqStm1Config

**描述**: This container contains the stm interrupt configuration parameters.

该容器没有参数。

### 143. IrqStm1CatConfig

**描述**: This container contains the parameter to configure the category of all the SRN supported by Stm1
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqStm1SR0Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of Stm1 Module.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqStm1SR1Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN1 of Stm1 Module.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 144. IrqStm1PrioConfig

**描述**: This container contains the parameter to configure the priority of all the SRN supported by Stm1
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqStm1SR0Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN0 of Stm1.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqStm1SR1Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN1 of Stm1.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
```

### 145. IrqStm1TosConfig

**描述**: This container contains the parameter to configure the type of service of all the SRN supported by
Stm1 module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqStm1SR0Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of Stm1 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqStm1SR1Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN1 of Stm1 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 146. IrqStm2Config

**描述**: This container contains the stm interrupt configuration parameters.

该容器没有参数。

### 147. IrqStm2CatConfig

**描述**: This container contains the parameter to configure the category of all the SRN supported by Stm2
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqStm2SR0Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of Stm2 Module.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqStm2SR1Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN1 of Stm2 Module.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 148. IrqStm2PrioConfig

**描述**: This container contains the parameter to configure the priority of all the SRN supported by Stm1
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqStm2SR0Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN0 of Stm2.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqStm2SR1Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN1 of Stm2.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
```

### 149. IrqStm2TosConfig

**描述**: This container contains the parameter to configure the type of service of all the SRN supported by
Stm2 module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqStm2SR0Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of Stm2 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqStm2SR1Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN1 of Stm2 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 150. IrqStm3Config

**描述**: This container contains the stm3 interrupt configuration parameters.

该容器没有参数。

### 151. IrqStm3CatConfig

**描述**: This container contains the parameter to configure the category of all the SRN supported by Stm3
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqStm3SR0Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of Stm3 Module.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqStm3SR1Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN1 of Stm3 Module.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 152. IrqStm3PrioConfig

**描述**: This container contains the parameter to configure the priority of all the SRN supported by Stm3
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqStm3SR0Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN0 of Stm3.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqStm3SR1Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN1 of Stm3.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
```

### 153. IrqStm3TosConfig

**描述**: This container contains the parameter to configure the type of service of all the SRN supported by
Stm3 module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqStm3SR0Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of Stm3 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqStm3SR1Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN1 of Stm3 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 154. IrqStm4Config

**描述**: This container contains the stm interrupt configuration parameters.

该容器没有参数。

### 155. IrqStm4CatConfig

**描述**: This container contains the parameter to configure the category of all the SRN supported by Stm4
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqStm4SR0Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of Stm4 Module.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqStm4SR1Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN1 of Stm4 Module.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 156. IrqStm4PrioConfig

**描述**: This container contains the parameter to configure the priority of all the SRN supported by Stm4
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqStm4SR0Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN0 of Stm4.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqStm4SR1Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN1 of Stm4.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
```

### 157. IrqStm4TosConfig

**描述**: This container contains the parameter to configure the type of service of all the SRN supported by
Stm4 module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqStm4SR0Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of Stm4 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqStm4SR1Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN1 of Stm4 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 158. IrqStm5Config

**描述**: This container contains the stm interrupt configuration parameters.

该容器没有参数。

### 159. IrqStm5CatConfig

**描述**: This container contains the parameter to configure the category of all the SRN supported by Stm5
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqStm5SR0Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of Stm5 Module.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqStm5SR1Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN1 of Stm5 Module.
                                    Depending upon the category the interrupt  Frame is different
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 160. IrqStm5PrioConfig

**描述**: This container contains the parameter to configure the priority of all the SRN supported by Stm5
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqStm5SR0Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN0 of Stm5.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqStm5SR1Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN1 of Stm5.
                                    The SRN number indicates the SRN configured
  默认值: 0
  最小值: 0
  最大值: 255
```

### 161. IrqStm5TosConfig

**描述**: This container contains the parameter to configure the type of service of all the SRN supported by
Stm5 module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqStm5SR0Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of Stm5 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqStm5SR1Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN1 of Stm5 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 162. IrqETHConfig

**描述**: This container contains the Ethernet interrupt configuration parameters.

该容器没有参数。

### 163. IrqETHCatConfig

**描述**: This container contains the parameter to configure the category of all the SRN supported by Ethernet
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqETHSR0Cat
  长名称: ''
  描述: |
    The interrupt category setting of Ethernet Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqETHSR1Cat
  长名称: ''
  描述: |
    The interrupt category setting of Ethernet Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqETHSR2Cat
  长名称: ''
  描述: |
    The interrupt category setting of Ethernet Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqETHSR3Cat
  长名称: ''
  描述: |
    The interrupt category setting of Ethernet Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: IrqETHSR4Cat
  长名称: ''
  描述: |
    The interrupt category setting of Ethernet Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: IrqETHSR5Cat
  长名称: ''
  描述: |
    The interrupt category setting of Ethernet Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: IrqETHSR6Cat
  长名称: ''
  描述: |
    The interrupt category setting of Ethernet Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: IrqETHSR7Cat
  长名称: ''
  描述: |
    The interrupt category setting of Ethernet Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: IrqETHSR8Cat
  长名称: ''
  描述: |
    The interrupt category setting of Ethernet Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: IrqETHSR9Cat
  长名称: ''
  描述: |
    The interrupt category setting of Ethernet Service Request.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 164. IrqETHPrioConfig

**描述**: This container contains the parameter to configure the priority of all the SRN supported by Ethernet
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqETHSR0Prio
  长名称: ''
  描述: The interrupt priority setting of Ethernet Service Request.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqETHSR1Prio
  长名称: ''
  描述: The interrupt priority setting of Ethernet Service Request.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: IrqETHSR2Prio
  长名称: ''
  描述: The interrupt priority setting of Ethernet Service Request.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: IrqETHSR3Prio
  长名称: ''
  描述: The interrupt priority setting of Ethernet Service Request.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: IrqETHSR4Prio
  长名称: ''
  描述: The interrupt priority setting of Ethernet Service Request.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: IrqETHSR5Prio
  长名称: ''
  描述: The interrupt priority setting of Ethernet Service Request.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: IrqETHSR6Prio
  长名称: ''
  描述: The interrupt priority setting of Ethernet Service Request.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 8
  名称: IrqETHSR7Prio
  长名称: ''
  描述: The interrupt priority setting of Ethernet Service Request.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 9
  名称: IrqETHSR8Prio
  长名称: ''
  描述: The interrupt priority setting of Ethernet Service Request.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 10
  名称: IrqETHSR9Prio
  长名称: ''
  描述: The interrupt priority setting of Ethernet Service Request.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 165. IrqETHTosConfig

**描述**: This container contains the parameter to configure the type of service of all the SRN supported by
Ethernet module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqETHSR0Tos
  长名称: ''
  描述: The interrupt type of service setting of Ethernet Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqETHSR1Tos
  长名称: ''
  描述: The interrupt type of service setting of Ethernet Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqETHSR2Tos
  长名称: ''
  描述: The interrupt type of service setting of Ethernet Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqETHSR3Tos
  长名称: ''
  描述: The interrupt type of service setting of Ethernet Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: IrqETHSR4Tos
  长名称: ''
  描述: The interrupt type of service setting of Ethernet Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: IrqETHSR5Tos
  长名称: ''
  描述: The interrupt type of service setting of Ethernet Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: IrqETHSR6Tos
  长名称: ''
  描述: The interrupt type of service setting of Ethernet Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: IrqETHSR7Tos
  长名称: ''
  描述: The interrupt type of service setting of Ethernet Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: IrqETHSR8Tos
  长名称: ''
  描述: The interrupt type of service setting of Ethernet Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: IrqETHSR9Tos
  长名称: ''
  描述: The interrupt type of service setting of Ethernet Service Request.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 166. IrqCanConfig

**描述**: This container contains the Can module interrupt configuration parameters.

该容器没有参数。

### 167. IrqCan0Config

**描述**: This container contains the Can module interrupt configuration parameters.

该容器没有参数。

### 168. IrqCanCatConfig

**描述**: This container contains the Can category configuration parameters.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqCanSR0Cat
  长名称: ''
  描述: The interrupt category setting of SRN0 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqCanSR1Cat
  长名称: ''
  描述: The interrupt category setting of SRN1 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqCanSR2Cat
  长名称: ''
  描述: The interrupt category setting of SRN2 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqCanSR3Cat
  长名称: ''
  描述: The interrupt category setting of SRN3 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: IrqCanSR4Cat
  长名称: ''
  描述: The interrupt category setting of SRN4 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: IrqCanSR5Cat
  长名称: ''
  描述: The interrupt category setting of SRN5 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: IrqCanSR6Cat
  长名称: ''
  描述: The interrupt category setting of SRN6 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: IrqCanSR7Cat
  长名称: ''
  描述: The interrupt category setting of SRN7 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: IrqCanSR8Cat
  长名称: ''
  描述: The interrupt category setting of SRN8 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: IrqCanSR9Cat
  长名称: ''
  描述: The interrupt category setting of SRN9 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: IrqCanSR10Cat
  长名称: ''
  描述: The interrupt category setting of SRN10 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: IrqCanSR11Cat
  长名称: ''
  描述: The interrupt category setting of SRN11 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: IrqCanSR12Cat
  长名称: ''
  描述: The interrupt category setting of SRN5 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: IrqCanSR13Cat
  长名称: ''
  描述: The interrupt category setting of SRN13 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: IrqCanSR14Cat
  长名称: ''
  描述: The interrupt category setting of SRN14 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: IrqCanSR15Cat
  长名称: ''
  描述: The interrupt category setting of SRN15 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 169. IrqCanPrioConfig

**描述**: This container contains the parameter to configure the priority of all the SRN supported by Can
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqCanSR0Prio
  长名称: ''
  描述: The interrupt priority setting of SRN0 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqCanSR1Prio
  长名称: ''
  描述: The interrupt priority setting of SRN1 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: IrqCanSR2Prio
  长名称: ''
  描述: The interrupt priority setting of SRN2 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: IrqCanSR3Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: IrqCanSR4Prio
  长名称: ''
  描述: The interrupt priority setting of SRN4 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: IrqCanSR5Prio
  长名称: ''
  描述: The interrupt priority setting of SRN5 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: IrqCanSR6Prio
  长名称: ''
  描述: The interrupt priority setting of SRN6 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 8
  名称: IrqCanSR7Prio
  长名称: ''
  描述: The interrupt priority setting of SRN7 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 9
  名称: IrqCanSR8Prio
  长名称: ''
  描述: The interrupt priority setting of SRN8 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 10
  名称: IrqCanSR9Prio
  长名称: ''
  描述: The interrupt priority setting of SRN9 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 11
  名称: IrqCanSR10Prio
  长名称: ''
  描述: The interrupt priority setting of SRN10 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 12
  名称: IrqCanSR11Prio
  长名称: ''
  描述: The interrupt priority setting of SRN11 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 13
  名称: IrqCanSR12Prio
  长名称: ''
  描述: The interrupt priority setting of SRN12 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 14
  名称: IrqCanSR13Prio
  长名称: ''
  描述: The interrupt priority setting of SRN13 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 15
  名称: IrqCanSR14Prio
  长名称: ''
  描述: The interrupt priority setting of SRN14 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 16
  名称: IrqCanSR15Prio
  长名称: ''
  描述: The interrupt priority setting of SRN15 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
```

### 170. IrqCanTosConfig

**描述**: This container contains the Can Type of Service configuration parameters.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqCanSR0Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqCanSR1Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN1 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqCanSR2Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN2 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqCanSR3Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN3 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: IrqCanSR4Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN4 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: IrqCanSR5Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN5 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: IrqCanSR6Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN6 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: IrqCanSR7Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN7 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: IrqCanSR8Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN8 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: IrqCanSR9Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN9 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: IrqCanSR10Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN10 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: IrqCanSR11Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN11 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: IrqCanSR12Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN12 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: IrqCanSR13Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN13 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: IrqCanSR14Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN14 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: IrqCanSR15Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN15 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 171. IrqCan1Config

**描述**: This container contains the Can module interrupt configuration parameters.

该容器没有参数。

### 172. IrqCanCatConfig

**描述**: This container contains the Can category configuration parameters.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqCanSR0Cat
  长名称: ''
  描述: The interrupt category setting of SRN0 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqCanSR1Cat
  长名称: ''
  描述: The interrupt category setting of SRN1 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqCanSR2Cat
  长名称: ''
  描述: The interrupt category setting of SRN2 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqCanSR3Cat
  长名称: ''
  描述: The interrupt category setting of SRN3 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: IrqCanSR4Cat
  长名称: ''
  描述: The interrupt category setting of SRN4 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: IrqCanSR5Cat
  长名称: ''
  描述: The interrupt category setting of SRN5 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: IrqCanSR6Cat
  长名称: ''
  描述: The interrupt category setting of SRN6 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: IrqCanSR7Cat
  长名称: ''
  描述: The interrupt category setting of SRN7 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: IrqCanSR8Cat
  长名称: ''
  描述: The interrupt category setting of SRN8 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: IrqCanSR9Cat
  长名称: ''
  描述: The interrupt category setting of SRN9 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: IrqCanSR10Cat
  长名称: ''
  描述: The interrupt category setting of SRN10 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: IrqCanSR11Cat
  长名称: ''
  描述: The interrupt category setting of SRN11 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: IrqCanSR12Cat
  长名称: ''
  描述: The interrupt category setting of SRN5 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: IrqCanSR13Cat
  长名称: ''
  描述: The interrupt category setting of SRN13 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: IrqCanSR14Cat
  长名称: ''
  描述: The interrupt category setting of SRN14 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: IrqCanSR15Cat
  长名称: ''
  描述: The interrupt category setting of SRN15 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 173. IrqCanPrioConfig

**描述**: This container contains the parameter to configure the priority of all the SRN supported by Can
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqCanSR0Prio
  长名称: ''
  描述: The interrupt priority setting of SRN0 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqCanSR1Prio
  长名称: ''
  描述: The interrupt priority setting of SRN1 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: IrqCanSR2Prio
  长名称: ''
  描述: The interrupt priority setting of SRN2 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: IrqCanSR3Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: IrqCanSR4Prio
  长名称: ''
  描述: The interrupt priority setting of SRN4 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: IrqCanSR5Prio
  长名称: ''
  描述: The interrupt priority setting of SRN5 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: IrqCanSR6Prio
  长名称: ''
  描述: The interrupt priority setting of SRN6 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 8
  名称: IrqCanSR7Prio
  长名称: ''
  描述: The interrupt priority setting of SRN7 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 9
  名称: IrqCanSR8Prio
  长名称: ''
  描述: The interrupt priority setting of SRN8 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 10
  名称: IrqCanSR9Prio
  长名称: ''
  描述: The interrupt priority setting of SRN9 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 11
  名称: IrqCanSR10Prio
  长名称: ''
  描述: The interrupt priority setting of SRN10 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 12
  名称: IrqCanSR11Prio
  长名称: ''
  描述: The interrupt priority setting of SRN11 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 13
  名称: IrqCanSR12Prio
  长名称: ''
  描述: The interrupt priority setting of SRN12 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 14
  名称: IrqCanSR13Prio
  长名称: ''
  描述: The interrupt priority setting of SRN13 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 15
  名称: IrqCanSR14Prio
  长名称: ''
  描述: The interrupt priority setting of SRN14 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 16
  名称: IrqCanSR15Prio
  长名称: ''
  描述: The interrupt priority setting of SRN15 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
```

### 174. IrqCanTosConfig

**描述**: This container contains the Can Type of Service configuration parameters.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqCanSR0Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqCanSR1Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN1 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqCanSR2Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN2 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqCanSR3Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN3 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: IrqCanSR4Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN4 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: IrqCanSR5Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN5 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: IrqCanSR6Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN6 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: IrqCanSR7Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN7 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: IrqCanSR8Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN8 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: IrqCanSR9Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN9 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: IrqCanSR10Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN10 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: IrqCanSR11Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN11 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: IrqCanSR12Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN12 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: IrqCanSR13Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN13 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: IrqCanSR14Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN14 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: IrqCanSR15Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN15 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 175. IrqCan2Config

**描述**: This container contains the Can module interrupt configuration parameters.

该容器没有参数。

### 176. IrqCanCatConfig

**描述**: This container contains the Can category configuration parameters.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqCanSR0Cat
  长名称: ''
  描述: The interrupt category setting of SRN0 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqCanSR1Cat
  长名称: ''
  描述: The interrupt category setting of SRN1 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqCanSR2Cat
  长名称: ''
  描述: The interrupt category setting of SRN2 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqCanSR3Cat
  长名称: ''
  描述: The interrupt category setting of SRN3 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: IrqCanSR4Cat
  长名称: ''
  描述: The interrupt category setting of SRN4 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: IrqCanSR5Cat
  长名称: ''
  描述: The interrupt category setting of SRN5 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: IrqCanSR6Cat
  长名称: ''
  描述: The interrupt category setting of SRN6 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: IrqCanSR7Cat
  长名称: ''
  描述: The interrupt category setting of SRN7 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: IrqCanSR8Cat
  长名称: ''
  描述: The interrupt category setting of SRN8 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: IrqCanSR9Cat
  长名称: ''
  描述: The interrupt category setting of SRN9 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: IrqCanSR10Cat
  长名称: ''
  描述: The interrupt category setting of SRN10 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: IrqCanSR11Cat
  长名称: ''
  描述: The interrupt category setting of SRN11 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: IrqCanSR12Cat
  长名称: ''
  描述: The interrupt category setting of SRN5 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: IrqCanSR13Cat
  长名称: ''
  描述: The interrupt category setting of SRN13 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: IrqCanSR14Cat
  长名称: ''
  描述: The interrupt category setting of SRN14 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: IrqCanSR15Cat
  长名称: ''
  描述: The interrupt category setting of SRN15 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 177. IrqCanPrioConfig

**描述**: This container contains the parameter to configure the priority of all the SRN supported by Can
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqCanSR0Prio
  长名称: ''
  描述: The interrupt priority setting of SRN0 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqCanSR1Prio
  长名称: ''
  描述: The interrupt priority setting of SRN1 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: IrqCanSR2Prio
  长名称: ''
  描述: The interrupt priority setting of SRN2 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: IrqCanSR3Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: IrqCanSR4Prio
  长名称: ''
  描述: The interrupt priority setting of SRN4 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: IrqCanSR5Prio
  长名称: ''
  描述: The interrupt priority setting of SRN5 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: IrqCanSR6Prio
  长名称: ''
  描述: The interrupt priority setting of SRN6 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 8
  名称: IrqCanSR7Prio
  长名称: ''
  描述: The interrupt priority setting of SRN7 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 9
  名称: IrqCanSR8Prio
  长名称: ''
  描述: The interrupt priority setting of SRN8 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 10
  名称: IrqCanSR9Prio
  长名称: ''
  描述: The interrupt priority setting of SRN9 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 11
  名称: IrqCanSR10Prio
  长名称: ''
  描述: The interrupt priority setting of SRN10 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 12
  名称: IrqCanSR11Prio
  长名称: ''
  描述: The interrupt priority setting of SRN11 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 13
  名称: IrqCanSR12Prio
  长名称: ''
  描述: The interrupt priority setting of SRN12 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 14
  名称: IrqCanSR13Prio
  长名称: ''
  描述: The interrupt priority setting of SRN13 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 15
  名称: IrqCanSR14Prio
  长名称: ''
  描述: The interrupt priority setting of SRN14 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 16
  名称: IrqCanSR15Prio
  长名称: ''
  描述: The interrupt priority setting of SRN15 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
```

### 178. IrqCanTosConfig

**描述**: This container contains the Can Type of Service configuration parameters.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqCanSR0Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqCanSR1Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN1 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqCanSR2Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN2 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqCanSR3Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN3 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: IrqCanSR4Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN4 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: IrqCanSR5Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN5 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: IrqCanSR6Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN6 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: IrqCanSR7Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN7 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: IrqCanSR8Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN8 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: IrqCanSR9Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN9 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: IrqCanSR10Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN10 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: IrqCanSR11Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN11 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: IrqCanSR12Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN12 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: IrqCanSR13Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN13 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: IrqCanSR14Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN14 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: IrqCanSR15Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN15 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 179. IrqCan3Config

**描述**: This container contains the Can module interrupt configuration parameters.

该容器没有参数。

### 180. IrqCanCatConfig

**描述**: This container contains the Can category configuration parameters.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqCanSR0Cat
  长名称: ''
  描述: The interrupt category setting of SRN0 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqCanSR1Cat
  长名称: ''
  描述: The interrupt category setting of SRN1 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqCanSR2Cat
  长名称: ''
  描述: The interrupt category setting of SRN2 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqCanSR3Cat
  长名称: ''
  描述: The interrupt category setting of SRN3 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: IrqCanSR4Cat
  长名称: ''
  描述: The interrupt category setting of SRN4 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: IrqCanSR5Cat
  长名称: ''
  描述: The interrupt category setting of SRN5 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: IrqCanSR6Cat
  长名称: ''
  描述: The interrupt category setting of SRN6 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: IrqCanSR7Cat
  长名称: ''
  描述: The interrupt category setting of SRN7 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: IrqCanSR8Cat
  长名称: ''
  描述: The interrupt category setting of SRN8 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: IrqCanSR9Cat
  长名称: ''
  描述: The interrupt category setting of SRN9 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: IrqCanSR10Cat
  长名称: ''
  描述: The interrupt category setting of SRN10 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: IrqCanSR11Cat
  长名称: ''
  描述: The interrupt category setting of SRN11 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: IrqCanSR12Cat
  长名称: ''
  描述: The interrupt category setting of SRN5 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: IrqCanSR13Cat
  长名称: ''
  描述: The interrupt category setting of SRN13 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: IrqCanSR14Cat
  长名称: ''
  描述: The interrupt category setting of SRN14 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: IrqCanSR15Cat
  长名称: ''
  描述: The interrupt category setting of SRN15 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 181. IrqCanPrioConfig

**描述**: This container contains the parameter to configure the priority of all the SRN supported by Can
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqCanSR0Prio
  长名称: ''
  描述: The interrupt priority setting of SRN0 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqCanSR1Prio
  长名称: ''
  描述: The interrupt priority setting of SRN1 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: IrqCanSR2Prio
  长名称: ''
  描述: The interrupt priority setting of SRN2 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: IrqCanSR3Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: IrqCanSR4Prio
  长名称: ''
  描述: The interrupt priority setting of SRN4 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: IrqCanSR5Prio
  长名称: ''
  描述: The interrupt priority setting of SRN5 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: IrqCanSR6Prio
  长名称: ''
  描述: The interrupt priority setting of SRN6 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 8
  名称: IrqCanSR7Prio
  长名称: ''
  描述: The interrupt priority setting of SRN7 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 9
  名称: IrqCanSR8Prio
  长名称: ''
  描述: The interrupt priority setting of SRN8 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 10
  名称: IrqCanSR9Prio
  长名称: ''
  描述: The interrupt priority setting of SRN9 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 11
  名称: IrqCanSR10Prio
  长名称: ''
  描述: The interrupt priority setting of SRN10 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 12
  名称: IrqCanSR11Prio
  长名称: ''
  描述: The interrupt priority setting of SRN11 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 13
  名称: IrqCanSR12Prio
  长名称: ''
  描述: The interrupt priority setting of SRN12 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 14
  名称: IrqCanSR13Prio
  长名称: ''
  描述: The interrupt priority setting of SRN13 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 15
  名称: IrqCanSR14Prio
  长名称: ''
  描述: The interrupt priority setting of SRN14 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 16
  名称: IrqCanSR15Prio
  长名称: ''
  描述: The interrupt priority setting of SRN15 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
```

### 182. IrqCanTosConfig

**描述**: This container contains the Can Type of Service configuration parameters.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqCanSR0Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqCanSR1Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN1 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqCanSR2Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN2 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqCanSR3Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN3 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: IrqCanSR4Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN4 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: IrqCanSR5Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN5 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: IrqCanSR6Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN6 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: IrqCanSR7Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN7 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: IrqCanSR8Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN8 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: IrqCanSR9Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN9 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: IrqCanSR10Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN10 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: IrqCanSR11Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN11 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: IrqCanSR12Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN12 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: IrqCanSR13Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN13 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: IrqCanSR14Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN14 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: IrqCanSR15Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN15 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 183. IrqCan4Config

**描述**: This container contains the Can module interrupt configuration parameters.

该容器没有参数。

### 184. IrqCanCatConfig

**描述**: This container contains the Can category configuration parameters.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqCanSR0Cat
  长名称: ''
  描述: The interrupt category setting of SRN0 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqCanSR1Cat
  长名称: ''
  描述: The interrupt category setting of SRN1 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqCanSR2Cat
  长名称: ''
  描述: The interrupt category setting of SRN2 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqCanSR3Cat
  长名称: ''
  描述: The interrupt category setting of SRN3 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: IrqCanSR4Cat
  长名称: ''
  描述: The interrupt category setting of SRN4 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: IrqCanSR5Cat
  长名称: ''
  描述: The interrupt category setting of SRN5 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: IrqCanSR6Cat
  长名称: ''
  描述: The interrupt category setting of SRN6 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: IrqCanSR7Cat
  长名称: ''
  描述: The interrupt category setting of SRN7 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: IrqCanSR8Cat
  长名称: ''
  描述: The interrupt category setting of SRN8 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: IrqCanSR9Cat
  长名称: ''
  描述: The interrupt category setting of SRN9 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: IrqCanSR10Cat
  长名称: ''
  描述: The interrupt category setting of SRN10 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: IrqCanSR11Cat
  长名称: ''
  描述: The interrupt category setting of SRN11 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: IrqCanSR12Cat
  长名称: ''
  描述: The interrupt category setting of SRN5 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: IrqCanSR13Cat
  长名称: ''
  描述: The interrupt category setting of SRN13 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: IrqCanSR14Cat
  长名称: ''
  描述: The interrupt category setting of SRN14 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: IrqCanSR15Cat
  长名称: ''
  描述: The interrupt category setting of SRN15 of Can Module.  Depending upon the category the
      interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 185. IrqCanPrioConfig

**描述**: This container contains the parameter to configure the priority of all the SRN supported by Can
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqCanSR0Prio
  长名称: ''
  描述: The interrupt priority setting of SRN0 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqCanSR1Prio
  长名称: ''
  描述: The interrupt priority setting of SRN1 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: IrqCanSR2Prio
  长名称: ''
  描述: The interrupt priority setting of SRN2 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: IrqCanSR3Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: IrqCanSR4Prio
  长名称: ''
  描述: The interrupt priority setting of SRN4 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: IrqCanSR5Prio
  长名称: ''
  描述: The interrupt priority setting of SRN5 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: IrqCanSR6Prio
  长名称: ''
  描述: The interrupt priority setting of SRN6 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 8
  名称: IrqCanSR7Prio
  长名称: ''
  描述: The interrupt priority setting of SRN7 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 9
  名称: IrqCanSR8Prio
  长名称: ''
  描述: The interrupt priority setting of SRN8 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 10
  名称: IrqCanSR9Prio
  长名称: ''
  描述: The interrupt priority setting of SRN9 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 11
  名称: IrqCanSR10Prio
  长名称: ''
  描述: The interrupt priority setting of SRN10 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 12
  名称: IrqCanSR11Prio
  长名称: ''
  描述: The interrupt priority setting of SRN11 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 13
  名称: IrqCanSR12Prio
  长名称: ''
  描述: The interrupt priority setting of SRN12 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 14
  名称: IrqCanSR13Prio
  长名称: ''
  描述: The interrupt priority setting of SRN13 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 15
  名称: IrqCanSR14Prio
  长名称: ''
  描述: The interrupt priority setting of SRN14 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 16
  名称: IrqCanSR15Prio
  长名称: ''
  描述: The interrupt priority setting of SRN15 of Can Module. 
  默认值: 0
  最小值: 0
  最大值: 255
```

### 186. IrqCanTosConfig

**描述**: This container contains the Can Type of Service configuration parameters.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqCanSR0Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqCanSR1Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN1 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqCanSR2Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN2 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqCanSR3Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN3 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: IrqCanSR4Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN4 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: IrqCanSR5Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN5 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: IrqCanSR6Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN6 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: IrqCanSR7Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN7 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: IrqCanSR8Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN8 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: IrqCanSR9Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN9 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: IrqCanSR10Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN10 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: IrqCanSR11Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN11 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: IrqCanSR12Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN12 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: IrqCanSR13Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN13 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: IrqCanSR14Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN14 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: IrqCanSR15Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN15 of Can Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 187. IrqAdcConfig

**描述**: This container contains the Adc interrupt configuration parameters.

该容器没有参数。

### 188. IrqAdc0Config

**描述**: This container contains the Adc0 interrupt configuration parameters.

该容器没有参数。

### 189. IrqAdc0CatConfig

**描述**: This container contains the parameter to configure the category of all the SRN supported by Adc
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqAdc0SR0Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of Adc Module. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqAdc0SR1Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN1 of Adc Module. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqAdc0SR2Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN2 of Adc Module. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqAdc0SR3Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN3 of Adc Module. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 190. IrqAdc0PrioConfig

**描述**: This container contains the parameter to configure the priority of all the SRN supported by Adc
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqAdc0SR0Prio
  长名称: ''
  描述: The interrupt priority setting of SRN0 of Adc.The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqAdc0SR1Prio
  长名称: ''
  描述: The interrupt priority setting of SRN1 of Adc.The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: IrqAdc0SR2Prio
  长名称: ''
  描述: The interrupt priority setting of SRN2 of Adc.The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: IrqAdc0SR3Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of Adc.The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 191. IrqAdc0TosConfig

**描述**: This container contains the parameter to configure the type of service of all the SRN supported by
Adc0 module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqAdc0SR0Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of Adc0 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqAdc0SR1Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN1 of Adc0 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqAdc0SR2Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN2 of Adc0 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqAdc0SR3Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN3 of Adc0 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 192. IrqAdc1Config

**描述**: This container contains the Adc1 interrupt configuration parameters.

该容器没有参数。

### 193. IrqAdc1CatConfig

**描述**: This container contains the parameter to configure the category of all the SRN supported by Adc
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqAdc1SR0Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of Adc Module. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqAdc1SR1Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN1 of Adc Module. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqAdc1SR2Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN2 of Adc Module. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqAdc1SR3Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN3 of Adc Module. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 194. IrqAdc1PrioConfig

**描述**: This container contains the parameter to configure the priority of all the SRN supported by Adc
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqAdc1SR0Prio
  长名称: ''
  描述: The interrupt priority setting of SRN0 of Adc.The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqAdc1SR1Prio
  长名称: ''
  描述: The interrupt priority setting of SRN1 of Adc.The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: IrqAdc1SR2Prio
  长名称: ''
  描述: The interrupt priority setting of SRN2 of Adc.The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: IrqAdc1SR3Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of Adc.The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 195. IrqAdc1TosConfig

**描述**: This container contains the parameter to configure the type of service of all the SRN supported by
Adc1 module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqAdc1SR0Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of Adc1 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqAdc1SR1Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN1 of Adc1 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqAdc1SR2Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN2 of Adc1 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqAdc1SR3Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN3 of Adc1 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 196. IrqAdc2Config

**描述**: This container contains the Adc2 interrupt configuration parameters.

该容器没有参数。

### 197. IrqAdc2CatConfig

**描述**: This container contains the parameter to configure the category of all the SRN supported by Adc
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqAdc2SR0Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of Adc Module. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqAdc2SR1Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN1 of Adc Module. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqAdc2SR2Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN2 of Adc Module. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqAdc2SR3Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN3 of Adc Module. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 198. IrqAdc2PrioConfig

**描述**: This container contains the parameter to configure the priority of all the SRN supported by Adc
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqAdc2SR0Prio
  长名称: ''
  描述: The interrupt priority setting of SRN0 of Adc.The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqAdc2SR1Prio
  长名称: ''
  描述: The interrupt priority setting of SRN1 of Adc.The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: IrqAdc2SR2Prio
  长名称: ''
  描述: The interrupt priority setting of SRN2 of Adc.The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: IrqAdc2SR3Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of Adc.The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 199. IrqAdc2TosConfig

**描述**: This container contains the parameter to configure the type of service of all the SRN supported by
Adc2 module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqAdc2SR0Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of Adc2 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqAdc2SR1Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN1 of Adc2 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqAdc2SR2Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN2 of Adc2 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqAdc2SR3Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN3 of Adc2 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 200. IrqAdc3Config

**描述**: This container contains the Adc3 interrupt configuration parameters.

该容器没有参数。

### 201. IrqAdc3CatConfig

**描述**: This container contains the parameter to configure the category of all the SRN supported by Adc
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqAdc3SR0Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of Adc Module. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqAdc3SR1Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN1 of Adc Module. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqAdc3SR2Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN2 of Adc Module. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqAdc3SR3Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN3 of Adc Module. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 202. IrqAdc3PrioConfig

**描述**: This container contains the parameter to configure the priority of all the SRN supported by Adc
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqAdc3SR0Prio
  长名称: ''
  描述: The interrupt priority setting of SRN0 of Adc.The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqAdc3SR1Prio
  长名称: ''
  描述: The interrupt priority setting of SRN1 of Adc.The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: IrqAdc3SR2Prio
  长名称: ''
  描述: The interrupt priority setting of SRN2 of Adc.The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: IrqAdc3SR3Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of Adc.The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 203. IrqAdc3TosConfig

**描述**: This container contains the parameter to configure the type of service of all the SRN supported by
Adc3 module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqAdc3SR0Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of Adc3 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqAdc3SR1Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN1 of Adc3 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqAdc3SR2Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN2 of Adc3 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqAdc3SR3Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN3 of Adc3 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 204. IrqAdc4Config

**描述**: This container contains the Adc4 interrupt configuration parameters.

该容器没有参数。

### 205. IrqAdc4CatConfig

**描述**: This container contains the parameter to configure the category of all the SRN supported by Adc
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqAdc4SR0Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of Adc Module. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqAdc4SR1Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN1 of Adc Module. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqAdc4SR2Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN2 of Adc Module. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqAdc4SR3Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN3 of Adc Module. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 206. IrqAdc4PrioConfig

**描述**: This container contains the parameter to configure the priority of all the SRN supported by Adc
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqAdc4SR0Prio
  长名称: ''
  描述: The interrupt priority setting of SRN0 of Adc.The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqAdc4SR1Prio
  长名称: ''
  描述: The interrupt priority setting of SRN1 of Adc.The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: IrqAdc4SR2Prio
  长名称: ''
  描述: The interrupt priority setting of SRN2 of Adc.The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: IrqAdc4SR3Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of Adc.The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 207. IrqAdc4TosConfig

**描述**: This container contains the parameter to configure the type of service of all the SRN supported by
Adc4 module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqAdc4SR0Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of Adc4 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqAdc4SR1Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN1 of Adc4 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqAdc4SR2Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN2 of Adc4 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqAdc4SR3Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN3 of Adc4 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 208. IrqAdc5Config

**描述**: This container contains the Adc5 interrupt configuration parameters.

该容器没有参数。

### 209. IrqAdc5CatConfig

**描述**: This container contains the parameter to configure the category of all the SRN supported by Adc
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqAdc5SR0Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of Adc Module. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqAdc5SR1Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN1 of Adc Module. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqAdc5SR2Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN2 of Adc Module. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqAdc5SR3Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN3 of Adc Module. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 210. IrqAdc5PrioConfig

**描述**: This container contains the parameter to configure the priority of all the SRN supported by Adc
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqAdc5SR0Prio
  长名称: ''
  描述: The interrupt priority setting of SRN0 of Adc.The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqAdc5SR1Prio
  长名称: ''
  描述: The interrupt priority setting of SRN1 of Adc.The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: IrqAdc5SR2Prio
  长名称: ''
  描述: The interrupt priority setting of SRN2 of Adc.The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: IrqAdc5SR3Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of Adc.The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 211. IrqAdc5TosConfig

**描述**: This container contains the parameter to configure the type of service of all the SRN supported by
Adc5 module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqAdc5SR0Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of Adc5 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqAdc5SR1Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN1 of Adc5 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqAdc5SR2Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN2 of Adc5 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqAdc5SR3Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN3 of Adc5 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 212. IrqAdc6Config

**描述**: This container contains the Adc6 interrupt configuration parameters.

该容器没有参数。

### 213. IrqAdc6CatConfig

**描述**: This container contains the parameter to configure the category of all the SRN supported by Adc
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqAdc6SR0Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of Adc Module. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqAdc6SR1Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN1 of Adc Module. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqAdc6SR2Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN2 of Adc Module. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqAdc6SR3Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN3 of Adc Module. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 214. IrqAdc6PrioConfig

**描述**: This container contains the parameter to configure the priority of all the SRN supported by Adc
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqAdc6SR0Prio
  长名称: ''
  描述: The interrupt priority setting of SRN0 of Adc.The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqAdc6SR1Prio
  长名称: ''
  描述: The interrupt priority setting of SRN1 of Adc.The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: IrqAdc6SR2Prio
  长名称: ''
  描述: The interrupt priority setting of SRN2 of Adc.The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: IrqAdc6SR3Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of Adc.The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 215. IrqAdc6TosConfig

**描述**: This container contains the parameter to configure the type of service of all the SRN supported by
Adc6 module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqAdc6SR0Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of Adc6 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqAdc6SR1Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN1 of Adc6 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqAdc6SR2Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN2 of Adc6 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqAdc6SR3Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN3 of Adc6 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 216. IrqAdc7Config

**描述**: This container contains the Adc7 interrupt configuration parameters.

该容器没有参数。

### 217. IrqAdc7CatConfig

**描述**: This container contains the parameter to configure the category of all the SRN supported by Adc
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqAdc7SR0Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of Adc Module. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqAdc7SR1Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN1 of Adc Module. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqAdc7SR2Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN2 of Adc Module. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqAdc7SR3Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN3 of Adc Module. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 218. IrqAdc7PrioConfig

**描述**: This container contains the parameter to configure the priority of all the SRN supported by Adc
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqAdc7SR0Prio
  长名称: ''
  描述: The interrupt priority setting of SRN0 of Adc.The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqAdc7SR1Prio
  长名称: ''
  描述: The interrupt priority setting of SRN1 of Adc.The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: IrqAdc7SR2Prio
  长名称: ''
  描述: The interrupt priority setting of SRN2 of Adc.The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: IrqAdc7SR3Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of Adc.The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 219. IrqAdc7TosConfig

**描述**: This container contains the parameter to configure the type of service of all the SRN supported by
Adc7 module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqAdc7SR0Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of Adc7 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqAdc7SR1Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN1 of Adc7 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqAdc7SR2Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN2 of Adc7 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqAdc7SR3Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN3 of Adc7 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 220. IrqAdc8Config

**描述**: This container contains the Adc8 interrupt configuration parameters.

该容器没有参数。

### 221. IrqAdc8CatConfig

**描述**: This container contains the parameter to configure the category of all the SRN supported by Adc
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqAdc8SR0Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of Adc Module. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqAdc8SR1Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN1 of Adc Module. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqAdc8SR2Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN2 of Adc Module. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqAdc8SR3Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN3 of Adc Module. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 222. IrqAdc8PrioConfig

**描述**: This container contains the parameter to configure the priority of all the SRN supported by Adc
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqAdc8SR0Prio
  长名称: ''
  描述: The interrupt priority setting of SRN0 of Adc.The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqAdc8SR1Prio
  长名称: ''
  描述: The interrupt priority setting of SRN1 of Adc.The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: IrqAdc8SR2Prio
  长名称: ''
  描述: The interrupt priority setting of SRN2 of Adc.The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: IrqAdc8SR3Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of Adc.The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 223. IrqAdc8TosConfig

**描述**: This container contains the parameter to configure the type of service of all the SRN supported by
Adc8 module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqAdc8SR0Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of Adc8 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqAdc8SR1Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN1 of Adc8 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqAdc8SR2Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN2 of Adc8 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqAdc8SR3Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN3 of Adc8 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 224. IrqAdc9Config

**描述**: This container contains the Adc9 interrupt configuration parameters.

该容器没有参数。

### 225. IrqAdc9CatConfig

**描述**: This container contains the parameter to configure the category of all the SRN supported by Adc
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqAdc9SR0Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of Adc Module. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqAdc9SR1Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN1 of Adc Module. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqAdc9SR2Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN2 of Adc Module. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqAdc9SR3Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN3 of Adc Module. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 226. IrqAdc9PrioConfig

**描述**: This container contains the parameter to configure the priority of all the SRN supported by Adc
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqAdc9SR0Prio
  长名称: ''
  描述: The interrupt priority setting of SRN0 of Adc.The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqAdc9SR1Prio
  长名称: ''
  描述: The interrupt priority setting of SRN1 of Adc.The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: IrqAdc9SR2Prio
  长名称: ''
  描述: The interrupt priority setting of SRN2 of Adc.The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: IrqAdc9SR3Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of Adc.The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 227. IrqAdc9TosConfig

**描述**: This container contains the parameter to configure the type of service of all the SRN supported by
Adc9 module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqAdc9SR0Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of Adc9 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqAdc9SR1Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN1 of Adc9 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqAdc9SR2Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN2 of Adc9 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqAdc9SR3Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN3 of Adc9 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 228. IrqAdc10Config

**描述**: This container contains the Adc10 interrupt configuration parameters.

该容器没有参数。

### 229. IrqAdc10CatConfig

**描述**: This container contains the parameter to configure the category of all the SRN supported by Adc
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqAdc10SR0Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of Adc Module. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqAdc10SR1Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN1 of Adc Module. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqAdc10SR2Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN2 of Adc Module. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqAdc10SR3Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN3 of Adc Module. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 230. IrqAdc10PrioConfig

**描述**: This container contains the parameter to configure the priority of all the SRN supported by Adc
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqAdc10SR0Prio
  长名称: ''
  描述: The interrupt priority setting of SRN0 of Adc.The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqAdc10SR1Prio
  长名称: ''
  描述: The interrupt priority setting of SRN1 of Adc.The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: IrqAdc10SR2Prio
  长名称: ''
  描述: The interrupt priority setting of SRN2 of Adc.The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: IrqAdc10SR3Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of Adc.The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 231. IrqAdc10TosConfig

**描述**: This container contains the parameter to configure the type of service of all the SRN supported by
Adc10 module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqAdc10SR0Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of Adc10 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqAdc10SR1Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN1 of Adc10 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqAdc10SR2Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN2 of Adc10 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqAdc10SR3Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN3 of Adc10 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 232. IrqAdc11Config

**描述**: This container contains the Adc10 interrupt configuration parameters.

该容器没有参数。

### 233. IrqAdc11CatConfig

**描述**: This container contains the parameter to configure the category of all the SRN supported by Adc11
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqAdc11SR0Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of Adc Module. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqAdc11SR1Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN1 of Adc Module. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqAdc11SR2Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN2 of Adc Module. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqAdc11SR3Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN3 of Adc Module. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 234. IrqAdc11PrioConfig

**描述**: This container contains the parameter to configure the priority of all the SRN supported by Adc11
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqAdc11SR0Prio
  长名称: ''
  描述: The interrupt priority setting of SRN0 of Adc.The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqAdc11SR1Prio
  长名称: ''
  描述: The interrupt priority setting of SRN1 of Adc.The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: IrqAdc11SR2Prio
  长名称: ''
  描述: The interrupt priority setting of SRN2 of Adc.The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: IrqAdc11SR3Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of Adc.The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 235. IrqAdc11TosConfig

**描述**: This container contains the parameter to configure the type of service of all the SRN supported by
Adc11 module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqAdc11SR0Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of Adc11 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqAdc11SR1Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN1 of Adc11 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqAdc11SR2Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN2 of Adc11 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqAdc11SR3Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN3 of Adc11 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 236. IrqAdcCG0Config

**描述**: This container contains the AdcCG0 interrupt configuration parameters.

该容器没有参数。

### 237. IrqAdcCG0CatConfig

**描述**: This container contains the parameter to configure the category of all the SRN supported by Adc
Common Group.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqAdcCG0SR0Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of Adc Common Group. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqAdcCG0SR1Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN1 of Adc Common Group. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqAdcCG0SR2Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN2 of Adc Common Group. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqAdcCG0SR3Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN3 of Adc Common Group. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 238. IrqAdcCG0PrioConfig

**描述**: This container contains the parameter to configure the priority of all the SRN supported by Adc
Common Group.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqAdcCG0SR0Prio
  长名称: ''
  描述: The interrupt priority setting of SRN0 of Adc Common Group.The SRN number indicates the SRN
      configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqAdcCG0SR1Prio
  长名称: ''
  描述: The interrupt priority setting of SRN1 of Adc Common Group.The SRN number indicates the SRN
      configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: IrqAdcCG0SR2Prio
  长名称: ''
  描述: The interrupt priority setting of SRN2 of Adc Common Group.The SRN number indicates the SRN
      configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: IrqAdcCG0SR3Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of Adc Common Group.The SRN number indicates the SRN
      configured.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 239. IrqAdcCG0TosConfig

**描述**: This container contains the parameter to configure the type of service of all the SRN supported by
Adc Common Group.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqAdcCG0SR0Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of Adc Common Group.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqAdcCG0SR1Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN1 of Adc Common Group.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqAdcCG0SR2Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN2 of Adc Common Group.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqAdcCG0SR3Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN3 of Adc Common Group.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 240. IrqAdcCG1Config

**描述**: This container contains the AdcCG1 interrupt configuration parameters.

该容器没有参数。

### 241. IrqAdcCG1CatConfig

**描述**: This container contains the parameter to configure the category of all the SRN supported by Adc
Common Group.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqAdcCG1SR0Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN0 of Adc Common Group. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqAdcCG1SR1Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN1 of Adc Common Group. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqAdcCG1SR2Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN2 of Adc Common Group. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqAdcCG1SR3Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN3 of Adc Common Group. The SRN number indicates the SRN
    configured.
                                    Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 242. IrqAdcCG1PrioConfig

**描述**: This container contains the parameter to configure the priority of all the SRN supported by Adc
Common Group.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqAdcCG1SR0Prio
  长名称: ''
  描述: The interrupt priority setting of SRN0 of Adc Common Group.The SRN number indicates the SRN
      configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqAdcCG1SR1Prio
  长名称: ''
  描述: The interrupt priority setting of SRN1 of Adc Common Group.The SRN number indicates the SRN
      configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: IrqAdcCG1SR2Prio
  长名称: ''
  描述: The interrupt priority setting of SRN2 of Adc Common Group.The SRN number indicates the SRN
      configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: IrqAdcCG1SR3Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of Adc Common Group.The SRN number indicates the SRN
      configured.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 243. IrqAdcCG1TosConfig

**描述**: This container contains the parameter to configure the type of service of all the SRN supported by
Adc Common Group.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqAdcCG1SR0Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of Adc Common Group.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqAdcCG1SR1Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN1 of Adc Common Group.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqAdcCG1SR2Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN2 of Adc Common Group.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqAdcCG1SR3Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN3 of Adc Common Group.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 244. IrqDMUConfig

**描述**: This container contains the DMU interrupt configuration parameters.

该容器没有参数。

### 245. IrqDMUCatConfig

**描述**: This container contains the parameter to configure the category of all the SRN supported by DMU
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqDMUHOSTCat
  长名称: ''
  描述: |
    The interrupt category setting of DMU HOST.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqDMUFSICat
  长名称: ''
  描述: |
    The interrupt category setting of DMU FSI.
                                  Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 246. IrqDMUPrioConfig

**描述**: This container contains the parameter to configure the priority of all the SRN supported by DMU
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqDMUHOSTPrio
  长名称: ''
  描述: The interrupt priority setting of DMU HOST.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqDMUFSIPrio
  长名称: ''
  描述: The interrupt priority setting of DMU FSI.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 247. IrqDMUTosConfig

**描述**: This container contains the parameter to configure the type of service of all the SRN supported by
DMU module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqDMUHOSTTos
  长名称: ''
  描述: The interrupt type of service setting of DMU HOST.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqDMUFSITos
  长名称: ''
  描述: The interrupt type of service setting of DMU FSI.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 248. IrqASCLINConfig

**描述**: This container contains the ASCLIN module interrupt nodes configuration parameters.

该容器没有参数。

### 249. IrqAsclinCatConfig

**描述**: This container contains parameters to configure the interrupt category of all SRN supported by
ASCLIN module.

该容器没有参数。

### 250. IrqAsclinTxCatConfig

**描述**: This container contains the parameter to configure the category of all the Transmit SRN supported by
Asclin module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqAsclin0TxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNTx of Asclin0 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqAsclin1TxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNTx of Asclin1 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqAsclin2TxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNTx of Asclin2 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqAsclin3TxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNTx of Asclin3 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: IrqAsclin4TxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNTx of Asclin4 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: IrqAsclin5TxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNTx of Asclin5 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: IrqAsclin6TxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNTx of Asclin6 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: IrqAsclin7TxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNTx of Asclin7 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: IrqAsclin8TxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNTx of Asclin8 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: IrqAsclin9TxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNTx of Asclin9 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: IrqAsclin10TxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNTx of Asclin10 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: IrqAsclin11TxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNTx of Asclin11 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: IrqAsclin12TxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNTx of Asclin12 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: IrqAsclin13TxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNTx of Asclin13 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: IrqAsclin14TxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNTx of Asclin14 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: IrqAsclin15TxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNTx of Asclin15 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 17
  名称: IrqAsclin16TxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNTx of Asclin16 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 18
  名称: IrqAsclin17TxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNTx of Asclin17 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 19
  名称: IrqAsclin18TxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNTx of Asclin18 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 20
  名称: IrqAsclin19TxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNTx of Asclin19 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 21
  名称: IrqAsclin20TxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNTx of Asclin20 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 22
  名称: IrqAsclin21TxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNTx of Asclin21 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 23
  名称: IrqAsclin22TxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNTx of Asclin22 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 24
  名称: IrqAsclin23TxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNTx of Asclin23 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 251. IrqAsclinRxCatConfig

**描述**: This container contains the parameter to configure the category of all the Receive SRN supported by
Asclin module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqAsclin0RxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNRx of Asclin0 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqAsclin1RxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNRx of Asclin1 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqAsclin2RxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNRx of Asclin2 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqAsclin3RxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNRx of Asclin3 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: IrqAsclin4RxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNRx of Asclin4 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: IrqAsclin5RxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNRx of Asclin5 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: IrqAsclin6RxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNRx of Asclin6 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: IrqAsclin7RxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNRx of Asclin7 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: IrqAsclin8RxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNRx of Asclin8 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: IrqAsclin9RxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNRx of Asclin9 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: IrqAsclin10RxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNRx of Asclin10 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: IrqAsclin11RxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNRx of Asclin11 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: IrqAsclin12RxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNRx of Asclin12 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: IrqAsclin13RxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNRx of Asclin13 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: IrqAsclin14RxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNRx of Asclin14 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: IrqAsclin15RxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNRx of Asclin15 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 17
  名称: IrqAsclin16RxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNRx of Asclin16 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 18
  名称: IrqAsclin17RxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNRx of Asclin17 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 19
  名称: IrqAsclin18RxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNRx of Asclin18 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 20
  名称: IrqAsclin19RxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNRx of Asclin19 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 21
  名称: IrqAsclin20RxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNRx of Asclin20 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 22
  名称: IrqAsclin21RxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNRx of Asclin21 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 23
  名称: IrqAsclin22RxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNRx of Asclin22 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 24
  名称: IrqAsclin23RxCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNRx of Asclin23 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 252. IrqAsclinErrCatConfig

**描述**: This container contains the parameter to configure the category of all the Error SRN supported by
Asclin module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqAsclin0ErrCat
  长名称: ''
  描述: |
    The interrupt category setting of SRN Err of Asclin0 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqAsclin1ErrCat
  长名称: ''
  描述: |
    The interrupt category setting of SRN Err of Asclin1 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqAsclin2ErrCat
  长名称: ''
  描述: |
    The interrupt category setting of SRN Err of Asclin2 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqAsclin3ErrCat
  长名称: ''
  描述: |
    The interrupt category setting of SRN Err of Asclin3 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: IrqAsclin4ErrCat
  长名称: ''
  描述: |
    The interrupt category setting of SRN Err of Asclin4 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: IrqAsclin5ErrCat
  长名称: ''
  描述: |
    The interrupt category setting of SRN Err of Asclin5 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: IrqAsclin6ErrCat
  长名称: ''
  描述: |
    The interrupt category setting of SRN Err of Asclin6 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: IrqAsclin7ErrCat
  长名称: ''
  描述: |
    The interrupt category setting of SRN Err of Asclin7 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: IrqAsclin8ErrCat
  长名称: ''
  描述: |
    The interrupt category setting of SRN Err of Asclin8 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: IrqAsclin9ErrCat
  长名称: ''
  描述: |
    The interrupt category setting of SRN Err of Asclin9 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: IrqAsclin10ErrCat
  长名称: ''
  描述: |
    The interrupt category setting of SRN Err of Asclin10 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: IrqAsclin11ErrCat
  长名称: ''
  描述: |
    The interrupt category setting of SRN Err of Asclin11 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: IrqAsclin12ErrCat
  长名称: ''
  描述: |
    The interrupt category setting of SRN Err of Asclin12 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: IrqAsclin13ErrCat
  长名称: ''
  描述: |
    The interrupt category setting of SRN Err of Asclin13 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: IrqAsclin14ErrCat
  长名称: ''
  描述: |
    The interrupt category setting of SRN Err of Asclin14 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: IrqAsclin15ErrCat
  长名称: ''
  描述: |
    The interrupt category setting of SRN Err of Asclin15 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 17
  名称: IrqAsclin16ErrCat
  长名称: ''
  描述: |
    The interrupt category setting of SRN Err of Asclin16 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 18
  名称: IrqAsclin17ErrCat
  长名称: ''
  描述: |
    The interrupt category setting of SRN Err of Asclin17 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 19
  名称: IrqAsclin18ErrCat
  长名称: ''
  描述: |
    The interrupt category setting of SRN Err of Asclin18 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 20
  名称: IrqAsclin19ErrCat
  长名称: ''
  描述: |
    The interrupt category setting of SRN Err of Asclin19 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 21
  名称: IrqAsclin20ErrCat
  长名称: ''
  描述: |
    The interrupt category setting of SRN Err of Asclin20 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 22
  名称: IrqAsclin21ErrCat
  长名称: ''
  描述: |
    The interrupt category setting of SRN Err of Asclin21 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 23
  名称: IrqAsclin22ErrCat
  长名称: ''
  描述: |
    The interrupt category setting of SRN Err of Asclin22 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 24
  名称: IrqAsclin23ErrCat
  长名称: ''
  描述: |
    The interrupt category setting of SRN Err of Asclin23 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 253. IrqAsclinPrioConfig

**描述**: This container contains the parameter to configure the priority of all the SRN supported by Asclin
module.

该容器没有参数。

### 254. IrqAsclinTxPrioConfig

**描述**: This container contains the parameter to configure the priority of all the Transmit SRN supported by
Asclin module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqAsclin0TxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNTx of Asclin0.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqAsclin1TxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNTx of Asclin1.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: IrqAsclin2TxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNTx of Asclin2.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: IrqAsclin3TxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNTx of Asclin3.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: IrqAsclin4TxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNTx of Asclin4.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: IrqAsclin5TxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNTx of Asclin5.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: IrqAsclin6TxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNTx of Asclin6.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 8
  名称: IrqAsclin7TxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNTx of Asclin7.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 9
  名称: IrqAsclin8TxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNTx of Asclin8.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 10
  名称: IrqAsclin9TxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNTx of Asclin9.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 11
  名称: IrqAsclin10TxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNTx of Asclin10.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 12
  名称: IrqAsclin11TxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNTx of Asclin11.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 13
  名称: IrqAsclin12TxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNTx of Asclin12.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 14
  名称: IrqAsclin13TxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNTx of Asclin13.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 15
  名称: IrqAsclin14TxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNTx of Asclin14.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 16
  名称: IrqAsclin15TxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNTx of Asclin15.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 17
  名称: IrqAsclin16TxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNTx of Asclin16.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 18
  名称: IrqAsclin17TxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNTx of Asclin17.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 19
  名称: IrqAsclin18TxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNTx of Asclin18.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 20
  名称: IrqAsclin19TxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNTx of Asclin19.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 21
  名称: IrqAsclin20TxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNTx of Asclin20.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 22
  名称: IrqAsclin21TxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNTx of Asclin21.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 23
  名称: IrqAsclin22TxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNTx of Asclin22.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 24
  名称: IrqAsclin23TxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNTx of Asclin23.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 255. IrqAsclinRxPrioConfig

**描述**: This container contains the parameter to configure the priority of all the Receive SRN supported by
Asclin module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqAsclin0RxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNRx of AscLin0.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqAsclin1RxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNRx of AscLin1.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: IrqAsclin2RxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNRx of AscLin2.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: IrqAsclin3RxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNRx of AscLin3.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: IrqAsclin4RxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNRx of AscLin4.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: IrqAsclin5RxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNRx of AscLin5.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: IrqAsclin6RxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNRx of AscLin6.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 8
  名称: IrqAsclin7RxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNRx of AscLin7.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 9
  名称: IrqAsclin8RxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNRx of Asclin8.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 10
  名称: IrqAsclin9RxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNRx of Asclin9.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 11
  名称: IrqAsclin10RxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNRx of Asclin10.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 12
  名称: IrqAsclin11RxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNRx of Asclin11.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 13
  名称: IrqAsclin12RxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNRx of Asclin12.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 14
  名称: IrqAsclin13RxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNRx of Asclin13.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 15
  名称: IrqAsclin14RxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNRx of Asclin14.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 16
  名称: IrqAsclin15RxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNRx of Asclin15.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 17
  名称: IrqAsclin16RxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNRx of Asclin16.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 18
  名称: IrqAsclin17RxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNRx of Asclin17.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 19
  名称: IrqAsclin18RxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNRx of Asclin18.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 20
  名称: IrqAsclin19RxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNRx of Asclin19.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 21
  名称: IrqAsclin20RxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNRx of Asclin20.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 22
  名称: IrqAsclin21RxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNRx of Asclin21.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 23
  名称: IrqAsclin22RxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNRx of Asclin22.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 24
  名称: IrqAsclin23RxPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNRx of Asclin23.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 256. IrqAsclinErrPrioConfig

**描述**: This container contains the parameter to configure the priority of all the Error SRN supported by
Asclin module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqAsclin0ErrPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN Error of Asclin0.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqAsclin1ErrPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN Error of Asclin1.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: IrqAsclin2ErrPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN Error of Asclin2.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: IrqAsclin3ErrPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN Error of Asclin3.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: IrqAsclin4ErrPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN Error of Asclin4.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: IrqAsclin5ErrPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN Error of Asclin5.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: IrqAsclin6ErrPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN Error of Asclin6.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 8
  名称: IrqAsclin7ErrPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN Error of Asclin7.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 9
  名称: IrqAsclin8ErrPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN Error of Asclin8.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 10
  名称: IrqAsclin9ErrPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN Error of Asclin9.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 11
  名称: IrqAsclin10ErrPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN Error of Asclin10.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 12
  名称: IrqAsclin11ErrPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN Error of Asclin11.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 13
  名称: IrqAsclin12ErrPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN Error of Asclin12.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 14
  名称: IrqAsclin13ErrPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN Error of Asclin13.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 15
  名称: IrqAsclin14ErrPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN Error of Asclin14.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 16
  名称: IrqAsclin15ErrPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN Error of Asclin15.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 17
  名称: IrqAsclin16ErrPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN Error of Asclin16.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 18
  名称: IrqAsclin17ErrPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN Error of Asclin17.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 19
  名称: IrqAsclin18ErrPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN Error of Asclin18.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 20
  名称: IrqAsclin19ErrPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN Error of Asclin19.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 21
  名称: IrqAsclin20ErrPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN Error of Asclin20.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 22
  名称: IrqAsclin21ErrPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN Error of Asclin21.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 23
  名称: IrqAsclin22ErrPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN Error of Asclin22.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 24
  名称: IrqAsclin23ErrPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN Error of Asclin23.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 257. IrqAsclinTosConfig

**描述**: This container contains the Asclin interrupt configuration parameters.

该容器没有参数。

### 258. IrqAsclinTxTosConfig

**描述**: This container contains the parameter to configure the Type of service of all the Transmit SRN
supported by Asclin module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqAsclin0TxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNTx of Asclin0 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqAsclin1TxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNTx of Asclin1 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqAsclin2TxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNTx of Asclin2 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqAsclin3TxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNTx of Asclin3 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: IrqAsclin4TxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNTx of Asclin4 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: IrqAsclin5TxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNTx of Asclin5 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: IrqAsclin6TxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNTx of Asclin6 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: IrqAsclin7TxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNTx of Asclin7 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: IrqAsclin8TxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNTx of Asclin8 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: IrqAsclin9TxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNTx of Asclin9 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: IrqAsclin10TxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNTx of Asclin10 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: IrqAsclin11TxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNTx of Asclin11 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: IrqAsclin12TxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNTx of Asclin12 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: IrqAsclin13TxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNTx of Asclin13 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: IrqAsclin14TxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNTx of Asclin14 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: IrqAsclin15TxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNTx of Asclin15 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 17
  名称: IrqAsclin16TxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNTx of Asclin16 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 18
  名称: IrqAsclin17TxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNTx of Asclin17 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 19
  名称: IrqAsclin18TxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNTx of Asclin18 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 20
  名称: IrqAsclin19TxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNTx of Asclin19 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 21
  名称: IrqAsclin20TxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNTx of Asclin20 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 22
  名称: IrqAsclin21TxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNTx of Asclin21 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 23
  名称: IrqAsclin22TxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNTx of Asclin22 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 24
  名称: IrqAsclin23TxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNTx of Asclin23 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 259. IrqAsclinRxTosConfig

**描述**: This container contains the parameter to configure the Type of service of all the Transmit SRN
supported by Asclin module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqAsclin0RxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNRx of Asclin0 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqAsclin1RxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNRx of Asclin1 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqAsclin2RxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNRx of Asclin2 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqAsclin3RxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNRx of Asclin3 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: IrqAsclin4RxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNRx of Asclin4 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: IrqAsclin5RxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNRx of Asclin5 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: IrqAsclin6RxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNRx of Asclin6 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: IrqAsclin7RxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNRx of Asclin7 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: IrqAsclin8RxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNRx of Asclin8 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: IrqAsclin9RxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNRx of Asclin9 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: IrqAsclin10RxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNRx of Asclin10 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: IrqAsclin11RxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNRx of Asclin11 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: IrqAsclin12RxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNRx of Asclin12 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: IrqAsclin13RxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNRx of Asclin13 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: IrqAsclin14RxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNRx of Asclin14 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: IrqAsclin15RxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNRx of Asclin15 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 17
  名称: IrqAsclin16RxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNRx of Asclin16 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 18
  名称: IrqAsclin17RxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNRx of Asclin17 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 19
  名称: IrqAsclin18RxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNRx of Asclin18 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 20
  名称: IrqAsclin19RxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNRx of Asclin19 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 21
  名称: IrqAsclin20RxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNRx of Asclin20 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 22
  名称: IrqAsclin21RxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNRx of Asclin21 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 23
  名称: IrqAsclin22RxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNRx of Asclin22 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 24
  名称: IrqAsclin23RxTos
  长名称: ''
  描述: The interrupt type of service setting of SRNRx of Asclin23 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 260. IrqAsclinErrTosConfig

**描述**: This container contains the parameter to configure the Type of service of all the Transmit SRN
supported by Asclin module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqAsclin0ErrTos
  长名称: ''
  描述: The interrupt type of service setting of SRN Err of Asclin0 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqAsclin1ErrTos
  长名称: ''
  描述: The interrupt type of service setting of SRN Err of Asclin1 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqAsclin2ErrTos
  长名称: ''
  描述: The interrupt type of service setting of SRN Err of Asclin2 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqAsclin3ErrTos
  长名称: ''
  描述: The interrupt type of service setting of SRN Err of Asclin3 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: IrqAsclin4ErrTos
  长名称: ''
  描述: The interrupt type of service setting of SRN Err of Asclin4 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: IrqAsclin5ErrTos
  长名称: ''
  描述: The interrupt type of service setting of SRN Err of Asclin5 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: IrqAsclin6ErrTos
  长名称: ''
  描述: The interrupt type of service setting of SRN Err of Asclin6 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: IrqAsclin7ErrTos
  长名称: ''
  描述: The interrupt type of service setting of SRN Err of Asclin7 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: IrqAsclin8ErrTos
  长名称: ''
  描述: The interrupt type of service setting of SRN Err of Asclin8 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: IrqAsclin9ErrTos
  长名称: ''
  描述: The interrupt type of service setting of SRN Err of Asclin9 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: IrqAsclin10ErrTos
  长名称: ''
  描述: The interrupt type of service setting of SRN Err of Asclin10 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: IrqAsclin11ErrTos
  长名称: ''
  描述: The interrupt type of service setting of SRN Err of Asclin11 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: IrqAsclin12ErrTos
  长名称: ''
  描述: The interrupt type of service setting of SRN Err of Asclin12 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: IrqAsclin13ErrTos
  长名称: ''
  描述: The interrupt type of service setting of SRN Err of Asclin13 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 15
  名称: IrqAsclin14ErrTos
  长名称: ''
  描述: The interrupt type of service setting of SRN Err of Asclin14 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 16
  名称: IrqAsclin15ErrTos
  长名称: ''
  描述: The interrupt type of service setting of SRN Err of Asclin15 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 17
  名称: IrqAsclin16ErrTos
  长名称: ''
  描述: The interrupt type of service setting of SRN Err of Asclin16 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 18
  名称: IrqAsclin17ErrTos
  长名称: ''
  描述: The interrupt type of service setting of SRN Err of Asclin17 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 19
  名称: IrqAsclin18ErrTos
  长名称: ''
  描述: The interrupt type of service setting of SRN Err of Asclin18 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 20
  名称: IrqAsclin19ErrTos
  长名称: ''
  描述: The interrupt type of service setting of SRN Err of Asclin19 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 21
  名称: IrqAsclin20ErrTos
  长名称: ''
  描述: The interrupt type of service setting of SRN Err of Asclin20 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 22
  名称: IrqAsclin21ErrTos
  长名称: ''
  描述: The interrupt type of service setting of SRN Err of Asclin21 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 23
  名称: IrqAsclin22ErrTos
  长名称: ''
  描述: The interrupt type of service setting of SRN Err of Asclin22 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 24
  名称: IrqAsclin23ErrTos
  长名称: ''
  描述: The interrupt type of service setting of SRN Err of Asclin23 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 261. IrqHsslConfig

**描述**: This container contains the Hssl interrupt configuration parameters.

该容器没有参数。

### 262. IrqHssl0Config

**描述**: This container contains the Hssl0 interrupt configuration parameters.

该容器没有参数。

### 263. IrqHssl0CatConfig

**描述**: This container contains the parameter to configure the category of all the SRN supported by Hssl
module.

该容器没有参数。

### 264. IrqHssl0COKCatConfig

**描述**: This container contains the parameter to configure the category of all the Transmit SRN supported by
Hssl module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqHssl0COK_0Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRNCOK of Hssl0_0 Module.
                                      Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqHssl0COK_1Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRNCOK of Hssl0_1 Module.
                                      Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqHssl0COK_2Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRNCOK of Hssl0_2 Module.
                                      Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqHssl0COK_3Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRNCOK of Hssl0_3 Module.
                                      Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 265. IrqHssl0RDICatConfig

**描述**: This container contains the parameter to configure the category of all the Transmit SRN supported by
Hssl module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqHssl0RDI_0Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRNRDI of Hssl0_0 Module.
                                      Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqHssl0RDI_1Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRNRDI of Hssl0_1 Module.
                                      Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqHssl0RDI_2Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRNRDI of Hssl0_2 Module.
                                      Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqHssl0RDI_3Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRNRDI of Hssl0_3 Module.
                                      Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 266. IrqHssl0ERRCatConfig

**描述**: This container contains the parameter to configure the category of all the Transmit SRN supported by
Hssl module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqHssl0ERR_0Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRNERR of Hssl0_0 Module.
                                      Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqHssl0ERR_1Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRNERR of Hssl0_1 Module.
                                      Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqHssl0ERR_2Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRNERR of Hssl0_2 Module.
                                      Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqHssl0ERR_3Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRNERR of Hssl0_3 Module.
                                      Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 267. IrqHssl0TRGCatConfig

**描述**: This container contains the parameter to configure the category of all the Transmit SRN supported by
Hssl module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqHssl0TRG_0Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRNTRG of Hssl0_0 Module.
                                      Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqHssl0TRG_1Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRNTRG of Hssl0_1 Module.
                                      Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqHssl0TRG_2Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRNTRG of Hssl0_2 Module.
                                      Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqHssl0TRG_3Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRNTRG of Hssl0_3 Module.
                                      Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 268. IrqHssl0EXICatConfig

**描述**: This container contains the parameter to configure the category of all the Transmit SRN supported by
Hssl module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqHssl0EXICat
  长名称: ''
  描述: |
    The interrupt category setting of SRNEXI of Hssl0 Module.
                                      Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 269. IrqHssl0PrioConfig

**描述**: This container contains the parameter to configure the priority of all the SRN supported by Hssl
module.

该容器没有参数。

### 270. IrqHssl0COKPrioConfig

**描述**: This container contains the parameter to configure the priority of all the Transmit SRN supported by
Hssl module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqHssl0COK_0Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNCOK of Hssl0.
                                      The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqHssl0COK_1Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNCOK of Hssl0.
                                      The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: IrqHssl0COK_2Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNCOK of Hssl0.
                                      The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: IrqHssl0COK_3Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNCOK of Hssl0.
                                      The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 271. IrqHssl0RDIPrioConfig

**描述**: This container contains the parameter to configure the priority of all the Transmit SRN supported by
Hssl module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqHssl0RDI_0Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNRDI of Hssl0.
                                      The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqHssl0RDI_1Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNRDI of Hssl0.
                                      The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: IrqHssl0RDI_2Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNRDI of Hssl0.
                                      The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: IrqHssl0RDI_3Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNRDI of Hssl0.
                                      The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 272. IrqHssl0ERRPrioConfig

**描述**: This container contains the parameter to configure the priority of all the Transmit SRN supported by
Hssl module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqHssl0ERR_0Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNERR of Hssl0.
                                      The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqHssl0ERR_1Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNERR of Hssl0.
                                      The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: IrqHssl0ERR_2Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNERR of Hssl0.
                                      The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: IrqHssl0ERR_3Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNERR of Hssl0.
                                      The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 273. IrqHssl0TRGPrioConfig

**描述**: This container contains the parameter to configure the priority of all the Transmit SRN supported by
Hssl module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqHssl0TRG_0Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNTRG of Hssl0.
                                      The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqHssl0TRG_1Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNTRG of Hssl0.
                                      The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: IrqHssl0TRG_2Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNTRG of Hssl0.
                                      The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: IrqHssl0TRG_3Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNTRG of Hssl0.
                                      The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 274. IrqHssl0EXIPrioConfig

**描述**: This container contains the parameter to configure the priority of all the Transmit SRN supported by
Hssl module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqHssl0EXIPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNEXI of Hssl0.
                                      The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 275. IrqHssl0TosConfig

**描述**: This container contains the parameter to configure the type of service of all the SRN supported by
Hssl0 module.

该容器没有参数。

### 276. IrqHssl0COKTosConfig

**描述**: This container contains the parameter to configure the Type of service of all the Transmit SRN
supported by Hssl module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqHssl0COK_0Tos
  长名称: ''
  描述: The interrupt type of service setting of SRNCOK of Hssl0 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqHssl0COK_1Tos
  长名称: ''
  描述: The interrupt type of service setting of SRNCOK of Hssl0 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqHssl0COK_2Tos
  长名称: ''
  描述: The interrupt type of service setting of SRNCOK of Hssl0 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqHssl0COK_3Tos
  长名称: ''
  描述: The interrupt type of service setting of SRNCOK of Hssl0 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 277. IrqHssl0RDITosConfig

**描述**: This container contains the parameter to configure the Type of service of all the Transmit SRN
supported by Hssl module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqHssl0RDI_0Tos
  长名称: ''
  描述: The interrupt type of service setting of SRNRDI of Hssl0 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqHssl0RDI_1Tos
  长名称: ''
  描述: The interrupt type of service setting of SRNRDI of Hssl0 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqHssl0RDI_2Tos
  长名称: ''
  描述: The interrupt type of service setting of SRNRDI of Hssl0 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqHssl0RDI_3Tos
  长名称: ''
  描述: The interrupt type of service setting of SRNRDI of Hssl0 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 278. IrqHssl0ERRTosConfig

**描述**: This container contains the parameter to configure the Type of service of all the Transmit SRN
supported by Hssl module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqHssl0ERR_0Tos
  长名称: ''
  描述: The interrupt type of service setting of SRNERR of Hssl0 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqHssl0ERR_1Tos
  长名称: ''
  描述: The interrupt type of service setting of SRNERR of Hssl0 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqHssl0ERR_2Tos
  长名称: ''
  描述: The interrupt type of service setting of SRNERR of Hssl0 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqHssl0ERR_3Tos
  长名称: ''
  描述: The interrupt type of service setting of SRNERR of Hssl0 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 279. IrqHssl0TRGTosConfig

**描述**: This container contains the parameter to configure the Type of service of all the Transmit SRN
supported by Hssl module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqHssl0TRG_0Tos
  长名称: ''
  描述: The interrupt type of service setting of SRNTRG of Hssl0 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqHssl0TRG_1Tos
  长名称: ''
  描述: The interrupt type of service setting of SRNTRG of Hssl0 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqHssl0TRG_2Tos
  长名称: ''
  描述: The interrupt type of service setting of SRNTRG of Hssl0 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqHssl0TRG_3Tos
  长名称: ''
  描述: The interrupt type of service setting of SRNTRG of Hssl0 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 280. IrqHssl0EXITosConfig

**描述**: This container contains the parameter to configure the Type of service of all the Transmit SRN
supported by Hssl module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqHssl0EXITos
  长名称: ''
  描述: The interrupt type of service setting of SRNEXI of Hssl0 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 281. IrqHssl1Config

**描述**: This container contains the Hssl1 interrupt configuration parameters.

该容器没有参数。

### 282. IrqHssl1CatConfig

**描述**: This container contains the parameter to configure the category of all the SRN supported by Hssl
module.

该容器没有参数。

### 283. IrqHssl1COKCatConfig

**描述**: This container contains the parameter to configure the category of all the Transmit SRN supported by
Hssl module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqHssl1COK_0Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRNCOK of Hssl1_0 Module.
                                      Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqHssl1COK_1Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRNCOK of Hssl1_1 Module.
                                      Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqHssl1COK_2Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRNCOK of Hssl1_2 Module.
                                      Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqHssl1COK_3Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRNCOK of Hssl1_3 Module.
                                      Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 284. IrqHssl1RDICatConfig

**描述**: This container contains the parameter to configure the category of all the Transmit SRN supported by
Hssl module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqHssl1RDI_0Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRNRDI of Hssl1_0 Module.
                                      Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqHssl1RDI_1Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRNRDI of Hssl1_1 Module.
                                      Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqHssl1RDI_2Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRNRDI of Hssl1_2 Module.
                                      Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqHssl1RDI_3Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRNRDI of Hssl1_3 Module.
                                      Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 285. IrqHssl1ERRCatConfig

**描述**: This container contains the parameter to configure the category of all the Transmit SRN supported by
Hssl module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqHssl1ERR_0Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRNERR of Hssl1_0 Module.
                                      Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqHssl1ERR_1Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRNERR of Hssl1_1 Module.
                                      Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqHssl1ERR_2Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRNERR of Hssl1_2 Module.
                                      Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqHssl1ERR_3Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRNERR of Hssl1_3 Module.
                                      Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 286. IrqHssl1TRGCatConfig

**描述**: This container contains the parameter to configure the category of all the Transmit SRN supported by
Hssl module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqHssl1TRG_0Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRNTRG of Hssl1_0 Module.
                                      Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqHssl1TRG_1Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRNTRG of Hssl1_1 Module.
                                      Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqHssl1TRG_2Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRNTRG of Hssl1_2 Module.
                                      Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqHssl1TRG_3Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRNTRG of Hssl1_3 Module.
                                      Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 287. IrqHssl1EXICatConfig

**描述**: This container contains the parameter to configure the category of all the Transmit SRN supported by
Hssl module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqHssl1EXICat
  长名称: ''
  描述: |
    The interrupt category setting of SRNEXI of Hssl1 Module.
                                      Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 288. IrqHssl1PrioConfig

**描述**: This container contains the parameter to configure the priority of all the SRN supported by Hssl
module.

该容器没有参数。

### 289. IrqHssl1COKPrioConfig

**描述**: This container contains the parameter to configure the priority of all the Transmit SRN supported by
Hssl module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqHssl1COK_0Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNCOK of Hssl1.
                                      The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqHssl1COK_1Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNCOK of Hssl1.
                                      The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: IrqHssl1COK_2Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNCOK of Hssl1.
                                      The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: IrqHssl1COK_3Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNCOK of Hssl1.
                                      The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 290. IrqHssl1RDIPrioConfig

**描述**: This container contains the parameter to configure the priority of all the Transmit SRN supported by
Hssl module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqHssl1RDI_0Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNRDI of Hssl1.
                                      The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqHssl1RDI_1Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNRDI of Hssl1.
                                      The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: IrqHssl1RDI_2Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNRDI of Hssl1.
                                      The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: IrqHssl1RDI_3Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNRDI of Hssl1.
                                      The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 291. IrqHssl1ERRPrioConfig

**描述**: This container contains the parameter to configure the priority of all the Transmit SRN supported by
Hssl module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqHssl1ERR_0Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNERR of Hssl1.
                                      The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqHssl1ERR_1Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNERR of Hssl1.
                                      The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: IrqHssl1ERR_2Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNERR of Hssl1.
                                      The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: IrqHssl1ERR_3Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNERR of Hssl1.
                                      The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 292. IrqHssl1TRGPrioConfig

**描述**: This container contains the parameter to configure the priority of all the Transmit SRN supported by
Hssl module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqHssl1TRG_0Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNTRG of Hssl1.
                                      The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqHssl1TRG_1Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNTRG of Hssl1.
                                      The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: IrqHssl1TRG_2Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNTRG of Hssl1.
                                      The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: IrqHssl1TRG_3Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNTRG of Hssl1.
                                      The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 293. IrqHssl1EXIPrioConfig

**描述**: This container contains the parameter to configure the priority of all the Transmit SRN supported by
Hssl module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqHssl1EXIPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNEXI of Hssl1.
                                      The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 294. IrqHssl1TosConfig

**描述**: This container contains the parameter to configure the type of service of all the SRN supported by
Hssl1 module.

该容器没有参数。

### 295. IrqHssl1COKTosConfig

**描述**: This container contains the parameter to configure the Type of service of all the Transmit SRN
supported by Hssl module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqHssl1COK_0Tos
  长名称: ''
  描述: The interrupt type of service setting of SRNCOK of Hssl1 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqHssl1COK_1Tos
  长名称: ''
  描述: The interrupt type of service setting of SRNCOK of Hssl1 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqHssl1COK_2Tos
  长名称: ''
  描述: The interrupt type of service setting of SRNCOK of Hssl1 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqHssl1COK_3Tos
  长名称: ''
  描述: The interrupt type of service setting of SRNCOK of Hssl1 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 296. IrqHssl1RDITosConfig

**描述**: This container contains the parameter to configure the Type of service of all the Transmit SRN
supported by Hssl module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqHssl1RDI_0Tos
  长名称: ''
  描述: The interrupt type of service setting of SRNRDI of Hssl1 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqHssl1RDI_1Tos
  长名称: ''
  描述: The interrupt type of service setting of SRNRDI of Hssl1 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqHssl1RDI_2Tos
  长名称: ''
  描述: The interrupt type of service setting of SRNRDI of Hssl1 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqHssl1RDI_3Tos
  长名称: ''
  描述: The interrupt type of service setting of SRNRDI of Hssl1 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 297. IrqHssl1ERRTosConfig

**描述**: This container contains the parameter to configure the Type of service of all the Transmit SRN
supported by Hssl module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqHssl1ERR_0Tos
  长名称: ''
  描述: The interrupt type of service setting of SRNERR of Hssl1 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqHssl1ERR_1Tos
  长名称: ''
  描述: The interrupt type of service setting of SRNERR of Hssl1 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqHssl1ERR_2Tos
  长名称: ''
  描述: The interrupt type of service setting of SRNERR of Hssl1 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqHssl1ERR_3Tos
  长名称: ''
  描述: The interrupt type of service setting of SRNERR of Hssl1 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 298. IrqHssl1TRGTosConfig

**描述**: This container contains the parameter to configure the Type of service of all the Transmit SRN
supported by Hssl module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqHssl1TRG_0Tos
  长名称: ''
  描述: The interrupt type of service setting of SRNTRG of Hssl1 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqHssl1TRG_1Tos
  长名称: ''
  描述: The interrupt type of service setting of SRNTRG of Hssl1 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqHssl1TRG_2Tos
  长名称: ''
  描述: The interrupt type of service setting of SRNTRG of Hssl1 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqHssl1TRG_3Tos
  长名称: ''
  描述: The interrupt type of service setting of SRNTRG of Hssl1 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 299. IrqHssl1EXITosConfig

**描述**: This container contains the parameter to configure the Type of service of all the Transmit SRN
supported by Hssl module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqHssl1EXITos
  长名称: ''
  描述: The interrupt type of service setting of SRNEXI of Hssl1 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 300. IrqSentConfig

**描述**: This container contains the Sent module interrupt configuration parameters.

该容器没有参数。

### 301. IrqSentCatConfig

**描述**: This container contains the Sent module category configuration parameters.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqSentSR0Cat
  长名称: ''
  描述: The interrupt category setting of SRN0 of Sent Module. The SRN number indicates the SRN
      configured. Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqSentSR1Cat
  长名称: ''
  描述: The interrupt category setting of SRN1 of Sent Module. The SRN number indicates the SRN
      configured. Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqSentSR2Cat
  长名称: ''
  描述: The interrupt category setting of SRN2 of Sent Module. The SRN number indicates the SRN
      configured. Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqSentSR3Cat
  长名称: ''
  描述: The interrupt category setting of SRN3 of Sent Module. The SRN number indicates the SRN
      configured. Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: IrqSentSR4Cat
  长名称: ''
  描述: The interrupt category setting of SRN4 of Sent Module. The SRN number indicates the SRN
      configured. Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: IrqSentSR5Cat
  长名称: ''
  描述: The interrupt category setting of SRN5 of Sent Module. The SRN number indicates the SRN
      configured. Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: IrqSentSR6Cat
  长名称: ''
  描述: The interrupt category setting of SRN6 of Sent Module. The SRN number indicates the SRN
      configured. Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: IrqSentSR7Cat
  长名称: ''
  描述: The interrupt category setting of SRN7 of Sent Module. The SRN number indicates the SRN
      configured. Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: IrqSentSR8Cat
  长名称: ''
  描述: The interrupt category setting of SRN8 of Sent Module. The SRN number indicates the SRN
      configured. Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: IrqSentSR9Cat
  长名称: ''
  描述: The interrupt category setting of SRN9 of Sent Module. The SRN number indicates the SRN
      configured. Depending upon the category the interrupt frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 302. IrqSentPrioConfig

**描述**: This container contains the parameter to configure the priority of all the SRN supported by Sent
module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqSentSR0Prio
  长名称: ''
  描述: The interrupt priority setting of SRN0 of Sent Module. The SRN number indicates the SRN
      configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqSentSR1Prio
  长名称: ''
  描述: The interrupt priority setting of SRN1 of Sent Module. The SRN number indicates the SRN
      configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: IrqSentSR2Prio
  长名称: ''
  描述: The interrupt priority setting of SRN2 of Sent Module. The SRN number indicates the SRN
      configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: IrqSentSR3Prio
  长名称: ''
  描述: The interrupt priority setting of SRN3 of Sent Module. The SRN number indicates the SRN
      configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: IrqSentSR4Prio
  长名称: ''
  描述: The interrupt priority setting of SRN4 of Sent Module. The SRN number indicates the SRN
      configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: IrqSentSR5Prio
  长名称: ''
  描述: The interrupt priority setting of SRN5 of Sent Module. The SRN number indicates the SRN
      configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: IrqSentSR6Prio
  长名称: ''
  描述: The interrupt priority setting of SRN6 of Sent Module. The SRN number indicates the SRN
      configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 8
  名称: IrqSentSR7Prio
  长名称: ''
  描述: The interrupt priority setting of SRN7 of Sent Module. The SRN number indicates the SRN
      configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 9
  名称: IrqSentSR8Prio
  长名称: ''
  描述: The interrupt priority setting of SRN8 of Sent Module. The SRN number indicates the SRN
      configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 10
  名称: IrqSentSR9Prio
  长名称: ''
  描述: The interrupt priority setting of SRN9 of Sent Module. The SRN number indicates the SRN
      configured.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 303. IrqSentTosConfig

**描述**: This container contains the Sent Module Type of Service configuration parameters.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqSentSR0Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN0 of Sent Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqSentSR1Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN1 of Sent Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqSentSR2Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN2 of Sent Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqSentSR3Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN3 of Sent Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: IrqSentSR4Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN4 of Sent Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: IrqSentSR5Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN5 of Sent Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: IrqSentSR6Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN6 of Sent Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: IrqSentSR7Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN7 of Sent Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: IrqSentSR8Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN8 of Sent Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: IrqSentSR9Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN9 of Sent Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 304. IrqI2cConfig

**描述**: This container contains the I2C module interrupt nodes configuration parameters.

该容器没有参数。

### 305. IrqI2cCatConfig

**描述**: This container contains parameters to configure the interrupt category of all SRN supported by I2C
module.

该容器没有参数。

### 306. IrqI2cDtrCatConfig

**描述**: This container contains the parameter to configure the category of all the Data Trasfer Request SRN
supported by I2C module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqI2c0DtrCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNDtr of I2c0 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqI2c1DtrCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNDtr of I2c1 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 307. IrqI2cErrCatConfig

**描述**: This container contains the parameter to configure the category of all the Error SRN supported by
I2c module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqI2c0ErrCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNErr of I2c0 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqI2c1ErrCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNErr of I2c1 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 308. IrqI2cPCatConfig

**描述**: This container contains the parameter to configure the category of all the Protocol SRN supported by
I2c module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqI2c0PCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNP of I2c0 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqI2c1PCat
  长名称: ''
  描述: |
    The interrupt category setting of SRNP of I2c1 Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 309. IrqI2cPrioConfig

**描述**: This container contains the parameter to configure the priority of all the SRN supported by I2c
module.

该容器没有参数。

### 310. IrqI2cDtrPrioConfig

**描述**: This container contains the parameter to configure the priority of all the Transmit SRN supported by
I2c module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqI2c0DtrPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNDtr of I2c0.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqI2c1DtrPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNDtr of I2c1.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 311. IrqI2cErrPrioConfig

**描述**: This container contains the parameter to configure the priority of all the Receive SRN supported by
I2c module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqI2c0ErrPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNErr of AscLin0.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqI2c1ErrPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNErr of AscLin1.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 312. IrqI2cPPrioConfig

**描述**: This container contains the parameter to configure the priority of all the Protocol SRN supported by
I2c module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqI2c0PPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNP of I2c0.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqI2c1PPrio
  长名称: ''
  描述: |
    The interrupt priority setting of SRNP of I2c1.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 313. IrqI2cTosConfig

**描述**: This container contains the I2c interrupt configuration parameters.

该容器没有参数。

### 314. IrqI2cDtrTosConfig

**描述**: This container contains the parameter to configure the Type of service of all the Transmit SRN
supported by I2c module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqI2c0DtrTos
  长名称: ''
  描述: The interrupt type of service setting of SRNDtr of I2c0 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqI2c1DtrTos
  长名称: ''
  描述: The interrupt type of service setting of SRNDtr of I2c1 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 315. IrqI2cErrTosConfig

**描述**: This container contains the parameter to configure the Type of service of all the Transmit SRN
supported by I2c module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqI2c0ErrTos
  长名称: ''
  描述: The interrupt type of service setting of SRNErr of I2c0 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqI2c1ErrTos
  长名称: ''
  描述: The interrupt type of service setting of SRNErr of I2c1 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 316. IrqI2cPTosConfig

**描述**: This container contains the parameter to configure the Type of service of all the Protocol SRN
supported by I2c module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqI2c0PTos
  长名称: ''
  描述: The interrupt type of service setting of SRNP of I2c0 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqI2c1PTos
  长名称: ''
  描述: The interrupt type of service setting of SRNP of I2c1 Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 317. IrqDsadcConfig

**描述**: This container contains the Dsadc interrupt configuration parameters.

该容器没有参数。

### 318. IrqDsadcCatConfig

**描述**: This container contains the parameter to configure the category of all the SRN supported by Dsadc
module.

该容器没有参数。

### 319. IrqDsadcSRMCatConfig

**描述**: This container contains the parameter to configure the category of all the Transmit SRN supported by
Dsadc module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqDSAdcSRM0Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN RM0 of Dsadc Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqDSAdcSRM1Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN RM1 of Dsadc Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqDSAdcSRM2Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN RM2 of Dsadc Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqDSAdcSRM3Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN RM3 of Dsadc Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: IrqDSAdcSRM4Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN RM4 of Dsadc Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: IrqDSAdcSRM5Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN RM5 of Dsadc Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: IrqDSAdcSRM6Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN RM 6 of Dsadc Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: IrqDSAdcSRM7Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN RM 7 of Dsadc Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: IrqDSAdcSRM8Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN RM 8 of Dsadc Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: IrqDSAdcSRM9Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN RM 9 of Dsadc  Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: IrqDSAdcSRM10Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN RM 10 of Dsadc Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: IrqDSAdcSRM11Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN RM 11 of Dsadc Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: IrqDSAdcSRM12Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN RM 12 of Dsadc Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: IrqDSAdcSRM13Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN RM 13 of Dsadc Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 320. IrqDsadcSRACatConfig

**描述**: This container contains the parameter to configure the category of all the Transmit SRN supported by
Dsadc module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqDSAdcSRA0Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN RA0 of Dsadc Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqDSAdcSRA1Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN RA1 of Dsadc Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqDSAdcSRA2Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN RA2 of Dsadc Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqDSAdcSRA3Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN RA3 of Dsadc Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: IrqDSAdcSRA4Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN RA4 of Dsadc Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: IrqDSAdcSRA5Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN RA5 of Dsadc Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: IrqDSAdcSRA6Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN RA 6 of Dsadc Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: IrqDSAdcSRA7Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN RA 7 of Dsadc Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: IrqDSAdcSRA8Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN RA 8 of Dsadc Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: IrqDSAdcSRA9Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN RA 9 of Dsadc  Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: IrqDSAdcSRA10Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN RA 10 of Dsadc Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: IrqDSAdcSRA11Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN RA 11 of Dsadc Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: IrqDSAdcSRA12Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN RA 12 of Dsadc Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: IrqDSAdcSRA13Cat
  长名称: ''
  描述: |
    The interrupt category setting of SRN RA 13 of Dsadc Module.
                                    Depending upon the category the interrupt  Frame is different.
  默认值: CAT1
  最小值: ''
  最大值: ''
```

### 321. IrqDsadcPrioConfig

**描述**: This container contains the parameter to configure the priority of all the SRN supported by Dsadc
module.

该容器没有参数。

### 322. IrqDsadcSRMPrioConfig

**描述**: This container contains the parameter to configure the priority of all the Transmit SRN supported by
Dsadc module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqDsadcSRM0Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN RM 0 of Dsadc.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqDsadcSRM1Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN RM 1 of Dsadc.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: IrqDsadcSRM2Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN RM 2 of Dsadc.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: IrqDsadcSRM3Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN RM 3 of Dsadc.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: IrqDsadcSRM4Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN RM 4 of Dsadc.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: IrqDsadcSRM5Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN RM 5 of Dsadc.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: IrqDsadcSRM6Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN RM 6 of Dsadc.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 8
  名称: IrqDsadcSRM7Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN RM 7 of Dsadc.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 9
  名称: IrqDsadcSRM8Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN RM 8 of Dsadc.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 10
  名称: IrqDsadcSRM9Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN RM 9 of Dsadc.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 11
  名称: IrqDsadcSRM10Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN RM 10 of Dsadc.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 12
  名称: IrqDsadcSRM11Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN RM 11 of Dsadc.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 13
  名称: IrqDsadcSRM12Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN RM 12 of Dsadc.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 14
  名称: IrqDsadcSRM13Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN RM 13 of Dsadc.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 323. IrqDsadcSRAPrioConfig

**描述**: This container contains the parameter to configure the priority of all the Transmit SRN supported by
Dsadc module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqDsadcSRA0Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN RA 0 of Dsadc.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: IrqDsadcSRA1Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN RA 1 of Dsadc.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: IrqDsadcSRA2Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN RA 2 of Dsadc.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: IrqDsadcSRA3Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN RA 3 of Dsadc.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: IrqDsadcSRA4Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN RA 4 of Dsadc.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: IrqDsadcSRA5Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN RA 5 of Dsadc.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: IrqDsadcSRA6Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN RA 6 of Dsadc.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 8
  名称: IrqDsadcSRA7Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN RA 7 of Dsadc.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 9
  名称: IrqDsadcSRA8Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN RA 8 of Dsadc.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 10
  名称: IrqDsadcSRA9Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN RA 9 of Dsadc.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 11
  名称: IrqDsadcSRA10Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN RA 10 of Dsadc.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 12
  名称: IrqDsadcSRA11Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN RA 11 of Dsadc.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 13
  名称: IrqDsadcSRA12Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN RA 12 of Dsadc.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 14
  名称: IrqDsadcSRA13Prio
  长名称: ''
  描述: |
    The interrupt priority setting of SRN RA 13 of Dsadc.
                                    The SRN number indicates the SRN configured.
  默认值: 0
  最小值: 0
  最大值: 255
```

### 324. IrqDsadcTosConfig

**描述**: This container contains the parameter to configure the type of service of all the SRN supported by
Dsadc0 module.

该容器没有参数。

### 325. IrqDsadcSRMTosConfig

**描述**: This container contains the parameter to configure the Type of service of all the Transmit SRN
supported by Dsadc module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqDsadcSRM0Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN RM 0 of Dsadc Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqDsadcSRM1Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN RM 1 of Dsadc Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqDsadcSRM2Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN RM 2 of Dsadc Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqDsadcSRM3Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN RM 3 of Dsadc Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: IrqDsadcSRM4Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN RM 4 of Dsadc Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: IrqDsadcSRM5Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN RM 5 of Dsadc Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: IrqDsadcSRM6Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN RM 6 of Dsadc Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: IrqDsadcSRM7Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN RM 7 of Dsadc Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: IrqDsadcSRM8Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN RM 8 of Dsadc Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: IrqDsadcSRM9Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN RM 9 of Dsadc Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: IrqDsadcSRM10Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN RM 10 of Dsadc Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: IrqDsadcSRM11Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN RM 11 of Dsadc Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: IrqDsadcSRM12Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN RM 3 of Dsadc Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: IrqDsadcSRM13Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN RM 13 of Dsadc Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 326. IrqDsadcSRATosConfig

**描述**: This container contains the parameter to configure the Type of service of all the Transmit SRN
supported by Dsadc module.

#### 参数列表

```yaml
- 
  序号: 1
  名称: IrqDsadcSRA0Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN RA 0 of Dsadc Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 2
  名称: IrqDsadcSRA1Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN RA 1 of Dsadc Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 3
  名称: IrqDsadcSRA2Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN RA 2 of Dsadc Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 4
  名称: IrqDsadcSRA3Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN RA 3 of Dsadc Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 5
  名称: IrqDsadcSRA4Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN RA 4 of Dsadc Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 6
  名称: IrqDsadcSRA5Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN RA 5 of Dsadc Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 7
  名称: IrqDsadcSRA6Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN RA 6 of Dsadc Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 8
  名称: IrqDsadcSRA7Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN RA 7 of Dsadc Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 9
  名称: IrqDsadcSRA8Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN RA 8 of Dsadc Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 10
  名称: IrqDsadcSRA9Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN RA 9 of Dsadc Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 11
  名称: IrqDsadcSRA10Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN RA 10 of Dsadc Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 12
  名称: IrqDsadcSRA11Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN RA 11 of Dsadc Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 13
  名称: IrqDsadcSRA12Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN RA 3 of Dsadc Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
- 
  序号: 14
  名称: IrqDsadcSRA13Tos
  长名称: ''
  描述: The interrupt type of service setting of SRN RA 13 of Dsadc Module.
  默认值: CPU0
  最小值: ''
  最大值: ''
```

### 327. CommonPublishedInformation

**描述**: Common container, aggregated by all modules. It contains published information about vendor and
versions.

#### 参数列表

```yaml
- 
  序号: 1
  名称: ArMajorVersion
  长名称: ''
  描述: Major version number of AUTOSAR specification on which the appropriate implementation is based
      on.
  默认值: 4
  最小值: 0
  最大值: 255
- 
  序号: 2
  名称: ArMinorVersion
  长名称: ''
  描述: Minor version number of AUTOSAR specification on which the appropriate implementation is based
      on.
  默认值: 2
  最小值: 0
  最大值: 255
- 
  序号: 3
  名称: ArPatchVersion
  长名称: ''
  描述: Patch level version number of AUTOSAR specification on which the appropriate implementation is
      based on.
  默认值: 2
  最小值: 0
  最大值: 255
- 
  序号: 4
  名称: SwMajorVersion
  长名称: ''
  描述: Major version number of the vendor specific implementation of the module. The numbering is
      vendor specific.
  默认值: 20
  最小值: 0
  最大值: 255
- 
  序号: 5
  名称: SwMinorVersion
  长名称: ''
  描述: Minor version number of the vendor specific implementation of the module. The numbering is
      vendor specific.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 6
  名称: SwPatchVersion
  长名称: ''
  描述: Patch level version number of the vendor specific implementation of the module. The numbering
      is vendor specific.
  默认值: 0
  最小值: 0
  最大值: 255
- 
  序号: 7
  名称: ModuleId
  长名称: ''
  描述: Module ID of this module ENom Module List
  默认值: 255
  最小值: 0
  最大值: 65535
- 
  序号: 8
  名称: VendorId
  长名称: ''
  描述: Vendor ID of the dedicated implementation of this module according to the AUTOSAR vendor list
  默认值: 17
  最小值: 0
  最大值: 65535
- 
  序号: 9
  名称: Release
  长名称: ''
  描述: Aurix2G derivative used for the implementation
  默认值: ''
  最小值: ''
  最大值: ''
```

