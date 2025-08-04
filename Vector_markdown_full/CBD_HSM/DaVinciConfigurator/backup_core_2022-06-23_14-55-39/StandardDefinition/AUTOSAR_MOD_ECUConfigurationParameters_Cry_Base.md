# Cry - 完整配置文档

*此文档由ARXML文件自动生成，采用层次化结构展示*

**生成时间**: 2025-06-16 14:51:12

## 📑 目录

- [📄 文件信息](#-文件信息)
- [🔧 模块定义](#-模块定义)
  - [Cry](#cry)
- [📦 包结构](#-包结构)

## 📄 文件信息

### Schema信息
- **Schema位置**: `http://autosar.org/schema/r4.0 AUTOSAR_4-0-3.xsd`
- **命名空间**: `http://autosar.org/schema/r4.0`

## 🔧 模块定义

### 1. Cry

#### 基本信息

- **UUID**: `6b3dab8e-0122-40c6-9146-7b2a4eb60c67`
- **模块名称**: `Cry`
- **类别**: `VENDOR_SPECIFIC_MODULE_DEFINITION`
- **多重性**: [0..infinite]
- **支持的变体**:
  - VARIANT-PRE-COMPILE

#### 模块描述

Cry for MICROSAR Cry Implementations

#### 配置容器

本模块包含 **49** 个配置容器：

##### 1. CryGeneral

**容器属性**:

- **UUID**: `3cffa08f-9ffe-4061-af62-fa09fb256467`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryGeneral`
- **多重性**: [1..1]
- **构建后可变**: false

###### 参数配置

此容器包含 **2** 个参数：

####### BOOLEAN 类型参数

######## 1. CryUseSyncJobProcessing

- **UUID**: `8346b738-5cef-4def-a133-ae9c9c5cf2e7`
- **参数名**: `CryUseSyncJobProcessing`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `true`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch to enable and disable synchronous job processing.

######## 2. CryVersionInfoApi

- **UUID**: `bdc72da2-5e4c-4e11-9782-f5cff094a199`
- **参数名**: `CryVersionInfoApi`
- **数据类型**: BOOLEAN
- **多重性**: [1..1]
- **默认值**: `false`
- **来源**: Vector Informatik
- **符号名值**: false
- **需要索引**: false
- **实现配置类**:
  - PRE-COMPILE: VARIANT-PRE-COMPILE
- **描述**: Pre-processor switch to enable and disable availability of the API Cry_GetVersionInfo(). True: API Cry_GetVersionInfo() is available.  False: API Cry_GetVersionInfo() is not available.

##### 2. CryAesEncrypt128

**容器属性**:

- **UUID**: `cf205048-ff2f-4d38-9f31-c63a3a2180f1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryAesEncrypt128`
- **多重性**: [0..1]
- **构建后可变**: false

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CryAesEncrypt128Config

**容器属性**:

- **UUID**: `33146fe0-0f5e-4113-ae9c-507838f90cd9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryAesEncrypt128Config`
- **多重性**: [1..32]
- **构建后可变**: false

##### 3. CryAesEncrypt128Config

**容器属性**:

- **UUID**: `33146fe0-0f5e-4113-ae9c-507838f90cd9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryAesEncrypt128Config`
- **多重性**: [1..32]
- **构建后可变**: false

##### 4. CryAesDecrypt128

**容器属性**:

- **UUID**: `54738a22-4adc-4908-a1ce-4fa9be7857d7`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryAesDecrypt128`
- **多重性**: [0..1]
- **构建后可变**: false

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CryAesDecrypt128Config

**容器属性**:

- **UUID**: `4b2cecc5-95b7-4094-9912-86ceb97d51e0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryAesDecrypt128Config`
- **多重性**: [1..32]
- **构建后可变**: false

##### 5. CryAesDecrypt128Config

**容器属性**:

- **UUID**: `4b2cecc5-95b7-4094-9912-86ceb97d51e0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryAesDecrypt128Config`
- **多重性**: [1..32]
- **构建后可变**: false

##### 6. CryFips186

**容器属性**:

- **UUID**: `a2b41667-8e8e-4bfe-b684-3bb9063c3a58`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryFips186`
- **多重性**: [0..1]
- **构建后可变**: false

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CryFips186Config

**容器属性**:

- **UUID**: `9110866d-9ff1-46eb-8895-ee87f4426627`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryFips186Config`
- **多重性**: [1..32]
- **构建后可变**: false

##### 7. CryFips186Config

**容器属性**:

- **UUID**: `9110866d-9ff1-46eb-8895-ee87f4426627`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryFips186Config`
- **多重性**: [1..32]
- **构建后可变**: false

##### 8. CryHmacSha1Verify

**容器属性**:

- **UUID**: `5697c465-4d34-4480-abfd-ce7277ac9b47`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryHmacSha1Verify`
- **多重性**: [0..1]
- **构建后可变**: false

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CryHmacSha1VerifyConfig

**容器属性**:

- **UUID**: `25f81b3e-a04c-467f-a614-af25fe9c5ca2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryHmacSha1VerifyConfig`
- **多重性**: [1..32]
- **构建后可变**: false

##### 9. CryHmacSha1VerifyConfig

**容器属性**:

- **UUID**: `25f81b3e-a04c-467f-a614-af25fe9c5ca2`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryHmacSha1VerifyConfig`
- **多重性**: [1..32]
- **构建后可变**: false

##### 10. CryCmacAes128Gen

**容器属性**:

- **UUID**: `8425b020-e237-4d17-83fb-9a3bff1ea6c1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryCmacAes128Gen`
- **多重性**: [0..1]
- **构建后可变**: false

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CryCmacAes128GenConfig

**容器属性**:

- **UUID**: `8b75ec67-1014-41e8-9e8d-f2222de7fe30`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryCmacAes128GenConfig`
- **多重性**: [1..32]
- **构建后可变**: false

##### 11. CryCmacAes128GenConfig

**容器属性**:

- **UUID**: `8b75ec67-1014-41e8-9e8d-f2222de7fe30`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryCmacAes128GenConfig`
- **多重性**: [1..32]
- **构建后可变**: false

##### 12. CryCmacAes128Ver

**容器属性**:

- **UUID**: `d3cae37c-65b8-45ed-ba2d-5050b479b38e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryCmacAes128Ver`
- **多重性**: [0..1]
- **构建后可变**: false

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CryCmacAes128VerConfig

**容器属性**:

- **UUID**: `d421ceb9-ac70-4117-b48d-3bad280db957`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryCmacAes128VerConfig`
- **多重性**: [1..32]
- **构建后可变**: false

##### 13. CryCmacAes128VerConfig

**容器属性**:

- **UUID**: `d421ceb9-ac70-4117-b48d-3bad280db957`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryCmacAes128VerConfig`
- **多重性**: [1..32]
- **构建后可变**: false

##### 14. CryRsaDecrypt

**容器属性**:

- **UUID**: `88733f78-ad9b-406e-8ed5-944ecef29d0d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryRsaDecrypt`
- **多重性**: [0..1]
- **构建后可变**: false

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CryRsaDecryptConfig

**容器属性**:

- **UUID**: `4b7e81a4-cfbf-421f-976d-0eff073fa9ae`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryRsaDecryptConfig`
- **多重性**: [1..32]
- **构建后可变**: false

##### 15. CryRsaDecryptConfig

**容器属性**:

- **UUID**: `4b7e81a4-cfbf-421f-976d-0eff073fa9ae`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryRsaDecryptConfig`
- **多重性**: [1..32]
- **构建后可变**: false

##### 16. CryRsaSha1SigVer

**容器属性**:

- **UUID**: `f2f90cc8-c459-430b-8b29-0b32a91bad32`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryRsaSha1SigVer`
- **多重性**: [0..1]
- **构建后可变**: false

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CryRsaSha1SigVerConfig

**容器属性**:

- **UUID**: `feed4ad3-bb61-46d9-907c-a6a05a8a804a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryRsaSha1SigVerConfig`
- **多重性**: [1..32]
- **构建后可变**: false

##### 17. CryRsaSha1SigVerConfig

**容器属性**:

- **UUID**: `feed4ad3-bb61-46d9-907c-a6a05a8a804a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryRsaSha1SigVerConfig`
- **多重性**: [1..32]
- **构建后可变**: false

##### 18. CryKdf2HmacSha1

**容器属性**:

- **UUID**: `9bf4aa4a-4583-4cef-b6c3-4a6444a7210a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryKdf2HmacSha1`
- **多重性**: [0..1]
- **构建后可变**: false

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CryKdf2HmacSha1Config

**容器属性**:

- **UUID**: `6c623e8a-2a43-4139-bcb9-2d4ca9a1b073`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryKdf2HmacSha1Config`
- **多重性**: [1..32]
- **构建后可变**: false

##### 19. CryKdf2HmacSha1Config

**容器属性**:

- **UUID**: `6c623e8a-2a43-4139-bcb9-2d4ca9a1b073`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryKdf2HmacSha1Config`
- **多重性**: [1..32]
- **构建后可变**: false

##### 20. CryHashSha256

**容器属性**:

- **UUID**: `5f48b0b0-5a7d-4d4d-913c-7aba6383906a`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryHashSha256`
- **多重性**: [0..1]
- **构建后可变**: false

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CryHashSha256Config

**容器属性**:

- **UUID**: `d808e6b9-a6f3-45a8-9e9c-3bd9851c605e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryHashSha256Config`
- **多重性**: [1..32]
- **构建后可变**: false

##### 21. CryHashSha256Config

**容器属性**:

- **UUID**: `d808e6b9-a6f3-45a8-9e9c-3bd9851c605e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryHashSha256Config`
- **多重性**: [1..32]
- **构建后可变**: false

##### 22. CryEcdsaSigGen

**容器属性**:

- **UUID**: `da91a4a8-d053-47bb-9f68-a44bda7d855d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryEcdsaSigGen`
- **多重性**: [0..1]
- **构建后可变**: false

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CryEcdsaSigGenConfig

**容器属性**:

- **UUID**: `0095e244-8ac0-4437-81a8-32f61b577291`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryEcdsaSigGenConfig`
- **多重性**: [1..32]
- **构建后可变**: false

##### 23. CryEcdsaSigGenConfig

**容器属性**:

- **UUID**: `0095e244-8ac0-4437-81a8-32f61b577291`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryEcdsaSigGenConfig`
- **多重性**: [1..32]
- **构建后可变**: false

##### 24. CryHmacSha256Verify

**容器属性**:

- **UUID**: `50072a8c-2813-4557-85c6-904d5173089d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryHmacSha256Verify`
- **多重性**: [0..1]
- **构建后可变**: false

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CryHmacSha256VerifyConfig

**容器属性**:

- **UUID**: `83be9728-2590-492e-b300-da52a37465b1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryHmacSha256VerifyConfig`
- **多重性**: [1..32]
- **构建后可变**: false

##### 25. CryHmacSha256VerifyConfig

**容器属性**:

- **UUID**: `83be9728-2590-492e-b300-da52a37465b1`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryHmacSha256VerifyConfig`
- **多重性**: [1..32]
- **构建后可变**: false

##### 26. CryHmacSha256Generate

**容器属性**:

- **UUID**: `8dda935b-6ed4-4ba9-8c08-b2c1477a85ff`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryHmacSha256Generate`
- **多重性**: [0..1]
- **构建后可变**: false

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CryHmacSha256GenerateConfig

**容器属性**:

- **UUID**: `5f0cd599-db5c-411f-b12d-1946120a934e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryHmacSha256GenerateConfig`
- **多重性**: [1..32]
- **构建后可变**: false

##### 27. CryHmacSha256GenerateConfig

**容器属性**:

- **UUID**: `5f0cd599-db5c-411f-b12d-1946120a934e`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryHmacSha256GenerateConfig`
- **多重性**: [1..32]
- **构建后可变**: false

##### 28. CryEcdsaSigVer

**容器属性**:

- **UUID**: `34c6dac7-f301-4aea-bd58-2b0e4f7fff08`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryEcdsaSigVer`
- **多重性**: [0..1]
- **构建后可变**: false

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CryEcdsaSigVerConfig

**容器属性**:

- **UUID**: `e20d7613-23fd-44b0-b343-c2d22376a447`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryEcdsaSigVerConfig`
- **多重性**: [1..32]
- **构建后可变**: false

##### 29. CryEcdsaSigVerConfig

**容器属性**:

- **UUID**: `e20d7613-23fd-44b0-b343-c2d22376a447`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryEcdsaSigVerConfig`
- **多重性**: [1..32]
- **构建后可变**: false

##### 30. CryEcdh

**容器属性**:

- **UUID**: `72500bf9-7dcd-4fdd-8473-1fa9db37575c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryEcdh`
- **多重性**: [0..1]
- **构建后可变**: false

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CryEcdhConfig

**容器属性**:

- **UUID**: `0a388f35-b69d-4a38-857b-7a9eb991e2eb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryEcdhConfig`
- **多重性**: [1..32]
- **构建后可变**: false

##### 31. CryEcdhConfig

**容器属性**:

- **UUID**: `0a388f35-b69d-4a38-857b-7a9eb991e2eb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryEcdhConfig`
- **多重性**: [1..32]
- **构建后可变**: false

##### 32. CryKeyExtract

**容器属性**:

- **UUID**: `10317102-4827-4bcf-ba6f-8a3a33538ee0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryKeyExtract`
- **多重性**: [0..1]
- **构建后可变**: false

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CryKeyExtractConfig

**容器属性**:

- **UUID**: `83037a94-8dcb-4c80-ba2d-ad76a3e97f11`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryKeyExtractConfig`
- **多重性**: [1..32]
- **构建后可变**: false

##### 33. CryKeyExtractConfig

**容器属性**:

- **UUID**: `83037a94-8dcb-4c80-ba2d-ad76a3e97f11`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryKeyExtractConfig`
- **多重性**: [1..32]
- **构建后可变**: false

##### 34. CryKeyWrapSym

**容器属性**:

- **UUID**: `ddaf755a-dd54-47cb-a495-16ad3071a087`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryKeyWrapSym`
- **多重性**: [0..1]
- **构建后可变**: false

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CryKeyWrapSymConfig

**容器属性**:

- **UUID**: `8f5423f4-ce3e-4681-8749-180fd243b34d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryKeyWrapSymConfig`
- **多重性**: [1..32]
- **构建后可变**: false

##### 35. CryKeyWrapSymConfig

**容器属性**:

- **UUID**: `8f5423f4-ce3e-4681-8749-180fd243b34d`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryKeyWrapSymConfig`
- **多重性**: [1..32]
- **构建后可变**: false

##### 36. CryRng

**容器属性**:

- **UUID**: `ba2cb564-2aea-4ec5-8011-19c1001bd536`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryRng`
- **多重性**: [0..1]
- **构建后可变**: false

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CryRngConfig

**容器属性**:

- **UUID**: `111cf229-c5d5-481e-8f0b-bb55284ced4c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryRngConfig`
- **多重性**: [1..32]
- **构建后可变**: false

##### 37. CryRngConfig

**容器属性**:

- **UUID**: `111cf229-c5d5-481e-8f0b-bb55284ced4c`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryRngConfig`
- **多重性**: [1..32]
- **构建后可变**: false

##### 38. CryHashSha512

**容器属性**:

- **UUID**: `e5541aa4-6b80-4689-8357-1cc4f33fbeb9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryHashSha512`
- **多重性**: [0..1]
- **构建后可变**: false

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CryHashSha512Config

**容器属性**:

- **UUID**: `c20d04d6-90a9-47cb-8525-c41dfc9ddb11`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryHashSha512Config`
- **多重性**: [1..32]
- **构建后可变**: false

##### 39. CryHashSha512Config

**容器属性**:

- **UUID**: `c20d04d6-90a9-47cb-8525-c41dfc9ddb11`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryHashSha512Config`
- **多重性**: [1..32]
- **构建后可变**: false

##### 40. CryHashSha1

**容器属性**:

- **UUID**: `faa20083-0bf4-419d-89b0-8993b4ba7de9`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryHashSha1`
- **多重性**: [0..1]
- **构建后可变**: false

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CryHashSha1Config

**容器属性**:

- **UUID**: `efcedeff-5dc9-4946-8553-c7756090c9d3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryHashSha1Config`
- **多重性**: [1..32]
- **构建后可变**: false

##### 41. CryHashSha1Config

**容器属性**:

- **UUID**: `efcedeff-5dc9-4946-8553-c7756090c9d3`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryHashSha1Config`
- **多重性**: [1..32]
- **构建后可变**: false

##### 42. CryHashRipemd160

**容器属性**:

- **UUID**: `78b54b05-b766-41a2-9b32-66a9e96649f0`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryHashRipemd160`
- **多重性**: [0..1]
- **构建后可变**: false

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CryHashRipemd160Config

**容器属性**:

- **UUID**: `bad86b4b-e4f9-487a-8414-df1d06b14450`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryHashRipemd160Config`
- **多重性**: [1..32]
- **构建后可变**: false

##### 43. CryHashRipemd160Config

**容器属性**:

- **UUID**: `bad86b4b-e4f9-487a-8414-df1d06b14450`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryHashRipemd160Config`
- **多重性**: [1..32]
- **构建后可变**: false

##### 44. CryEd25519SigGen

**容器属性**:

- **UUID**: `a270ab75-73b0-4538-aeee-42ddc9affe0f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryEd25519SigGen`
- **多重性**: [0..1]
- **构建后可变**: false

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CryEd25519SigGenConfig

**容器属性**:

- **UUID**: `35d7c397-ccfc-4ac7-895e-a7b413edffcb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryEd25519SigGenConfig`
- **多重性**: [1..32]
- **构建后可变**: false

##### 45. CryEd25519SigGenConfig

**容器属性**:

- **UUID**: `35d7c397-ccfc-4ac7-895e-a7b413edffcb`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryEd25519SigGenConfig`
- **多重性**: [1..32]
- **构建后可变**: false

##### 46. CryEd25519SigVer

**容器属性**:

- **UUID**: `d5147c3b-f5e7-4aea-9d08-f3797919235f`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryEd25519SigVer`
- **多重性**: [0..1]
- **构建后可变**: false

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CryEd25519SigVerConfig

**容器属性**:

- **UUID**: `0842164e-005b-463d-8803-e8d6eac3f232`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryEd25519SigVerConfig`
- **多重性**: [1..32]
- **构建后可变**: false

##### 47. CryEd25519SigVerConfig

**容器属性**:

- **UUID**: `0842164e-005b-463d-8803-e8d6eac3f232`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryEd25519SigVerConfig`
- **多重性**: [1..32]
- **构建后可变**: false

##### 48. CryDhX25519CalcSecret

**容器属性**:

- **UUID**: `1f558f10-f6d8-4117-9b42-e7027805df71`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryDhX25519CalcSecret`
- **多重性**: [0..1]
- **构建后可变**: false

###### 配置容器

本模块包含 **1** 个配置容器：

####### 1. CryDhX25519CalcSecretConfig

**容器属性**:

- **UUID**: `4c0d2879-9022-4482-8d4c-cccafaf2e9ab`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryDhX25519CalcSecretConfig`
- **多重性**: [1..32]
- **构建后可变**: false

##### 49. CryDhX25519CalcSecretConfig

**容器属性**:

- **UUID**: `4c0d2879-9022-4482-8d4c-cccafaf2e9ab`
- **容器类型**: PARAM-CONF-CONTAINER
- **容器名称**: `CryDhX25519CalcSecretConfig`
- **多重性**: [1..32]
- **构建后可变**: false

## 📦 包结构

此ARXML文件包含 **2** 个包：

### 1. AUTOSAR

- **UUID**: `a0d0cbce-5923-4afd-816f-504cafb0ecc5`
- **包名称**: `AUTOSAR`
- **包含元素数量**: 0

### 2. EcucDefs

- **UUID**: `ae3de62a-7bfc-4c52-95a4-e4c90e5782fd`
- **包名称**: `EcucDefs`
- **包含元素数量**: 1

#### 包含的元素

##### ECUC-MODULE-DEF 类型元素

1. **Cry**
