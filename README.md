
### jeremy-ellis-tinyML-teacher-feedback-2022



##### version 0.1.0-3


Demo of this Github at [https://hpssjellis.github.io/jeremy-ellis-tinyML-teacher-feedback-2022/](https://hpssjellis.github.io/jeremy-ellis-tinyML-teacher-feedback-2022/)


This Github Repository at  [https://github.com/hpssjellis/jeremy-ellis-tinyML-teacher-feedback-2022](https://github.com/hpssjellis/jeremy-ellis-tinyML-teacher-feedback-2022)

 To make your own version of this webApp just copy this readme file in your own Gitpages activated repository and link to the readme.md file as a webpage.

Number of Slides: <input type="text" id="myCountLinks" size="6" value="15" >, Seconds per Slide: <input type="text" id="myCountMax" size="6" value="20" >

<div id="myNumSlides" style=" position:sticky; top:0px; left:20px; height:25px; "> ...</div>  <br>

  









<div id="myStick"  style=" position:sticky; top:30px; display:inline; ">
 
 <input type=button value="Start-No-Sound" onclick="{
   document.getElementById('myStick').style.display = 'none';                                                 
   xSlide  = document.getElementById('myCountLinks').value; 
   myMainNum = document.getElementById('myCountMax').value;    
   myAudio01.pause();
   myAudio01.currentTime = 0;  
   myIndex = 0;  
   clearInterval(myLooper);  
   myCountUp = -1;
   carousel();  
}">
 
<input type=button value="Start-Pre-Recorded" onclick="{                                                        
   document.getElementById('myStick').style.display = 'none';   
   xSlide  = document.getElementById('myCountLinks').value; 
   myMainNum = document.getElementById('myCountMax').value;  
   myAudio01.pause();
   myAudio01.currentTime = 0;                                                
   myAudio01 = new Audio('recorded-talk.m4a');
   myAudio01.play(); 
   myIndex = 0;  
   clearInterval(myLooper);  
   carousel();                                                
}">  
 
  <input type=button value="Rewind" onclick="{
   myIndex = 0;  
   clearInterval(myLooper);
   clearInterval(myCounting);
   if (myAudio01.paused && myAudio01.currentTime > 0 && !myAudio01.ended) {
      } else {
         myAudio01.pause();
     }
}">   

 <input type=button value="-" onclick="{
   clearInterval(myLooper);
   clearInterval(myCounting);
   myIndex -= 1;    
   window.location.href='#'+myIndex;
}">   
  
<input type=button value="+" onclick="{
  clearInterval(myLooper);
  clearInterval(myCounting);
  myIndex += 1;  
  window.location.href='#'+myIndex;
}"> 
  
<input type=button value="Back" onclick="{
   myIndex = myIndex - 2;    
   if (myIndex <= 0){myIndex=0};                                      
   myNext();
}">   
  
<input type=button value="Next" onclick="{
   myNext();
}"> 
 
    
  
 <input id="myPause" type=button value="Pause" onclick="{ 
   clearInterval(myLooper);
   clearInterval(myCounting);
   if (this.value == 'Pause'){                                                     
       this.value = 'Play / Pause'; 
       if (myAudio01.paused && myAudio01.currentTime > 0 && !myAudio01.ended) {
      } else {
         myAudio01.pause();
     }
   } else {    
     myIndex -= 1; 
     myCountUp += 1;
     carousel();                                                 
     this.value = 'Pause';  
     if (myAudio01.paused && myAudio01.currentTime > 0 && !myAudio01.ended) {
         myAudio01.play();
      }                                                    
   }
}"> 
 
<input type=button value="Hide" onclick="{
   document.getElementById('myStick').style.display = 'none';
}"> 
  <input type=button value="TOP" onclick="{ 
   window.location.href='#top'; 
}">  
  
 </div>
 
<hr>
 
#### 1
# Intro: Jeremy Ellis (@rocksetta) TinyML Teacher Feedback 2022

I am Jeremy Ellis, Twitter <a href="https://twitter.com/rocksetta">@rocksetta</a>, <a href="https://github.com/hpssjellis">Github Profile</a>, <a href="https://rocksetta.com/">www.rocksetta</a>
I can teach anything complex that I understand to a 10 year old! The problem is getting me to understand it! 
I am still a bit stuck on Quantum Computing, my Github about it is <a href="https://github.com/hpssjellis/my-examples-for-quantum-computing">here</a>

I presently teach: 3D Printing, Animation, Game Development (Coding) and Robotics with Machine Learning

I strongly feel University Undergrads of all disciplines should have some form of hands on Machine Learning and Robotics before graduation. Unfortunately, simplification often results in a loss of creative flexibility. So the challenge is: how to simplify ML without losing computing flexibility. 
 
 
 
