# Proposal

## Why

NightClock currently stops checking the alarm when the console enters sleep mode. A closed 3DS should be usable as an alarm clock with sound from its built-in speakers.

## What Changes

- Investigate scheduled wake from genuine sleep and validate it on physical hardware before relying on it.
- Provide a test build that keeps the system awake while an alarm is enabled if timed wake cannot yet be established.
- Build 3DSX and CIA artifacts with GitHub Actions and document the hardware results and limitations.

## Capabilities

### New Capabilities

- `closed-lid-alarm`: Alarm scheduling and audible notification while the console is closed.

### Modified Capabilities

None.

## Impact

The change affects the NightClock alarm lifecycle, its documentation, and the GitHub Actions build. Real hardware is required to validate lid behavior and speaker output.