
### Jeremy Ellis TinyML Teacher Feedback 2022



##### version 0.3.2-9


Demo of this Github at [https://hpssjellis.github.io/jeremy-ellis-tinyML-teacher-feedback-2022/](https://hpssjellis.github.io/jeremy-ellis-tinyML-teacher-feedback-2022/)


This Github Repository at  [https://github.com/hpssjellis/jeremy-ellis-tinyML-teacher-feedback-2022](https://github.com/hpssjellis/jeremy-ellis-tinyML-teacher-feedback-2022)

 To make your own version of this web-app just copy this README.md file in your own Gitpages activated repository (makes it act as a webpage) and link to the README.md file as the main webpage (it replaces an index.html file).

Number of Slides: <input type="text" id="myCountLinks" size="6" value="18" >, Seconds per Slide: <input type="text" id="myCountMax" size="6" value="30" >

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
Follow with this link <a href="https://hpssjellis.github.io/jeremy-ellis-tinyML-teacher-feedback-2022/">hpssjellis.github.io/jeremy-ellis-tinyML-teacher-feedback-2022/</a><br>
I am Jeremy Ellis, Twitter <a href="https://twitter.com/rocksetta">@rocksetta</a>, <a href="https://github.com/hpssjellis">Github Profile</a>, <a href="https://rocksetta.com/">www.rocksetta.com</a>, <a href="https://www.youtube.com/c/Rocksetta/videos"> Youtube Rocksetta Playlist</a><br><br>
I have a gift for academic creativity and the ability to teach complex things, that I understand, to young people! The problem is getting me to understand the complex things! I am still a bit stuck on learning Quantum Computing, my Github about Quantum is <a href="https://github.com/hpssjellis/my-examples-for-quantum-computing">here.</a>

I presently teach: 3D Printing, Animation, Game Development (Coding) and Robotics with Machine Learning

I strongly feel university undergrads of all disciplines should have some form of hands on machine learning and robotics before graduation. Unfortunately, simplification often results in a loss of big picture knowledge and capability.<br><br>

<b>So the challenge is how to simplify ML without losing computing flexibility. </b>
 
<br><br><br>
<hr>

#### 2 
# My Background

<img src="https://user-images.githubusercontent.com/5605614/176367428-196bd8d2-e10d-4030-9de0-09f150028431.png" width="160" /> 
<img src="https://user-images.githubusercontent.com/5605614/189508144-36c33186-8607-40a0-91d6-0e90586df633.png" width="200" /> 

About 1976, when I was in Grade 8, I taught myself how to computer program on both the HP67 and HP97 Calculators. Since then, I have had no formal machine learning training, but was writing neural networks using Pascal in the early 1990s (simple multi layer array "nodes", holding an integer between -1 and 1, interconnected to all nodes of the next layer, all incoming amounts for each node were summed and then fired if the sum was above zero). My NN's never worked but unfortunately only oscillated between classification. 

Not until Tensorflow was released about 2015 was I able to teaching ML. I have been teaching robotics and machine learning now for about 6 years. <a href="https://www.rocksetta.com/tensorflow-teacher/3d-print-tensorflow/">Here</a> is a 2016 RNN model I made that self-generated multiple 3D printable objects.
I also did a lot of teaching with TensorflowJS <a href="https://hpssjellis.github.io/beginner-tensorflowjs-examples-in-javascript/">here</a><br><br>

In 2016, I may have made the first computer generated 3D printable object using a machine learning program!  
<img src="https://user-images.githubusercontent.com/5605614/189014529-cb8ebd7e-7023-4471-aec9-141d03e535b1.png" width="150" /> 


<hr>

#### 3
# Nano 33 Ble Sense with an OV767x Camera

A few years ago, my students chose to work with the Nano-33-Ble-Sense and we purchased a $10 OV7670 camera to go with it.<br>  
This is my first successful OV7670 image

<img src="https://user-images.githubusercontent.com/5605614/189017911-edacb75a-07ee-4ec7-a586-a6bdf7644412.png" width="300" /> 

In September 2020, I helped problem solve the OV767x camera with the Nano-33-Ble-Sense <a href="https://github.com/arduino-libraries/Arduino_OV767X/issues/5"> here</a> and also got it working on EdgeImpulse <a href="https://forum.edgeimpulse.com/t/ov7670-cam-with-nano33ble-sense/917">here</a>. This was the first step that I believe helped get working the Arduino TinyML kit.

This image is of my first clear 48x48 pixel image from the OV7670 camera uploaded to EdgeImpulse for a classification model.<br>  
<img src="https://user-images.githubusercontent.com/5605614/189018161-b31d90a6-d5b8-43b6-a70d-80601f526e94.png" width="48" /> 
<br><br><br><br><br><br><br>
<hr>


#### 4
# High School, Grad School partnerships

I would be interested in partnering with grad students or professors trying to simplify machine learning. I can provide students to test their ideas and maybe give feedback about the steps that were most confusing. In this presentation, I will suggest multiple paths for advanced use of TinyML. I will not have time to continue to research all of these ideas, but would help support others interested in them.  I turn 60 next year and will retire from teaching in a few years. I would like to continue working part time on tech solutions after retiring if anyone is hiring. 


<b>This presentation is going to seem like I don't like the Arduino TinyML Kit with EdgeImpulse, I love it, I just need to push tech boundaries. It is part of my personality.</b>
 
 A few Robotics and ML projects my students are working on:<br>
 <img src="https://user-images.githubusercontent.com/5605614/189260231-a3271b84-45b2-487b-a377-82e91cbe0665.jpg" width="200" /><img src="https://user-images.githubusercontent.com/5605614/189260239-b712fd21-b9f8-4ac7-afae-46c5220c2e08.jpg" width="200" /> <img src="https://user-images.githubusercontent.com/5605614/189260245-b4bcf40a-5b44-42a7-923f-7d027bb10bf0.jpg" width="200" /> 

<br><br><br><br><br>
<hr>

#### 5
# TinyML: Multiple constraints (cost, computer power, electrical power, data security, connectivity...)

We wish tinyML hardware cost less than a dollar, did all training and analysis client-side, had 5G connectivity, ran on a coin battery for multiple years, and had the computing power of a TPU, but that dream is not a reality.
The reality is we have constraints: In 2022 these look like: 
 
 For hardware, we use the $60.00 USD Arduino ML Kit (Arduino Nano 33 BLE Sense with a OV7675 Camera),<br>
 which is a 3.3V Nordic nRF52840 chip with 14 pins at 15 mA per pin, 64 MHz clock, 1MB flash memory and 256 KB SRAM<br>
 For connectivity, we can use BLE or Serial:UART/I2C/SPI<br> 
 For machine learning simplicity and cloud training, we use <a href="https://www.an edgeimpulse.com">edgeimpusle.com</a><br>
 EdgeImpulse makes it fairly easy to do: motion, sound, vision (classification and FOMO) and also regression (for size) and anomaly detection (for differences).
 
<img src="https://user-images.githubusercontent.com/5605614/189539237-ae66c32b-ff13-4760-af43-04d789025db3.png" width="400" /> 
<br><br><br><br><br><br><br>
<hr>

#### 6
# Teaching Frustration: Loading EdgeImpulse Client

Sometimes, in a classroom computer lab that has locked-down software, it is difficult to load the EdgeImpulse Client on an Arduino

# My solution 1 (Client): <br>
Install the client software on my laptop and individually install it on the students' Arduino's

# My solution 2 (Client): <br>
Use a cell phone for data collection (Motion, Sound, Vision) and build as normal on EdgeImpulse, then download the Arduino build for model installation on the device.

# My solution 3 (Client): <br>
Have students build the EdgeImpulse client firmware from scratch. Nano 33 Ble <a href="https://github.com/edgeimpulse/firmware-arduino-nano-33-ble-sense">Github here</a>, Portenta <a href="https://github.com/edgeimpulse/firmware-arduino-portenta-h7">Github here</a>. This has a few extra issues, such as long file names and storing a build.local.txt to your arduino hardware file that you then have to remove for normal arduino compiling.

# My solution 4 (Client): <br>
Create a .hex or .bin file of the client and force installing it using Arduino installation tools. This seems to be frowned upon by the Arduino community, but seems like a very sensible solution to me. I think I have done it before, but it was too confusing to teach to my students.

This year, I hope NodeJS is installed on my new computers. 
<hr>

#### 7
# Teaching Frustration: EdgeImpulse model builds near 100% success, reality < 30% success

It is common for students to build a model that has a very high success rate on EdgeImpulse with the student's collected data, but when the student tests it in a real environment it performs poorly or not at all. This can also have several reasons.

# My solution 1 (Reality): <br>
Sometimes the students software changes to test their model have bugs in their code. This is fixable but needs the instructor to have a very good knowledge of coding.

# My solution 2 (Reality): <br>
A great teaching opportunity for understanding machine learning. With guidance the students learn how to make a better model using better, more realistic data, or just better thought out data collection.

# My solution 3 (Reality): <br>
For vision models, switching the concept from 3D to 2D often helps. So the camera is positioned in a way that the incoming data is always showing the same face. (Camera above a conveyor belt). This often simplifies vision data collection.

# My solution 4 (Reality): <br>
Students often have difficulty realising that for the problem they are trying to solve the Arduino ML kit does not have the computing power to solve it at the accuracy required. This is also a good ML learning experience. More on solutions for this later.
<hr>

#### 8
# Teaching Frustration:  EdgeImpulse C++ compile
In a teaching computer lab, sometimes the GNU C++ environment is not well setup. Using GNU C++ is not really a strength of mine since I typically use the Arduino IDE or Platform.io, but occasionally some code would be better compiled using C++.

# My solution 1 (C++): <br>
<a href="https://www.gitpod.io/">Gitpod</a> is an amazing browser based docker container giving 50 hours a month for free student use. The containers save but are only active for 10-30 minutes after the last entered command. I often test Github node projects using Gitpod by simply inserting <pre>gitpod.io/#</pre>  in front of the normal Github URL.<br>
For this solution, I tried to make a Gitpod that loads all the development environments that edgeImpulse uses. It was only partially successful and GNU C++ is a too advanced for my average High School student.<br>
This is my Gitpod of the edgeimpulse dev environment. It is fairly advanced and may not have survived updates to EdgeImpulse. <a href="https://github.com/hpssjellis/my-gitpod-of-edge-impulse">my-gitpod-of-edge-impulse</a>

<img src="https://user-images.githubusercontent.com/5605614/189805421-43ec705c-c85a-4e01-9f09-15eeb3225507.png" width="300" />

 <br><br><br> <br>
 <hr>

#### 9
# Teaching Frustration:  not enough pins!

This is not necessarily to do with machine learning but whenever students work on their own robotics projects they always want a few more pins to allow a few more servo motors, LED's, sensors etc for their final project. The Arduino ML kits have 14 available pins.
 
# My solution 1 (Pins): <br>
Use the expensive but more powerful ($113.90 USD) <a href="https://store-usa.arduino.cc/products/portenta-h7?selectedStore=us">Arduino PortentaH7</a> with 28 pins and potentially up to 160 pins<br>
<img src="https://user-images.githubusercontent.com/5605614/189020875-c7431f79-9102-471d-84c2-6b2657078268.png" width="200" /> <img src="portenta320x320-first.gif" width="200" /> 
 
Note: I am working on a PCB to allow access to all 160 pins without using the <a href="https://store-usa.arduino.cc/products/arduino-portenta-breakout?pr_prod_strat=copurchase&pr_rec_id=c6455b41f&pr_rec_pid=6545910694095&pr_ref_pid=6544099082447&pr_seq=uniform"> Arduino Breakout Board</a> ($55 USD). Note: The breakout board has the pins organised by concept. My board has the pins organised by the High Density connectors J1 and J2
  
<img src="https://user-images.githubusercontent.com/5605614/189260205-6059bafb-1f3b-4099-ae65-8ad85cd722f3.png" width="150" />  <img src="https://user-images.githubusercontent.com/5605614/189260212-60662463-21f2-4779-ac27-2879ee6fad51.png" width="150" /> <img src="https://user-images.githubusercontent.com/5605614/189260224-b0aee2be-3a41-4a42-ad4d-3afc393123e9.jpg" width="150" /> 
 
# My solution 2 (Pins): <br>
Use multiple microcontrollers connected by Serial: UART, I2C, or SPI
 
Example of 4 x $5 XIAO all running tensorflow Sine Hello World program, all connected using the I2C protocol.<br>
<img src="https://user-images.githubusercontent.com/5605614/189020637-6917686b-3847-427f-87ee-94a82ee7a398.png" width="200" /> 
<hr>

#### 10
# Teaching Frustration: BLE low power connectivity
For the Nano 33 Ble Sense (in my opinion) BLE is frustrating to code as you must know or discover hash numbers for everything you wish to code.
 
# My Solution 1 (BLE)
The <a href="https://store-usa.arduino.cc/products/arduino-portenta-vision-shield-lora%C2%AE?pr_prod_strat=copurchase&pr_rec_id=c6455b41f&pr_rec_pid=6544223535311&pr_ref_pid=6544099082447&pr_seq=uniform">PortentaH7 LoRa Vision Shield </a> ($69 USD USD)
I think LoRa and LoRaWan connectivity makes sense for any low power application. Note: The <a herf="https://explorer.helium.com/">Helium</a> LoRaWan network is a solid solution especially in North America. <a href="https://docs.helium.com/use-the-network/devices/development/arduino/lora-vision-shield/arduino/">Here</a> is my writeup about using the Portenta with Helium and <a href="https://io.adafruit.com/">adafruit.io</a> 

The <a herf="https://explorer.helium.com/">Helium LoRaWan Coverage Map</a> for Spain<br>
<img src="https://user-images.githubusercontent.com/5605614/189534669-b3a0e8df-b1b2-4085-8666-9dff683903ad.png" width="200" /> 

# My Solution 2 (BLE)
If electrical power is not an issue, why not use WiFi or Ethernet? The Portenta can have both. They allow a large data bandwith. 
If monthly cost is not an issue then Celluar could be considered (This I have never tested), options are presently 2G and 3G with the <a href="https://docs.arduino.cc/tutorials/portenta-cat-m1-nb-iot-gnss-shield/cheat-sheet"> Portenta CAT </a>, but I am sure 4G and 5G are coming soon. 
Full connectivity also opens up the door for cloud classification, like SiRi and other methods. Not really sure if that is still TinyML, but is something students should consider to solve specific ML problems.


 <hr>

#### 11
# Teaching Frustration: High Cost and now the Chip shortage.

Eventually a set of very cheap microcontrollers will be available, hopefully with LoRaWan capability, camera, and/or sound and/or motion, but presently the main solution is to make your own PCB.

# My Solution 1 (Cost)
Many of my students can both 3D print and computer animate. We found several students quickly understood the main issues around PCB development from this one simple video for JLCPCB and easyEDA <br> 
<a href="https://github.com/hpssjellis/maker100#31">here</a> for which the cost is about $35 for 5 boards and takes about 10 days to deliver.

Excellent video on making a PCB 
<iframe width="300" height="150" src="https://www.youtube.com/embed/gjPNYMRA0m8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


Note: The $6000 <a href="https://www.voltera.io/">Voltera.io </a> is a possible educational solution for at school PCB production.<img src="https://user-images.githubusercontent.com/5605614/176255114-435ef8c9-1989-4761-ae3b-daebea51492f.png" width="50" /> <br>

# My Solution #2 (Cost)
This is only cheaper since most students have a cell phone! I think we could do the machine learning on a cell phone using TensorflowJS and then use UsbSerial to connect any microcontroller like the Nano 33 Ble Sense or the $5 Seeedstudio XIAO. This has lots of teaching potential and is my main research area at present. Edgeimpulse even outputs a WASM for the web.
<hr>

#### 12 
# Teaching Frustration: Hard to connect raw sensor data to EdgeImpulse
 
# My Solution 1 (Data)

I spent some time connecting multiple Nano 33 Ble sensors to EdgeImpulse and have lots of examples. This is my Maker101 repository folder link <a href="https://github.com/hpssjellis/maker101/tree/main/ml-kit-nano-33-ble-sense-examples">here</a><br> This folder goes through steps to get raw data from the Nano 33 Ble Sense into EdgeImpulse. This needs the EdgeImpulse serial client connectivity on your computer. Much easier if you can get EdgeImpulse webUSB connectivity working, but that does not always work for me without having the EdgeImpulse client installed on the device.<br>

Image of the Nano33 Ble Sense showing all raw sensor data, shifted vertically to allow each sense to have its own row.
 <img src="https://user-images.githubusercontent.com/5605614/189539030-785ddfc7-a8e8-4a2f-8ef5-c39faa6d5cda.png" width="300" /> 


 
 
 
 <hr>

#### 13 
# Teaching Frustration: It is hard to teach Keras Machine Learning using EdgeImpulse

Don't get me wrong, EdgeImpulse is amazing for simplifying machine learning. I can teach an entire class of grade 10s in 40 minutes how to make a vision classification model to classify a pen from unknowns and they actually understand how to do it, but making your own Keras models that work well with complete Keras flexibility is harder. 

# My Solution 1 (Keras)
Here is a link to my maker101 draft repository with some ideas on this topic <a href="https://github.com/hpssjellis/maker101/tree/main/edgeimpulse-keras-expert-mode-for-sensors"> here</a>
 
# My Solution 2 (Keras)
Use TensorflowJS and WebSerial. Getting EdgeImpulse models to tensorflowJS is a bit confusing. It would be nice if the data could be exported and loaded directly onto the browser, or better yet loaded completely in the browser

# Other Solutions (Keras)
 
<b>TensorflowLIte</b> 

My old version of TensorflowLite adapted for the Portenta<a href="https://github.com/hpssjellis/my-examples-for-the-arduino-portentaH7/tree/master/m09-Tensoflow"> here</a>. Note: The Arduino_TensorflowLite library seems to have disappeared, so here is a backup in zip format that can easily be installed with the Arduino library zip upload. <a href="Arduino_TensorFlowLite.zip">Arduino_TensorFlowLite.zip</a>
 
<b>ALFES</b>  on board ML for Arduino my video <a href="https://youtu.be/SJk2q1katgw">here</a> ALFES Github <a href="https://github.com/Fraunhofer-IMS/AIfES_for_Arduino"> here</a>

Just saw <a href="https://github.com/Bobingstern/MicroFlow"><b>MicroFlow</b></a> I know nothing about it.
 
<hr>

#### 14
# Teaching Frustration: Students should not be loading their faces onto a Cloud Server for youth privacy issues

My Solution 1 (Security)
Use TensorflowJS and WebSerial, load data completely client side. I am working on this solution.

<img src="https://user-images.githubusercontent.com/5605614/176290714-58fa7196-fe53-4ce9-a77b-2687b4e757fa.png" width = "400" /> 

<br><br><br><br><br>

<hr>

#### 15
# Teaching Frustration: relying on any cloud server. (Typically a good cloud server is purchased after a few years and the free component is removed!)
This probably will not happen with Edge Impulse, but if it does it can be devastating to your course.<br>

Example: July 14, 2016 I spent had about 2 years designing Android tools for the browser on Cloud9, after the AWS purchase all my work was no longer free and worse was deprecated.<br>
<a href="https://techcrunch.com/2016/07/14/amazons-aws-buys-cloud9-to-add-more-development-tools-to-its-web-services-stack"><img src="https://user-images.githubusercontent.com/5605614/189539603-1339cb02-162c-4910-8969-4ed4b6697322.png" width="300" />  </a>


My Solution 1 (Cloud)
Use TensorflowJS and WebSerial, load data completely client side.

<img src="https://user-images.githubusercontent.com/5605614/189277126-d531a405-89ec-4f8d-9bbe-bca30397e0bb.png" width="400" />  


My Solution 2 (Cloud)
Use TensorflowJS and TensorflowLite (or my version <a href="https://github.com/hpssjellis/my-examples-for-the-arduino-portentaH7/tree/master/m09-Tensoflow">here</a>), load data completely client side and transfer the model to the Nano 33 Ble Sense or other microcontroller. If TensorflowLite stays deprecated this is not a great idea. Here is a backed up TFlite library: [Arduino_TensorFlowLite.zip](Arduino_TensorFlowLite.zip)
<br><br><br> 
<hr> 
#### 16
# Summary
 
<a href="https://www.edgeimpulse.com/">Edgeimpulse.com<a/> and the Arduino ML kit are a great way to easily get students started in TinyML, but how to continue for advanced students? I hope to partner with a few professors to try some learning extensions. Here are a few of my relevant references:
 
 My Robotics and ML course <a href="https://github.com/hpssjellis/maker100">Maker100</a><br>
 My Portenta MBED library called the <a href="https://github.com/hpssjellis/portenta-pro-community-solutions">portenta-pro-community-solutions</a> which will have some Nano 33 Ble Sense working code<br>
 My <a href="https://github.com/hpssjellis/maker101">Maker101</a> repository that addresses many of the ideas mentioned today.<br>
 My Twitter feed for easy communication <a href="https://twitter.com/rocksetta">@rocksetta</a><br>
 
 Image of the PortentaH7 ( with LoRa Vision shield attached behind it) running a 72 ms FOMO vision model with a 128x128 WaveShare 16 bit Grayscale OLED, and the Portenta Pro Community Solutions library of MBED examples<br>
 <img src="https://user-images.githubusercontent.com/5605614/189260249-f8164979-f697-40b8-9e7a-d29934f28bb2.jpg" width="250" />  <img src="https://user-images.githubusercontent.com/5605614/189810188-c209fc84-a711-4b68-a495-ba3feb6af9ec.png" width="400" /> 



<br><br><br> 
<hr> 
#### 17
# Summary Mind Map of the topics today.

 <img src="https://user-images.githubusercontent.com/5605614/189808930-99d614a7-43bf-4129-bf23-23ebd05f1372.png" width="600" /> 

 <hr>
 
 

#### 18
# End of presentation

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
<br><br><br><br><br><br><br><br><br><br><br>
 <hr>
 


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
