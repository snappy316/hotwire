```swift
// Note: I don't know much about Swift...and apparently the `SceneDelegate.swift` file isn't tracked by Git?!
//       Because I want to keep track of the changes I make through the tutorial, I'll duplicate them here...

import UIKit

class SceneDelegate: UIResponder, UIWindowSceneDelegate {

    var window: UIWindow?

    func scene(_ scene: UIScene, willConnectTo session: UISceneSession, options connectionOptions: UIScene.ConnectionOptions) {
        guard let _ = (scene as? UIWindowScene) else { return }
    }

}

```
