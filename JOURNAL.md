---
title: "Osmium"
author: "Parker Rupe"
description: "Osmium, a name chosen for the sheer absurd density of this project, is a custom halo-frame based ultra compact cross gantry 3D printer. The entire printer should fit inside the build volume of most normal printers (like a bambu p1), with its own build volume of as close to 120mm^3 as possible. As the main design aspect, it features a 1” thick machined steel halo that the entire rest of the printer is referenced off of. Further design restrictions/goals include using nema 17 motors for all axes, including the extruder, a custom hotend, Bowden + CPAP for an ultra light toolhead, 9mm belts (without long shaft motors), and a custom bent sheet metal cantilever z assembly."
created_at: "2026-04-04"
---

# April 4: Began Design

Today is the first day of design for my cross gantry project. I think I will be doing this for hack club infill - thus, the printer needs to be "silly"/unique. That means it will be a wooden halo! I spent an hour looking at different wood types and sources and what wood has been used by others for printers. I looked at blank unfinished board, lasercut plywood, different hardwoods or softwoods, and more.
Ultimately, I decided I was going to machine the halo on my school's ShopBot CNC router, using a 1/2" thick bamboo cutting board for my source material. I would also be using 1/4" lasercut plywood for my rail backers and other structural elements. 
I also made plans to vacuum resin stabilize the wood. This is important as it allows for the bearing seats to maintain shape under belt tension and constant use. 
I then spent another half hour deciding various other aspects of the printer. For now I am really only focusing on the gantry. So, I decided:
120mm x 120mm bed size
230mm x 230mm printer footprint
Nema 17 motors for xy, non awd
MGN9C Linear rails

If this sounds similar to another printer, that's because it is! It is the same bed size, footprint, and rail size as the Voron v0 - just bigger motors. And more motors. And more rails. It is going to be quite fun making everything fit. 
Oh, quick thing. What is a halo, and why am I designing around one? 
In super high performance 3D printing, a halo is a concept that covers a unibody piece of material, usually metal, that the gantry all bolts to and references off of. This allows for unparalleled stability and alignment, as everything is mounted to the one part. 
Mine is just wood! 

With all that decided, I started with the aforementioned halo. 

<img width="1201" height="970" alt="image" src="https://github.com/user-attachments/assets/b637839d-7f26-43b4-9378-ff5430770766" />

<img width="1274" height="1161" alt="image" src="https://github.com/user-attachments/assets/ed1cacd8-894b-462d-a8dc-a9ec61aa8db0" />

<img width="1102" height="911" alt="image" src="https://github.com/user-attachments/assets/35e7e5a0-436c-4c52-8e57-363c72fd489b" />

I kinda just guesstimated the exact measurements, using an existing printer, Splendacross, as well as the Voron 0, for rough sizing ideas. I then added the linear rails and one motor so I could start trying to package things nicely. I opted for 150mm rails as this is what both the v0 and splendacross use. 
I fiddled with sizing for a bit but I ended up pretty happy with this. The footprint is 234x234mm, which is quite close to my original goal. 

<img width="1182" height="1151" alt="image" src="https://github.com/user-attachments/assets/d79a274e-037b-4388-a0f3-30975265f587" />

I then started adding pulleys and idlers. I set a pretty unique challenge for myself here - I want to keep the corner assemblies of pulleys/idlers entirely within the footprint of the nema 17 motor, and I did not want to have to buy long shaft motors as they cost way more. 
So, there are two dead shaft idlers and one pulley, all for 6mm belt. 

<img width="1172" height="910" alt="image" src="https://github.com/user-attachments/assets/b59a4759-f410-4b81-9484-05b134d34df6" />

