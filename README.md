# M3 Onboarding - Git Gud!

I'm following the M3 onboarding guide so I can become a certified citizen of the Metaverse! 
https://github.com/M3-org/git-gud

# ToDo:
- [x] Mindset
- [x] Email address (Identity)
- [x] Hackmd journal
- [x] Git
- [x] Create Avatar
    - [x] Install VRoid Studio
    - [x] Skeletonize
    - [x] Golden Jaw
	- [x] Hood
    - [x] Export
- [x] Pick engine(s)
- [x] 3D Scan
    - [x] Scan rocks
    - [x] clean up loose geometry
    - [x] Decimate
    - [x] export gltf
    - [x] compressed jpeg textures
    - [x] export glb
- [ ] Create World
	- [x] Skybox
	- [x] Moon
	- [x] Terrain
	- [x] Water
	- [ ] Rocks
	- [x] Skeleton
	- [x] Lighting
- [ ] Host
	- [ ] Fleek
	- [ ] Pinata
- [ ] Video

### Extra stuff:
- [ ] Create wallet
- [ ] ENS Address
- [ ] Custom Skeleton Avatar
	- [ ] Sculpt
	- [ ] Simplify
	- [ ] Texture
	- [ ] Rig
	- [ ] Fix bones

# The Journey
## Mindset
I'm doing all of this on my Cyberdeck...I've been deep in the mindset for a while:
![](https://i.imgur.com/rutCYHu.jpg)

## Identity
I want to treat the concept of my Identity separately from my Avatar. My Identity will be shared across platforms and I can take different forms (avatars) while still presenting as the same Identity. I created a new email address to serve as the base Identity for account registration and communication. I'm trying out ProtonMail because it's free and encrypted.

The alternative would be to treat the Avatar as its own identity and create new accounts "belonging" to the avatar. I see value in that approach, I might try it in the future.

## HackMD Journal
I don't usually like sharing things until they're finished but here we are. I'll be using this as my working task list and dev log. 
https://hackmd.io/@Knar/M3-Onboarding

## GitHub
There are probably better (decentralized) options but I'm using Github for now.
https://github.com/KnarXR/M3-Onboarding

## Avatar
The first Avatar I'm creating is Golden Jaw, a gray skeleton with a jawbone made of gold. The basic ingredients for this Avatar are:
- Skull head (or gray skin + black face paint)
- Golden jawbone (or gold face paint + gold bottom grillz)
- Black Hood

Concept Art - Acrylic on Cotton
![](https://i.imgur.com/DKz4ljM.jpg)

These are some Google Image results for "Golden Jaw" that show some of the ways I can adapt the basic ingredients into future variations of the avatar:
![](https://i.imgur.com/y4GaDzu.jpg)

I created a version of Golden Jaw using VRoid Studio. It's a great tool, very simple to use! I exported two versions of the VRM: a full quality version with ~19,000 polygons, and an optimized version with smaller textures and just under 10,000 polygons. 
![](https://i.imgur.com/maT8PYg.png)

With my shiny new VRM avatar, I can test it out in Webaverse (https://app.webaverse.com) by dragging the VRM file into the world and interacting with the e key to equip it. 
![](https://i.imgur.com/0nwIglP.jpg)

ToDo:
- [ ] Tweak VRoid jaw/skil color, re-export

## Engine
I need to pick the right engine to host my world. My criteria:
- Web based
- Self hosted
- Multiplayer
- VRM Support
- Mobile friendly

These are some of my options:
- AFrame - Seems very simple to use
- Babylon.Js - Good if I want full control, self hosting. Not as strong XR/avatar support
- XREngine - Insane feature set and web based, but installing isn't very straight-forward
- Webaverse - Drag and dropping files into the world is magic, need to dig into self-hosting
- Janusweb (Janus VR) - Runs very well, need to dig into self-hosting
- Neos VR - Pushes my gpu to the limit.
- VRChat - I only tried the steam desktop mode with a free account...They didn't let me register for an account with the Protonmail address.

I'm going with Aframe because of how simple it is to get a scene up and running. I don't want to waste much time coding, I just need a single player home world for now. 

## 3D Scanning
I don't have a compatible GPU for Meshroom so I tried an Android app called 3D Live Scanner by https://lvonasek.github.io/. The room scanning worked pretty well but the small object failed to connect to the cloud. I didn't want to pay $29.99 to try the Pro version of the app, so I tried another app called Qlone. This one requires a printed QR looking mat to scan, so it's perfect for the small objects I'm scanning. I wanted to 3D scan some big boulders but I scanned some small stones I found outside instead. 

When I first scanned the rocks, I moved around the table and I had the TV on, so the textures are pretty messed up:
![](https://i.imgur.com/Yca2BVz.jpg)
![](https://i.imgur.com/aZN6lij.png)

The free-tier scans were impressive enough to throw some support at the developer and export models so I bought the Premium version and re-scanned the rocks in "high-def" mode. I kept the camera stationary and rotated the mat, they came out a lot better this way. These are the final scans vs the real rocks:
![](https://i.imgur.com/xaj1ARC.png)
![](https://i.imgur.com/9uPN8uG.png)

Rock 1 in blender
Cleaning up loose geometry
![](https://i.imgur.com/RQ7wZIh.png)
![](https://i.imgur.com/84K5DSf.jpg)

Before/after decimating - Decimating exposes any holes/loose geometry
![](https://i.imgur.com/dYRBr1H.png)

When I exported my cleaned up rock as gltf + bin + texture, it was already a jpeg. I opened it in GIMP and further compressed it from 276kb down to 76kb. I re-imported the gltf into Blender and exported as a glb. 


## World
I really like the idea of each avatar having a home world that matches their aesthetic/personality. No matter where you go in the metaverse your avatar will have a place where they belong. 

Golden Jaw's home world is the desolate island Cairn:
> Cairn is dominated by arid, viciously sun-scorched plains strewn with shattered and twisted rock formations. The plains are tortured by winds that blast mercilessly across the flats, howling around the jagged stands of rock. Tornados and dust devils spawn in the scrublands, and wild, rainless electrical storms dance across the blasted plains.

Inspiration:
![](https://i.imgur.com/qS9svJN.jpg)

During development I will be hosting the world on Github pages
https://knarxr.github.io/

I'm following this tutorial to get started with A-Frame
https://aframe.io/docs/1.2.0/guides/building-a-basic-scene.html

I did all of my image editing using GIMP, it could be cleaned up but it's fine for now. For the skybox I took shots of the sky, padded the top/bottom edges with a solid color, and edited the left and right edges into a continuous image. I made a tiling texture for the ground and applied it to a flat plane object to serve as a placeholder terrain. An orb ties it all together. After I 3D scan some stuff I'll come back and create a proper sculpted terrain, add water, and put Golden Jaw in his home.
![](https://i.imgur.com/WORYaat.jpg)

I tried using a free mountain landscape terrain from cgtrader for the island which worked pretty well: https://www.cgtrader.com/free-3d-models/exterior/landscape/low-poly-realistic-mountain 

I'd rather make my own terrain though, so I sculpted a grid mesh (32x32) until it vaguely resembled an island. I added a texture to the grid and played around with the shading settings until it looked OK in A-Frame:
![](https://i.imgur.com/Tk3Vsxc.png)
![](https://i.imgur.com/7TgJrVU.jpg)

I took a free rigged skeleton model from CGTrader (https://www.cgtrader.com/free-3d-models/character/fantasy/skull-18fbb65b-38cd-445c-9929-5e39669ae61e), posed it, and painted the jaw gold. I had to edit the UV because Blender unwrapped it in a weird way where lots of bones overlapped. When I painted part of the jaw, many other parts of the skeleton would be painted as well. I selected every part of the body except for the head and moved them to one side of the texture, and sloppily painted the gold areas gold. I exported as GLTF and arranged it into the scene. 

![](https://i.imgur.com/uPm4Xe2.jpg)


I downloaded this free sack model (https://www.cgtrader.com/items/2555762/download-page), replaced the texture and exported as GLTF.
![](https://i.imgur.com/hGKpW54.jpg)

Except for the rocks, the island is done:
![](https://i.imgur.com/iakBFuS.jpg)
