# Tasks

## 1. Test Build

- [x] 1.1 Add a GitHub Actions workflow that builds 3DSX and CIA and verify both artifacts are uploaded by a successful run.
- [ ] 1.2 Prevent sleep while an alarm is enabled or ringing and verify normal sleep is allowed otherwise; build with GitHub Actions.
- [ ] 1.3 Document the experimental hardware test, power implications, foreground requirement and unverified speaker behavior; review the instructions against the test build.
- [ ] 1.4 Test on a physical 3DS with the lid closed, first without headphones and then with headphones, and record the results and device model.

## 2. Reliable Alarm

- [ ] 2.1 Investigate PTM timed wake, permissions and alarm ownership; document the evidence and whether a safe implementation is possible.
- [ ] 2.2 Implement a verified timed wake if available, otherwise retain the awake fallback; verify the chosen behavior on physical hardware.
- [ ] 2.3 Display an audio initialization failure to the user and verify the failure path does not present the alarm as functional.
- [ ] 2.4 Verify alarm repetition, stopping, normal sleep restoration and existing timer behavior on physical hardware; update the documentation with verified limits.