# MOV、TSS、TVS、ESD、GDT、SPG、PPTC 

主流的电路保护器件：瞬态电压抑制器，Transient Voltage Suppressors，简称TVS；  
压敏电阻，Metal Oxide Varistors，简称MOV；  
静电保护元件，Electrostatic Discharge Protection Devices，简称ESD；  
陶瓷气体放电管，Gas Discharge Tubes，简称GDT；  
玻璃气体放电管，Spark Gap Protectors，简称SPG；  
半导体放电管，Thyristor Surge Suppressors，简称TSS；  
自恢复保险丝，Polymer Positive Temperature Coefficient，简称PPTC。  
按照器件的伏安特性，保护器件可分为三大类：箝位型（MOV、TVS、ESD）、开关型（GDT、SPG、TSS）、过电流型（PPTC）。箝位型过电压保护器件为电压控制型器件。  

在电压达到击穿电压时，器件的电阻瞬间减小为低阻抗，泄放大浪涌电流，从而将浪涌电压限制在一个较低的水平。导通后，器件的箝位电压会高于击穿电压，器件两端的箝位电压与瞬间通过的浪涌电流大小成正比关系    


按照器件的伏安特性，保护器件可分为***三大类：箝位型（MOV、TVS、ESD）、开关型（GDT、SPG、TSS）、过电流型（PPTC）***。箝位型过电压保护器件为电压控制型器件。在电压达到击穿电压时，器件的电阻瞬间减小为低阻抗，泄放大浪涌电流，从而将浪涌电压限制在一个较低的水平。导通后，器件的箝位电压会高于击穿电压，器件两端的箝位电压与瞬间通过的浪涌电流大小成正比关系。  
![image](https://github.com/rasputin2020/DAS_TECH_blog/assets/84896436/d2251782-5aa6-48ad-9fce-1ac713a0c590)  
***箝位型过电压保护器件***常应用于电源线、低频通信线路的过电压防护，代表产品有：金属氧化物压敏电阻（MOV）、瞬态电压抑制二极管（TVS）、静电保护（ESD）元件。  
金属氧化物压敏电阻MOV的通流量仅次于GDT，响应速度为纳秒级，广泛应用于交流电源线，低频信号线的防雷保护。使用中，由于GDT和SPG具有较大的绝缘阻抗，在AC输入端，常常和MOV串联到共模地来应用，以减缓MOV的老化。  
瞬态（瞬变）电压抑制二极管简称TVS器件，在规定的反向应用条件下，当承受一个高能量的瞬时过压脉冲时，其工作阻抗能立即降至很低的导通值，允许大电流通过，并将电压箝制到预定水平，从而有效地保护电子线路中的精密元器件免受损坏。TVS能承受的瞬时脉冲功率可达上千瓦，其响应时间仅为1ps（10^-12S）。TVS允许的正向浪涌电流在T =25℃，T=10ms条件下，可达50～200A 。  
双向TVS可在正反两个方向吸收瞬时大脉冲功率，并把电压箝制到预定水平，双向TVS适用于交流电路，单向TVS一般用于直流电路。    

对于***开关型过电压保护器件***，当电压达到击穿电压后，其电阻瞬间减小为低阻态，泄放浪涌电流，并将浪涌电压限制在一个较低的水平。开关型过电压保护器件的特点是器件导通后其两端的电压会低于器件的击穿电压，常用于通信系统高频信号线浪涌防护，主要有陶瓷气体放电管（GDT）、玻璃气体放电管（SPG）、半导体放电管（TSS）。  
![image](https://github.com/rasputin2020/DAS_TECH_blog/assets/84896436/a5d2c391-c707-465d-aa98-2f07fb1f5ae5)  
  
陶瓷气体放电管（Gas Discharge Tubes, GDT）由封装在充满惰性气体的陶瓷管中具有一个或一个以上的放电间隙组成。GDT电气性能取决于气体种类、气体压力、内部电极结构、制作工艺等因素。GDT可以承受高达数十甚至数百千安培的浪涌电流冲击，具有极低的结电容，应用于保护电子设备和人身免遭瞬态高压的危害。GDT可用于高速通信电路防雷保护，如同轴电缆，电话线接口，以太网端口等。

TSS为一种具有负阻特性的浪涌保护器件，由于其特殊的PNPN结结构设计，在相同的芯片面积上，TSS可以做到比同尺寸及电压的TVS通流量大几倍，而电容比同规格的TVS小几倍，可以用于一些通信线路的浪涌保护，如RS485、RS232、CAN总线等。TSS具有较高的性价比，是低速通信线路浪涌防护的理想选择。

除了上述三大类器件，FAE工程师在系统电路设计中，应组合使用多个电路保护器件及方案。  
![image](https://github.com/rasputin2020/DAS_TECH_blog/assets/84896436/01ded8e3-f9a4-4cfb-86aa-4ceb8414830e)  

————————————————————————————————————————————————————————————————————————  
![image](https://github.com/rasputin2020/DAS_TECH_blog/assets/84896436/5e4eeefc-26ff-4de4-9116-bd5615f75d3c)  
TSS由于寄生电容稍低，多用于信号接口应用保护，如音视频接口和串口防雷保护，而TVS寄生电容高，有箝位，多用于电源口的过压保护   

——————————————————————————————————————————————————————————————————————————————————  
from：3  
TVS器件具有很高的对地阻抗。当在系统输入端存在一个大于TVS击穿电压的瞬变电压时，TVS被击穿并提供低阻抗接地路径，将瞬变电流从开关输入端转移到地，从而输入端电压被箝位。TVS器件的重要参数包括：工作峰值反向电压，低于此电压便不会发生明显的导通；
击穿电压，在该电压时发生一定程度的导通；以及最大箝位电压，这是传导额定最大电流时器件上的最大电压。    

选择TVS器件时，另一个要考虑的参数是其最大箝位电压。在浪涌事件期间，当越来越大的电流流过TVS器件时，TVS的箝位电压可以升高到最大箝位电压。对于TVS，此最大箝位电压高于击穿电压。高击穿电压（如54 V）TVS的最大箝位电压
大于ADG5412F数据手册中针对源极引脚规定的±55 V直流绝对最大额定值。但是，“浪涌测试，IEC61000-4-5”部分证明，在浪涌瞬变持续时间内，ADG5412F可以承受大于直流最大额定值的电压。这是因为浪涌瞬变的上升时间比ESD脉冲慢得多，故在浪涌瞬变持续时间内，ADG5412F内部ESD保护不会触发。   

————————————————————————————————————————————————————————  
![image](https://github.com/rasputin2020/DAS_TECH_blog/assets/84896436/c05d56ab-abe9-4684-bd11-9b002bce0e27)



## 参考   
1.https://bbs.eeworld.com.cn/thread-1170094-1-1.html   
2.采用 TVS 二极管的高压 ADC 电路输入保护  
https://www.ti.com.cn/cn/lit/an/zhcacm1a/zhcacm1a.pdf?ts=1718676384534&ref_url=https%253A%252F%252Fwww.bing.com%252F    
[采用 TVS 二极管的高压 ADC 电路输入保护.pdf](https://github.com/user-attachments/files/15967724/TVS.ADC.pdf)  
3.利用ADG5412F解决模拟输入的IEC系统保护  https://www.analog.com/media/cn/technical-documentation/application-notes/an-1436_cn.pdf  
[采用 TVS 二极管的高压 ADC 电路输入保护.pdf](https://github.com/user-attachments/files/15967761/TVS.ADC.pdf)  
4.电路保护器件的电气特性 https://mbb.eet-china.com/forum/topic/132927_1_1.html  



