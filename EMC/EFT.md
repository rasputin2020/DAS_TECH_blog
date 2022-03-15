# EFT
http://cn.noiseken.com/uploads/photos0/50.pdf      IEC61000-4-4

http://cn.noiseken.com/uploads/photos0/85.pdf      IEC61000-4-5 Ed.2的试验标准


应用EFT脉冲  
      首先，测试涉及注入EFT脉冲到设备的AC电源线。的EFT波形也可以注入到信号线和控制线，和接地连接，以模拟的瞬态噪声的耦合到这些行。脉冲波形具有高振幅，短上升时间，高重复率和低能量含量。  
      它由每300毫秒重复一次的75个脉冲组成，持续时间为1分钟。在测试期间注入正极性和负极性EFT脉冲。    
![image](https://user-images.githubusercontent.com/84896436/158327462-7ab4597c-b293-4977-a70a-f5883c4c29c9.png)

 
EUT位于绝缘支撑上水平接地平面上方10厘米的非金属工作台上。水平接地平面与接地系统以及测试发生器和耦合解耦网络相连。被测设备应按设备安装规范进行布置和连接，以满足其功能要求。  

![image](https://user-images.githubusercontent.com/84896436/158327554-b71a5010-5894-4e2c-a04e-2d3bbd0632c3.png)  

      使用耦合/去耦网络在电源端口上直接耦合EFT电压是优选的。对于具有没有接地端子的电源端口的被测设备，测试电压仅应用于L和N线。如果合适的偶联去耦网络不可用时，可替代方法中的一种，可以使用：
•在公共和未对称模式的情况下，直接注射使用（33 ± 6，6）nF电容是优选的耦合模式;   
•如果直接喷射不实用，则应使用电容钳。  
 
对于信号，控制和电信端口，使用电容耦合钳位。对于接地端子，耦合去耦装置是优选的。

***From <http://www.cerz8.com/news/gongsixinwen/349.html> ***


Test Levels  
Standard	Applicability	Test Voltage  
EN 50082-1	Generic Immunity - Residential, Commercial and Light Industrial	1kV  
EN 50082-1 Draft	Draft Generic Immunity - Residential, Commercial and Light Industrial	1kV  
EN 50082-2	Generic Immunity - Industrial Environment	2kV  
EN 50082-2 Draft	Generic Immunity - Industrial Environment	2kV  
EN 55104	Immunity for Household Appliances, Tools and Similar Apparatus	1kV  
 
Test Set-Up    
![image](https://user-images.githubusercontent.com/84896436/158328688-6d5e2c4e-a08f-4b0e-ac20-042453452548.png)

![image](https://user-images.githubusercontent.com/84896436/158328713-54cae222-8ae6-4c64-93cb-95b88b551d55.png)
 
Coupling Methods  
Capacitive coupling via 33nF capacitors is the required coupling method for AC or DC power mains. These coupling capacitors are included as part of a Coupler/ Decoupler (C/D) in commercially available EFT simulators. The design of the decoupling portion of the C/D, which prevents the EFT burst from traveling back onto the power mains, is also specified in IEC 61000-4-4.

A capacitive coupling clamp is used to couple EFT bursts onto data, I/O, and telecommunications lines. Construction of the clamp is shown in Figure 5 of IEC 61000-4-4; however, considerable differences exist in commercially available clamps. Some clamps use higher quality materials and some designs allow for the use of an optional safety interlocked cover.
 
Waveforms  
![image](https://user-images.githubusercontent.com/84896436/158328745-9481fe9a-5659-48db-95d4-b0aa2c06b50b.png)

***From <https://www.atecorp.com/compliance-standards/iec/iec-61000-4-4>*** 

IEC/EN 61000-4-5 Surge 雷擊突波耐受


