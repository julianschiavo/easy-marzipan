# Marzipan Cheatsheet
Want to avoid going through manually and finding every single missing framework, method, or issue? Use this quick cheatsheet to check your code for any issues before building on Marzipan.

## __Unavailable Frameworks__
### Apple
- AppKit (possible via lldb but not recommended)
- AddressBook/Contacts/ContactsUI
- CoreTelephony (`CTTelephonyNetworkInfo`)
- CloudKit
- EventKit
- GameplayKit
- IntentsUI (Intents works)
- LocalAuthentication
- MapKit
- MessageUI (`MFMailComposeViewController`)
- Photos (causes AppKit to load)
- SafariServices (`SFSafariViewController`)
- Social (`SLComposeViewController`)

### Third Party
- Firebase by Google
- Realm
- SwiftEntryKit
- WeScan

<br>

## __Unavailable Methods/Properties__
### UIKit
- `accessibilityIgnoresInvertColors` (Invert Colors)
- `UIDocumentBrowser`
- `UINotificationFeedbackGenerator` (Haptic Feedback)
- `UIPrintInfo` (Printing)
- `UIWebView`

### Other (import [Workarounds.swift](Workarounds.swift) to fix)
- `-[NSFont isSystemFont]` (Called by dynamic type)
- `-[NSFont _fontAdjustedForContentSizeCategoryCompatibleWithTraitCollection:]` (Called by `UILabel` to adjust dynamic type sizing)
