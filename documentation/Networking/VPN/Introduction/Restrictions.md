# 使用限制
#### 京东云对客户端VPN设备的要求
* 支持标准的IPsec协议，支持隧道模式，支持ESP；
* 支持IKE、IPsec两阶段协商的相关参数；
* 支持基于Route-Based VPN，需绑定隧道至设备的逻辑接口；
* 客户端使用Static的、Internet-routable的IPv4地址作为隧道外层地址，用于终结VPN隧道；
* 若客户端是防火墙设备，或配置了安全策略，需放行如下协议端口：
  - UDP 500，用于IKE协商；
  - IP 50，用于IPsec ESP协商及加密的数据包传输；
  - UDP 4500，若您的客户端设备位于NAT设备之后，则需要同时启用NAT Traversal (NAT-T)；
* MTU不超过1450；


#### 客户端兼容性
已测试通过的客户端列表：
  * 硬件设备：
    - Cisco IOS 15.0(or later) software；
    - HUAWEI USG6500系列防火墙；
  * 开源VPN解决方案：如strongSwan等；
  * 其它公有云厂商的VPN产品；


``测试连通性未通过的客户端列表：``
  * 深信服硬件设备或网关镜像，京东云VPN是基于路由的IPsec，深信服设备仅支持基于策略的IPsec，在隧道第二阶段协商时存在问题，故连通性测试未通过，已与深信服相关部门同事沟通，双方将于近期分别更新各自的软件版本，以便支持双方的VPN连通性。



#### VPN相关资源配额

|   产品   |                            资源                             |                                  限制                                  | 例外申请方式 |
|:--------:|:-----------------------------------------------------------:|:----------------------------------------------------------------------:|:------------:|
| VPN连接  |         同一地域每个边界网关支持创建的VPN连接的数量         |                                   10                                   |     工单     |
|          |                同一VPN连接云端公网地址的数量                |                                   2                                    |   不可提升   |
|          |               同一VPN连接可创建VPN隧道的数量                | 最多创建(VPN连接的云端公网地址数量  * 客户网关的公网地址数量个)VPN隧道 |   不可提升   |
|          | 同一对云端公网地址和客户网关公网地址之间可创建VPN隧道的数量 |                                   1                                    |   不可提升   |
| 边界网关 |                  同一地域下边界网关的数量                   |                                   5                                    |     工单     |
|          |                同一边界网关可创建的VPC接口数                |                                   50                                   |     工单     |
|          |               同一边界网关静态路由规则的数量                |                                   50                                   |     工单     |
|          |               同一边界网关动态路由规则的数量                |                                  300                                   |     工单     |
| VPC接口  |        同一对VPC和边界网关之间可创建的VPC接口的数量         |                                   1                                    |   不可提升   |
| 客户网关 |                  同一地域下客户网关的数量                   |                                   10                                   |     工单     |
|          |                 同一客户网关公网地址的数量                  |                                   4                                    |   不可提升   |
