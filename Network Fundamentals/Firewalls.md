# 防火墙
典型的防火墙有两个借口，连接到全球互联网的外部接口和连接到受信任网络的内部接口。

## Stateless Vs. Stateful Firewalls

A firewall that does not maintain the state of flows passing through it is known as a stateless firewall.

However, a stateful firewall, on the other hand, sees the first packet in a flow that is allowed by the configured security rules it creates a session state for it.

All subsequent packets belonging to that flow are allowed to go through. This filtering is more efficient compared to stateless firewalls that have to apply their rules to each and every packet. The flip side is the maintenance of state, which needs to be controlled.

## Host-based Vs. Network-based Firewalls
Network-based firewalls are hardware based and generally deployed on the edge of a network. They are easy to scale and simple to maintain.

A host based firewalls, however, are software based and are deployed on end-systems. They are generally not easy to scale and require maintenance.