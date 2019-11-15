提供基于 Java 的常见服务监控服务，以插件形式来支持未来新增服务监控。

预计提供的功能：

1. 监控功能，为告警和图表化提供基础数据支撑
2. 告警功能，提供丰富的告警通道
3. 图表功能，可视化监控指标

系统只提供一个监控框架，包括：

1. 网络通信模块，以便与不同网络协议的服务建立通信通道
2. 协议模块，用于认证、协调、识别不同服务的监控数据，需要定义一个通用的监控协议（参考 JMX），开发者负责编写具体的协议逻辑
3. 数据模块，采用时序数据库保存协议采集到的各类数据
4. 告警模块，用于向预定义用户组发送告警信息
5. 图表模块，展示时序数据库内的各类数据库

那么，为什么不使用 ELK stack ？
