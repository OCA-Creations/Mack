# Mack - Features
This document outlines all features, in any state of completion, for the `Mack` library. Any features that you do not see here may not have yet been considered - if you have an idea for a feature, please open an Issue to discuss it. See Feature Notes for a specific feature
# Features
## Legend
- `🕰️` - Planned
    - This means that the feature is planned for future versions of Mack, but has not yet been implimented in any way. This library is currently unstable and in early preview, so many features will have this symbol.
- `🚧` - In Progress
    - This means that this feature is currently in development, and is not yet fully implimented. This is different from the `⚠️` symbol.
- `⚠️` - Unstable
    - This means that a feature has been implimented, but is not currently guarenteed to be usable or stable. This may be because core functionality has been implimented in an unreliable way or some other reason, but any features with this symbol are to be used with caution and are likely not ready for production usage.
- `🚨` - DANGER (do not use)
    - Features with this symbol are NOT READY for use of any kind, and will lead to unstable or dangerous behavior. There are numerous reasons a feature could be of this status, but unless their is a special note, these features are not to be used.
- `✅` - Complete
    - Features that are 'Complete' have been fully implimented and tested, and are ready for production use. NOTE: This does not mean that the full library is ready for production use, but merely signifies that this feature is ready and will not block eventual use in production.
    
## SwiftUI Features
- `.onRightClick` Modifier
    - Status: 🚧
    - Description: The `.onRightClick` modifier provides the ability to perform actions when a `View` is right-clicked by the user on macOS.
    - Platform Availability: macOS 13.0 or later
    - Further Notes Page: [`/SwiftUI/Feature_Notes/onRightClick.md`](https://github.com/OCA-Creations/Mack/Planning/SwiftUI/Feature_Notes/onRightClick.md)
- `.if` Modifier
    - Status: 🕰️
    - Description: In SwiftUI, there is often a need to apply a modifier conditionally. This satisfies that issue.
    - Platform Availability: iOS 13+, macOS 10.15+, iPadOS 13+
    - Further Notes Page: [`/SwiftUI/Feature_Notes/if.md`](https://github.com/OCA-Creations/Mack/Planning/SwiftUI/Feature_Notes/if.md)
### Dragging API
#### Mack makes it easier to add draggable functionality to `View`s, especially `Button`s.

## Swift (or sublibraries) Features
