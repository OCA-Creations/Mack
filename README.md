# Mack: Supercharge Swift and SwiftUI

<!--[![Swift](https://img.shields.io/badge/Swift-5.5-orange.svg)](https://swift.org)!-->
[![Swift](https://img.shields.io/badge/Swift-5.5-orange.svg)](https://swift.org)
[![SwiftPM Compatible](https://img.shields.io/badge/SwiftPM-Compatible-brightgreen.svg)](https://swift.org/package-manager/)
[![Platform](https://img.shields.io/badge/platform-macOS%2013%2B-blue)](https://developer.apple.com/macos)
[![GitHub tag](https://img.shields.io/github/tag/OCA-Creations/Mack?include_prereleases=&sort=semver&color=blue)](https://github.com/OCA-Creations/Mack/releases/)
[![License](https://img.shields.io/badge/License-MIT-blue)](#license)
[![issues - Mack](https://img.shields.io/github/issues/OCA-Creations/Mack)](https://github.com/OCA-Creations/Mack/issues)

SwiftUI has more functionality and ease-of-use features on iOS than macOS. `SwiftUI + Mack`, on the other hand, makes development more convenient, has built-in workarounds for common issues, and makes interface development quicker and more intuitive. Instead of creating new APIs or capabilities themselves, Mack makes it easier to interact with the tools you aready have. Whether it's making it easier to detect right clicks on a view or simple `String` convenience methods, Mack streamlines Swift and SwiftUI every step of the way.

# ⚠️⚠️ Mack is in **Active Development** ⚠️⚠️
Mack is currently being developed by OCA Creations LLC and the open source community, and is **not yet ready for use of any kind**. Contributors are welcome - see [Contributing](#contributing) for more information. For now, check out the Feature Roadmap, or contribute:

<a href="https://github.com/OCA-Creations/Mack/blob/main/Planning/PlannedFeatures.md"> <img src="https://img.shields.io/badge/Features-rrr?style=for-the-badge" height=50 /> </a>
<a href="https://github.com/OCA-Creations/Mack/README.md#contributing"> <img src="https://img.shields.io/badge/Contribute-000?style=for-the-badge" height=50 /> </a>


## Table of contents:

- [What is Mack?](#what)
- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Documentation](#documentation)
- [Contributing](#contributing)
- [License](#license)

## What
Mack is not a new way to write code. In fact, it aims to be the exact opposite - the functionality that Mack provides should directly augment the code that you write, and seem as natural as any functionality from SwiftUI. The main idea behind the library is to impliment lower-level solutions that are commonly used or workarounds that are currently necessary. For example, SwiftUI does not currently have a way to detect a right click on a `View`. Following Apple paradigms as closely as possible, the `.onRightClick` modifier provides the same structure as a native modifier, `.onTapGesture`, but adds a feature. 
### The Ultimate Goal
"Import and forget": *Developers shouldn't even realize they are using features provided by Mack*. Functionality should feel so *right*, so *native*, that they can type code that Mack provides like it is part of the standard libraries. This is a long way off, but in the end, a developer should be able to use Mack easily and naturally.

## Features

- **Easy to use**: Mack's natural syntax and comprehensive documentation make it a breeze to pick up and integrate into your project.
- **Ultramodern**: Adding Mack to your project doesn't change any functionality. Mack only provides features that simplify development, but never replaces existing functionality.
- **Commonly Used Types**: Created with fluidity in mind, Mack solves commonly encountered problems without you having to impliment a workaround. Everything included could (hopefully) be a part of the standard library, and Mack's types are ↩️
- **Natively Written**: Mack follows Apple stylization guidelines, naming conventions, and documentation methods as closely as possible. Every Mack type should feel like something from out-of-the-box SwiftUI.
- **Ultramodern**: Mack uses the latest interface technology and Swift versions (though it supports older versions as well), and intregrates directly with your current code. Import Mack and that's it - use all functionality as though it was there already.
- **Customizability**: Modify Mack components to meet your own requirements, or propose new functionality to the library to solve your solutions. All of Mack aims to be as customizeable as possible.

## Requirements

- macOS 13.0+
- iOS/iPadOS Support not yet available, still a WIP with many features not at all available
- Swift 5.5+ (not tested below 5.8)
- Xcode 14.0+

## Installation

Mack is available through CocoaPods, Carthage, and the Swift Package Manager (SPM). Choose your preferred dependency manager, and follow the instructions below:

### CocoaPods - NOT YET AVAILABLE!

To integrate Mack into your Xcode project using CocoaPods, add the following line to your `Podfile`:

```ruby
pod 'Mack'
```

Then, run `pod install`.

### Carthage - NOT YET AVAILABLE!

To integrate Mack into your Xcode project using Carthage, add the following line to your `Cartfile`:

```ogdl
github "your_username_here/Mack"
```

Then, run `carthage update` and follow the [Carthage integration guide](https://github.com/Carthage/Carthage#adding-frameworks-to-an-application) to link the built framework to your project.

### Swift Package Manager

To integrate Mack into your Xcode project using the Swift Package Manager, add the following to your `Package.swift` file:

```swift
dependencies: [
  .package(url: "https://github.com/OCA-Creations/Mack.git", .upToNextMajor(from: "1.0.0"))
]
```

## Usage

To get started with Mack, simply import it into your project:

```swift
import Mack
```

As aformentioned, Mack's goal is to "import and forget". Functionality intregrates seemlessely with standard code (please note that not all functionality below is implimented completely):

```swift
import Mack

struct LoginView: View {
  @SecurePersisted("email") private var email = ""
  //Ensure this value is saved in secure storage, so it will not be blank next time
  @SecurePersisted("password") private var password = ""

  var body: some View {
    VStack {
      Header("Welcome Back")

      TextField("Email", text: $email)
        .placeholderColor(.blue)

      SecureField("Password", text: $password)
        .style(.passwordLight)

      Spacer()

      Image("ClickMe")
      .onRightClick {
        print("You have right-clicked this item.")
      }
      Text("This text will not allow screenshots.")
      .allowsScreenshots(false)
    }
    .padding()
  }

  func loginUser() -> Bool {
    // A simple password comparison
    let correctPassword = SecureStorage.getByID("correct_password")
    let storedEmail = Secure
  }
}
```

For more examples and usage instructions, please refer to the [full documentation](ocacreations.github.io/mack).

## Documentation

Mack's comprehensive [documentation](ocacreations.github.io/mack) covers everything you need to know, including component guides, styling instructions, and advanced topics.

## Contributing

Thank you for your interest in contributing to Mack! In order to get set up for development, follow these steps:
1. Ensure you have the proper software for development: while some Mack features support older OS versions, to develop Mack, you must have macOS 13+ and Xcode 14+ installed. Mack is developed at OCA Creations LLC with Xcode 15 and macOS 13.4.
2. Fork this repository
3. Clone this repo on your local machine: `git clone https://github.com/YOUR_USERNAME/Mack.git && cd Mack`
4. Open the Mack folder in Xcode. You can open it with Finder or: `open . -a Xcode`

If you have any questions or suggestions, feel free to [open an issue](https://github.com/OCA-Creations/Mack/issues/new).

## License

Mack is released under the [MIT License](/LICENSE) by [`@OCA-Creations` LLC](https://github.com/OCA-Creations).
