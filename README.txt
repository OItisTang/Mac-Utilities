Some useful utilities:

* Auto_Softoken_VPN.app
  auto connecting to vpn, including auto getting Softoken dynamic password

* Auto_Softoken_AnyConnect_VPN.app
  auto connecting to AnyConnect vpn, including auto getting Softoken dynamic password

* Book2Images.app
  screenshot each page of epub in iBooks

* CloseOrHide.app
  an apple script wrapped in app, that determines whether to close an app or hide an app.
  For example: OneNote for Mac quit on close, annoying, so we want to hide it by default.
  I have a mouse, I have assigned opening this app on clicking a special key on the mouse.
  So that app knows whether to close or hide an app.
  Run this.

* Image2PDF.app
  create PDF file from images

* PDF2Image.app
  convert PDF file to a image for each page


* ics2iCalendar.app
  .ics files exported from Microsoft Outlook can be imported into iCloud/iCalendar.
  
  However, if you wish to remove those events, you must send a "decline" mail to its organizer other than deleting it directly.
  
  To convert that .ics file into a pure event, we only need to remove "ATTENDEE", "ORGANIZER" and "UID" fields.
  
  This app also inserts those deleted fields as meeting meta info into DESCRIPTION content, so that you will not miss anything about this meeting.
  
  Make it easier to use:
  
  Register this app into “open with” menu for “.ics” file type,
  first, change “CFBundleTypeExtensions" key's value into “ics” in ics2iCalendar.app/Contents/Info.plist
  second, please run:
  /System/Library/Frameworks/CoreServices.framework/Versions/A/Frameworks/LaunchServices.framework/Versions/A/Support/lsregister -f ~/Applications/ics2iCalendar.app/
  killall Finder
  
  
  Now you can right click on a foo.ics file, then open with "ics2iCalendar.app",
  it will create a foo.iCalendar.ics for you.
  
  After that, you can save that foo.iCalendar.ics to your calendar.
  That event will be synced through iCloud to all your devices.
  
  Any time you want to drop that event, just delete that from your calendar, nobody else will be notified.
  
  # Dependencies:
  #     bash
  #     sed >= 4.0.7
  #     grep
  #     wc
  #     cut
  #

* Reconnect_wired_802.1x.app
  If Mac fails to pass wired dot1x authentication, disconnect and connect again, mostly, it helps.
