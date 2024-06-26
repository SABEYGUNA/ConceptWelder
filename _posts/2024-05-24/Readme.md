

# Pair-programming with Kids

One day I try to teach programming language to my three kids. First I start with HTML as thinking it will be easily understand. 
But only one was interest.

I am always inspired by watching Dr. Ruchira Wijerathna's ['Science With Ruchira'](https://www.youtube.com/@ScienceWithRuchira) Youtube channel. One day I show this ['DIY Arduino RC Car'](https://www.youtube.com/watch?v=T7A0ICf_pa4) video (In Sinhala Language) to my kids as they are fan of vehicales.

[![Watch the video](/DIY%20Arduino%20RC%20Car%20%20-%20Sceince%20with%20Ruchira.PNG)](https://www.youtube.com/watch?v=T7A0ICf_pa4)

After watching that they aks from me can we build a one?. I said yes, but you have to build it I am only going to guide you.
Then the next question they had is 'Can we build such a vehicale our self?'
When I heard that I remember what I leaned from [Johanes Broadwell](https://github.com/jhannes) in 10 years back,  Still I remember what we learned in one project anything we can build in 4 steps, [Pair programming with Sankalpa](https://johannesbrodwall.com/2014/06/27/pair-programming-with-sankalpa/)
And we applied it in several other software projects and I personally also.

We break any unknown task in to 4 differnt simple steps and followed. 
1. Experimental version
2. Basic version
3. Simplified version
4. Complete version

I said 'Yes, you can build anything in 4 steps'. 

1. Experimental jeep version.
2. Basic jeep version.
3. Simplified jeep version.
4. Complete jeep version.
5. Enhanced jeep version. (Optional)

We expect complete version to be a all terrain vehicale with camera.
Lets call it 'jeep' they named it.

Then we started our experimental task. Milestone we were set to have something control by Arduino board. 

To start the project we had only 1 NodeMCU board, laptop only in hand. I said ok lets order 2 differntials from online store as it may take time to deliver. 
Noo, We have some old parts of remote controlled jeep we can build a chassie from that, Brothers said. 

ESP8266 and two batteris.
![Items found from home](/Items%20in%20hand.jpg "Items found from home")

Front and rear axle from old toy
![Front axle](/Front%20axle.jpg "Items found from home")

![Rear axle](/Rear%20axle%202.jpg "Items found from home")

After spending 1 - 2 days of working on vehicale they came back with chassie built on based on the plastic bar and 2 differnt types of wheels and working front axle. 
Vehicale is not very solid but enought for experimental version. 
Front axle consist two motors one for going forward reverse and other for turn left and right. 
Then we tested both axle machanism with external power source, Only fron axle is completely working rear one have some machanical issue. 
And we could find two 1200mah batteries from old emergency lamp.
We start setting up Arduino IDE, and kids start with ['Blink'](https://blynk.io/) sample code and try to understand the code.  
And I asked to write some pseudo code of the program, Elder brather already learned that lesson in school. What they write is acceptable. 

Pseudo code

![Pseudo code](/Pseudo%20code.jpg "Pseudo code")

That was the first virtual sprint we ran.

Next day we together create a list of hardware items required. I shared the guideline article them then they complete the wiring of two motors, motor control, node mcu with battery pack.
We start our program and try to do run car forward for 5 seconds. After succssful with that. I asked them to complete the other movements. 
Our plan was to do Forward, reverse, turn-left and turn-rigth in given time period with small time gap.
After few round of test and bug fixing they could achive that.
Then I thought this is good time to introduce refactring. 
And we write first custom function to move car forward, with time period as parameter. And they have write other functions alone.
Thats the second sprint and Experimental jeep version.

They egally wating for this step to controll there 'jeep' remotly. And already watching some vedios how to do that have found they can do that using 'Blnk' platform.
First my plan was to build a web page and controlled 'jeep' over that, But I thought 'Blnk' is easy to understand them. 
Then we installed required library, download mobile app, and modify the code to support 'Blnk' with only forward. 
Code compiled but failed to upload to the module. Trying few more time but result was same.
Then we found issue is with board, we were using CH340 board which is less reliable than CP2102 board. 
We have to wait about 5-6 days till the new board received. 

NodeMcu V3 Lua CP2102 ESP8266 Development Board
![New board](/CP2102%20ESP8266%20board.jpg "NodeMcu V3 Lua CP2102 ESP8266 Development Board")

Re-start the project again, upload the code and tested. But 'jeep' only going forward, no turning or even not stopping regardless of what ever the command we sent. 
First we thought issue with the wiring, but later found issue with code it self. 
In code refactring they have copy and paste the same values to every function. 
Finally its working. 
They built there own remote controlled car. 

![Pseudo code](/Completed%20top%20view.jpg "Completed top view")
![Pseudo code](/Completed%20Front%20view.jpg "Completed front view")
I am going to stop here with the end of Basic jeep version. 
Simplified and complete version yet to come.



