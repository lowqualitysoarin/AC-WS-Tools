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

Then go to the "PravusFrame" folder and drag the "PravusFramework_Base" prefab in your weapon.

<br    />

**Heads Up!!!**

() Do not rename the base prefab. Or else Pravus Framework won't be able to recognise if it has support.

() Try not to put the base prefab outside the weapon's prefab. It won't work.

() Not recommended putting the base prefab inside the weapon model's prefab. Issues may occur.


<br    />

###### [] Step Three: Configuration (Finishing Touches)

Click on the base prefab. And you should see two missing spaces there.

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

**What is this**

() This is a setting if the firearm is suppressed by default. Like if its a AS VAL or something you might want to leave this checked.

<br    />

###### [] Other Important Things To Edit

By Expanding the "weaponattachments" prefab. You'll see a few prefabs with dropdowns. Which you'll need to setup as well.