The pathing looks a bit like this, with the bottom left idler being the idler for the opposite side's motor, and the pulley and bearing stack (bearing stack is dead shaft idlers for the smooth side of the belt) are the driving side of the belt routing. The bearing stack is needed to route the belt far enough back to not hit the linear rail. In most cross gantries they just run the belt over the rail - however, this requires either long shaft motors or not mounting the double shear bearings to the halo. The first one goes against my design goals and the second one kinda defeats the point of a halo as you lose the alignment of your motors. 
This was all I got done today ! Next steps are to figure out mounting for the pulleys/idlers and of course the rest of the printer.

**Total time spent: 6.5 hours**

# April 5: Gantry Dev, mainly Motors/Mounting

Day two. Very first thing I did was work on packaging/mounting for the corner motor/idler assemblies. 

<img width="1076" height="1135" alt="image" src="https://github.com/user-attachments/assets/49999a23-1119-4295-a289-f324e7d71fc4" />

<img width="1186" height="1089" alt="image" src="https://github.com/user-attachments/assets/33e407d1-f780-450d-8ed5-c19441d2e710" />

I came up with this. I am only able to have two screws mounting the corners to the halo as the other two are blocked by the idlers but I honestly thing this is fine, especially since the press fit shafts of the idlers will help a lot with stabilizing everything, plus there is a decent amount of interface with the halo. The bearing at the bottom of the pulley, as well as the ends of the two idler shafts, interface/mount directly to the halo. This ensures alignment and rigidity within the gantry system. Also, like I stated with my earlier goal - this all fits in the xy footprint of the nema 17 ! I love it. 

<img width="1784" height="449" alt="image" src="https://github.com/user-attachments/assets/a4bf7840-b440-40b5-9a57-ad42d2b36d43" />

From there I actually sketched the belts ! I wanted to get a better representation of the pathing since it can get pretty confusing with everything in such a tight space. I do this by creating a sketch with each of the pulleys/idlers projected onto it and then offset those by the belt thickness, 1.2mm. From there I connect it all with tangent lines and we are good ! My belt attachment points are offset from eachother by a few mm but this should be no issue due to the reverse happening on the opposing side, so any force imbalance cancels out. 

<img width="1234" height="874" alt="image" src="https://github.com/user-attachments/assets/dea90e38-62f7-4377-a707-b767b23d296f" />

<img width="1136" height="1054" alt="image" src="https://github.com/user-attachments/assets/dfacae93-77ce-4aca-a788-dc55ebddf83a" />

This ends up looking pretty nice ! It is super, super compact, and having this physical representation of the belts helps a lot with visualizing routing. 

<img width="968" height="985" alt="image" src="https://github.com/user-attachments/assets/f836099b-efaf-4799-9bf0-2eb231758d4c" />

Here is that 234x234 footprint I mentioned earlier. This will not be getting any larger. 

<img width="1557" height="1309" alt="image" src="https://github.com/user-attachments/assets/0eb7fbee-0771-4492-887d-30e7aab776e3" />

Next I actually decided to work on the cross bars for the gantry. These connect opposing sides of the same axis, so there is two total, one for x and one for y. These are offset due to cross gantry's inherent offset of the toolhead. This is because the toolhead has to go next to the rails, not under. This actually exists in almost all motion systems, it's just that cross gantry is the only one that directly offsets the toolhead in both axes. I offset it as far as I could while still maintaining a minimum width for the backer that I felt comfortable with. This allows me to get the nozzle as close to centered as possible. Also, I have to keep in mind that the offset portion of the cross bars needs to fit between the motors at the end of the travel, so it is physically limited to being exactly 150mm or less. These cross bars are going to be 1/4" lasercut plywood as that is what I have on hand. 

However, I realized I need the blocks that go between the carriages and cross bars first ! Silly me. These exist for belt tensioning/attachment. 

<img width="909" height="804" alt="image" src="https://github.com/user-attachments/assets/bd1583fa-7742-4096-bdaf-c2c346e240e8" />

I started off making a simple block thing that extends past the side of the carriage, as the belts are off to the side. 

<img width="820" height="659" alt="image" src="https://github.com/user-attachments/assets/2f580806-8c56-4e90-83ff-c29d1777a26d" />

