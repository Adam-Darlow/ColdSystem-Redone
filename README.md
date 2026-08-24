# Cold System - Redone

An adaptation and visual overhaul of the original **Cold System** mod for S.T.A.L.K.E.R. Anomaly / G.A.M.M.A.

This version was built and tested for **G.A.M.M.A. 0.9.5**. It should be relatively straightforward to patch for future G.A.M.M.A. updates if changes to the original Cold System or HUD files cause compatibility issues.

If you are using **DynaHUD**, please see the dedicated compatibility instructions below.

---

# What Does Cold System - Redone Change?

This version of Cold System focuses primarily on changing how the cold system is presented visually and how the player receives feedback from their cold level.

### Changes include:

- Tweaked the UI graphics.
- Removed the coloured icons for items such as food.
- Reworked the screen effects and their implementation.
- Replaced the original full-screen colour tint with a gradual screen-edge overlay.
- Added separate **Regular** and **Winter** versions of the overlay.
- Added an optional patch which allows the Cold System HUD to only appear when opening the player's inventory.

The biggest change is the cold screen effect.

Instead of gradually tinting the **entire screen** as the player's cold level increases, Cold System - Redone gradually builds an overlay texture around the **edges of the screen**.

This allows the effect to become increasingly noticeable without significantly affecting the overall brightness or colour of the game world.

It also makes it possible to hide the Cold System HUD completely and use the screen effect itself as the primary visual feedback for your cold level.

---

# Inventory HUD

I have also included an optional patch which allows the Cold System HUD to only appear when the player opens their inventory.

The overlay effect remains completely separate from the HUD and can be enabled or disabled independently.

This patch is an adaptation of **Cold System Inventory UI by Dedokpensioner**, with the script modified to work with Cold System - Redone.

With the patch installed, you can open your inventory to get a more detailed view of your current cold and fever levels, then close the inventory and rely entirely on the screen effect.

This allows for a more immersive, HUD-less experience without removing access to the Cold System information when you need it.

---

# Versions

Cold System - Redone is available in two versions:

### Regular

A blue-ish texture gradually builds up around the edges of the screen as your cold level increases.

### Winter

A frosted texture gradually builds up around the edges of the screen as your cold level increases.

The **Winter** version is intended to work particularly well with snowy/winter overhauls such as **INVERNO**.

The original Cold System effect tinted the entire screen which affected the brightness of the game. Both versions of Cold System - Redone aim to avoid this by changing only the edges of the screen and increasing in intensity/opacity as you get colder.

---

# Installation

> **REQUIRES G.A.M.M.A. Minimalist HUD to be enabled.**
>
> Minimalist HUD should be enabled by default in G.A.M.M.A.

Choose either the **Regular** or **Winter** version, download the ZIP and install it through **Mod Organizer 2 (MO2)**.

After installation:

1. Make sure **G.A.M.M.A. Minimalist HUD** is enabled.
2. Place **Cold System - Redone** at the **bottom of your load order**.
3. Launch the game and configure the Cold System settings through the MCM.

### Using both versions

If you play both regular and winter setups, you can install both versions through MO2 and enable only the version you currently want to use.

For example:

- **Regular** for a standard G.A.M.M.A. setup.
- **Winter** for a winter overhaul such as INVERNO.

> **Inventory Patch:** If you are using the Inventory HUD patch, load the patch **after Cold System - Redone**.

---

# Uninstalling

If you are currently in the middle of a playthrough, the safest way to uninstall Cold System - Redone is to completely remove your current cold and fever effects first.

Before uninstalling:

1. Lower your cold level to **0**.
2. Lower your fever level to **0** using the available medical treatments.
3. Save the game.
4. Exit the game completely.
5. Remove Cold System - Redone from MO2.

The effectiveness of medical items and the ways of lowering your cold and fever levels can be changed through the Cold System MCM.

---

# Installing for Future Versions of G.A.M.M.A.

Cold System - Redone was built and tested with G.A.M.M.A. 0.9.5. Future versions of G.A.M.M.A. may change the `ui_custom_msgs.xml` file used by G.A.M.M.A. Minimalist HUD.

If this happens, you can manually reapply the Cold System - Redone HUD changes.

