
### jeremy-ellis-tinyML-teacher-feedback-2022



##### version 0.0.2-2


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
# Intro: jeremy-ellis-tinyML-teacher-feedback-2022

I am Jeremy Ellis, Twitter <a href="https://twitter.com/rocksetta">@rocksetta</a>, <a href="https://github.com/hpssjellis">Github Profile</a>, <a href="https://rocksetta.com/">www.rocksetta</a>
I have a gift, anything I understand I can teach to a 10 year old! The problem is getting me to understand it! 
I am still a bit stuck on Quantum Computing, my Github about it is <a href="https://github.com/hpssjellis/my-examples-for-quantum-computing">here</a>

I presently teach: 3D Printing, Animation, Game Development (Coding) and Robotics with Machine Learning

I strongly feel undergrads of all disciplines should have some form of hands on Machine Learning and Robotics before graduation. Unfortunately simplification often results in a loss of understanding and the ability to create new methods. So the challenge is: how to simplifiy ML without losing computing flexibility. 
 
 
 
<br><br><br><br><br>
<hr>

#### 2 
# My High School Teaching Background

<img src="https://user-images.githubusercontent.com/5605614/176367428-196bd8d2-e10d-4030-9de0-09f150028431.png" width="200" /> 

About 1976 when I was in grade 8 I taught myself how to computer program on a HP97 Calculator. Since then I have had no formal machine learning training, but was writing neural networks using Pascal in the early 1990's (simple multi layer array "nodes", holding an integer between -1 and 1, interconnected to all nodes of the next layer, all incoming amount summed and the nodes fire if the sum was above zero). My NN's  unfortunately only oscillated between solutions. 

Not until Tensorflow was released about 2015 was I able to start teaching ML. I have been teaching Robotics and Machine learning now for about 6 years, <a href="https://www.rocksetta.com/tensorflow-teacher/3d-print-tensorflow/">Here</a> is a 2016 RNN model I made that self-generated multiple 3D Printable objects.

Is this the first computer generated 3D printed object that I made in 2016?  
<img src="https://user-images.githubusercontent.com/5605614/189014529-cb8ebd7e-7023-4471-aec9-141d03e535b1.png" width="400" /> 



I also did a lot of educational work with TensorflowJS <a href="https://hpssjellis.github.io/beginner-tensorflowjs-examples-in-javascript/">here</a>
I turn 60 next year and will retire from teaching in a few years (I will probably continue to work on tech solutions after retiring). 




<hr>

#### 3
Nano 33 Ble Sense with a OV767x Camera

A few years ago my students chose to work with the Nano-33-ble-sense and we purchased a $10 ov7670 camera to go with it.  
This is my first successful ov7670 image

<img src="https://user-images.githubusercontent.com/5605614/189017911-edacb75a-07ee-4ec7-a586-a6bdf7644412.png" width="400" /> 


In September 2020 I helped problem solve the ov767x camera with the Nano-33-Ble-Sense <a href="https://github.com/arduino-libraries/Arduino_OV767X/issues/5"> here</a> and also to get it working on EdgeImpulse <a href="https://forum.edgeimpulse.com/t/ov7670-cam-with-nano33ble-sense/917">here</a>. This was the first steps that I believe helped the Arduino TinyML kit to work well.

My first clear 48x48 image from the OV7670 camera inputed into EdgeImpulse  
<img src="https://user-images.githubusercontent.com/5605614/189018161-b31d90a6-d5b8-43b6-a70d-80601f526e94.png" width="48" /> 

<hr>


#### 4
# High School, Grad School partnerships

I would be interested in partnering up with grad students trying to simplify machine learning. I can provide students to test their ideas and possibly give some feedback about the steps that were most confusing. In this presentation I will suggest multiple paths for advanced use of TinyML. I will not be research all of these ideas but would help support others interested in them.

 
 <img src="https://user-images.githubusercontent.com/5605614/189260231-a3271b84-45b2-487b-a377-82e91cbe0665.jpg" width="200" /><img src="https://user-images.githubusercontent.com/5605614/189260239-b712fd21-b9f8-4ac7-afae-46c5220c2e08.jpg" width="200" /> 

 <img src="https://user-images.githubusercontent.com/5605614/189260245-b4bcf40a-5b44-42a7-923f-7d027bb10bf0.jpg" width="200" /> 

<br><br>
<hr>

#### 5
# TinyML: Multiple constraints (cost, computer power, electrical power, data security, connectivity...)

