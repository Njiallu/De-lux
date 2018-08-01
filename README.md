<h1 align=center>De-Lux project</h1>

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

- Wm
- Dock / taskbar / status bar
- Notification daemon
- Configurator
- Screen locker
- Session manager

----

## Window manager

### 2 Modes:
  #### 1. Floating
  #### 2. Tiled
  * Dynamic grid based tiling.  
     There is a dynamic grid that parts of it are asigned to certains windows to display.  
     There could be manual tiling or auto tiling on the windows.  
     One of the modes could be a fullscreen tiling and the other a minimal size tiling.  
	
