# Marzipan Cheatsheet
Want to avoid going through manually and finding every single missing framework, method, or issue? Use this quick cheatsheet to check your code for any issues before building on Marzipan.

## __Unavailable Frameworks__
### Apple
- AppKit (possible via lldb but not recommended)
- AddressBook/Contacts/ContactsUI
- CoreTelephony (`CTTelephonyNetworkInfo`)
- CloudKit (couldn't get it working)
- GameplayKit
- IntentsUI (Intents seems to work)
- LocalAuthentication
- MessageUI (`MFMailComposeViewController`)
- Photos (causes AppKit to load)
- SafariServices (`SFSafariViewController`)
- Social (`SLComposeViewController`)

### Third Party
- Firebase by Google
- Realm (immediate crash)
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

### Patchable (import [Workarounds.swift](Workarounds.swift))
- `-[NSFont isSystemFont]` (Called by dynamic type)
- `-[NSFont _fontAdjustedForContentSizeCategoryCompatibleWithTraitCollection:]` (Called by `UILabel` to adjust dynamic type sizing)
