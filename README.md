# Cold System - Redone

An adaptation of the Cold System mod for Stalker. This was built to be used with GAMMA 0.9.5. It is relatively straightforward to patch for future updates to GAMMA though.

If you are using DynaHud, I have provided installation instructions below.

This version of the cold system tweaks the ui graphics, removes the coloured icons for items such as food and revamps the screen effects.

Instead of adding a tint to the entire screen as you cold meter increases, I wanted to have it so a texture slowly builds up.

This would also allow you to hide the UI of the cold system and use the on-screen effect as feedback.

I HIGHLY recommend pairing this with the mod Cold System Inventory UI by Dedokpensioner and can be found here: https://www.moddb.com/mods/stalker-anomaly/addons/cold-system-inventory-ui

With the above mod, you can glance at your cold level when opening the inventory for a more descriptive version of your cold and fever level then rely on your on screen effect for a full hud-less experience.

For a list of the rest of the features from Cold System, check out the original mod by bvcx: https://www.moddb.com/mods/stalker-anomaly/addons/cold-system-01

---

# Versions

Two versions: Regular and Winter

- Winter: The edges of the screen becomes a frosted texture that increases in opacity.
- Regular: A blue-ish texture builds up around the screen edges which increases in opacity.

The orignal version of the mod tinted your entire screen which affected your brightness. Both versions above aim to avoid this by changing only the edges of your screen and increase in intensity / opacity as you get colder. 

---

# Installation

*REQUIRES enabling G.A.M.M.A. Minimalist HUD (should be on by default in GAMMA)

Choose either the regular or winter version, download the zip then install through MO2.

Alternatively, download both, install with MO2 then enable one or the other if you play both regular versions or with winter overhauls like INVERNO.

Add to bottom of your load order.

---

# Installing for future versions of GAMMA

Choose either the regular or winter version, download the zip then install through MO2.

Then:

1. Go into the mod 'G.A.M.M.A. Minimalist HUD' and copy the file 'ui_custom_msgs.xml' and paste into gamedata\configs\ui in the Cold System - Redone mod. This will overwrite the current 'ui_custom_msgs.xml'.
2. Open the newly pasted 'ui_custom_msgs.xml' file.
3. Add the code below to the very top of the xml file, just underneath where it says 'header':
   
```
<cold_overlay x="0" y="0" width="1024" height="768" stretch="1" complex_mode="1">
    <texture>ui\freezex\cold_overlay</texture>
</cold_overlay>
```

4. It should now look like this:
   
```
<header>

    <!-- Cold Overlay -->

	<cold_overlay x="0" y="0" width="1024" height="768" stretch="1" complex_mode="1">
		<texture>ui\freezex\cold_overlay</texture>
	</cold_overlay>

	<!-- Rest of the Hud -->
```
6. Click save and you are done. Make sure Cold System - Redone is at the bottom of your load order.
---

# Compatibility with DynaHud

DynaHUD may modify the ui_custom_msgs.xml file depending on your installation / configuration. If you use DynaHUD, install DynaHud with your custom settings then follow the manual patch instructions below rather than allowing Cold System - Redone to overwrite your existing ui_custom_msgs.xml file.

Instructions:

1. Locate your DynaHud mod.
2. Open it, navigate to gamedata\configs\ui\ui_custom_msgs.xml.
3. Copy the file 'ui_custom_msgs.xml' and paste into gamedata\configs\ui in the Cold System - Redone mod. This will overwrite the current 'ui_custom_msgs.xml'.
4. Open the newly pasted 'ui_custom_msgs.xml' file.
5. Add the code below to the very top of the xml file, just underneath where it says 'header':
   
```
<cold_overlay x="0" y="0" width="1024" height="768" stretch="1" complex_mode="1">
    <texture>ui\freezex\cold_overlay</texture>
</cold_overlay>
```

6. It should now look like this:
   
```
<header>

    <!-- Cold Overlay -->

	<cold_overlay x="0" y="0" width="1024" height="768" stretch="1" complex_mode="1">
		<texture>ui\freezex\cold_overlay</texture>
	</cold_overlay>

	<!-- Rest of the Hud -->
```

7. Click save and you are done. Make sure Cold System - Redone is at the bottom of your load order.
   

If you use dynahud, which comes with visibility settings in it's MCM for the cold system ui, AND you are using Cold System Inventory UI, make sure to disable all the cold system features in Dynahud in MCM otherwise you will have crashes due to conflicts.

---

# Original Mods Credits

All credit goes to the original mod makers for Cold System and the Frosted Winter Mask Overlay mods. I simply tweaked the script, the UI, some configs and re-configured the overlay texture.

Original Cold System mod by bvcx, arti and RavenAscendant

Mod link: https://www.moddb.com/mods/stalker-anomaly/addons/cold-system-01

Frosted Winter Mask Overlay mod by wesmontomato

Mod link: https://www.moddb.com/mods/stalker-anomaly/addons/fx

# Disclaimer

I am not an expert coder in lua scripts. I used ChatGPT to help edit the scripts for the purposes of these mod tweaks. The other features such as config edits and textures where done by me and wesmontomato for the frost texture.

---