This has some simple features that interface with the recessed sections of the linear rail, hopefully increasing rigidity due to more surface contact. 

<img width="1167" height="1178" alt="image" src="https://github.com/user-attachments/assets/a66e8e49-dbc1-40ed-bcff-82566551c220" />

Here it is in place with the cross bar, which is lasercut wood. The little rib you see is for belt tensioning, which I shall now cover.   

<img width="1534" height="873" alt="image" src="https://github.com/user-attachments/assets/4420cfb5-bf9c-40ff-a522-6c6c69de33b2" />

I started with using my belt sketch to align some wedge clip tensioners I have used on previous designs. These clips utilize wedges with belt teeth to clamp onto the belt - belt tension thus increasing the clamping force. The belt will tear before the belt clip slips.

<img width="798" height="603" alt="image" src="https://github.com/user-attachments/assets/1dd62ba1-cbd2-4832-be0f-84c227ed4e8a" />

Like this! 

<img width="947" height="895" alt="image" src="https://github.com/user-attachments/assets/c5c53f77-aff7-42d2-9d5c-0dcba28850c0" />

From there I added two bolts on one side and two nuts on the other, with bolt passthroughs on that center rib. 

<img width="984" height="706" alt="image" src="https://github.com/user-attachments/assets/1c29bb6d-01af-44fc-932b-1add22c4bafb" />

You can see that here. This allows for belt tensioning from both sides evenly via tightening the two screws, while the rib holds it all in place. 

<img width="932" height="692" alt="image" src="https://github.com/user-attachments/assets/2859e2a7-a9eb-46a1-a541-846a8b8ee08b" />

I also made a shorter version for the other side. The only feature shorter is the mounting block between the linear rail carriages and the cross bar. This is because the two cross bars/rails have to be vertically offset or they will intersect eachother. 

<img width="1523" height="1079" alt="image" src="https://github.com/user-attachments/assets/9d322b52-ccc2-4461-b735-d4fdad69ddf3" />

That all looks like this !

At this point, I spoke with an engineer friend, who informed me that the small bearings in dead shaft idlers die very quickly under proper belt tension. So, I was like, "what if live shaft fits?"
And it does ! 

<img width="958" height="928" alt="image" src="https://github.com/user-attachments/assets/2d2065ac-9293-45ff-a9cd-a368758be0a6" />

<img width="1062" height="943" alt="image" src="https://github.com/user-attachments/assets/e5a716e8-195b-436f-b620-415691669127" />

<img width="814" height="1118" alt="image" src="https://github.com/user-attachments/assets/f1bae09b-b653-496d-b5a2-bf8831fd7f69" />

I know this is a bit of a mess, but just scroll back up to the belt routing sketch from earlier, except now with different looking idlers. These idlers have "live shafts" - the 5mm shaft spins instead of sitting in place, placing the belt tension load onto the much beefier 695 bearings. 

<img width="781" height="987" alt="image" src="https://github.com/user-attachments/assets/9526ebbb-7bf6-4fbd-bbb1-5f9a10866b49" />

In place, those look like this ! 

<img width="1005" height="728" alt="image" src="https://github.com/user-attachments/assets/52a282b0-b937-4308-acfe-d1b5d9a8d38e" />

Here is the halo interface which I forgot to show last time. The larger stepped bores are for bearings and pulley clearance while the middle one is for the motor double shear bearing. 

<img width="387" height="1204" alt="image" src="https://github.com/user-attachments/assets/ac1a06e2-c60d-4f88-bfe8-9829311c93a3" />

And here is the slightly different belt path with the new live shaft idlers. 

<img width="1311" height="931" alt="image" src="https://github.com/user-attachments/assets/4490f339-972b-446d-bfa9-245051a60185" />

These can handle a ton of belt tension now ! Enough to rip 6mm belts (or, potentially use 9mm or 12mm belt, but I think I need long shaft motors for that). 
And it still fits in the nema 17 XY footprint !!!

