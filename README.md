<h1 align=center>De-Lux project</h1>

---

## Goal

The De-Lux project's goal is to provide an easy, efficient and versatile desktop experience for users of the X server. The main focus at the moment is defining what De-Lux will be. But we already have some guidelines following the `a*ap` mantra:

- As light as possible.  
   Most of the code will be written is C to ensure memory efficiency and application performance.
- As configurable as possible.  
   Everything should be configurable by remote config and support common technologies like GTK+
- As modular as possible.  
   You should be able to take a bit of the De-Lux like the Wm and be able to use it on it's own or in conjunction of other things.
- As adaptable as possible.  
   It should be able to be used with either touchscreen, keyboard and mouse at a time.
- As Interchangeable as possible.  
   You should be able to change bits of the De without experiencing any major problems.

## Components

- [ ] Window manager
- [ ] Dock / taskbar / status bar
- [ ] Notification daemon
- [ ] Configurator / Centralized config panel
- [ ] Screen locker
- [ ] Session manager

----

## Window manager

### 2 Modes:
Any of those modes could be turned as a default by the user but system default will be floating.  
In that path the modes are set by group
#### 1. Floating
   There will be a floating mode in which you would be able move a window freely in the workspace. If you wish to put the window in another workspace, bindings, mouse interactions and touch interactions (that are likely to ressemble the mouse interactions by default) would permmit that. to be noted that a window floating outward of the worspace would not be fully rendered or even rendered at all.
   * Dynamic window size.  
      The size of a window could be changed in cunjunction with other actions.
   * Groups.
      There should be a grouping system based on relative spacial positioning and cardinal positions slaving.
#### 2. Tiled  
   There will be a tile grid and on which windows can be layed down.  
   This is still to be determined if you should be able to make L shaped assignations but whatever.
   It's not really needed but this sould be discussed as a core feature as it will define a great part of the code architecture.
  * Dynamic grid based tiling.  
     There is a dynamic grid that parts of it are asigned to certains windows to display.  
     There could be manual tiling or auto tiling on the windows.  
     One of the modes could be a fullscreen tiling and the other a minimal size tiling.
  * Groups.  
     There should be a grouping system based on relative tile positioning and cardinal positioned tiles window slaving.
  * Overlap.  
     Tiling overlap should be possible with the groups feature as long as this is not the same group.
	 
### Bindings:

This will discuss what should be considered as a binding and what those are bound to do.

* Bindings would be anything related to HMI peripherals:
   * Keyboard
   * Mouse
   * Screen
   * Touchscreen
   * Controller
   * etc...
   But we will only support the first 4s.
* Bindings would have combinations that will be atributed to actions that the window manager can do.  
   For example pressing the `q` key while swiping right with the touch pad would be closing a window.
* There could be any amount of binding for the same action.
* The same binding on different actions is totally acceptable.

## Screen locker / Session manager

The screen locker and session manager would idealy be the same. this concept is to be expanded.

## Screen locker  

The screen locker will have the option to be displayed only on selected monitor or primary or all at once.  
   Every module can be placed as your liking based of screen percent, pixels, dpi and points.

* #### Layout field

   * Keyboard layout field.
   * Point of access for virtual keyboard.
   * String and toggle keys can be changed as will: 'Caps lock' -> '', etc...

* #### Date | time field

   * Date and time can be displayed separatly or together.
   * The format of both can be changed as a string following stdio's format.

* #### Password field  
   The password field would have different ways of being displayed:

   * Standard password field with stars replacing the characters.
   * An i3-like circle that changes the color of an arc randomly at each keypress.
   * An i3-like shapes that changes the color of a part randomly at each keypress.
   * An i3-like bar that changes the color of a section randomly at each keypress.

* #### Power panel  
   The power panel would have 4 buttons, which can swaped in any position:

   * Sleep
   * Hibernate
   * Poweroff
   * Restart

* #### Wallpaper  

The wallpaper would have an option to select a different wallpaper from a list randomly or ordered.  
A Wallpaper can be an image of any format or video in the mp4 format.  
Of course the audio will be ignored.