<br><br><br><br><br>
<hr>

#### 2 
# My High School Teaching Background

<img src="https://user-images.githubusercontent.com/5605614/176367428-196bd8d2-e10d-4030-9de0-09f150028431.png" width="200" /> 

About 1976 when I was in grade 8, and I taught myself how to computer program on a HP97 Calculator. Since then, I have had no formal machine learning training, but was writing neural networks using Pascal in the early 1990s (simple multi layer array "nodes", holding an integer between -1 and 1, interconnected to all nodes of the next layer, all incoming amount summed and the nodes fire if the sum was above zero). My NN's  unfortunately only oscillated between solutions. 

Not until Tensorflow was released about 2015 was I able to start teaching ML. I have been teaching Robotics and Machine learning now for about 6 years, <a href="https://www.rocksetta.com/tensorflow-teacher/3d-print-tensorflow/">Here</a> is a 2016 RNN model I made that self-generated multiple 3D Printable objects.

I possibly made the first ever fully computer generated 3D printable object in 2016?  
<img src="https://user-images.githubusercontent.com/5605614/189014529-cb8ebd7e-7023-4471-aec9-141d03e535b1.png" width="300" /> 



I also did a lot of educational work with TensorflowJS <a href="https://hpssjellis.github.io/beginner-tensorflowjs-examples-in-javascript/">here</a><br><br>
I turn 60 next year and will retire from teaching in a few years (I will probably continue to work on tech solutions after retiring). 




<hr>

#### 3
Nano 33 Ble Sense with a OV767x Camera

A few years ago my students chose to work with the Nano-33-ble-sense, and we purchased a $10 ov7670 camera to go with it.  
This is my first successful ov7670 image

<img src="https://user-images.githubusercontent.com/5605614/189017911-edacb75a-07ee-4ec7-a586-a6bdf7644412.png" width="400" /> 


In September 2020 I helped problem solve the ov767x camera with the Nano-33-Ble-Sense <a href="https://github.com/arduino-libraries/Arduino_OV767X/issues/5"> here</a> and also to get it working on EdgeImpulse <a href="https://forum.edgeimpulse.com/t/ov7670-cam-with-nano33ble-sense/917">here</a>. This was the first steps that I believe helped the Arduino TinyML kit to work well.

My first clear 48x48 image from the OV7670 camera inputed into EdgeImpulse  
<img src="https://user-images.githubusercontent.com/5605614/189018161-b31d90a6-d5b8-43b6-a70d-80601f526e94.png" width="48" /> 

<hr>


#### 4
# High School, Grad School partnerships

I would be interested in partnering up with grad students trying to simplify machine learning. I can provide students to test their ideas and possibly give some feedback about the steps that were most confusing. In this presentation, I will suggest multiple paths for advanced use of TinyML. I will not be able to research all of these ideas, but would help support others interested in them.

 
 <img src="https://user-images.githubusercontent.com/5605614/189260231-a3271b84-45b2-487b-a377-82e91cbe0665.jpg" width="200" /><img src="https://user-images.githubusercontent.com/5605614/189260239-b712fd21-b9f8-4ac7-afae-46c5220c2e08.jpg" width="200" /> 

 <img src="https://user-images.githubusercontent.com/5605614/189260245-b4bcf40a-5b44-42a7-923f-7d027bb10bf0.jpg" width="200" /> 

<br><br>
<hr>

#### 5
# TinyML: Multiple constraints (cost, computer power, electrical power, data security, connectivity...)

We wish tinyML hardware cost less than a $1, did all training and analysis client-side, had 5G connectivity, ran on a coin battery for multiple years and had the computing power of a TPU, but that dream is not a reality.
The reality is we have constraints: In 2022 these look like: 
 
 For hardware, we use the $60.00 USD Arduino ML Kit (Arduino Nano 33 BLE Sense with a OV7675 Camera)  
 Which is a 3.3V nordic nRF52840 chip with 14 pins at 15 mA per pin, 64 MHz clock, 1MB flash memory and 256 KB SRAM  
 For connectivity, we can use BLE or Serial:UART/I2C/SPI 
 For Machine Learning simplicity and cloud training we use <a href="https://www.an edgeimpulse.com">edgeimpusle.com</a>  
 Which is fairly easy to do: motion, sound, vision (classification and FOMO) and also regression (for size) and anomaly detection (for differences)
 
 <hr>

#### 6
# Teaching Frustration, not enough pins!
 
This is not necessarily to do with machine learning but whenever students start working on their own robotics projects they always want a few more pins to allow a few more servo motors, LED's, sensors etc for their final project. 
 
