# Sheep_link

### Design Pitch Project (ESC301)

Cluster based sheep tracking system using Global Positioning System (GPS) and Global System for Mobile Communications (GSM).

**Opportunity:**
- In Mthatha, South Africa, many farmers face problems with missing sheep. It is tedious work to look for the missing sheep as neither the shepherds nor the farmers have cars and information on where the sheep are. Therefore, they are looking for a cost-effective solution to make finding missing sheep easier. 

**Stakeholders:**
- Primary Stakeholders: Sheep owners in the rural town Rosedale, Mthatha
- Secondary Stakeholders: Sheperds, Sheep, Design Team

**Team Values:**
- sustainability
- functionality
- accessibility

**Scope:**
- Make a reliable sheep tracking system that is accessible to everyone in the community and prevents sheep from wandering off or mixing with other flocks. 

**Highlighted Features:**
- Accessibility
  - Inexpensive due to use of GSM for transmittion
  - Offered in both English and Xhosa (local language)
- Effectiveness
  - Locates the sheep and notifies the shepherds once they go missing. 
  - Prototype battery life is 24 hours, which can be made rechargeable and longer lasting.
- Durability
  - Waterproof, dustproof, and dropproof. 
  - Withstands the harsh conditions in the use case.
- Safety
- Portability

**Design Concept**
- Each tracker stores a unique sheep ID
- Two types of sheep trackers: leader and follower
  - Leader: ID starts with L, has GPS + Bluetooth transceiver
  - Follower: ID starts with F, only has Bluetooth transceiver
- Sheep information update:
  - Leaders "ping" nearest followers based on the Received Signal Strength Indicator (RSSI), and followers respond by sending their ID to the leader, then leader stores all IDs.
  - All leaders send their current cluster GPS location + stored follower IDs to the backend database.
  - Backend Clustering algorithm will send missing sheep alerts through User Interface whenever missing sheep is detected.
