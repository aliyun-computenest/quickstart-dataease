# 快速部署DataEase社区版

## 服务说明
DataEase 是开源的数据可视化分析工具，帮助用户快速分析数据并洞察业务趋势，从而实现业务的改进与优化。
DataEase 支持丰富的数据源连接，能够通过拖拉拽方式快速制作图表，并可以方便地与他人分享。详情请看[DataEase官网](https://dataease.io/docs/v2/)。

## 服务架构

DataEase社区版服务的部署架构为单机ecs部署。

<img src="architecture_ecs_single.png" width="600" height="400" align="bottom"/>

## 计费说明
DataEase社区版服务本身不收取费用。  
用户部署构建出的服务时，资源费用主要涉及：
- 所选ECS实例规格
- 磁盘容量
- 公网带宽

计费方式包括：
- 按量付费（小时）
- 包年包月

预估费用在部署前可实时看到。

## RAM账号所需权限

DataEase社区版服务需要对ECS、VPC等资源进行访问和创建操作，若使用RAM用户创建服务实例，需要在创建服务实例前，对使用的RAM用户的账号添加相应资源的权限。添加RAM权限的详细操作，请参见[为RAM用户授权](https://help.aliyun.com/document_detail/121945.html)。所需权限如下表所示：

| 权限策略名称                              | 备注                            |
|-------------------------------------|-------------------------------|
| AliyunECSFullAccess                 | 管理云服务器服务（ECS）的权限              |
| AliyunVPCFullAccess                 | 管理专有网络（VPC）的权限                |
| AliyunROSFullAccess                 | 管理资源编排服务（ROS）的权限              |
| AliyunComputeNestUserFullAccess     | 管理计算巢服务（ComputeNest）的用户侧权限    |
| AliyunComputeNestSupplierFullAccess | 管理计算巢服务（ComputeNest）的服务商侧权限 ｜ |

## 服务实例部署流程

### 部署参数说明

| 参数组                             | 参数项        | 说明                                                                      |
|---------------------------------|------------|-------------------------------------------------------------------------|
| 服务实例                            | 服务实例名称     | 长度不超过64个字符，必须以英文字母开头，可包含数字、英文字母、短划线（-）和下划线（_）。                          |
|                                 | 地域         | 服务实例部署的地域。                                                              |
|                                 | 付费类型       | 资源的计费类型：按量付费和包年包月。                                                      |
| ECS实例配置                         | 实例类型       | ECS实例规格配置。                                                              |
|                                 | 实例密码       | 长度8-30，必须包含三项（大写字母、小写字母、数字、 ()`~!@#$%^&*-+=&#124;{}[]:;'<>,.?/ 中的特殊符号）。 |
| 网络配置                            | 可用区        | ECS实例所在可用区。                                                             |
|                                 | 专有网络VPC实例ID | ECS实例所在专有网络VPC实例ID。                                                     |
|                                 | 交换机实例ID    | ECS实例所在交换机实例ID。                                                         |

### 部署步骤

1. 单击[部署链接](https://computenest.console.aliyun.com/service/instance/create/cn-hangzhou?type=user&ServiceId=service-f462f9b21cb7477381f0)，进入服务实例部署界面。
2. 选择新建ECS实例并根据界面提示配置参数，配置完成后点击下一步：确认订单。
