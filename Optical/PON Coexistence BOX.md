



参考资料

How Does XGS-PON Coexist With GPON and XG-PON?

https://www.glsunmall.com/fiber-optic-articles/how-does-xgs-pon-coexist-with-gpon-and-xg-pon-.html 

What is XGS-PON?

XGS-PON is a type of Passive Optical Network (PON) technology. PONs use fiber optic cables to transmit data over long distances with minimal signal loss. In a PON network, a single fiber optic cable connects a service provider's central office (called an OLT - Optical Line Terminal) to multiple user s (connected by ONUs - Optical Network Units).

XGS-PON, or 10 Gigabit-capable Symmetric Passive Optical Network, is a cutting-edge technology for fiber optic internet access. It offers a significant leap forward in internet speeds compared to its predecessors, GPON (Gigabit PON) and XG-PON (10G-PON).

XG-PON and XGS-PON both belong to the GPON series. From a technical roadmap, XGS-PON is the technological evolution of XG-PON.
<img width="500" height="279" alt="image" src="https://github.com/user-attachments/assets/2c4f87b5-8ce2-4d7b-8ac3-de2cddb13c60" />

 

XG-PON and XGS-PON are both 10G PON. The main difference is that,XG-PON is an asymmetric PON, and the upstream/downstream rate of the PON port is 2.5G/10G; XGS-PON is a symmetrical PON, and the upstream/downstream rate of the PON port is 10G/10G.

Feature	GPON	XG-PON	XGS-PON
Maximum Downstream Speed	2.5 Gbps	10 Gbps	10 Gbps
Maximum Upstream Speed	1.25 Gbps	2.5 Gbps	10 Gbps
Symmetry	Asymmetrical	Asymmetrical	Symmetrical
Maturity	Mature	More advanced	Newest
Cost	More cost-effective	Moderately priced	More expensive

The main PON technologies currently used are GPON and XG-PON, both of which are asymmetric PON. Since the user's uplink/downlink data is generally asymmetrical, taking a certain first-tier city as an example, among the OLT's uplink traffic, the uplink traffic averages only 22% of the downlink traffic. Therefore, the technical characteristics of asymmetric PON are basically in line with the needs of users. match. More importantly, the uplink rate of asymmetric PON is low, the cost of transmitting components such as lasers in ONU is low, and the equipment price is correspondingly low.

However, user needs are diverse. With the rise of live broadcasting, video surveillance and other services, there are more and more scenarios where users are more concerned about uplink bandwidth. Inbound private lines need to provide uplink/downlink symmetrical circuits. These businesses promote the demand for XGS-PON.

XGS-PON is the technological evolution of GPON and XG-PON, and supports hybrid access of three types of ONUs: GPON, XG-PON and XGS-PON.

Coexistence of XGS-PON and XG-PON

Like XG-PON, XGS-PON uses broadcasting for downlink and TDMA for uplink.

Since the downlink wavelength and downlink rate of XGS-PON and XG-PON are the same, the downlink of XGS-PON does not distinguish between XGS-PON ONU and XG-PON ONU. The optical splitter broadcasts the downlink optical signal to the same ODN link. For each XG(S)-PON (XG-PON and XGS-PON) ONU, each ONU chooses to receive its own signal and discards other signals.
<img width="512" height="283" alt="image" src="https://github.com/user-attachments/assets/b9104c96-a992-4718-a5a5-97befe441371" />

 

The uplink of XGS-PON transmits data according to time slots, and the ONU sends data within the time slots allowed by the OLT. OLT dynamically allocates time slots based on the traffic requirements of different ONUs and the type of ONU. In the time slot allocated to XG-PON ONU, the data transmission rate is 2.5Gbps; in the time slot allocated to XGS-PON ONU, the data transmission rate is 10Gbps.
<img width="520" height="280" alt="image" src="https://github.com/user-attachments/assets/29d7538b-96d9-40d8-a423-ab989f230f07" />

 

It can be seen that XGS-PON supports mixed access with XG-PON and XGS-PON ONUs.

Coexistence of XGS-PON and GPON

Since the upstream/downstream wavelengths are different from GPON, XGS-PON uses the Combo solution to share ODN with GPON. XGS-PON's Combo optical module integrates GPON optical modules, XGS-PON optical modules and WDM combiners.

