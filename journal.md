<img width="814" height="1118" alt="image" src="https://github.com/user-attachments/assets/097eb7d5-1501-4db6-88a8-8198bc78df4c" /># Entry 1 4/4/2026 - 6 Hours Spent
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

# Entry 2 4/5/2026 -7 Hours Spent
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
