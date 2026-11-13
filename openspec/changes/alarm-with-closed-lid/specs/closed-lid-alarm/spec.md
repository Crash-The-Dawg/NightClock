# Closed Lid Alarm

## Purpose

Allow NightClock to notify the user audibly when an enabled alarm becomes due while the console is closed.

## ADDED Requirements

### Requirement: Audible closed-lid alarm
When NightClock is running in the foreground with an enabled alarm, the system SHALL play the alarm through the built-in speakers when its configured time is reached, including while the lid is closed and no headphones are connected.

#### Scenario: Alarm becomes due with closed lid
- **GIVEN** an alarm is enabled and no headphones are connected
- **WHEN** the lid is closed before the configured alarm time and that time arrives
- **THEN** the built-in speakers repeatedly play the alarm until the user stops it

#### Scenario: Alarm stopped after opening the lid
- **GIVEN** the alarm is ringing after the lid was closed
- **WHEN** the user opens the lid and stops the alarm
- **THEN** playback stops and the alarm is disabled as in existing behavior

### Requirement: Sleep behavior
The application SHALL prefer a verified timed wake from system sleep. If that is not available, it MAY prevent sleep while the alarm is enabled, and SHALL document the resulting power consumption and foreground requirement.

#### Scenario: Alarm disabled
- **WHEN** no alarm is enabled and no alarm is ringing
- **THEN** NightClock allows the normal lid-closed sleep behavior

### Requirement: Audio failure is visible
The application SHALL inform the user when alarm audio cannot be initialized so a silent alarm is not presented as functional.

#### Scenario: Audio initialization fails
- **WHEN** the audio service or alarm buffer cannot be initialized
- **THEN** the user is visibly warned that the alarm cannot play

### Requirement: Hardware verification
Closed-lid speaker behavior SHALL be validated on a physical 3DS before the feature is described as reliable.

#### Scenario: Hardware verification is pending
- **WHEN** the closed-lid speaker test has not succeeded
- **THEN** documentation identifies the build as experimental and warns against relying on it as the sole alarm