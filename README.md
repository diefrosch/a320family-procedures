# A320 Family -- Procedures
This is a draft of a Quick Start Guide for the A320-family aircraft for FlightGear

## Aircraft keys
### View keys

* `1`: Captain view
* `2`: First Officer view
* `3`: Overhead panel
* `4`: Forward pedestal
* `5`: Rear pedestal
* `6`: Center panel/Autopilot FCU

### Throttle
* `F`: Set TO/GA thrust
* `ctrl-F`: Set MCT/FLEX thrust
* `shift-F`: Set CLB thrust
* `E`: Set idle thrust
* `delete`: Set max reverse thrust

### Autopilot
* `shift-D`: Disconnect autopilot
* `ctrl-D`: Disconnect autothrust

### Other
* `B`: Cycle speedbrakes

## Basic procedures
### Cold and dark startup

* [overhead] BATT 1/2 ON
* [overhead] ADIRS 1-2-3 NAV [takes about 10 min. to align, you can proceed to next steps*]
* [overhead] APU master switch ON - APU start on [wait > 60” for APU to spool up]
* [overhead] APU bleed on
* [overhead] APU gen check on [= not illuminated]
* [overhead] ENG 1/2 LTK pumps on - CTR TK pump 1/2 on
* [pedestal] ENG mode START
* [pedestal] ENG 2 master switch ON
* [pedestal] when N1 stable > 18%: ENG 1 master switch ON
* [pedestal] when N1 stable > 18%: ENG mode NORMAL
* [overhead] GEN 1/2 check on
* [overhead] APU master switch OFF

*) Note: for the ADIRS to align the plane must be stationary. Do not start taxiing until alignment is complete.

### Before take-off

* Parking brake SET [shift-B]
* Auto-brakes MAX
* Gnd spoilers ARMED [click on the lever handle]
* Flaps T/O
* TCAS TA/RA [click 4 times on the knob]
* Cabin signs ON (Seat belts - No smoking)
* Landing lights ON

### Take-off

* Release parking brake [shift-B]
* Throttle TO/GA [F key]
* At Vr rotate and lift off
* Retract gear [G key]
* Maintain V2+10 with pitch
* Throttle CLB [shift-F]

### Climb

* Retract flaps
* Engage A/P
* Set climb speed [max 250 @ < 10000]
* [overhead] at > 4000ft Air cond. packs 1&2 ON (if not already ON)
* [overhead] Landing lights OFF

### Landing

* [overhead] Landing lights ON
* Flaps FULL
* Auto-brakes MIN or MED
* Gnd spoilers ARMED (click on the lever handle)
* Gear down (3 green)

## Autopilot basics
### Engaging/disengaging

* To engage the autopilot press either `AP1` or `AP2` button.
* The autothrust is engaged automatically at takeoff when you retard the throttle levers from `TO/GA` (takeoff thrust) to `CLB` (climb thrust). You can also engage/disengage it manually by pressing the `A/THR` button.

### Shortcuts:

* `Shift-D` to disengage the autopilot. (Shift-D again to silence A/P disconnect alarms.)
* `Control-D` to disengage the autothrust.

### Modes of operation

The Airbus autopilot has two modes of operation, *selected* and *managed*.

* In *selected mode* the autopilot is driven by values set in the FCU (Flight Control Unit, the autopilot control panel in the middle of the instrument panel).
* In *managed mode* the autopilot is driven by the flight computer.

Selected and managed modes can be set independently for speed, heading and altitude. Initially, all three parameters are set to selected mode.

* To engage managed mode, push (left click) the relevant knob. The display shows all dashes. [Except for altitude?]
* To return to selected mode, pull (middle click) the relevant knob. The set value reappears on the display.

NOTE: There is no managed mode for vertical speed. Clicking on the V/S knob will level off the plane.

### Altitude management

At the time of this writing [Dec. 2021] managed altitude is not yet fully implemented. To manage the altitude you can choose between Vertical Speed (`V/S`) mode and Open Climb/Open Descent (`OP CLB/OP DES`) mode.

**For `V/S` mode:**

* Dial the altitude using the knob. (Shift-mousewheel to go faster.)
* Push the altitude knob to go into Vertical Speed (V/S) mode.
* Set the desired vertical speed with the V/S knob. (Set a negative value if you want to descend.) The autopilot will climb/descend at the selected vertical speed until it reaches the set altitude.
* The A/P will try to maintain current speed by adjusting the thrust.

**For `OP CLB/OP DES` mode:**

* Dial the altitude using the knob.
* Pull the altitude knob to go into Open Climb/Open Descent mode.
* The autopilot will set climb/idle thrust and will climb/descend to the set altitude.
* The A/P will maintain current speed using pitch.

## Flight Management System
### Basic concepts

* Interaction with the FMS is via the screen and keyboard units located on the pedestal on either side of the throttle levers.
* These units are called the `MCDU`s (Multifunction Control and Display Units).
* The MCDU screen consists of 12 data fields (6 on the left and 6 on the right) and a bottom row called the scratchpad.
* On both sides of the screen are 6 buttons called the line select keys; they are numbered `L1` to `L6` on the left and `R1` to `R6` on the right.
* You enter data by typing it in the scratchpad and then pressing the line select key next to the data field into which you want to insert it.
* You clear a field (or restore it to its default value) by pressing the `CLR` key and then the line select key of the relevant data field.

### Example setup

We are going to set up the FMS for a short flight from Frankfurt (EDDF) to Paris Charles de Gaulle (LFPG).

#### Initial setup

* On the initial menu screen press `1L` to select `FMGC`
* Press the `INIT` key in the top row of the keyboard
* Type `EDDF/LFPG` and press `1R` (`FROM/TO`)
* Type a flight number of your choice and press `L3` (`FLT NBR`)
* Type `50` and press `L5` (`COST INDEX`)
* Type `270` and press `L6` (`CRZ FL/TEMP`)

#### Flight Plan

* Press the `FPLN` key to go to the flight plan page
* Type `LIMGO` and press the LSK to the left of `F-PLN DISCONTINUITY`; the discontinuity shifts down and `LIMGO` is inserted in between
* Repeat the previous step for waypoints `MEDOX` and `SUIPE`.
* Press the `CLR` key and press the `LSK` to the left of `F-PLN DISCONTINUITY` to clear it
* Press `R6` (`TMPY INSERT`) to insert your flight plan.

    To scroll the view use the UP and DOWN arrow keys (they move the view, so they do the opposite of what you think – use UP to go down and vice versa). [has this changed recently??]
    To delete what you write in the scratchpad use the CLR key.

#### Other Settings

* Press `PERF` to go to the performance settings page
* Set `138`, `142` and `146` as `V1`, `VR` and `V2` respectively.
* Set `5000` as `TRANS ALT`.
* Set the `FLAPS/THS` field to `3`.

Just prior to takeoff click on the airspeed and the heading knobs on the FCU (the autopilot control panel) to put them in managed mode. When airborne and stabilized in a climb, click on the `AP1` button – the autopilot will follow the route that you entered in the FMS.

Note – The above flight plan will bring you over the destination airport, it will not auto-land the plane. You will need to manage the approach and landing yourself.
