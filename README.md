# NightClock
A relaxing clock app for Nintendo 3ds called NightClock.

## Experimental closed-lid alarm

This feature is not yet verified on physical hardware. Do not rely on it as your only alarm.
When an alarm is enabled, NightClock prevents system sleep while the app remains in the foreground. This is not true standby and consumes more battery; keep the console charged. Normal sleep is allowed again when the alarm is disabled or stopped. The timer does not prevent sleep.

To test on a 3DS:
1. Set the system clock and volume, remove any headphones, and leave NightClock running in the foreground.
2. Set an alarm a few minutes ahead and close the lid before it is due.
3. Listen for the alarm through the closed lid, then keep it closed until at least two minutes after the alarm time. Open the lid and check whether the alarm popup is already active.
4. Repeat with headphones and note the console model, whether sound played with the lid closed, and whether the alarm popup appeared after opening.
5. Disable the alarm and check that closing the lid allows normal sleep.

Speaker output, continued rendering and audio initialization have not yet been verified for this use. The alarm will not run after the app is closed, while it is suspended in the HOME menu, or while the console is powered off.

On a New 2DS XL, the earlier test build `f2e5b00` produced no speaker sound with the lid closed and rang immediately after opening. The later build removes display synchronization while an alarm is active; its closed-lid behavior still needs hardware testing.

Hello, my name is Michele, let me introduce my first app for Nintendo 3ds (all models).
It has been in development by me since June 5th 2026 and tested on Citra and on my own Nintendo 3ds XL.
I love to keep my New 3ds XL switched on while I work at my desktop or while I watch tv so had the Idea to create a relaxing clock app full of features.
FEATURES:
- the night stars sky is randomly generated every time you open the app and the stars blink
- The sleeping moon gently glows
- the clouds are randomly generated on a 7-layer system
- the planes spawn randomly
- the shooting stars spawn randomly
- The clock (and date) is synced with the internal clock of the 3ds, to sync the clock with the Internet time please use rosalina: (Open the Rosalina menu by pressing L + Down on the D-Pad + Select.Select Miscellaneous options.Choose Update date and time via NTP, quit Rosalina)
- SELECT key cycle between time+date, only time, blank
- D-pad left and right cycle between three Hour and Date sizes
- START key will gently close the app
- Every shooting star, plane and cloud is recorded on the Records menu (you can reset the counter)
- By the Settings Menu you can change time/date colour, sky theme, clock format, date format
- On every hour change a "special event" will occur on screen...
- Lower Screen can be switched off to preserve screen and save battery
- The Rainbow Dream colour mode for clock and date helps preserve the screen from static images ghosting
- more features to come...
- please send feedbacks to my mail : michelep3ds@gmail.com
- thanks

Ver 1.02 
-added ISO date format

Ver 1.03
-added an alarm clock and a time
-fixed save data to save settings only on app quit (Start button) to prevent lags in app usage.
