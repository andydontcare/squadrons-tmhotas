# Star Wars Squadrons 
A ThrustMaster HOTAS Target Script

### What is this?
This is a TARGET script that blends roll and yaw to give your starfighter a similar handling to that of the old X-Wing/TIE Fighter games.

### Installation
Simply download the .tmc file and open it with the TARGET GUI. Click "run configuration" and open the .tmc file.

### Configuration

1. On the throttle, make sure **both** FUEL switches are on NORM (very important, see why below)
1. Start Squadrons, go to flight stick configuration in options and find roll/yaw.
1. Switch **both** FUEL switches to OVERRIDE, the throttle backlight will go out
1. Initiate axis binding for yaw right, move the stick right.
1. Initiate axis binding for yaw left, move the stick left.
1. Switch **both** FUEL switches to NORM.  Throttle backlight will come back on.
1. Initiate axis binding for roll right, move the stick right.
1. Initiate axis binding for roll left, move the stick left.
1. Bind any other axis (pitch, throttle, etc) or buttons you require.

### Configuration explanation/how this works

When binding an axis in Squadrons, you should only send one axis at a time.  The obvious problem is tilting the stick left and right will send both roll and yaw to squadrons.  So it is necessary to disable roll while binding the yaw axis.  When the FUEL switches are both switched to OVERRIDE, roll is disabled and the stick only manipulates the yaw axis.  This allows us to bind the yaw axis.

You may be asking: *but what about the yaw axis when binding the roll axis?*  It appears whichever axis has the greater value is the one that gets bound.  The script translates the roll value divided by 48 to the yaw axis, so the roll will always be greater and squadrons will pick the stick's X-axis over the yaw axis.