Oh, you may have noticed that at one point throughout those photos, the halo got a lot thicker. Turns out, 1" cutting boards are not any more expensive than 1/2" ones when you buy the cheapo bamboo kind. So I figured, might as well have more wood to show off !

<img width="2160" height="1153" alt="image" src="https://github.com/user-attachments/assets/90184af4-0b85-4ffb-90be-efa9ea7759a2" />

Here is a quick and dirty render I did to verify the fusion 360 wood textures/colors and get a "vibe check" of sillyness/cool factor. 
That is all for today ! Next should be finishing up tensioners and beginning toolhead design. 

**Total time spent: 7.2 hours**

# April 6: Pivot design goals for Forge

Today was... entertaining. So, I determined I just cannot make the infill deadline work. That's ok.
Because forge is happening. This means my budget can increase by a lot. This extremely silly printer has now been advanced to moderately silly - I am abandoning wood. 
Am I abandoning the super compact size? No. Am I abandoning the 1" thick halo? No. It will just be metal now. Specifically, stainless steel. That means the halo weighs 6kg. Teehee. However, we gotta get through the first things first. 

I realized something exciting ! I can fit 9mm belts without long shaft motors. How? I am not actually sure. But it fits. 

<img width="904" height="991" alt="image" src="https://github.com/user-attachments/assets/489000e4-cab3-4cdf-bcb1-69d56a24958d" />

<img width="1076" height="902" alt="image" src="https://github.com/user-attachments/assets/ae7a1707-13a7-4fe4-86e0-fb45ddd5e8f5" />

Kinda hard to get good photos of it but there you go. It doesn't really change the corner module itself.

<img width="1422" height="1084" alt="image" src="https://github.com/user-attachments/assets/004f6c43-1ba0-4402-aa7e-b96711532a3e" />

It does change the halo though. You can see that the hubs of the pulleys are recessed into the halo - this is the only way it fits. But it works so I don't mind. 

Notice how the halo is metal! I am so excited. 

<img width="1502" height="1193" alt="image" src="https://github.com/user-attachments/assets/c1cc1d41-1687-4286-9a31-5ec053d3a835" />

Most of todays entry was spent converting to metal. I had to completely redesign the halo. 

<img width="2154" height="608" alt="image" src="https://github.com/user-attachments/assets/01c65655-ad11-40db-99a7-41b15d49f2bf" />

That does mean we get these cool alignment pins though. For the wood halo this would have been pointless since there really is no way to align it on wood. With metal I can hold proper tolerances, so I can use two 3mm pins to locate my rails. These will be used for assemby and then removed.
Also, with a metal halo, I can tap the halo directly for rail bolting ! No need for pass through nuts and super long screws. 

<img width="1536" height="1039" alt="image" src="https://github.com/user-attachments/assets/4143dc5b-13b3-4500-8816-73572108a9d7" />

From there I was able to work on tensioners. I determined that I made a bit of a stupid mistake the first time around. The tensioners would have been able to slide back and forth on the carriage since there was no clamping. So, I made one side stationary while the other has one screw to actually pull tension and then two more to clamp the tensioner block in place. 

I actually changed it pretty quick though. 

<img width="774" height="638" alt="image" src="https://github.com/user-attachments/assets/4a0a8ab6-b986-419c-9aa0-774286e77b1f" />

I really just switched to one clamping screw and tried to minimize the height of the side blocks so that the overall gantry was shorter and thus more stable. 

<img width="1394" height="852" alt="image" src="https://github.com/user-attachments/assets/a907ac78-8a9c-4412-9d43-50319f50adfc" />

<img width="1768" height="876" alt="image" src="https://github.com/user-attachments/assets/5e4e0fc3-0556-4c98-8d4b-2caa4e1d2b61" />

Here is a closeup on the shorter side. I used an insert nut instead of a heat insert here because I don't trust the heat insert to not slip, and the nut doesn't require nearly as much work on my end for alignment, as I don't have to actively keep it straight myself. 

