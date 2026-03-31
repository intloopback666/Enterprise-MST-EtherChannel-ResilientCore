Task summary:
1. Set VTP transparent on all switches (local VLAN administration everywhere).
2. Build five EtherChannel trunk bundles with specific protocols and “active vs passive” behavior:
   - Po1 DLS1–DLS2: mode on
   - Po2 DLS1–ALS1: LACP (DLS1 active, ALS1 passive)
   - Po3 DLS1–ALS2: PAgP (DLS1 desirable, ALS2 auto)
   - Po4 DLS2–ALS1: LACP (DLS2 active, ALS1 passive)
   - Po5 DLS2–ALS2: PAgP (DLS2 desirable, ALS2 auto)
3. Protect against EtherChannel mismatch loops using EtherChannel misconfig guard, and enable errdisable recovery for channel-misconfig after 10 minutes.
4. Create VLANs 100–800 (100,200,300,400,500,600,700,800) on all switches.
5. Configure MST with your own region name/revision; map VLANs to instances 1–4 and force each instance root to a different switch.
6. Use 802.1t long path costs.

> *Note: “mode on” bundles don’t negotiate and are easy to misconfigure; used for lab learning, not recommended operationally.*
