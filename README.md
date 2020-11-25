## PCB Routing Speed Run Challenges
 How fast can you route a PCB in KiCad? 

## What is PCB Routing Speed Run
The PCB routing speed run is a self-moderated contest to see how fast you can route a PCB in KiCad.

The first circuit is a 555-timer board with multiple capacitor footprints. (Eventually, this could turn into a soldering challenge.)

## What are the rules?
1. No modifications to the `.kicad_pcb` or `kicad_pcb-bak` file until the timer starts.
2. The board must pass DRC. (DRC rules are already configured).
3. There must be 0 unrouted routes either: when the timer stops or after DRC runs.
4. For this challenge, no components or pads can be moved.

## How is time counted?
Time is counted from when the LiveSplit global hotkey is pressed until it is pressed again. 

To accommodate computers of various speeds, DRC can be run AFTER the timer has stopped. However, if the board does not pass or there are unconnected nets, the run is disqualified. 

## Running DRC
Zone fills are not required during the run. (Default files have zones hidden.) You may let DRC fill them. This approach means the "unrouted" indicator may be more than zero when the timer is stopped. However, if the board does not pass DRC or there are unconnected nets, the run is disqualified.

When running DRC, these boxes should be checked:
1. Refill all zones before performing DRC
2. Report all errors for tracks (slower)
3. Test tracks against filled copper areas (very slow)

## Why is there a `kicad_pcb-bak` file?
It is a duplicate of the `.kicad_pcb` file, so you can just use "Revert to last backup" before starting a new run.

## What version of KiCad do I need?
These files were created with KiCad 5.1.6.

Not sure if or how the KiCad version matters, but results should report the version as shown in the About box in PCBnew.

## How do I start?
Install KiCad. Download this repository and open the `.kicad_pcb` file. Ideally, you'll also want to get LiveSplit. LiveSplit is an on-screen timer used by speedrunners for a first-order time result and lets viewers see what is happening.

And then practice. :)


## How are results certified?
Configuration files for LiveSplit will be uploaded soon to match @baldengineer's setup. Like video game speedrunning, the final results need to come from a video recording. Until then, let's just do pull-requests and add your times to the file "results.csv." Please, submit an issue or PR if you have a better idea.


## Where do results go?
Create a pull-request with modifications to the "results.csv" file. Results without video proof will be not be merged.

## Do I have to live stream?
Ehhh, for now, no. But I do want to track results of live vs. not-live, at least for now.

## This content is poorly thought out and stupid.
Oops! Looks like you thought this one YouTube and not GitHub. 

---

Watch James do his routing speed runs on Twitch:
https://twitch.tv/baldengineer