<img width="1400" height="1005" alt="image" src="https://github.com/user-attachments/assets/95570bcc-7046-4fb2-88f4-eae3c99f9d29" />

On that note, here is a cool sense of scale ! It is so tiny.

At this point I started looking into how much build volume I would actually have and realized it would be slightly less than 120mm due to the offset of the cross carriages vs the sides. 

<img width="1217" height="996" alt="image" src="https://github.com/user-attachments/assets/ee708b69-a87d-4adb-a189-e698117856ae" />

So, the real size is closer to 115x115. Which is fine! 
I decided to maximize this by trying to move the rails as far towards the outside of the printer as possible. I mainly did this by moving the belt attachment point outwards so the rail could move. 

<img width="1190" height="868" alt="image" src="https://github.com/user-attachments/assets/ea78ab80-64b9-411b-9ae6-fbbe3ac011b4" />

<img width="1235" height="940" alt="image" src="https://github.com/user-attachments/assets/4f4b9ba8-5275-4eef-873c-530d9480ff18" />

You can see the before vs after here. It's a small move, about 3mm, but keep in mind this is doubled due to the belts on each side. So, it makes a bigger difference than you would think when hyper optimizing. 

<img width="1587" height="438" alt="image" src="https://github.com/user-attachments/assets/2643df36-303a-4d90-a6a3-ea9bdc1a8d31" />

This also made the belt attachment points way less offset, helping mitigate any potential issues (though I explained earlier how those would cancel out either way, in theory).

<img width="1327" height="1093" alt="image" src="https://github.com/user-attachments/assets/8dc36630-bb09-40f8-b65d-e334e3573b1c" />

So this is what we are working with now. 

<img width="1239" height="953" alt="image" src="https://github.com/user-attachments/assets/b2ae6de3-2374-437d-abc0-a4bb2907e8b9" />

You can also see here how I made the cross bars and toolhead a bit thinner. I figure I can get away with 3mm instead of 6mm since I swapped to metal. 

<img width="1194" height="965" alt="image" src="https://github.com/user-attachments/assets/61ab237a-4c60-4404-af9f-80134a5401b3" />

Last big thing, I dehubbed the idler pullies like how Monolith does it, allowing for me to remove the weird thin walls on the edge of the halo. 

<img width="1015" height="698" alt="image" src="https://github.com/user-attachments/assets/39c55f07-d8c1-4595-9d15-3bbd2ff33900" />

These. Now it looks like: <img width="1080" height="750" alt="image" src="https://github.com/user-attachments/assets/db501188-553e-4cf7-be9c-1764338aa4e5" />

There was a lot of stuff I didn't necessarily cover as it gets super repetitive but you can see some of the progression through the photos. A lot of small changes that cascade into a lot of work because fusion back propagation of feature changes is abbhorent, so I have to manually fix it every time. 

<img width="1665" height="1051" alt="image" src="https://github.com/user-attachments/assets/e2f27ced-fb0c-4d23-8106-860cc1612250" />

So many errors. Literal hours of make small change -> fix issues -> make small change -> fix issues.

It looks great now though! I have been putting a lot of thought into where the rest of this printer will end up. I ideally want to use duet electronics/rrf, a bowden toolhead with cpap, structural panels, and more funky stuff. I really want to keep it all contained within the printer, including electronics, so it will be quite the challenge. 
I have even been looking into designing a custom beefy cantilever z out of bent sheet metal, utilizing a ballscrew ! I have so many fun plans. 
However, my next step is the toolhead before anything else, for real this time. 

Custom hotend anyone?

**Total time spent: 5.8 hours**

# April 9: Hot End Design

I started off my venture into the fine details of the toolhead with a custom hotend. Given my two previous hotend designs for Rework, I feel fairly comfortable doing this.
This hot end will have the same melt zone length as a supervolcano, but with different mounting, size, and less weight.

