# 绑定弹性公网IP

## 操作步骤

容器实例与Pod的弹性公网IP绑定流程除第一步其余流程完全一致    
1a. 打开京东云控制台，选择【弹性计算】-【原生容器】-【容器实例】进入原生容器实例列表页。  
1b. 打开京东云控制台，选择【弹性计算】-【原生容器】-【Pod】进入Pod实例列表页。  
2.  在实例列表中选择需要绑定弹性公网IP的实例，点击名称进入详情页。  
3.  点击【弹性网卡】Tab，选择需要绑定弹性公网IP的弹性网卡，找到需要绑定的内网IP，点击【绑定公网IP】按钮。
4.  在弹出弹窗中，选择未绑定资源的公网IP，点击【确定】。
		
		请注意：
		* 辅助网卡不允许绑定单可用区公网IP；
		* 列表页绑定公网IP即为云主机主网卡主内网IP绑定。
		
此外，您还可以：

* 在实例列表页面操作对实例主网卡主内网IP绑定弹性公网IP，操作步骤如下：  
	1a. 打开京东云控制台，选择【弹性计算】-【原生容器】-【容器实例】进入原生容器实例列表页。  
	1b. 打开京东云控制台，选择【弹性计算】-【原生容器】-【Pod】进入Pod实例列表页。  
	2. 在实例列表中选择需要对主网卡主内网IP绑定弹性公网IP的实例，点击绑定公网IP。
	3. 在弹出弹窗中，选择未绑定资源的公网IP，点击【确定】。
	 
* 从弹性网卡控制台进行绑定操作，详细步骤请参见[弹性网卡侧绑定公网IP](../../../../Networking/Elastic-Network-Interface/Operation-Guide/Private-IP-Management/Associate-Elastic-IP.md)。

## 相关参考

[弹性网卡侧绑定公网IP](../../../../Networking/Elastic-Network-Interface/Operation-Guide/Private-IP-Management/Associate-Elastic-IP.md)