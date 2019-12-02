# Disbale-Dark-mode-in-entire-App-
This will disable the dark/light mode in the entire app and overrides the system default values for the specific app.

Source :- 
https://medium.com/@akshay.s.somkuwar/disable-dark-mode-in-ios-13-for-your-ios-app-c025b446d87b

## First tip: To override the ViewController style
you can override the interface style of UIViewController by
1: overrideUserInterfaceStyle = .dark //For dark mode
2: overrideUserInterfaceStyle = .light //For light mode

```swift
class ViewController: UIViewController {
    override func viewDidLoad() {
        super.viewDidLoad()
        overrideUserInterfaceStyle = .light    
    }
}
```

## Second tip: Adding a key in info.plist
Simply you can add a new key UIUserInterfaceStyle in your app info.plist and set its value to Light or Dark. this will override the app default style to the value you provide.
You dont have to add overrideUserInterfaceStyle = .light this line in every viewController, just one line in info.plist that’s it.