<img width="1107" height="726" alt="image" src="https://github.com/user-attachments/assets/a6956ed6-b572-43b3-b84f-d012baa0cb1c" />

I started off with a simple sketch consisting of literally just circles. One bore, the top one, is the melt zone bore, while the lower one is the heater bore. The two side circles are to define outer shape. 
The melt zone and heater will only be like 3mm apart. Good stuff. 

<img width="506" height="866" alt="image" src="https://github.com/user-attachments/assets/2aba3ecb-4748-420a-9ab1-082f5223dd08" />

When extruded, we get this tall figure 8 looking thing. 

<img width="854" height="808" alt="image" src="https://github.com/user-attachments/assets/3b515234-58d0-4e09-b3f9-e58f09dd4092" />

And then it gets meltzone threads.
This is just M6 threading. The nozzle, supervolcano meltzone adapter, and heatbreak are all just m6 threaded, making assembly easy. 
Why this figure 8 shape? I realize I did not explain much. Long story short, it helps minimize mass without looking stupid or having too thin of walls. Since I defined the circle locations off of tangent circles, it physically cannot make my predefined wall thicknesses any thinner (as any cutouts will remain tangent to those outer faces). 

However, I do have to add some material for set screws and thermitors. 

<img width="641" height="942" alt="image" src="https://github.com/user-attachments/assets/2fe0337a-5c3f-4111-bf8c-dee6bbad63fa" />

I came up with this end cap type thing. It is wider on the heater side because I have a silly idea for hot end bracing that you will see in a second. 

<img width="744" height="1055" alt="image" src="https://github.com/user-attachments/assets/2b8f0cb0-ea50-42b8-bb35-556f6986c9c0" />

It gets a chamfer and mirrored, making a pretty cooling looking heater block that doesn't weigh much! Ideally I will get this made out of copper or steel, both of which are very dense, so mass minimizing is important. This toolhead will be bowden and cpap so it is genuinely possible for the hotend to be the heaviest component. 

<img width="736" height="1036" alt="image" src="https://github.com/user-attachments/assets/f680ab01-b6be-4ac9-8b8b-23252b7876af" />

4 M3 holes on the rear bore. Two for set screws, two for thermistors. Dealers choice on which hole is which. 

<img width="565" height="1192" alt="image" src="https://github.com/user-attachments/assets/f232e4d2-638c-44ce-b4c3-af395891cbc1" />

Yay, I added the nozzle and heatbreak. The melt zone adapter is there too but not visible. It is a standard length v6 nozzle and a "v6 smooth heatbreak" from aliexpress that I used on my other hotends. 

<img width="474" height="812" alt="image" src="https://github.com/user-attachments/assets/0e5fc43e-656f-426a-a644-4f5f8b3abb77" />

I made a quick and dirty heater cartridge model and that gets added too. This will likely be one of the high wattage 48v cartridges from Luke's Lab. 

<img width="612" height="924" alt="image" src="https://github.com/user-attachments/assets/9534241d-d97b-44c2-8c12-6edf2fd30cf7" />

In place, it looks pretty neat. 
And finally, to reveal the silly hotend bracing I mentioned earlier. 

<img width="937" height="841" alt="image" src="https://github.com/user-attachments/assets/7eb9bf97-1f77-45b9-954d-d553be8c4d71" />

Two M2 screws on the bottom of the hotend itself. I know, it's unique. Kinda. It is actually similar to how chube mounts it's bracing, except mine will be the part cooling ducts for space saving reasons.

<img width="471" height="1166" alt="image" src="https://github.com/user-attachments/assets/6891fb60-6d58-4096-86c9-b9135c029c09" />

<img width="612" height="997" alt="image" src="https://github.com/user-attachments/assets/326c98c4-875c-4268-840a-5addf361c23b" />

Oooo so shiny. I really hope I won't have to change this hotend much at all. I can just like, stay strict to it while designing the rest of my toolhead. 

Next is when things get harder. Ducts, making things fit. Bleh.

**Total time spent: 3.5 hours**
