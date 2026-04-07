# Entry 1 4/4/2026 - 6 Hours Spent
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
