```swift
// Note: I don't know much about Swift...and apparently the `SceneDelegate.swift` file isn't tracked by Git?!
//       Because I want to keep track of the changes I make through the tutorial, I'll duplicate them here...

import UIKit
import Turbo

class SceneDelegate: UIResponder, UIWindowSceneDelegate {

    var window: UIWindow?

    private let session = Session()
    private let navigationController = UINavigationController()

    func scene(_ scene: UIScene, willConnectTo session: UISceneSession, options connectionOptions: UIScene.ConnectionOptions) {
        guard let windowScene = (scene as? UIWindowScene) else { return }
        self.window = UIWindow(windowScene: windowScene)
        self.window?.rootViewController = navigationController
        self.window?.makeKeyAndVisible()

        visit()
    }

    private func visit() {
        let url = URL(string: "http://localhost:3000")!
        let controller = VisitableViewController(url: url)
        session.visit(controller, action: .advance)
        navigationController.pushViewController(controller, animated: true)
    }
}

```