Choose either the **Regular** or **Winter** version, download the ZIP, then install it through MO2.

Then:

1. Go into the **G.A.M.M.A. Minimalist HUD** mod and copy the file `ui_custom_msgs.xml`.

2. Paste it into `gamedata\configs\ui` inside the **Cold System - Redone** mod. This will overwrite the existing `ui_custom_msgs.xml`.

3. Open the newly pasted `ui_custom_msgs.xml` file.

4. Add the following code to the very top of the XML file, immediately underneath `<header>`:

```
<cold_overlay x="0" y="0" width="1024" height="768" stretch="1" complex_mode="1">
    <texture>ui\freezex\cold_overlay</texture>
</cold_overlay>
```

5. It should now look like this:
   
```
<header>

    <!-- Cold Overlay -->

	<cold_overlay x="0" y="0" width="1024" height="768" stretch="1" complex_mode="1">
		<texture>ui\freezex\cold_overlay</texture>
	</cold_overlay>

	<!-- Rest of the Hud -->
```

6. Save the file.

You are now finished. Make sure **Cold System - Redone** is at the bottom of your load order.

---

# Compatibility with DynaHud

DynaHUD may modify the `ui_custom_msgs.xml` file depending on your installation and configuration.

If you use DynaHUD, install and configure DynaHUD with your preferred settings first. Then follow the manual patch instructions below rather than allowing Cold System - Redone to overwrite your existing `ui_custom_msgs.xml`.

Instructions:

1. Locate your **DynaHud** mod.

2. Open it, navigate to: `gamedata\configs\ui\ui_custom_msgs.xml.`

3. Copy the file `ui_custom_msgs.xml`.

4. Paste it into: `gamedata\configs\ui` inside the **Cold System** - Redone mod. This will overwrite the existing `ui_custom_msgs.xml`.

5. Open the newly pasted `ui_custom_msgs.xml` file.

6. Add the following code to the very top of the XML file, immediately underneath `<header>`:

```
<cold_overlay x="0" y="0" width="1024" height="768" stretch="1" complex_mode="1">
    <texture>ui\freezex\cold_overlay</texture>
</cold_overlay>
```

7. It should now look like this:

```
<header>

    <!-- Cold Overlay -->

	<cold_overlay x="0" y="0" width="1024" height="768" stretch="1" complex_mode="1">
		<texture>ui\freezex\cold_overlay</texture>
	</cold_overlay>

	<!-- Rest of the Hud -->
```

8. Save the file.

# DynaHUD Cold System Compatibility

DynaHUD includes visibility settings for the Cold System UI in its MCM.

If you are using both **DynaHUD** and the **Cold System Inventory UI patch**, make sure to disable all Cold System features in the DynaHUD MCM menu.

Otherwise, the two mods may conflict and cause crashes.

---

# Original Mods Credits

All credit goes to the original mod makers for **Cold System**, **Frosted Winter Mask Overlay**, and **Cold System Inventory UI**.

I have adapted the existing scripts, created new scripts, changed how the UI is displayed, modified configuration files, and reconfigured/updated the overlay textures.


## Cold System

Original Cold System mod by **bvcx, arti and RavenAscendant**.

Mod link:

https://www.moddb.com/mods/stalker-anomaly/addons/cold-system-01


## Original Frosted Winter Mask Overlay (before I edited it)

Frosted Winter Mask Overlay mod by **wesmontomato**.

Mod link:

https://www.moddb.com/mods/stalker-anomaly/addons/fx


## Cold System Inventory UI

Cold System Inventory UI by **Dedokpensioner**.

**Do not download this mod for Cold System - Redone. Use the custom patch provided with Cold System - Redone instead.**

Mod link:

https://www.moddb.com/mods/stalker-anomaly/addons/cold-system-inventory-ui

Even though you should not use this mod alongside Cold System - Redone, I am still crediting Dedokpensioner for the original `cold_system_hud.script` supplied with their mod.

Without that script, I would not have been able to adapt the inventory-only HUD functionality for Cold System - Redone.

---

# Disclaimer

I am not an expert Lua developer. I used ChatGPT to help write and edit the Lua scripts for the purposes of this mod.

The other aspects of the mod, including the configuration edits, UI changes, and texture editing/reconfiguration, were done by me.
