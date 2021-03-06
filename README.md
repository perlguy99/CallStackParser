[![Carthage compatible](https://img.shields.io/badge/Carthage-compatible-4BC51D.svg)](https://github.com/gumob/CallStackParser)
[![Version](http://img.shields.io/cocoapods/v/CallStackParser.svg)](http://cocoadocs.org/docsets/CallStackParser)
[![Platform](http://img.shields.io/cocoapods/p/CallStackParser.svg)](http://cocoadocs.org/docsets/CallStackParser)
[![Build Status](https://travis-ci.com/gumob/CallStackParser.svg?branch=master)](https://travis-ci.com/gumob/CallStackParser)
![Language](https://img.shields.io/badge/Language-Swift%204.2-orange.svg)
![Packagist](https://img.shields.io/packagist/l/doctrine/orm.svg)

# CallStackParser
A swift library to parse call stack symbol supporting iOS, tvOS, watchOS, and macOS.
Most of all source codes are ported from [GDXRepo/CallStackParser](https://github.com/GDXRepo/CallStackParser).
The version on this repository is added multiple platform support, support for Carthage and Cocoapods.

## Requirements

CallStackParser supports multiple platforms
- iOS 9.0 or later
- macOS 10.10 or later
- tvOS 9.0 or later
- watchOS 2.0 or later
- Swift 4.2

## Installation

### Carthage

Add the following to your `Cartfile` and follow [these instructions](https://github.com/Carthage/Carthage#adding-frameworks-to-an-application).

```
github "gumob/CallStackParser"
```

### CocoaPods

To integrate CallStackParser into your project, add the following to your `Podfile`.

```ruby
pod 'CallStackParser'
```

## Usage

Print simplified call stack symbols:
```swift
import CallStackParser

class ViewController: UIViewController {

    override func viewDidLoad() {
        super.viewDidLoad()
        foo()
    }

    func foo() {
        bar()
    }

    func bar() {
        print(Thread.simpleCallStackString)
        // [CallStack:3/3] ViewController                       bar()
        // [CallStack:2/3] ViewController                       foo()
        // [CallStack:1/3] ViewController                       viewDidLoad()
    }

}
```

Read the [API reference](https://gumob.github.io/CallStackParser/Classes/CallStackParser.html), or check [example projects](https://github.com/gumob/CallStackParser/tree/develop/Example) for detailed information.

## Copyright

CallStackParser is released under MIT license, which means you can modify it, redistribute it or use it however you like.
