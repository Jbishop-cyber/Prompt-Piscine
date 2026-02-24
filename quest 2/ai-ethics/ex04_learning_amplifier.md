# Exercise 4: AI as Learning Amplifier

## Phase 1: Build Foundation

### Active Reading & Self-Explanation

I studied wireless routing protocols including OSPF, RIP, and AODV.  

I explained to myself:

- **What is routing**

Routing is the process of selecting the best path for data packets to travel across a network from a source to it's destination

- **How do nodes discover paths**
  
They do so by using two strategies: Proactive(Table-driven) and Reactive(On-demand)

- **What is a routing table?**
- 
A routing table is a dynamic or static data table stored in a router or network device (like a computer) that acts as a map, listing routes to specific network destinations.

- **What happens when a link fails?**
  
Each routing protocols handle this differently:

- **RIP (Routing Information Protocols):** This is a bit slow as it uses routing timers, if nothing is heard from it's neighbors for a long time, it will eventually realize that the link is dead. This can lead to routing loops where data packets go in circles until the update spreads.

- **OSPF(Open Shortest Path First):** Unlike RIP, OSPF is very fast. When a link drops, the nose send a link state advertisement to the whole network, then the Dijkstra's algorithm is instantly used to find a detour.

- **AODV(Ad-hoc on demand Distance Vector):** If a link breaks while data is flowing, a Route Error(RERR) message is sent back to the source.

- **How routers discover and maintain paths?**

- Proactive (OSPF/RIP) are always chatting, they send hello packets to neighbors to confirm that they are still there.

- Reactive (AODV) stay silent until there is a packet to send, it will then brodcast a Route Request (RREQ). The neighbors would pass this message along until it gets to it's destination, which sends back a Route Reply (RREP).

### Simple Scenario Design (5–10 Devices)

- 6 IoT devices in a smart building; Temperature sensors, smart lights, security cameras.
- 2 access points (APs) for connectivity.
- 1 local controller to aggregate data.

### Justification:

- 6 devices are enough to simulate routing table updates.
- Access points reduce network congestion.
- Centralized controller ensures efficient data aggregation while maintaining local device communication.

### Self-Explanation Questions:

- Who talks to who?

IoT Devices sends small data to the two access points, the two access points acts as bridges, by collecting wireless signals and forwarding them to the local controller.

- What if one router dies?

If one access point dies, the devices would notice a link failure because they stopped receiving data or signals, this would prompt the device to start scanning other for other channels. 

- How does traffic reroute?

This is where the routing protocol starts, after the device finish scanning for other channels, it would hear access point two and joins with it, then access point two would then send a message to the controller tell it to stop sending messages to access point one, the controller then updates it's own internal routing table.

## Phase 2: Strategic AI Use:

- Question: 

I designed a 6-device IoT network using AODV. Are there edge cases I didn’t consider?

- Answer: 

AI helped me identify edge cases like sudden device failure, traffic congestion during route delivery, battery imbalance and link instability.

## Phase 3: Real Application:

- Design a small smart-city network (1,000 IoT sensors, 50 traffic lights, 10 emergency vehicles). Decide protocols, justify choices, list failure points, then refine with AI feedback.

- Answer:
A core backbone would be needed to connect everything together, because without it diffent parts of the city would operate in isolation, causing delays, poor cordination and unreliable emergency response.

The smart-city network is split into different parts: the sensors would use AODV to save power, the traffic ligths and the core backbone use OSPF to ensure quick and reliable communication, while the emergency vehicles would most likely use a hybrid protocol.

### AI Feedback:

- Network Architecture (Layered Model)

Instead of one giant flat network, we segment:

Layer A — Sensor Mesh Network

Clusters of 50–100 sensors per zone
Each zone connects to a local gateway.

Layer B — Traffic Control Network

Dedicated wired/wireless backbone connecting all 50 intersections.

Layer C — Emergency Vehicle Network

Mobile nodes connecting via cellular + city wireless.

Layer D — Core Backbone

Fiber-based IP backbone connecting:

Gateways, Traffic controllers, Data center and Emergency dispatch.

### Protocol Decisions & Justification:

- Sensor Layer (1,000 IoT Devices)

The protocol Type would be a reactive mesh routing (AODV-style) or RPL. This is because of low power consumption, the routes create only when needed and it is suitable for constrained IoT hardware. The downside to this would be a route discovery delay and a flooding overhead in dense clusters. To prevent this we would create a cluster-based gateways, limit hop count and data aggregation at edge.

- Traffic Light Layer (50 Intersections):

The protocol type for this would be a link-state routing like OSPF, because of it's fast convergence, dterministic routing, precomputed paths (no first-packet delay) and it's reliablity for mission-critical timing. But the downside to this is the higher memory/CPU usage and constant control traffic, to mitigate this we make use of industrial-grade controllers and segment the OSPF areas.

- Emergency Vehicles (Mobile Nodes):

The protocol type in this case is Hybrid (i.e both LTE/5G connectivity and Ad-hoc reactive routing), because of it's high mobility, the constant need for maintaining connection during disasters and it would need priority routing (QoS). The problem with this is the dependence on carrier infrastructure and network hand-off latency, but this can be fixed by using dual radio interfaces and prioritize traffic tagging.

- Core Backbone: 

The protocle type is the OSPF, because it scales well, supports hierarchical design, a fast failure detection and the fiber links in ring topology for redundancy.

### Failure Points:
The failure points for he entire system include gateway failure, link congestion, cascading controller failure, routing Instability and security threats. 

## Reflection:

- % human judgment vs. AI contribution:

About 65% of the design decisions came from me, AI helped me consider rear problems, validate downsides, and suggest improvement needed.

- Could you defend decisions without AI?

Yes, because I understand why each protocol was chosen, the layered architecture, and the mitigation strategies for failure points.

- What will you still remember in 6 months?

I will remember the importance of segmenting networks, choosing protocols based on device constraints, and planning for failure points. 

Did AI make you sharper, or think for you?

AI amplified my thinking by showing me rear problems and solutions, but the architecture design, and mitigation strategies were all my own work.
