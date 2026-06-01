# GhostCutter

*Exported 2026-06-01 · 3 entries*

---

## Day 1 - Thursday, 28 May 2026 - Importing Progress
Today I started journaling by getting some of my progress from the CAD I already did, I already started a bit of this project before journaling so apologies.
The first important step was choosing what extrusions/how I was going to make the frame. I've seen and assembled/torn down a lot of 3d printers before + have an ender 5 pro on hand to take a look at. My main choice was to go with 2020 aluminium extrusions as these are light weight, popular and strong as well. I could have gone with 4040's but honestly they are too big and bulky for a simple laser cutter

Once I chose my frame I began a fusion design!
This was a rough design - sorry I don't have more pictures because this is from the past!

![image.png](https://cdn.aaravj.tech/files/e7a13159-9143-4d9e-b5b6-08e058cbd58c/image.png)

I decided to use corner brackets (however this is the fifth time I've changed them as I could never figure out how I'm going to make my frame).
The dimensions I chose was 500x500mm for the cuttting area however after moving on with the design I soon realised that realistically if the machine was 500x500 I would only get about 300x300 cutting area, for future versions I would like to expand on this!

The next step was to research movement systems, I chose CoreXY since I like how it works and wanted to experiment with a corexy laser cutter. Personally I haven't seen anyone build a laser cutter with a 3d printers frame and feel this would be really cool!

Since I've never made a coreXY machine before I had to do tonss of research, this included stuff like understanding corexy kinematics and how they worked

![image.png](https://cdn.aaravj.tech/files/b28d9803-2494-44f5-a5bb-2162665da0ea/image.png)

[This video](https://www.youtube.com/watch?v=_ramiM3KHYE)
Was a great resource to help me get started

Another vid I used as reference was [this one](https://www.youtube.com/watch?v=KqbJemLnnNM&pp=ygUWY29yZSB4eSBsYXNlciBlbmdyYXZlctIHCQkNCwGHKiGM7w%3D%3D)

Through this research + bugging souptik about his 3dp design I started to design the actual laser cutter.

[This](https://github.com/souptik-samanta/ChaosCompiler) design was an absolute life saver working as a great reference for me.

### Started Designing Motion Systems

I then started to design motion systems - this included having a middle rail and 2 linear rails on the side to house the y carriage 

![image.png](https://cdn.aaravj.tech/files/c28b1fa7-0297-4734-be2e-c9c6c856711a/image.png)

After this I created a middle rail for the XY gantry

![image.png](https://cdn.aaravj.tech/files/ab7b75db-4600-4ae0-900b-e34dd812f6d6/image.png)

You can also see in this design I'm not using the corner brackets ^ One of my many changes and inability to choose what bracket I wanted to go with.

Thats it for the journal impor (I'll won't drag the journal too long)

**Time Spent : 7 hours including research, design and iterations**

---

# Day 2

Okkii whats next? I took at look at some more docs and printed some prototypes. The main focus is this prototype


![image.png](https://cdn.aaravj.tech/files/dfb56df4-339a-4790-be59-e0ca2c1a55cb/image.png)

The first version of this - 
![image.png](https://cdn.aaravj.tech/files/72499cd1-b592-42e0-9adf-7182fbbb9ded/image.png)

![image.png](https://cdn.aaravj.tech/files/4b69c01a-3d9e-4238-938f-fa44cb0f2e08/image.png)

^^ back when I had NO idea what I was doing with the movement gantry (had some help from a friend)


This part is what holds the entire Y gantry in place so this component is crucial as without it the cutter would collapse. If you look closer at the moddle its currently split into 2 parts however this creates unneccasary weakness in the system, to combat this the simple fix was to add material on the side and combine both parts together like so

![image.png](https://cdn.aaravj.tech/files/ffc41465-9ab1-4199-b4ab-55b83845e858/image.png)

This adds more reinforcement to the sides allowing for a singular 3d print improving strenght as well.

After adding that I also added the linear rail onto the Y gantry, I've chosen to mount it sideways for now but after looking at other designs due to bend/flex I'm going to change it to the top
  
![image.png](https://cdn.aaravj.tech/files/b13c18b2-fe8c-4bfd-a295-d4fcaa623682/image.png)

Another change I made was to extend the front and back top rail to 650mm to allow for the motor and pulley mounts, I grabbed the motor mount from grabcad 
![image.png](https://cdn.aaravj.tech/files/b0eed3d4-8f29-4c0e-aae9-9bea964223b3/image.png)
And planned to weld this on (future me - I'm going to switch to another plate because I don't have a welder lol)

Changing the lengths of the rod meant that I can't use my custom corner brackets anymore and I would have to use these L brackets to secure everything together. I made a crucial mistake on the bottom for these brackets and I'll explain in a bit

![image.png](https://cdn.aaravj.tech/files/64dd9310-ed0c-42d2-87a7-ad659e36ac2b/image.png)


The next thing I added was these pulley mounts for the core XY belts as per core xy kinematics :D

![image.png](https://cdn.aaravj.tech/files/645a5dc9-9b52-45f0-9099-a8b492355807/image.png)
 
These will route the belts around the entire gantry and are a crucial part of corexy (mount stolen from a friend @souptiksamanta) ty


I also added a 3d model of the nema 17 steppers that I'm going to be using

![image.png](https://cdn.aaravj.tech/files/144a5688-cc2e-41a1-b284-36cae1314d01/image.png)

NOW time for the big mistake - 
![image.png](https://cdn.aaravj.tech/files/522a3433-1137-4519-a35e-fcbc813df9ca/image.png)

Didja spot it? I made a huge mistake down here

![image.png](https://cdn.aaravj.tech/files/52dcb18e-2d78-46c8-8ad9-11cdca701f40/image.png)
By switching to these brackets, the problem with them is since they are plastic there is a tiny bit of flex so making a square with 4 of them doesn't result in a perfect square, I only realised this AFTER i started cutting the aluminium extrusions but not to worry! it can be easily fixed by switching to my ORIGINAL design of using cubed corner brackets (I'm yet to fix this in my design)


### Part 2 - Building the bed

Have you ever thought how a laser cutter bed works? I mean the laser is *cutting* through the material so it will cut through the bed as well right? Thats where a honeycomb bed comes in, it looks something like this

![image.png](https://cdn.aaravj.tech/files/f38b5a21-1112-428a-a1fb-e77c14669a1c/image.png)
 
And its basically a block of aluminium milled in a thin honeycomb pattern that basically spreads heat and doesn't allow the laser to cut it. Now the problem with using this in my case is 2 things

1 - Am I made of money - NO, is hackclub made of money - NO
2 - is this expensive and heavy - yes, do i want to use it - NO

To combat these problems I spent a couple hours with my teacher sketching possibly bed designs (I don't have the sketches unfortunatley)

TLDR I'm planning on using a diode laser for my build, what if I use its weakness to my advantage - A major weakness for a diode laser is that it cannot cut through clear/light acrylic as the 450nm blue lenght laser light cannot penentrate. This can be used to our advantage as we can make a bed out of clear acrylic to ensure the laser won't cut through it!

The problem still remains though that the acrylic will heat up due to the  laser intensity and burn anyway, to combat this I whent back to the honey comb design and came up with a design of my own. What if I made a bed that has vertical *slats* instead of a honeycomb design, slats would help spread the heat + they would also be spaced thin enough to keep the cut pieces from falling in the bed. Since I also had access to a MASSIVE co2 laser cutter at school that could cut clear acrylic + a prusa xl for the bed size I decided to take advantage of both of them.


### Part 3 - designing the bed in fusion


Ok so to start designing the bed I first layed out a bed cutting area of 400x400, my laser cutter was initially meant to be 500x500 but i kinda forgot about the mounts and whatnot that would reduce the area to 400x400, anway I started by making a base for the bed like so


![image.png](https://cdn.aaravj.tech/files/a7ad84eb-cb86-4399-83f5-15cb729687d0/image.png)

I then continued by designing the slat border and slat holes for the acrylic to slide into making the final bed


![image.png](https://cdn.aaravj.tech/files/00505e6f-2bb8-4ead-9b7a-c4c863133872/image.png)

Two sides are smooth and 2 sides have the slats, the smooth is just for a border and to provide a vertical boundry and the slats is where the acrylic strips will go. 

One part of the bed has lower grooves just as a resting point for the slats like so

![image.png](https://cdn.aaravj.tech/files/9094099c-fe78-40f0-a197-2e668288868d/image.png)

The other side has deeper grooves for the slats to properly slide into

![image.png](https://cdn.aaravj.tech/files/0ac12b4a-9939-460f-915b-75768bd3c463/image.png)


These 2 combined let 3mm thick acrylic strips go into the bed like so

![image.png](https://cdn.aaravj.tech/files/bd7f6d50-a7b1-42cb-8816-6647b3cca923/image.png)

### Final Bed


![image.png](https://cdn.aaravj.tech/files/06d52da7-07e9-407a-916f-04b7625a4693/image.png)

### Laser Cutter With Bed


![image.png](https://cdn.aaravj.tech/files/395d9bd3-09fa-47fa-baf9-c3c8495fbb8c/image.png)


# Time spent - ~15 hours

---

# Day 3

Day 3 lets go, couple goals for today. So far I've finished the xy gantry and the base. My next goals are to add the laser head mount (basically the X carriage that houses the laser and belt grips.


Before we get to redesigning that I need to cleanup the fusion tree. Our project currently looks like this


![image.png](https://cdn.aaravj.tech/files/bebb5ec8-a705-46fd-8e47-2987ac438114/image.png)


A tad bit messy I know, to combat this I used a lil bit of help from claude! believe it or not, claude works suprising well using the fusion mcp (it can't design things but its create for cleanup and organsing your working tree), I sent a single prompt to claude and my tree whent from looking like this


![image.png](https://cdn.aaravj.tech/files/42eee54f-2823-4966-8167-9d4b149e049c/image.png)

To this

![image.png](https://cdn.aaravj.tech/files/0ab0e825-f203-4e94-b642-51b873474b37/image.png)

AI really can be amazing sometimes :D
Alright moving on, the next thing I added was a laser mount, to do this I need to research different type's of laser available for me to use. My design uses a diode laser and I want to keep things light on the tool head and not use a bulky laser. Some of the best laser's I found where by LaserTree and they had amazing documentation online aswell!

The biggest contender's are
- LT-20W-A
- LT-40W-AA
- LT-80W AA

For this project, I'm going to choose the 80w model, this is because the 80 stands for input power and *not output power*, Instead theres a metric caled optical output that properly shows the output power, in my case for the 40w model its optical output is a 5w laser and for the 80w module its optical power is 10w which is ideal. 


To actually make the mount for it, I need to import the step file for the laser into fusion, I found the 40w AA and that should be fine for making the designs as both versions fit together

![image.png](https://cdn.aaravj.tech/files/a0a8a879-f1ce-4e1c-86d9-dcc81aa68611/image.png)


I then used the plate on the laser, extruded a plate and designed this mount around it

![image.png](https://cdn.aaravj.tech/files/1621ffd7-0557-44d5-a5b4-2715f2752f55/image.png)


*Future me here, this mount was designed for a vertical mount of the laser head (meaning the rail is on the side) however I will change this to be the top and completley redesign this peice*


I then added both the laser and the mount to my cad model! 
![image.png](https://cdn.aaravj.tech/files/1de0025c-82e6-4103-8d1a-47f83a22d458/image.png)


Ok now time for the big change, I've read + seen other people's projects online and most of them mount the X rail (laser cutter head rail) on the top and not the side to prevent flex, I would rather be cautious and add this now rather than add it when something goes wrong.


![image.png](https://cdn.aaravj.tech/files/40e83eb6-2636-4314-8b1c-1590e220662c/image.png)


I removed the laser head and carriage and added the rail on top!
After I added this rail I need to redesign the laser head mount as the old mount is designed for a side rail, Again I did the same thing taking the laser cutter's plate profile, plonking it in a new file and designing a lil bracket around it like so!


![image.png](https://cdn.aaravj.tech/files/eea9e2a7-6c2d-4faa-b735-d795f61e44ff/image.png)

Now to patch things off I wanted to add a back panel but I didn't want to use heated inserts as my projects have gone prettty bad with them in the past with plastic clogging up my soldering iron. To combat this I brainstormed different solutions till I came up with an idea I previously used 5 years ago! 

My idea was to embed a normal m3 nut within the plastic as a press fit and then add a hole for the screw to go into, the nut would act as "metal" threads for the screw ensuring that I could screw and rescrew as many times as I wished without the threads wearning out!!


To implement this, I needed to find the m3 nut profile and design a reccess hole in fusion first!
Found an amazing resource at [this website](https://www.joom.com/en/products/6a0436ffde85040178f3c099?currency=AUD&utm_productid=6a0436ffde85040178f3c099&utm_freeze_token=eyJraWQiOiJ2MSIsInR5cCI6IkpXVCIsImFsZyI6IkVTMjU2In0.eyJleHAiOjE3ODAyNzc2NDksInIiOiJBVSIsImMiOiJBVUQiLCJ2Ijp0cnVlLCJwcyI6W3sicCI6IjZhMDQzNmZmZGU4NTA0MDE3OGYzYzA5OSIsInYiOiI2YTA0MzZmZmRlODUwNDY0NzhmM2MwOWQiLCJjIjoxNy4yNSwic3AiOjE3LjI1fV19.s9gphjSX1E3JCoX-1myAE_lFzFfy4msPOd3hpt96n6BEQKBuoyudRDxKfHEaa9W_f4DFp9U1TzGjhHjuXsZoiA&variant_id=6a0436ffde85046478f3c09d&gsAttrs=eyJyZWdpb24iOiJBVSJ9&u=1&utm_audienceid=advertising_web_gg_2d&utm_source=google&utm_medium=cpc&utm_campaign=21750412689&utm_term=assgid-6519992501%2Cagi-%2Cadi-%2Ctid-%2Cdev-c%2Creg-9071272%2Cmd-6a0436ffde85046478f3c09d&gad_source=1&gad_campaignid=21760644364&gclid=Cj0KCQjwlerQBhDMARIsAB16H-WSWmkYPF39-fpAhJJOtg2ZOVNrSGYjFvYwKlJ-xwNDJsWJ2mj3CZIaAqKgEALw_wcB)

![image.png](https://cdn.aaravj.tech/files/5b08a96d-1b84-449e-a630-64bb67d1484e/image.png)

That basically showed me how to perfectly design a press fit for a m3 nut in fusion! I then designed something like this

![image.png](https://cdn.aaravj.tech/files/fc597229-b2eb-469b-9c98-534ef1d1d1ab/image.png)
That should technically allow me to press fit the nut inside and get a nice screw going through!

### Did it x6

![image.png](https://cdn.aaravj.tech/files/77368736-02ef-4906-84ad-383c500ffbc5/image.png)

### Final design with 3d models + back plate (laser cut ironically lol)

![image.png](https://cdn.aaravj.tech/files/bf023146-7f38-4825-8441-7e9b02af16b8/image.png)

### Final design with laser cutter

![image.png](https://cdn.aaravj.tech/files/ff39f876-6210-4e42-bf78-0446863c775a/image.png)


# Almost done!!!
Exciting, I'm almost done! The last part is to add some safety! Especially since I'm working with lasers (class 4 laser scaryyy)
I need to add an enclosure with laser proof acrylic panels + use some special looking goggles that look like this

![image.png](https://cdn.aaravj.tech/files/cf623d9d-529f-47ab-be9e-b170b34d2cf6/image.png)

These are both ugly AND Expensive but I cannot stress HOW important it is to have laser goggles with a class 4, class 4 means permanent eye damage in milseconds and is EXTREMELY dangerous even WITH an enclosure - [link](https://www.amazon.com.au/xTool-Laser-Safety-Glasses-Goggles/dp/B0GMQJHD33?source=ps-sl-shoppingads-lpcontext&ref_=fplfs&psc=1&smid=A3O42K7KL1SSHC)


I then added a quick enclosure (clear because I wanna see the design) will be not clear irl

![image.png](https://cdn.aaravj.tech/files/9ceb35c7-1a01-4c15-be00-088f013fd1a3/image.png)

I then also added a little pocket at the bottom to allow for electronics and wiring to sit! 

![image.png](https://cdn.aaravj.tech/files/388dc004-76f9-477f-a52c-f71cb2b0c619/image.png)

Among the little things, also added little risers for the bed to sit in

![image.png](https://cdn.aaravj.tech/files/3493ac88-be76-4102-820c-c469b12afcde/image.png)


AAAND YEAH! Thats it - the laser **"*should*"** technically be done but I'm sure more changes will be needed as I progress in the IRL build!

Picture - 
![image.png](https://cdn.aaravj.tech/files/42531106-fd2c-4656-8fdf-3f6565d05ac9/image.png)


# Bonus pics 
(I've funded a lot of components myself and already started builing IRL cause I couldn't wait :P)

![image.png](https://cdn.aaravj.tech/files/147c317e-f212-4e31-acc2-045d626fe28e/image.png)

![image.png](https://cdn.aaravj.tech/files/7bb4d26b-e975-4033-8aa3-0c2d20b28b18/image.png)

![image.png](https://cdn.aaravj.tech/files/6d114246-0edc-4427-9e11-4636322840e7/image.png)

![image.png](https://cdn.aaravj.tech/files/3a9ac4f9-f0c9-4341-8ea4-b7af9305729e/image.png)

## I HATE TAPPING - no joke spent 4 hours tapping 16 connections

![image.png](https://cdn.aaravj.tech/files/677fb78d-2046-40e5-9745-e83b672f836d/image.png)

![image.png](https://cdn.aaravj.tech/files/59732c30-49af-4b8f-a4c2-92e7e40bfc26/image.png)


# Time spent : ~20 hours
^ probably undercounting here because I haven't included the IRL build time of cutting the rods + assembling everything