# My solution 1 (Pins): <br>
 A. use the Arduino PortentaH7 with 28 pins and potentially up to 160 pins<br>
 <img src="https://user-images.githubusercontent.com/5605614/189020875-c7431f79-9102-471d-84c2-6b2657078268.png" width="200" /> <img src="portenta320x320-first.gif" width="200" /> 
 
  Note: I am working on a PCB to allow access to all 160 pins without using the Arduino Breakout Board.
  
 <img src="https://user-images.githubusercontent.com/5605614/189260205-6059bafb-1f3b-4099-ae65-8ad85cd722f3.png" width="200" />  <img src="https://user-images.githubusercontent.com/5605614/189260212-60662463-21f2-4779-ac27-2879ee6fad51.png" width="200" /> 

 
 
 <img src="https://user-images.githubusercontent.com/5605614/189260224-b0aee2be-3a41-4a42-ad4d-3afc393123e9.jpg" width="200" /> 
 

 
# My solution 2 (Pins): <br>
 Use multiple microcontrollers connected by Serial: UART, I2C, or SPI
 
Example of 4 x $5 XIAO all running tensorflow Sine Hello World program 
<img src="https://user-images.githubusercontent.com/5605614/189020637-6917686b-3847-427f-87ee-94a82ee7a398.png" width="400" /> 


 <hr>

#### 7
# Teaching Frustration, BLE low power connectivity
For the Nano 33 Ble Sense in my opinion BLE is frustrating to code as you must know or discover hash numbers for everything you wish to do.
Note: Cellular and WiFi typically use a lot of electrical power, but they are both still a viable solution for microcontrollers with large batteries or electrically connected.
 
# My Solution 1 (BLE)
The PortentaH7 LoRa Vision Shield
I think LoRa and LoRaWan connectivity makes a lot of sense for low power applications. 
Note: The <a herf="https://explorer.helium.com/">Helium</a> LoRaWan network is a solid solution especially in North America. <a href="https://docs.helium.com/use-the-network/devices/development/arduino/lora-vision-shield/arduino/">Here</a> is my writeup about using the Portenta with Helium and adafruit.io 
 
 <hr>

#### 8
# Teaching Frustration, High Cost


Eventually a set of very cheap microcontrollers will be available, hopefully with LoRaWan capability, camera, sound and motion, but presently the main solution is to
make your own PCB.



# My Solution 1 (Cost)
Many of my students both 3D Print and computer animate. We found several students quickly understood the main issues around PCB development from this one simple video for JLCPCB and easyEDA <br> 
<a href="https://github.com/hpssjellis/maker100#31">here</a> for which the cost is about $35 for 5 boards and takes about 10 days to deliver.

Excellent video on making a PCB 
<iframe width="560" height="315" src="https://www.youtube.com/embed/gjPNYMRA0m8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<br><br>
Note: The $6000 <a href="https://www.voltera.io/">Voltera.io </a> is a possible educational solution for at school PCB production.
<img src="https://user-images.githubusercontent.com/5605614/176255114-435ef8c9-1989-4761-ae3b-daebea51492f.png" width="200" /> 



# My Solution #2 (Cost)
This is only cheaper since most students have a cell phone! Do the machine learning on a cell phone using TensorflowJS and then use UsbSerial to connect any microcontroller, even the $5 Seeedstudio XIAO. This would take a lot of work, but sensors could upload to a model and actuators could be controlled by a model. The advantage of this is you get the much more computer power of the cell phone with the microcontroller allowing sensors and actuators. Has lots of teaching portential.






<hr>

#### 9 
# Teaching Frustration, Hard to connect raw sensor data to EdgeImpulse
 
# My Solution 1 (Data)

I spent some time connecting multiple Nano 33 Ble sensors to edgeImpulse and have lots of examples. This is my Maker101 repository folder link <a href="https://github.com/hpssjellis/maker101/tree/main/ml-kit-nano-33-ble-sense-examples">here</a>
 

 
 
 
 
 <hr>

#### 10 
# Teaching Frustration, Hard to teach Keras Machine Learning using EdgeImpulse

Don't get me wrong, EdgeImpulse is amazing for simplifying machine learning. I can teach an entire class of grade 10's in 40 minutes how to make a vision classification model to classify a pen from unknowns and they actually understand how to do it, but making your own models that work is a bit harder. 

# My Solution 1 (Keras)
Here is a link to my maker101 draft repository with some ideas on this topic <a href="https://github.com/hpssjellis/maker101/tree/main/edgeimpulse-keras-expert-mode-for-sensors"> here</a>
 
# My Solution 2 (Keras)
Use TensorflowJS and WebSerial. Getting EdgeImpulse models to tensorflowJS is a bit confusing. It would be nice if the data could be exported and loaded directly onto the browser, or better yet loaded completely in the browser

# Other Solutions (Keras)
 
<b>TensorflowLIte</b> 

