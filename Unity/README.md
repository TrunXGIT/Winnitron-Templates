Winnitron Unity Template
=============================

A bunch of preconfigured input settings and scripts for your Winnitron Unity projects.

This also disables Unity's startup display resolution dialog. (Found at  `Edit > Project Settings > Player > Inspector > Standalone Player Options`)


## Inputs

Mapped Inputs can be found by going to **Edit -> Project Settings -> Input**.  All 4 directions and 2 buttons for each player have been mapped according to the [Winnitron Requirements](https://github.com/winnitron/WinnitronLauncher/wiki/Requirements-for-Winnitron-Games).  In your game, you should use the GetButton methods and reference the name of the button.

```csharp
// Returns true during the frame the user pressed down the virtual button identified by buttonName.
Input.GetButtonDown("P1_Button1");

// Returns true while the virtual button identified by buttonName is held down.
Input.GetButton("P1_Button1");

// Returns true the first frame the user releases the virtual button identified by buttonName.
Input.GetButtonUp("P3_Button1");
```
## Install InputManager

In the *ProjectSettings* directory exists the **InputManager.asset** which can replace any existing InputManager.asset in your project.  It's a good idea to branch your code before overriding the InputManager.asset since the input mappings are not intuitive and can affect local testing of your game.

## Test Scene

In the project exists a Main.scene which can be used to test inputs on the actual arcade box.  In the scene are two lights next to each possible input for each player.  The light on the left will turn yellow while the input is in the ON state and then turn off when there is no input.  The light on the right will turn from red to green the first time the input for that button is detected.

## Credits

This template is based on https://github.com/DSOP/Arcade-Unity-Input-Controller. All code and assets are used with permission.