In the upstream direction, after the optical signal enters the XGS-PON Combo port, WDM filters the GPON signal and XGS-PON signal according to the wavelength, and then sends the signal to different channels.
<img width="573" height="343" alt="image" src="https://github.com/user-attachments/assets/7d0d168b-d868-431c-9ac1-f5feac242e83" />

 

In the downstream direction, signals from GPON channels and XGS-PON channels are multiplexed through WDM, and mixed signals are downlinked to ONUs through ODN. Since the wavelengths are different, different types of ONUs their required wavelengths through internal filters to receive signals.
<img width="425" height="244" alt="image" src="https://github.com/user-attachments/assets/41448844-cab1-4830-9b3c-827f1eb4f225" />

 

Since XGS-PON naturally supports coexistence with XG-PON, the Combo solution of XGS-PON supports hybrid access of three types of ONUs: GPON, XG-PON and XGS-PON. The Combo optical module of XGS-PON is also called triple Mode Combo optical module (the Combo optical module of XG-PON is called a two-mode Combo optical module because it supports the mixed access of two types of ONUs, GPON and XG-PON).




https://www.softeloptic.com/news/what-is-xgs-pon-how-does-xgs-pon-coexist-with-gpon-and-xg-pon/

2. Coexistence of XGS-PON, XG-PON and GPON

XGS-PON is the technological evolution of GPON and XG-PON, and supports mixed access of three types of ONUs: GPON, XG-PON and XGS-PON.

2.1 Coexistence of XGS-PON and XG-PON

Like XG-PON, the downlink of XGS-PON adopts the broadcast method, and the uplink adopts the TDMA method.
Since the downstream wavelength and downstream rate of XGS-PON and XG-PON are the same, the downstream of XGS-PON does not distinguish between XGS-PON ONU and XG-PON ONU, and the optical splitter broadcasts the downstream optical signal to the same ODN link For each XG(S)-PON (XG-PON and XGS-PON) ONU, each ONU chooses to receive its own signal and discards other signals.
The uplink of XGS-PON performs data transmission according to time slots, and ONU sends data in the time slots permitted by OLT. The OLT dynamically allocates time slots according to the traffic demands of different ONUs and the type of ONU (is it XG-PON or XGS-PON?). In the time slot allocated to XG-PON ONU, the data transmission rate is 2.5Gbps; in the time slot allocated to XGS-PON ONU, the data transmission rate is 10Gbps.
It can be seen that XGS-PON naturally supports mixed access with two types of ONUs, XG-PON and XGS-PON.
<img width="750" height="422" alt="image" src="https://github.com/user-attachments/assets/511c3340-c5c5-415c-93df-55d0adaa5613" />
<img width="750" height="290" alt="image" src="https://github.com/user-attachments/assets/e86b9c30-9fdd-4677-a8b7-232fc692f208" />







https://www.prysmian.com/sites/default/files/atoms/files/AC036-01%20CoEx.pdf  

https://www.lightoptics.co.uk/blogs/news/full-coexistence-of-gpon-xgs-pon-and-ng-pon2




https://www.corning.com/catalog/coc/documents/selection-guides/CRR-1836-AEN.pdf

CRR-1836-AEN.pdf 
<img width="1130" height="676" alt="image" src="https://github.com/user-attachments/assets/32961654-e557-4bd7-af3b-1940f3b03eee" />
<img width="1122" height="666" alt="image" src="https://github.com/user-attachments/assets/168d70a5-8f7e-4023-9281-d4faf2e2609b" />
<img width="1131" height="765" alt="image" src="https://github.com/user-attachments/assets/ebfbbadf-999e-4fb1-b3a9-c63df8ddbb09" />
<img width="855" height="738" alt="image" src="https://github.com/user-attachments/assets/d316851f-a759-403d-8ef5-3a6264a7f12e" />

 ----------------------------
 

https://webresources.commscope.com/download/assets/Specification+Guide:+Coexistence+(CEx)+Singlemode+Devices/b57d7bfa3bd811f0b092ea1fa90d937b 

Specification Guide: Coexistence (CEx) Singlemode Devices

Specification Guide Coexistence (CEx) Singlemode Devices.pdf
<img width="1147" height="456" alt="image" src="https://github.com/user-attachments/assets/0ac62b50-670d-47b8-8504-0408f21e78d1" />


