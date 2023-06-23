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
Mack is currently being developed at OCA Creations LLC and the open source community, and is not yet ready for use of any kind. For now, check out the Feature Roadmap:

<a href="https://github.com/OCA-Creations/Mack/blob/main/Planning/PlannedFeatures.md"> <img src="https://img.shields.io/badge/Features-000?style=for-the-badge" height=50 /> </a>


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

## Features

- **Easy to use**: Mack's clean syntax and comprehensive documentation make it a breeze to pick up and integrate into your project.
- **Stylish by default**: With a handpicked selection of beautiful, customizable default styles, your app will look professional without spending hours on design.
- **Focused on performance**: Optimized for high performance and built on top of Apple's SwiftUI framework, Mack allows for seamless and fluid user interfaces.
- **Cross-platform**: Supports iOS, macOS, tvOS, and watchOS right out of the box. Write your app once and target multiple platforms effortlessly.
- **Composability**: Mack components play well with each other, making it easy to create modular building blocks for your app.
- **Customizability**: Modify Mack components to meet your design requirements, or create your own components with Mack's powerful styling and layout system.
- **Localization**: Built-in support for multiple languages enables truly global apps.
- **Accessibility**: Designed with accessibility in mind, Mack ensures your app can be used by everyone, including people with disabilities.

## Requirements

- iOS 13.0+ / macOS 10.15+ / tvOS 13.0+ / watchOS 6.0+
- Swift 5.0+
- Xcode 12.0+

## Installation

Mack is available through CocoaPods, Carthage, and the Swift Package Manager (SPM). Choose your preferred dependency manager, and follow the instructions below:

### CocoaPods

To integrate Mack into your Xcode project using CocoaPods, add the following line to your `Podfile`:

```ruby
pod 'Mack'
```

Then, run `pod install`.

### Carthage

To integrate Mack into your Xcode project using Carthage, add the following line to your `Cartfile`:

```ogdl
github "your_username_here/Mack"
```

Then, run `carthage update` and follow the [Carthage integration guide](https://github.com/Carthage/Carthage#adding-frameworks-to-an-application) to link the built framework to your project.

### Swift Package Manager

To integrate Mack into your Xcode project using the Swift Package Manager, add the following to your `Package.swift` file:

```swift
dependencies: [
  .package(url: "https://github.com/your_username_here/Mack.git", .upToNextMajor(from: "1.0.0"))
]
```

## Usage

To get started with Mack, simply import it into your project:

```swift
import Mack
```

Then, you can use Mack components to build your user interface. For example, here's how you can create a simple login screen:

```swift
import Mack

struct LoginView: View {
  @State private var email = ""
  @State private var password = ""

  var body: some View {
    VStack {
      Header("Welcome Back")

      TextField("Email", text: $email)
        .style(.textLight)

      TextField("Password", text: $password)
        .style(.passwordLight)

      Spacer()

      Button(action: loginUser) {
        Text("Login")
      }
      .style(.primary)
    }
    .padding()
  }

  func loginUser() {
    // Handle login logic
  }
}
```

For more examples and usage instructions, please refer to the [full documentation](https://github.com/your_username_here/Mack/wiki).

## Documentation

Mack's comprehensive [documentation](https://github.com/your_username_here/Mack/wiki) covers everything you need to know, including component guides, styling instructions, and advanced topics.

## Contributing

We welcome and appreciate all contributions to Mack. To contribute, please follow these steps:

1. Fork this repository
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Open a Pull Request on GitHub

If you have any questions or suggestions, feel free to [open an issue](https://github.com/your_username_here/Mack/issues/new).

## License

Mack is released under the [MIT License](/LICENSE) by [`@OCA-Creations` LLC](https://github.com/OCA-Creations).
