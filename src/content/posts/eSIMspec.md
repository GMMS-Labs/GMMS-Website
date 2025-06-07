---
title: A Technical Introduction to eSIM
description: "A breif overview of how eSIM provisioing works in M2M and Consumer usecases"
pubDate: 6/7/2025
author: guyphy
tags: 
    - test
    - example
    - "this is how tags are set up"
type: post
---

The change from the Removable SIM to an eSIM provides benefits for many players:

- For everyone, eSIM provides an equivalent level of security as the removable SIM card. This is vital as it is the subscription credentials stored on the SIM card that enable secure and private access to mobile networks. It also supports the integrity of the billing process, especially in roaming scenarios.
- For the device end user, eSIM enables simplified management of subscriptions and connections. End users will no longer have to manage several SIM cards.
- For organisations, eSIM enables remote management of subscriptions. This is a significant benefit where devices are not managed by the end user or are not be readily accessible (for example due to operational scale, making individual device management cost prohibitive). This enables pioneering categories of connected devices.
- For distributors, simplified logistics are possible, customisation for specific operators or regions may be reduced.
- Operators will have simpler means to expand their businesses into emerging markets, for example, automotive, wearables and consumer electronics. SIM card distribution costs will be eliminated, and eSIMs will enable new distribution models for devices and for marketing of subscriptions.
- Device Manufacturers, can exploit the reduced space within their products to make smaller devices. Their products could also be made more tolerant to environmental factors such as dampness, temperature and vibration as they can be hermetically (completely airtight) sealed. Manufacturers can also leverage eSIMs to optimise supply chain processes.

There are two types of RSP specifications in use today, these are:

- Consumer solution - for the ‘direct consumer’ channel. This specification assumes that the end user is familiar with operating end user UI and actively choses their network connectivity provider.
- M2M solution - for the ‘business to business to consumer’ channels, this solution serves the needs of business to business customers, specifically in the Internet of Things (IoT) market.

The profile enables root functionality of RSP and allows user device to understand and use the data provided from network operator to provide functional connectivity. A profile comprises of the operator data related to a subscription, including operator's credentials and potentially operator or third-party SIM based applications. The secure element in
the eSIM solution is called the eUICC, this can accommodate multiple Profiles. Profiles are
remotely downloaded over-the-air into a eUICC. Although the eUICC is an integral part of the
device, the Profile remains the property of the operator as it contains items “owned” by the
operator (IMSI, ICCID, security algorithms, etc.) and is supplied under licence.
The content and structure for interoperable Profiles stored on eUICCs are similar to those installed on traditional SIMs. The interoperable description of these Profiles is defined by the [SIMAlliance](https://trustedconnectivityalliance.org/technology_overview/esim/). 

## M2M Solution

The GSMA M2M RSP solution was first to be developed. There are two reasons for this:

- The M2M solution is simpler to design as end user interactions are not required and desired.
- The commercial need for technical solution that supported B2B2C deployment scenarios was greater compared to consumer focused solution at the time.

### Main System Elements

Remote SIM Provisioning for M2M utilises a server driven (push model) to provision and remotely manage operator Profiles. The solution is organised around 3 elements: the SM-DP (Subscription Manager - Data Preparation), the SM-SR (Subscription Manager - Secure Routing) and the eUICC.

The diagram below is the high-level representation of the M2M main system elements. Beyond common SIM functions, such as SIM Toolkit and Bearer Independent Protocol (BIP) support, the M2M solution does not impose additional requirements on M2M devices to enable usage of eUICCs.

SIM Toolkit - ETSI TS 102 223
BIP - ETSI TS 102 127
