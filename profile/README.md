# WiMoVE - Wireless Mobility through VXLAN EVPN

In large Wi&#8209;Fi systems, broadcast traffic can take up large amounts of airtime[^1].
Partitioning a Wi&#8209;Fi system into multiple subnets breaks handover while solutions like broadcast suppression break user functionality.

**WiMoVE** is a scalable Wi&#8209;Fi System that partitions stations into overlay L2 domains to limit the amount of wireless L2 broadcast traffic.
Overlay L2 domains "follow" the stations, being resized on demand, thus preserving handover.

WiMoVE is built with standard network protocols, on top of open&#8209;source technology:

- The overlay networks use [BGP EVPN](https://www.rfc-editor.org/rfc/rfc8365.html) with [VXLAN](https://www.rfc-editor.org/rfc/rfc7348) encapsulation.
- All BGP speakers run [FRRouting](https://frrouting.org/) to exchange EVPN routes.
- The access points run [OpenWRT](https://openwrt.org/) with a custom, open&#8209;source daemon called [wimoved](https://github.com/wimove-oss/wimoved).

This solution allows for using commodity access points running OpenWRT for large&#8209;scale Wi&#8209;Fi deployments, even from different vendors.

[^1]: See <https://www.youtube.com/watch?v=v8y-r9JBhmw> for a talk on this issue.
