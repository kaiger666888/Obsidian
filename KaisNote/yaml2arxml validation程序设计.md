# 流程设计
## 从yaml中提取字典
```python
yamlAttributeDict
```
## 设置arxmlAttributeDict
```python
targetAttributeAddrDict = {
	"SoftwareComponents":
		{"TargetList_SWCs":
			{"runnables": 
				{"TargetList_Runnables"}
			}
		}
	}
```
## attribute2xpathMapping
```python
attribute2xpathMappingDict = {
	"SoftwareComponents": 'APPLICATION-SW-COMPONENT-TYPE', 
	"TargetList_SWCs": 'SHORT-NAME',
	"runnables": 'RUNNABLE-ENTITY' ,
	"TargetList_Runnables": 'SHORT-NAME'
	}
```
## 从arxml中提取目标attribute，形成字典
```python

arxmlAttributeDict={}
for attrib in targetAttributeAddrDict:
	if attrib in attribute2xpathMappingDict:
		将该attrib加入arxmlAttributeDict的key中
		在arxml中找到所有elements，将elements变为该key的值
		return 
```
## Template
```python

```
## Template
```python

```
## Template
```python

```
## Template
```python

```
## Template
```python

```