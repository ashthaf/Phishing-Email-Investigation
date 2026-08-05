### Hop 1

**Receiving Server:** mail-ot1-f72.google.com

**Protocol:** SMTP

**Observation:**

This is an internal Google SMTP processing record. The header contains only a `by` clause and does not specify the originating server. No suspicious behavior was identified. This hop represents internal message handling within Google's mail infrastructure.

### Hop 2

**Source Server:** mail-ot1-f72.google.com

**Source IP:** 209.85.210.72

**Observation:**

The email was relayed through Google's SMTP infrastructure. The source IP belongs to Google's mail network, indicating the message originated from or passed through a trusted Google-hosted mail service. No evidence of direct delivery from an unknown or suspicious host was observed at this hop.

### Hop 3

**Source Server:** DU2PEPF00028D01.eurprd03.prod.outlook.com

**Organization:** Microsoft Exchange Online

**Observation:**

The email entered Microsoft's Exchange Online infrastructure after leaving Google's mail servers. The hostname belongs to Microsoft's official Outlook/Exchange Online environment. No suspicious routing behavior was identified at this hop.

### Hop 4

**Source Server:** DB9PR06CA0009.eurprd06.prod.outlook.com

**Source IP:** 2603:10a6:10:1db::14 (IPv6)

**Organization:** Microsoft Exchange Online

**Observation:**

The email was relayed internally within Microsoft's Exchange Online infrastructure. The IPv6 address belongs to Microsoft's mail network and represents normal internal routing between Exchange Online servers. No suspicious activity was identified at this hop.

### Hop 5

**Source Server:** DS0PR10MB8080.namprd10.prod.outlook.com

**Source IP:** ::1 (IPv6 Loopback)

**Organization:** Microsoft Exchange Online

**Observation:**

The final processing occurred on a Microsoft Exchange Online mailbox server. The loopback address (::1) indicates local processing within the Exchange server during mailbox delivery. This is expected behavior and is not considered suspicious.

---

# Investigation Evidence

## Mail Route

![Mail Route](../Screenshots/mail-route-numbered.png)

The complete delivery path was reconstructed from the Received headers.

---

## Hop Analysis

![Hop Analysis](../Screenshots/hop-analysis.png)

Each mail hop was reviewed to identify suspicious routing behaviour.

---

## Received Headers

![Received Headers](../Screenshots/received-hops.png)

The Received header chain was analyzed.

---

## Routing Reconstruction

![Routing Analysis](../Screenshots/routing-analysis.png)

The email routing path was reconstructed successfully.

---

## Host Analysis

![Host Analysis](../Screenshots/host-analysis.png)

Mail server host information was examined.

---

## Host Information

![Host Information](../Screenshots/host-information.png)

Supporting host information collected during routing analysis.