We wish tinyML hardware cost less than a $1, did all training and analysis client-side, had 5G connectivity, ran on a coin battery for multiple years and had the computing power of a TPU, but that dream is not a reality.
The reality is we have constraints: In 2022 these look like: 
 
 For hardware we use the $60.00 USD Arduino ML Kit (Arduino Nano 33 BLE Sense with a OV7675 Camera)  
 Which is a 3.3V nordic nRF52840 chip with 14 pins at 15 mA per pin, 64 MHz clock, 1MB flash memory and 256KB SRAM  
 For connectivity we can use BLE  
 For Machine Learning simplicity and cloud training we use <a href="https://www.an edgeimpulse.com">edgeimpusle.com</a>  
 Which is fairly easy to do motion, sound, vision (classification and FOMO) and also regression (for size) and anomaly detection (for differences)
 
 <hr>

 #### 6
 # Teaching Frustration, not enough pins!
 
This is not necessaryily to do with machine learning but whenever students start working on their own robotics projects they always want a few more pins to allow a few more servo motors, LED's, sensors etc for their final project. 
 
 # My solution 1 (Pins): <br>
 A. use the Arduino Portenta with 28 pins and potentially up to 160 pins<br>
 <img src="https://user-images.githubusercontent.com/5605614/189020875-c7431f79-9102-471d-84c2-6b2657078268.png" width="200" /> <img src="portenta320x320-first.gif" width="200" /> 
 
  Note: I am working on a pcb to allow access to all 160 pins witout using the Arduino Breakout Board.
  
 <img src="https://user-images.githubusercontent.com/5605614/189260205-6059bafb-1f3b-4099-ae65-8ad85cd722f3.png" width="200" />  <img src="https://user-images.githubusercontent.com/5605614/189260212-60662463-21f2-4779-ac27-2879ee6fad51.png" width="200" /> 

 
 
 <img src="https://user-images.githubusercontent.com/5605614/189260224-b0aee2be-3a41-4a42-ad4d-3afc393123e9.jpg" width="200" /> 
 

 
# My solution 2(Pins): <br>
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


Eventually a set of very cheap microcontrollers will be available hopefully with LoRaWan capability, camera, sound and motion, but presently the main solution is to
make your own PCB.



# My Solution 1 (Cost)
Many of my students both 3D Print and computer animate. We found several students quickly understood the main issues around PCB development from this one simple video for JLCPCB and easyEDA  <a href="https://github.com/hpssjellis/maker100#31">here</a> for which the cost is about $35 for 5 boards and takes about 10 days to deliver.

Excellent video on making a PCB 
<iframe width="560" height="315" src="https://www.youtube.com/embed/gjPNYMRA0m8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

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

Don't get me wrong, EdgeImpulse is amazing for simplifying machine learning. I can teach an entire class of grade 10's in 40 minutes how to make a vision classification model to classfiy a pen from unknowns and they actually understand how to do it, but making your own models that work is a bit harder. 

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

my Solution 2 (Cloud)
Use TensorflowJS and TensorflowLite (or my version), load data completely client side and transfer the model to the Nano 33 Ble Sense or other microcontroller.
 
 
#### 13
# Summary
 
 
 <img src="https://user-images.githubusercontent.com/5605614/189260249-f8164979-f697-40b8-9e7a-d29934f28bb2.jpg" width="400" /> 


 
 
 
 
 
 
<br><br><br><br<br><br><br><br><br>
<hr><br><br><br><br><br>
<hr><br><br><br><br><br>
<hr><br><br><br><br><br>
<hr><br><br><br><br><br>
<hr><br><br><br><br><br>
<hr><br><br>
<hr><br><br><br><br><br>
<hr><br><br><br><br><br>
<hr><br><br><br><br><br>
<hr><br><br><br><br><br>
<hr><br><br>
<hr>
 
 
 # Old stuff below. still here in case I need something from it

#### 1
# Intro: Lightning Talks in Pecha Kucha Format

**~15 slides, 20 seconds per slide works out to about 5 min per Presenter**  
**Traditional Business/Education Format: Powerpoint, PDF (Issue for audience not able to click links)**  
**But Coders use Github!**  
**So I made a Github README.md file that works with Javascript for both audio and automatic scrolling**  
**This Lightning Talk is a summary of what I am working on to simplify Machine Learning for any interested student and Educators.**