My old version of TensorflowLite adapted for the Portenta<a href="https://github.com/hpssjellis/my-examples-for-the-arduino-portentaH7/tree/master/m09-Tensoflow"> here</a>. Note: The Arduino_TensorflowLite library seems to have disappeared, so here is a backup in zip format that can easily be installed with the Arduino library zip upload. <a href="Arduino_TensorFlowLite.zip">Arduino_TensorFlowLite.zip</a>
 
<b>ALFES</b>  on board ML for Arduino my video <a href="https://youtu.be/SJk2q1katgw">here</a>ALFES Github <a href="https://github.com/Fraunhofer-IMS/AIfES_for_Arduino"> here</a>

Just saw <a href="https://github.com/Bobingstern/MicroFlow"><b>MicroFlow</b></a> I know nothing about it.
 
<hr>

#### 11
# Teaching Frustration, Students should not be loading their faces onto a Cloud Server for security issues

My Solution 1 (Security)
Use TensorflowJS and WebSerial, load data completely client side. 

<img src="https://user-images.githubusercontent.com/5605614/176290714-58fa7196-fe53-4ce9-a77b-2687b4e757fa.png" width = "400" /> 



<hr>

#### 12
# Teaching Frustration, relying on any cloud server. (Typically a good cloud server is purchased after a few years and the free componenet is removed!)

My Solution 1 (Cloud)
Use TensorflowJS and WebSerial, load data completely client side.

<img src="https://user-images.githubusercontent.com/5605614/189277126-d531a405-89ec-4f8d-9bbe-bca30397e0bb.png" width="400" />  


My Solution 2 (Cloud)
Use TensorflowJS and TensorflowLite (or my version), load data completely client side and transfer the model to the Nano 33 Ble Sense or other microcontroller.
 
 
#### 13
# Summary
 
 
 <img src="https://user-images.githubusercontent.com/5605614/189260249-f8164979-f697-40b8-9e7a-d29934f28bb2.jpg" width="400" /> 


 
 
 




<a href="#top">Top of page</a>





Template for this from <a href="https://github.com/hpssjellis/pecha-kucha-lightning-talks-template">pecha-kucha-lightning-talks-template</a>



 ### By Jeremy Ellis Twitter <a href="https://twitter.com/rocksetta">@Rocksetta </a> Use at your own Risk!


### By Jeremy Ellis Twitter @Rocksetta Use at your own Risk!
### Note when looking at the markdown none of the javascript buttons appear, you must go to your Gitpages Demo Link!
A few Javascript abilites do not work, such as hiding the code. So all the Javascript not in buttons is below. 

Note: 
1. Old ML presentation [here](https://hpssjellis.github.io/my-robotics-machine-learning-teaching-lightning-talk-pecha-kucha/)
2. Old TensorflowJS presentation [here](https://hpssjellis.github.io/lightening-talk-Pecha-Kucha-tensorflowjs/)
3. Pecha Kucha template [here](https://github.com/hpssjellis/pecha-kucha-lightning-talks-template)



<script>
 let myIndex = 1;
 let myLooper = 0;
 let myCounting = 0;
 let myMainNum = 20;   
 let myCountUp = 0;
 let xSlide = 3;
 let myAudio01 = new Audio();
 
;
function carousel() {
  clearInterval(myCounting);
  myCountUp = -1;
  var i;
;
  myIndex++;
  if (myIndex > xSlide) {myIndex = xSlide};    
  window.location.href='#'+myIndex;
  myCountDown();
  myCounting = setInterval(myCountDown, 1000);
  myLooper = setTimeout(carousel, myMainNum*1000); 
}
  
function myCountDown(){
  myCountUp++;
  if (myCountUp >= myMainNum ) {
    myCountUp = myMainNum;                              
  }
  if (myIndex >= xSlide && myMainNum == myCountUp){ 
     document.getElementById("myNumSlides").innerHTML = `&nbsp;&nbsp;&nbsp; Slide ${myIndex} of ${xSlide} slides. ALL DONE <input type=button value="Show"  style="height:25px; " onclick="{document.getElementById('myStick').style.display = 'inline'; }"> `;
     clearInterval(myCounting);             
     clearInterval(myLooper);  
  }
  else {    
     document.getElementById("myNumSlides").innerHTML = `&nbsp;&nbsp;&nbsp; Slide ${myIndex} of ${xSlide} slides. ${myMainNum-myCountUp} seconds remaining <input type=button value="Show" style="height:25px; " onclick="{document.getElementById('myStick').style.display = 'inline'; }"> `;
  }
}
;
function myNext(){   
  xSlide  = document.getElementById('myCountLinks').value; 
  myMainNum = document.getElementById('myCountMax').value;                        
  clearInterval(myLooper) ; 
  carousel();  
}  
;
</script>  
