# Design

## Context

The alarm time check and repeated NDSP playback run in NightClock's main loop. The reference player rejects sleep with `aptSetSleepAllowed(false)` and documents headphone playback, but does not prove speaker playback or scheduled wake.

## Goals / Non-Goals

**Goals:** Establish a reproducible 3DS hardware test, investigate timed wake, and retain normal sleep when no alarm needs the system awake.

**Non-Goals:** Waking a powered-off system, running after the app exits, or modifying the independent timer's behavior.

## Decisions

- First build a reversible sleep-prevention test using the existing alarm and NDSP audio. Test speakers with no headphones and headphones separately; the reference does not establish speaker behavior.
- Investigate PTM RTC alarm ownership, semantics, wake triggers and permissions before implementing timed wake. Do not write undocumented MCU registers or overwrite system alarms speculatively.
- Keep the app awake only for an enabled or ringing alarm in the experimental fallback. Restore normal sleep when no longer needed.
- Build 3DSX and CIA in GitHub Actions, since local compilation is unavailable. Use the existing feature branch and do not modify the default branch without approval.

## Risks / Trade-offs

- Speaker output or frame progress with the lid closed may differ from the reference player; require physical hardware verification.
- Preventing sleep consumes more battery; document the power cost and the need to leave the app in the foreground.
- An RTC alarm may be shared with system services or lack a usable wake path; reject undocumented or unsafe implementations.
- Failed NDSP initialization can produce a silent alarm; surface the failure to the user.