![image](https://user-images.githubusercontent.com/5605614/176367069-0d77f700-2863-47e2-b0d8-7bdf8e0433b5.png)

 <br><br><br><br><br>
<hr>


#### 2
# Who:

**I am Jeremy Ellis, Twitter <a href="https://twitter.com/rocksetta">@rocksetta</a>**  
**<a href="https://github.com/hpssjellis"> Jeremy Ellis Github Profile</a>**   
**Canadian High School Technology Teacher, with greater than 30 years experience teaching coding.**   
**Presently teaching Animation, Coding, 3D Printing and Robotics with Machine Learning**  

**I started my Data Science interests when I tried to understand patterns in music and developed a <a href="http://www.keyfreemusic.com/keyfreemusic/">sing-able</a> music notation and other stuff at <a href="https://rocksetta.com/">rocksetta.com</a>. This project is ongoing**  
**In the early 1990's I was designing fully connected Neural Networks using Quick Pascal. (Not that hard to program), but they never worked, they just kept oscillating between solutions. I did other things until Tensorflow was made public in 2015. I knew this was something that students would benefit from but had to wait until 2017 when deeplearnJS came out.**
 
<img src="https://user-images.githubusercontent.com/5605614/176365703-37896963-67d5-48c5-bcb2-543fb5ed7c19.png" width = 400 />
 
<br><br><br><br><br><br><br><br>
<hr>


#### 3
# Topic: 
 
**I believe all educated people should have some form of hands on Robotics and Machine Learning Education. It doesn't matter if the person is at University to become a Lawyer, Accountant, Scientist, Educator or any field.  Machine Learning is here to stay, and will have an enormous effect, both good and bad, on all areas of society. Knowing how deep learning works might be the most important thing Educators teach.**  

**Some ML Educational Issues:**   

**Traditional Method is too difficult for the general population and gives no preparation for Embedded devices**

**Online Simplifications: (<a href="https://www.edgeimpulse.com/">EdgeImpulse</a>, <a href="https://ide.tinkergen.com/">CodeCraft-tinkergen</a>, <a href="https://scratch.mit.edu/studios/3995548/">Scratch</a>) (Motion, Sound, Vision:Classification and FOMO) Very simple for any age group of students with cell phones to quickly (under 40 minutes) understand how to create a dataset and train a Machine Learning model and test it's effectiveness.**  
 
**There is a huge gap between the Traditional and Online teaching methods.**  
 
**Issues: The Online is simpler but advanced issues are: How to program the embedded device after analysis, how to use other sensors, and ability to do advanced model manipulation.**   

<img src="https://user-images.githubusercontent.com/5605614/176488598-72170886-92d9-4263-9da8-12a6c602b022.png" width = 300 />

<br><br><br>
<hr>


#### 4
# <a href="https://keras.io/">Keras</a>, <a href="https://www.tensorflow.org/">Tensorflow</a> , <a href="https://pytorch.org/">PyTorch</a>, <a href="https://theano-pymc.readthedocs.io/en/latest/introduction.html">Theano</a> ...
 
**The traditional way to teach Machine Learning and the subset Deep Learning is with these platforms. Mainly for students with some advanced Math skills. These platforms typically involve only the computer and not directly using sensors and/or sending output to actuators. Typically a known dataset is loaded and the Machine Learning model is manipulated to demonstrate understanding of the concept with the output generated for the computer screen.** 
 
 **Tensorflow**

 ![image](https://user-images.githubusercontent.com/5605614/176306964-fbaff0bf-6e02-4f1a-a2db-e55132cecb70.png)

 
**Note: <a href="Gitpod.io">https://gitpod.io/</a> can help enormously with teaching the above as most Github sites can be loaded into Gitpod (an online browser docker) and ran with only a few starting commands. With a github login you just need to add to the front of a github URL ``` gitpod.io/#  ``` My Gitpod  (old) examples are <a href="https://hpssjellis.github.io/rocksetta-gitpod-links/">rocksetta-gitpod-links</a>**
 
![image](https://user-images.githubusercontent.com/5605614/176337919-108d2c72-6113-4195-a156-23e9775413b1.png)

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

<hr>

#### 5
# The $58.00 <a href="https://store-usa.arduino.cc/products/arduino-tiny-machine-learning-kit"> Arduino Tiny Machine Learning Kit</a>

**Very well supported by Harvard SEAS (School of Engineering and Applied Science) Education <a href="http://tinyml.seas.harvard.edu/">TinyMLEdu</a>  The Github at <a href="https://github.com/tinyMLx/courseware/tree/master/edX">tinyMLx Github</a>**
 
<img src="https://user-images.githubusercontent.com/5605614/176305111-3c0cc679-9b9e-4939-8e04-9d9a45f17435.png" width = 400 />
 
**Also by <a href="https://edgeimpulse.com/university">EdgeImpulse University</a> Github of the course at <a href="https://github.com/edgeimpulse/courseware-embedded-machine-learning">courseware-embedded-machine-learning</a>**

<img src="https://user-images.githubusercontent.com/5605614/176258229-111d35ef-e27f-4c83-9abf-e9e264306b73.png" width = 400 />  
**Often a university can get a few free sets of the Arduino Tiny Machine Learning Kits or other hardware from either of these groups.**

<br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>
 
#### 6
# <a href="https://www.amazon.ca/Raspberry-Model-2019-Quad-Bluetooth/dp/B07TD42S27">Raspberry Pi 4B</a>
**All RPI's and other single board computers such as the <a href="https://www.seeedstudio.com/NVIDIA-Jetson-Nano-2GB-Developer-Kit-Wireless-Adapter-Included-p-4707.html">NVIDIA® Jetson Nano™ 2GB Developer Kit </a> have the advantage of near full computer power with up to 40 pins for connectivity to sensors, actuators and built in Communication. Really the best situation, except for the larger amount of electricity used, hardware cost and larger size compared to other microcontrollers.**

![image](https://user-images.githubusercontent.com/5605614/176316438-fca02195-da34-4a78-b472-73345b93698e.png)
 
### TinyML should be inexpensive
**As Educators we purchase kits that allow students to experience many facets of Robotics and Embedded Machine Learning, however the big picture goal is for student's to be able to design specific combinations of components that they have a Proof of Concept that the components can do the job. The individual components can be very cheap. The $111 Arduino PortentaH7 chip costs $10.00**
 
<br><br><br><br><br><br><br><br><br><br>
<hr>


#### 7
# My Maker100 
**For the $111 <a href="https://store-usa.arduino.cc/products/portenta-h7">Arduino PortentaH7</a> with the $68 <a href="https://store-usa.arduino.cc/products/arduino-portenta-vision-shield-lora%C2%AE">LoRa Vision Shield</a> and/or $7 <a href="https://www.seeedstudio.com/Seeeduino-XIAO-Pre-Soldered-p-4747.html">Seeedstudio XIAO </a>  Github of my course at <a href="https://github.com/hpssjellis/maker100">https://github.com/hpssjellis/maker100</a>**

**My main Robotics and Machine Learning course is called <a href="https://github.com/hpssjellis/maker100">Maker 100</a> and is fully on Github, with plans to make all parts available for individual equipment purchase and a fully online component for technologically capable teenagers to complete before going to University.**

**I believe that Machine Learning needs to be taught within an understanding of Robotic sensors (flex, touch, light...), actuators (DC motors, stepper, servo, LED's... ), communication (Ethernet, WiFI, BLE, LoRa) and PCB design ( best PCB video <a href="https://www.youtube.com/watch?v=gjPNYMRA0m8&list=PLbKMtvtYbdPMZfzGuVTdc0MWKrFvU4nsu&index=3">here</a>). The Maker100 course quickly touches on all these areas and leaves more advanced topics to the as yet not developed <a href="https://github.com/hpssjellis/maker101">Maker101</a> course.**

![image](https://user-images.githubusercontent.com/5605614/176285054-ea98ff42-df6e-408a-b7c8-f480d5912d73.png)
 
<br><br><br><br><br><br><br><br><br><br>
<hr>



#### 8
# <a href="https://github.com/hpssjellis/portenta-pro-community-solutions">Portenta Pro Community Solutions </a> Arduino Library
**Has over 100 examples to help MBED Arduino Coders get up and running fast.** 
 
<img src="ppcs08-main.png" width = 800 />
 
<br><br><br><br><br><br><br><br><br><br>
<hr>


 
 
#### 9
# <a href="https://www.tensorflow.org/js/">TensorflowJS</a> Can reach a large Web capable audience
**In 2017 TensorflowJS was introduced originally as deeplearnJS, using TypeScript and some compiled Javascript. I spent a lot of time converting the @Google Brain code for Single page Vanilla Javascript that student's could use without installing anything, <a href="https://hpssjellis.github.io/beginner-tensorflowjs-examples-in-javascript/#tfjs-models">beginner-tensorflowjs-examples-in-javascript</a> In my opinion TensorflowJS is the best, most powerful platform to truly teach Machine Learning to the largest audience.**  
 
**Note: I have converted TensorflowJS models to arduino <a href="https://github.com/hpssjellis/my-examples-for-the-arduino-portentaH7/tree/master/m09-Tensoflow/tfjs-convert-to-arduino-header">here</a> but it is a bit complex and size is always an issue, much easier to work with EdgeImpulse!**


<img src="https://user-images.githubusercontent.com/5605614/176290714-58fa7196-fe53-4ce9-a77b-2687b4e757fa.png" width = "600" /> 

<br><br><br><br><br>
<hr>
 
#### 10
# Vanilla Javascript Single Page TensorflowJS
**A Working xOr example <a href="https://www.rocksetta.com/tensorflowjs/beginner-keras/20keras-xOr.html">here</a> that can be edited live and copied to your own website.**   
 
<img src="tensorflowJS-xor.png" width = "800" /> 

<br><br><br>
<hr>
 
#### 11
# WebSerial Possible Teaching Potential
**WebSerial is an interesting combination of microcontrollers with Javascript webpages such as TensorflowJS and working on Desktop or Android Cell Phone. See demo page <a href="https://hpssjellis.github.io/my-examples-of-arduino-webUSB-webSerial/public/webserial-and-polyfill.html">here</a> which has links to the Arduino files. Teaching power of TensorflowJS, cheap microcontroller to connect with Actuators (to do something), possibly connect with Sensors, but a cell phone has a lot of sensors built in. Interesting potential here for education with minimal cost. Any Grad students with a strong Javascript background interested in this?**   


<img src="https://user-images.githubusercontent.com/5605614/176287664-bd0f1893-c3df-4f50-bcc4-86091141569f.png" width = 700 />


**Combining WebSerial with EdgerImpulse WASM (Web Assembly) would be very interesting. See my WASM examples <a href="https://hpssjellis.github.io/my-examples-of-edge-impulse/public/index.html">here</a>. Note: these WASM assignments are very easy to get students to make and test on their cell phones.**
 
 
<hr>

#### 12
# Maker101 Advanced ML  

**EdgeImpulse expert Keras Mode for <a href="https://docs.edgeimpulse.com/docs/edge-impulse-studio/learning-blocks/object-detection/fomo-object-detection-for-constrained-devices#expert-mode-tips">Model Manipulation </a>**    
 
**Expert mode on EdgeImpulse is a must-learn area for advanced use of Machine Learning Models. Hopefully future videos will be on my playlist <a href="https://www.youtube.com/playlist?list=PL57Dnr1H_egsQPnEObWHPhK1Q4g_IDWcR">here<a/>.** 

<img src="https://user-images.githubusercontent.com/5605614/176312017-21b191b3-342e-4816-916c-6946190c8d37.png" width="300" />
 
**After Classification Coding What I found really interesting this year with my <a href="https://www.gearbots.org/stem-academy/">GearBotsBC</a> group was using EdgeImpulse models but then coding the results to drive a car. This model sensed the white line, but the processing of the information was very interesting to drive the car. This is on going.**
 
 
 
 
<img src="rccar.gif" width="140" />    <img src="https://user-images.githubusercontent.com/5605614/176314510-2caa178c-580d-4060-b15d-cec285d00b11.png" width="200" />    




<br><br><br><br><br><br><br>
<hr>

#### 13
# Boards other than the $57.50 <a href="https://store-usa.arduino.cc/products/arduino-tiny-machine-learning-kit">Arduino ML Kit</a> and $111 <a href="https://store-usa.arduino.cc/products/portenta-h7">PortentaH7</a> mentioned earlier)
1. The $5.40 USD [Seeeduino XIAO](https://www.seeedstudio.com/Seeeduino-XIAO-Arduino-Microcontroller-SAMD21-Cortex-M0+-p-4426.html)  Only a limited number of pins, but works with my Arduino MBED code<br><img src="https://user-images.githubusercontent.com/5605614/176248216-7a99f725-e3c6-4698-a1e5-56bfd34dcf54.png" width = 40/><br>
2. The $37 USD [Seeeduino Wio Terminal](https://www.seeedstudio.com/Wio-Terminal-p-4509.html) <br><img src="https://user-images.githubusercontent.com/5605614/176248954-38cad413-3c2d-47cb-84a3-60359ba7e863.png" width = 70/>   
3. The $115.00 USD [NiclaVision](https://store-usa.arduino.cc/products/nicla-vision?selectedStore=us) could be very good for Color Vision, sound and accelerometer Machine Learning <br><img src="https://user-images.githubusercontent.com/5605614/157479032-f93ac6e1-1139-4886-bf40-9dfc6e8c2b9c.png" width = 70/>
4. The $33.40 USD [Nano 33 Ble Sense](https://store.arduino.cc/usa/nano-33-ble-sense-with-headers) is very good for sound and accelerometer Machine Learning <br><img src="https://user-images.githubusercontent.com/5605614/176252302-5f9474d1-07cc-4912-ae73-cc96aaeed92c.png" width = 55/>
5. The $129 USD [Sony Spresense Kit](https://shop.framos.com/us/spresense) with Breakout Board and Camera and now works on the Arduino IDE. Absolutely nothing wrong with this board, I have just not yet got it doing Machine Learning on the Arduino IDE yet. Note: uses LED0, LED1, LED2, LED3 instead of LEDB, LEDG, LEDR <br><img src="https://user-images.githubusercontent.com/5605614/176248308-bad3aaa0-fa86-4b34-9a98-e140af242199.png"  width = 55/>
6. The $25.50 USD [Arduino Nano-RP2040-Connect](https://store.arduino.cc/usa/nano-rp2040-connect-with-headers) Is very new but has lots of potential over the RPI Pico as it has WiFi and BLE onboard and the $4 USD [RPI Pico](https://www.raspberrypi.org/products/raspberry-pi-pico/) Amazing board for the price. <br><img src="https://user-images.githubusercontent.com/5605614/176248392-4cfa47f3-5533-40eb-a8f6-00b2faef2ae8.png"  width = 20/> 
7. The $25.00 USD [ArducamPico-4ML](https://www.arducam.com/raspberry-pi-pico-machine-learning/) This board looks like it would be perfect for machine learning with a mini screen and camera but I have never got it properly working on the Arduino IDE.<br><img src="https://user-images.githubusercontent.com/5605614/176248456-b4cda708-2995-4f6b-8d02-47915015c2fb.png"  width = 50/> 
8. What boards will be available in 2023? Cheaper, faster, more efficient. 
 
 <br><br><br>
<hr>

#### 14
## <a href="https://www.voltera.io/">Voltera.io </a> at School PCB design
  
**<a href="https://www.voltera.io/">Voltera.io </a> is a possible educational solution, similar to a 3D printer, but for PCB's. Takes a set size small board, drills holes, manual install copper vias, prints traces, print solder paste, manual place SMD's (surface mount components), auto heat, long cool down. Uses very low temperature silver solder for through-hole-technology (THT) components.**  
 
**I have asked my school to purchase a V-One, but the $6000 USD price tag might be too steep. Perhaps someone has a suggestion for how to get a grant to get one of these?**  
 
 ![image](https://user-images.githubusercontent.com/5605614/176255114-435ef8c9-1989-4761-ae3b-daebea51492f.png)

 My animation/3D Printing students can do a lot of PCB design from this one 6 minute video <a href="https://www.youtube.com/watch?v=gjPNYMRA0m8&list=PLbKMtvtYbdPMZfzGuVTdc0MWKrFvU4nsu&index=2">here</a> about <a href="https://easyeda.com/">EasyEDA</a> and <a href="https://jlcpcb.com/">JLCPCB</a>. 
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<hr>

#### 15
# Summary:
 
**I am Jeremy Ellis, Twitter <a href="https://twitter.com/rocksetta">@rocksetta</a> Canadian High School Technology Teacher.**
 
**<a href="https://github.com/hpssjellis"> Jeremy Ellis Github Profile</a>**
 
**Lots of ways to teach Machine Learning and even more will be available in the future.**  
 
**It is an exciting world with lots of changes due to Machine Learning, as Educators I feel we have a responsibilty to promote understanding of this new tool and not just Machine Learning but how it all fits together with Embedded Devices, Sensors, Actuators, Communication and PCB Design.**

 <img src="https://user-images.githubusercontent.com/5605614/176367428-196bd8d2-e10d-4030-9de0-09f150028431.png" width="400" /> 
 

 <br><br><br><br><br>
<hr>






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
