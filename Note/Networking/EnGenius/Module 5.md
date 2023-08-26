**Failover**: Either WAN1 or WAN2 can be configured as Primary WAN. For internal clients' outbound sessions for Internet access, all outbound sessions use Primary WAN(in the diagram below, WAN1 is Primary WAN), and Secondary WAN is used as Standby which is active when Primary fails.



**Load Balance**: Either WAN1 or WAN2 can be configured as Primary WAN. WAN1 and WAN2 are used for internal clients' outbound sessions for Internet access. The Load Balance algorithm is based on WRR (Weighted Round Robin) with WAN1/WAN2 ISP upload bandwidth. For example, if WAN1 download/upload bandwidth is 50Mbps/20Mbps, and WAN2 download/upload bandwidth is 35 Mbps/6 Mbps, then the Load Balance outbound sessions distribution ratio will be WAN1:WAN2 = 20:6 = 10:3.
Cellular failover is activated when both WAN1/WAN2 fails.



![network type.jpg](../../_resources/network%20type.jpg)
***
ESG510 Dual WAN for Inbound Service Sessions

Active/Standby: Either WAN1 or WAN2 can be configured as Primary WAN. For the following inbound services: Port Forwarding, 1:1 NAT, Web(Local Status Page Status & Configuration), Primary is active, Secondary WAN is Standby, Secondary WAN is active when Primary WAN fails
Active on Primary only: Either WAN1 or WAN2 can be configured as Primary WAN. For inbound Client VPN and Site to Site VPN Services, only Primary WAN is active. When Primary WAN fails, Secondary WAN will not become active automatically. Therefore, secondary WAN must be manually reconfigured as Primary to take service when Primary WAN is down.