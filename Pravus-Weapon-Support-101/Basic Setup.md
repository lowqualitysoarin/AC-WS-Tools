# Welcome to the Modding 101 of Pravus Framework

## A Text guide that should get you set up with your first Pravus Framework supported firearm.
<br    />

###### [] Step One: Installation

Download the Pravus Framework modding tools via "github page".

Just click on the file and click "Download" or open the "Raw File".

###### Unity Setup

Open up your Unity Project and then find the Pravus Framework tools in your directory and open it.

Just hit "Import" and you are all set.


<br     />

###### [] Step Two: Basic Setup

Find the "Pravus Framework Tools" Folder

<br     />


Then go to the "PravusFrame" folder and drag the "PravusFramework_Base" prefab in your weapon.

<br    />

![baseprefab](https://github.com/lowqualitysoarin/Pravus-Framework-Tools/blob/main/Pravus-Weapon-Support-101/Guide-Images/baseprefab.png?raw=true)

**Heads Up!!!**

() Do not rename the base prefab. Or else Pravus Framework won't be able to recognise if it has support.

() Try not to put the base prefab outside the weapon's prefab. It won't work.

() Not recommended putting the base prefab inside the weapon model's prefab. Issues may occur.


<br    />

###### [] Step Three: Configuration (Finishing Touches)

Click on the base prefab. And you should see two missing spaces there.

<br     />

![spaces](https://github.com/lowqualitysoarin/Pravus-Framework-Tools/blob/main/Pravus-Weapon-Support-101/Guide-Images/audioclip.png?raw=true)

<br    />

![spaces](https://github.com/lowqualitysoarin/Pravus-Framework-Tools/blob/main/Pravus-Weapon-Support-101/Guide-Images/muzzleflash.png?raw=true)

Which is the "unSilFireSoundEffect" and "unSilMuzzleFlash"

<br    />

**What Are These?**

() These are the defaults. If you are going to use suppressors, and muzzle brakes in your firearm.
> Since those attachments will modify your gun's "Muzzle Flash" and "Fire Sounds".

<br   />

Put your default fire audio clip and default muzzle flash game object in the respective containers.
And you are done in this part.

<br     />

###### [] Weapon Settings

When expanding the prefab you'll see another game object called "Weapon Settings".
Though at the moment it only includes a single setting. Which is "pravcSuppressedByDefault"

<br    />

![spaces](https://github.com/lowqualitysoarin/Pravus-Framework-Tools/blob/main/Pravus-Weapon-Support-101/Guide-Images/suppressedbydefault.png?raw=true)

**What is this**

() This is a setting if the firearm is suppressed by default. Like if its a AS VAL or something you might want to leave this checked.

<br    />

###### [] Other Important Things To Edit

By Expanding the "weaponattachments" prefab. You'll see a few prefabs with dropdowns. Which you'll need to setup as well.

By going to the "barrelattachments" prefab then expanding it. You''l see a prefab named "defaultrecoilvalues".
> This is important because these helps to reset your recoil if you unequip a muzzle brake.

<br    />

![spaces](https://github.com/lowqualitysoarin/Pravus-Framework-Tools/blob/main/Pravus-Weapon-Support-101/Guide-Images/defaultrecoilvalues.png?raw=true)

<br      />

To set them up. There is a text file that shows what will you put in those values. Just search up in your unity search "How to set up muzzle brake." Or something like that and it should lead you to that text file.

<br      />

**Inside the text file.**

```
Be sure you've set up the default recoil values

If you don't this is how you set it up...


defaultrecoilval1 = Base Kickback
defaultrecoilval2 = Kickback Prone Multiplier
defaultrecoilval3 = Random Kickback
defaultrecoilval4 = Snap Duration
defaultrecoilval5 = Snap Frequency
defaultrecoilval6 = Snap Magnitude
defaultrecoilval7 = Snap Prone Multiplier


To set it up for the muzzle brake.. Its the same thing! As how you set up the
default values.. But this time is the recoil reduction values..
```


<br    />

After that's done. lets get to the next one.

<br    />

The next one is in the "opticsattachments" prefab.
Which is called "defaultaiminginteger".

<br    />

![spaces](https://github.com/lowqualitysoarin/Pravus-Framework-Tools/blob/main/Pravus-Weapon-Support-101/Guide-Images/defaultaimingint.png?raw=true)

<br    />

This one is easy. We'll get to animator integers later.. That means, leave it to zero.

<br    />

And next is the "defaultskin", which is inside the "skins" prefab.

<br    />

![spaces](https://github.com/lowqualitysoarin/Pravus-Framework-Tools/blob/main/Pravus-Weapon-Support-101/Guide-Images/defaultskin.png?raw=true)

Just put your magazine's prefab in the "gunrenderermagazine" game object container. And you are set.
But if you are planning to add skins in your gun.

<br     />

Make a array. (Like add more game objects inside the game object data container).

For Example.
```
gunrenderer1 = body
gunrenderer2 = mag
gunrenderer3 = slide
gunrenderer4 - infinity = blah blah how many default seperate object is in your gun.
```

**Why This?**

These are needed soo you put your gun's default skin again. And won't overlap with another skin you put.

<br    />

When you are finished. Now go to the "ammotypes" prefab.

<br    />

![spaces](https://github.com/lowqualitysoarin/Pravus-Framework-Tools/blob/main/Pravus-Weapon-Support-101/Guide-Images/defaultammotype.png?raw=true)

In this one is really simple. Just put your gun's default projectile prefab in "ammotype0" container.
> Again this is the default just incase you swap weapons or change ammotypes.

<br    />

Next.. Is the "defaultmagazineproperties". Which is inside the "magtypes" prefab.

<br    />

![magprop](https://github.com/lowqualitysoarin/Pravus-Framework-Tools/blob/main/Pravus-Weapon-Support-101/Guide-Images/defaultmagazineproperties.png?raw=true)

Just simply put your default magazine capacity in the float, and you are done.
> Example: M16A4 with a regular stanag mag = 30.

And as for the "defaultreloadint". We'll get to that later.. Leave it zero.

<br    />

Next up. The "defaultfiremodeproperties" inside the "firearmmechanisms" prefab.

<br     />

![spaces](https://github.com/lowqualitysoarin/Pravus-Framework-Tools/blob/main/Pravus-Weapon-Support-101/Guide-Images/firemodeproperties1.png?raw=true)

<br     />

![spaces](https://github.com/lowqualitysoarin/Pravus-Framework-Tools/blob/main/Pravus-Weapon-Support-101/Guide-Images/firemodeproperties2.png?raw=true)

In this part, You'll have to put your firearm's default cooldown, does it have heat?, is it auto, default fire sound, etc...

**Description Of The Containers**

```
pravcDefaultIsAuto = Check if your firearm is automatic.
pravcDefaultHasHeat = Check if your firearm can overheat (Useful if the gun is burst fire.)

defaultfiremodeanimint = We'll get to this later.. Again..

pravcDefaultCooldown = Your weapon's cooldown value.
pravcDefaultHeatGainPerShot = Your weapon's heat gain value. (Only works if your weapon has heat.)
pravcDefaultHeatDrainRate = Your weapon's drain rate value. (Only works if your weapon has heat.)

defaultfiremodesound = Your weapon's default firing sound.
```

<br     />

Last but not the least.. The "weapondesc" inside the "Weapon Info" prefab.

![spaces](https://github.com/lowqualitysoarin/Pravus-Framework-Tools/blob/main/Pravus-Weapon-Support-101/Guide-Images/weaponinfo.png?raw=true)

Simply just follow what it says. 


# And you are done!

You've finish the basic setup of your Pravus Framework supported firearm. Export the weapon with the Pravus Framework Mutator enabled and try it out.

<br     />

**Other stuffs**

You can open up your console by hitting "PageUP".

This will help you if you missed something or missing some dependecies.
Since Pravus Framework spits custom errors if there are some!

<br       />

##### [] Pravus Framework Syntax

Green = Indicates if Pravus Framework found a addon for it or a good firearm status.

<br   />

Yellow = Indicates if Pravus Framework found something missing that is optional or a Heads Up changes. (Just a light warning.)

<br   />

Red = Indicates if Pravus Framework found something missing that is important. (Heavy Warning.)


<br   />

There is also a Example Weapon Prefab that shows examples on how to add suppressors and adding skins in your.
Yep the example weapon is not finished. But gonna add new examples for it soon!









