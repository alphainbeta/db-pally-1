# Development Cooperation

Technical discussion about the data processing logic (likely in a manufacturing control system), where the issue lies in the incorrect evaluation of a part's position and its processing status.
It aims on debugging of product, solution design and cooperation in technical team that involves PLC, Process Engineering and Data Layer.
<br>

<img width="900" height="300" alt="1" src="https://github.com/user-attachments/assets/a9a19e86-6dd3-4a62-8043-f3a2af59ad6c" />

<br>
<br>

## Summary of the Main Issue
- A part was physically processed on spindle 2, but the system incorrectly evaluates it as processed on spindle 1 when input value 1 is entered.
- The system logic compares the current position of the part with the options from the configuration, which leads to incorrect results because it contains all possible combinations (e.g., 1 and 2), so the condition is always met.
- Process overview suggests that the comparison should not be made against the options in configuration, but rather against the actual record of where the part was processed.

## Key Suggestions and Insights
- The “green logic” (comparison with actual processing records) is correct and should be used as the foundation.
- Configurability at original model is unnecessary in this case, as it always returns a match due to its universal options.
- It is important not to affect the existing logic, which works correctly for other scenarios.

## Team Relation

Collegial and technical. Work together to debug or redesign system logic, likely as part of a shared responsibility for system integrity or automation.

## Session

Demonstration is available as .mp3 audio file, able to directly stream at <b>SoundCloud</b> platform.
It's best example based on raw experience how's important that things needs to click together.

https://on.soundcloud.com/0tgRhlAtM95si8yv5K

