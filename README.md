
# B24PaymentSdk

**B24PaymentSdk** is a swift framework library that provides payment methods via bank deeplink, bank web checkout, and KHQR. 

## Features
- **Bank Deeplink**
- **Bank Web Checkout**
- **KHQR**
- **Add to favorite**

## Getting started
    This instructions will get you a complete guide on how to integrate with our sdk to allow your consumer to make payment via bill24 financial partner
    
### Grant Permission 
   Allow permission to save image in photos inside `info.plist`
   
    <key>Privacy - Photo Library Additions Usage Description</key>
    <string>App needs access to the photo library for saving images.</string>
    
### 1. Requirement

  Require `UIkit`, `Swift version 5.0.0`, `IOS minimum version 13.0`, `Xcode version 15.0` 

### 2. CocoaPods 1.13.0 or later 

Create `Podfile` and add `pod 'B24PaymentSdk'`
```
  use_frameworks!

  target 'MyApp' do
    pod 'B24PaymentSdk', :http => 'https://b24sdk.s3.ap-southeast-1.amazonaws.com/B24PaymentSdk-1-0-10.zip'
  end
```
### 3. Run this command  
```
  pod install
```
### 4. Usage

```

import UIKit
import B24PaymentSdk
class ViewController: UIViewController {
    override func viewDidLoad() {
        super.viewDidLoad()
    }

    @IBAction func onClickCheckoutButton(_ sender: Any) {
       B24PaymentSdk().initSdk(
            controller: self,
            transactionId: "19F84F284841",
            refererKey: "123X",
            language: "km",
            darkMode: false,
            isProduction: false
      )
    }
}
```
  

  




