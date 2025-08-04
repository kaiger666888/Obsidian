# AUTOSAR Module - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:49:21

## 📑 目录

- [📄 文件信息](#-文件信息)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 autosar_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 📦 包结构

此ARXML文件包含 **9** 个包：

### 1. ECUSystem

- **包名称**: `ECUSystem`
- **包含元素数量**: 0

### 2. DemoEcuSPA

- **UUID**: `AA2BC68294B5D8F47EC90829497FDEA2`
- **包名称**: `DemoEcuSPA`
- **包含元素数量**: 0

### 3. DemoEcuMAIN

- **UUID**: `A2E3C08C0CA23AD18BA7AA6A012199D0`
- **包名称**: `DemoEcuMAIN`
- **包含元素数量**: 1

#### 包含的元素

##### ECU-INSTANCE 类型元素

1. **DemoEcu**

### 4. VehicleTopology

- **包名称**: `VehicleTopology`
- **包含元素数量**: 0

### 5. BackboneMAIN

- **UUID**: `A971B92AF21CC8FDCBA44EBC40996B73`
- **包名称**: `BackboneMAIN`
- **包含元素数量**: 1

#### 包含的元素

##### FLEXRAY-CLUSTER 类型元素

1. **Backbone**

### 6. Communication

- **UUID**: `4f7060be-0a4d-4fc1-bcc0-869dc91937b6-Communication`
- **包名称**: `Communication`
- **包含元素数量**: 0

### 7. Frame

- **UUID**: `4f7060be-0a4d-4fc1-bcc0-869dc91937b6-Frame-2`
- **包名称**: `Frame`
- **包含元素数量**: 30

#### 包含的元素

##### FLEXRAY-FRAME 类型元素

1. **DemoEcuBackBoneDiagResFrame1**
2. **DemoEcuBackBoneDiagResFrame2**
3. **TesterBackBoneDiagReqFrame1**
4. **TesterBackBoneDiagReqFrame2**
5. **TesterBackBoneDiagReqFrame3**
6. **TesterBackBoneDiagReqFrame4**
7. **TesterBackBoneDiagReqFrame5**
8. **TesterBackBoneDiagReqFrame6**
9. **TesterBackBoneDiagReqFrame7**
10. **TesterBackBoneDiagReqFrame8**
11. **TesterBackBoneDiagReqFrame9**
12. **TesterBackBoneDiagReqFrame10**
13. **TesterBackBoneDiagReqFrame11**
14. **TesterBackBoneDiagReqFrame12**
15. **TesterBackBoneDiagReqFrame13**
16. **TesterBackBoneDiagReqFrame14**
17. **TesterBackBoneDiagReqFrame15**
18. **TesterBackBoneDiagReqFrame16**
19. **TesterBackBoneDiagReqFrame17**
20. **TesterBackBoneDiagReqFrame18**
21. **TesterBackBoneDiagReqFrame19**
22. **TesterBackBoneDiagReqFrame20**
23. **TesterBackBoneDiagReqFrame21**
24. **TesterBackBoneDiagReqFrame22**
25. **TesterBackBoneDiagReqFrame23**
26. **TesterBackBoneDiagReqFrame24**
27. **TesterBackBoneDiagReqFrame25**
28. **TesterBackBoneDiagReqFrame26**
29. **KeySlot1Frame**
30. **KeySlot6Frame**

### 8. Pdu

- **UUID**: `4f7060be-0a4d-4fc1-bcc0-869dc91937b6-Pdu-2`
- **包名称**: `Pdu`
- **包含元素数量**: 33

#### 包含的元素

##### N-PDU 类型元素

1. **DemoEcuBackBoneDiagResNpdu1**
2. **DemoEcuBackBoneDiagResNpdu2**
3. **TesterBackBoneDiagReqNpdu1**
4. **TesterBackBoneDiagReqNpdu2**
5. **TesterBackBoneDiagReqNpdu3**
6. **TesterBackBoneDiagReqNpdu4**
7. **TesterBackBoneDiagReqNpdu5**
8. **TesterBackBoneDiagReqNpdu6**
9. **TesterBackBoneDiagReqNpdu7**
10. **TesterBackBoneDiagReqNpdu8**
11. **TesterBackBoneDiagReqNpdu9**
12. **TesterBackBoneDiagReqNpdu10**
13. **TesterBackBoneDiagReqNpdu11**
14. **TesterBackBoneDiagReqNpdu12**
15. **TesterBackBoneDiagReqNpdu13**
16. **TesterBackBoneDiagReqNpdu14**
17. **TesterBackBoneDiagReqNpdu15**
18. **TesterBackBoneDiagReqNpdu16**
19. **TesterBackBoneDiagReqNpdu17**
20. **TesterBackBoneDiagReqNpdu18**
21. **TesterBackBoneDiagReqNpdu19**
22. **TesterBackBoneDiagReqNpdu20**
23. **TesterBackBoneDiagReqNpdu21**
24. **TesterBackBoneDiagReqNpdu22**
25. **TesterBackBoneDiagReqNpdu23**
26. **TesterBackBoneDiagReqNpdu24**
27. **TesterBackBoneDiagReqNpdu25**
28. **TesterBackBoneDiagReqNpdu26**
29. **KeySlot1Npdu**
30. **KeySlot6Npdu**

##### DCM-I-PDU 类型元素

1. **TesterToAllFuncDiagIpdu**
2. **TesterToDemoEcuDiagIpdu**
3. **DemoEcuToTesterDiagIpdu**

### 9. TpConfig

- **UUID**: `4f7060be-0a4d-4fc1-bcc0-869dc91937b6-TpConfig-2`
- **包名称**: `TpConfig`
- **包含元素数量**: 1

#### 包含的元素

##### FLEXRAY-TP-CONFIG 类型元素

1. **FlexrayTpConfig1**