The operating wavelength band specified in Table B.9.4 is 1260-1280 nm. This corresponds to UW0 in IEEE 802.3ca. Additionally, UW1 (from IEEE 802.3ca) and UW3 (new for the 25GS-PON MSA) are also usable wavelengths for 10G upstream.

UW: upstream wavelength




downstream wavelengths (DW0-DW3) and four upstream wavelengths (UW0-UW3).




--------------------------------------

UW0, UW1, and UW3 are defined as specific wavelength ranges used in 25GS-PON (25 Gigabit Symmetric Passive Optical Network). These wavelengths are used for upstream transmission, with UW0 and UW1 being defined in IEEE 802.3ca and UW3 being a new wavelength for the 25GS-PON MSA (Multi-Source Agreement). 

Here's a more detailed breakdown:

UW0: Specifically refers to the wavelength range of 1290-1310 nm. 
UW1: Refers to the wavelength range of 1260-1280 nm. 
UW3: A new wavelength range introduced for 25GS-PON, its specific range is not mentioned in the provided context but is described as being used for 10G upstream signals. 

These wavelengths are used in 25GS-PON to allow for greater bandwidth and efficient network utilization through wavelength division multiplexing (WDM). 

-----------------------------------------

<img width="1226" height="730" alt="image" src="https://github.com/user-attachments/assets/014250ae-71de-4039-9971-6e0a95622280" />
<img width="862" height="741" alt="image" src="https://github.com/user-attachments/assets/332177ad-6b21-4360-a2f0-c827ceb6db65" />
<img width="1145" height="443" alt="image" src="https://github.com/user-attachments/assets/e2876d9f-1693-447c-9ee0-fad035e72ba8" />
<img width="912" height="806" alt="image" src="https://github.com/user-attachments/assets/ea6271e5-dcd0-4ed4-91a4-1cf4a705f12c" />
<img width="1082" height="420" alt="image" src="https://github.com/user-attachments/assets/4b6f0293-ba27-4f67-b824-dfe1b50689ff" />







https://www.zte.com.cn/content/dam/zte-site/res-www-zte-com-cn/mediares/zte/global/productimages/fm_pictures/others/White%20Paper%20on%2050G%20PON%20Technology%20V2.0_EN.pdf

White Paper on 50G PON Technology V2.0  

<img width="799" height="226" alt="image" src="https://github.com/user-attachments/assets/83519abd-aeae-4600-a156-7eca8c13a566" />




-----------------------------

https://www.ieee802.org/3/ca/public/meeting_archive/2017/09/kramer_3ca_2_0917.pdf

[kramer_3ca_2_0917.pdf](https://github.com/user-attachments/files/21932946/kramer_3ca_2_0917.pdf)





-------------------------------
https://www.itu.int/en/ITU-T/Workshops-and-Seminars/202001/Documents/Vince_Ferreti.pdf
<img width="1218" height="624" alt="image" src="https://github.com/user-attachments/assets/c378108f-e420-4568-8656-08cf38fdbbd9" />

-----------------------------
https://www.25gspon-msa.org/wp-content/uploads/2020/10/25GS-PON-Specification-V1.0-public.pdf
-------------------



https://docbox.etsi.org/ISG/F5G/Open/F5G%20External%20Presentations%202021/ECOC2021/ECOC2021%20F5G%20Workshop%20Mo2F%20(Frank%20Effenberger).pdf 

Microsoft PowerPoint - ECOC21_Effenberger_50GPONv2.pptx
<img width="1208" height="559" alt="image" src="https://github.com/user-attachments/assets/0eb1c7b2-358b-4ae6-98ba-882976ed7327" />



-------------------------
https://www.ieee802.org/3/ca/public/meeting_archive/2018/03/zhou_3ca_1_0318.pdf

Symmetric 50G PON using NRZ
<img width="1193" height="711" alt="image" src="https://github.com/user-attachments/assets/a754ba5f-dcb6-41fa-b288-b4b8c1614bfa" />
<img width="1167" height="745" alt="image" src="https://github.com/user-attachments/assets/39fca4e7-e989-4160-a357-705226075c99" />


--------------------------------------

--------------------------------------
