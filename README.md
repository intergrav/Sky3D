# Sky3D
Roblox module for creating custom 3D skies.

Highly inspired by [Skybox3D](https://devforum.roblox.com/t/a-free-dynamic-3d-skybox-module/789302), I have gotten confirmation to upload mine though. Check his out too!

If someone can, please help me with uploading source code to the repo. I know how to do releases but not source code ;-; (I just want to get PRs working with the code)

# How to use
### Note, you must have basic knowledge in modulescripts and scripting in general.
Sorry if this documentation is bad, I wrote it in about 20 minutes since I need to do school stuff. You can make a PR if you want to improve this though.
## Installation
To use this, you must install the module first by downloading it from the [releases](https://github.com/devinkid1/Sky3D/releases).
After you do that, put it somewhere in ReplicatedStorage.

## Creating a sky
Make a small model of what your sky will be like (it is recommended to make it small for performance reasons, but you CAN make it normal sized).

Make sure it is at the camera origin you want to set.

![image](https://user-images.githubusercontent.com/42325132/116599975-c24a4300-a8f6-11eb-8ca3-83eaaaa4773d.png)

You are done with this part!

## Scripting a sky
To make the sky actually visible, we must script it.

Make a localscript somewhere where a player can access, like StarterPlayerScripts, StarterGui, etc. 

Put your created model inside of the script, and call it something. I usually do "environment" if there is only going to be 1 sky.

Require the module, like this:
```lua
local Sky3D = require(game:GetService("ReplicatedStorage").Sky3D)
```

After that, we need to create a sky. Like this:
```lua
local sky = Sky3D.new()
```

Now we need to move your created sky into the viewport, so we do it like this: (replace modelname with your sky model's name.)
```lua
script.modelname.Parent = sky.ViewportFrame
```

Now we need to activate the sky.
```lua
sky.Active = true
```

You can see it works, but it might look a bit odd. This is because (if you made it small) we need to make the WorldScale smaller.
![image](https://user-images.githubusercontent.com/42325132/116601873-faeb1c00-a8f8-11eb-97c6-79b38790e909.png)

To do this, it is like setting a property. Just type something like this:
```lua
sky.WorldScale = 0.1 -- Smaller value = bigger sky.
```

There are many other properties of a sky, which will be listed in the properties section.

# Properties
