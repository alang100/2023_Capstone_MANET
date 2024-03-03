# 2023_Capstone_MANET

The repository contains our final submission for our capstone project which was completed in May 2023.

### Introduction and Description of the Project

A Mobile Ad Hoc Network (MANET) is a type of wireless network where several devices, such as radios, smartphones, laptops, cars, drones, or sensors, communicate directly without needing any pre-existing or centralized infrastructure. MANETs are self-configuring and self-maintained by their nodes, making them ideal for situations where existing network infrastructure is damaged, unavailable, or not possible such as in disaster-stricken areas, military operations, or remote regions.
For example, in a region recently devastated by an earthquake, communication infrastructure such as mobile networks may be severely damaged. In such an event, rescue and emergency services could rapidly set up a MANET to quickly establish a wireless network among their devices to exchange vital information and communications. Likewise, in military operations where fixed network infrastructure is unavailable, MANETs can enable military personnel and unmanned devices to communicate and share tactical information in real-time using wireless devices.
A commonly used routing protocol in MANETs is the Ad-hoc On-Demand Distance Vector (AODV) protocol. AODV is a reactive routing protocol, which means that it establishes routes between nodes on-demand when required rather than maintaining pre-established routes. AODV uses a route discovery mechanism where nodes broadcast route requests to find a route to a destination node. When a route is discovered, AODV establishes a temporary route and maintains it for as long as the nodes are actively communicating. AODV protocol is widely used in MANETs due to its simplicity, scalability, and adaptability to changing network topologies due to the mobility of nodes.
However, protocols like AODV are vulnerable to various types of cyber-security threats, one of the most common being black hole attacks. A black hole attack is a type of cyber-attack where a malicious node infiltrates the network and falsely claims to have the shortest route to a destination, making it the prioritized path for link establishment. Doing so attracts routing and data traffic towards it, but it drops the received packets instead of forwarding them to the desired destination. This will severely disrupt communication in the network between nodes and cause the loss of vital data, leading to performance degradation and network instability. Hence, black hole attacks can cause severe disruptions in critical operations, making them a significant security concern in MANET environments.

Figure 1 in the final report shows a diagram of a MANET where the source node S sends a route request to the destination node D. The malicious node A replies with a fake route response message, claiming to have the shortest route to node D. Node S would then establish a route to node D through node A, but the packets would be dropped by node A instead of being forwarded to the destination.
This project aimed to develop a solution using machine learning techniques that could detect black hole intruders in a MANET utilizing the AODV protocol. The project consisted of three major phases.

**Phase 1**
In the data creation phase, a MANET network would be simulated using the NS3 simulator, incorporating the AODV routing protocol. The simulation would also include a small number of black hole nodes. Finally, the simulation would generate output files comprising various network metrics, AODV messaging, and data flow between the nodes.
**Phase 2**
In the data preparation phase, a script would be developed to process the simulation files and convert them into a dataset that could be used to train a machine learning classifier. This would involve identifying and extracting various relevant features that could be used to detect the behaviour of black hole nodes.

**Phase 3**
The machine learning (ML) phase would develop a machine learning process using the dataset generated in stage 2 as input to train ML classifiers to detect which neighbour nodes were black hole nodes.
