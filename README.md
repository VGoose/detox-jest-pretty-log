# detox-jest-pretty-log
Jest Reporter to suppress long view tree log for Detox

## Instructions

1. Add `detox-jest-pretty-log.js` file to your e2e folder.
2. Add one of the following to your jest config:

  ```    
    "reporters": [
          "<rootDir>detox-jest-pretty-log.js"
      ]
  ```
  
   If you want to keep default reporter:
     
  ```    
    "reporters": [
          "default", 
          "<rootDir>detox-jest-pretty-log.js"
      ]
  ```

## Example Output

```
App Start Up 
 should show home screen with weather and transit data -- failed in 889 ms 
 
 Error: Failed: [Error: Error: An assertion failed.
Exception with Assertion: {
  "Assertion Criteria":  "assertWithMatcher:notVisible",
  "Element Matcher":  "((!(kindOfClass('RCTScrollView')) && (respondsToSelector(accessibilityIdentifier) && accessibilityID('home-screen'))) || (((kindOfClass('UIView') || respondsToSelector(accessibilityContainer)) && parentThatMatches(kindOfClass('RCTScrollView'))) && ((kindOfClass('UIView') || respondsToSelector(accessibilityContainer)) && parentThatMatches((respondsToSelector(accessibilityIdentifier) && accessibilityID('home-screen'))))))"
}


Error Trace: [
  {
    "Description":  "Assertion with matcher [M] failed: UI element [E] failed to match the following matcher(s): [S]",
    "Description Glossary":    {
      "M":  "notVisible",
      "E":  "<ABI32_0_0RCTScrollView:0x7faa7706da00; AX=N; AX.id='home-screen'; AX.label='weather forecast Powered By Dark Sky 12:21 PM ￼ 37 F Temp 30 F Feels Like 1 PM ￼ 37   31 2 PM ￼ 38   31 3 PM ￼ 38   31 4 PM ￼ 37   30 5 PM 13 % ￼ 35   28 nearby stations 110 St 4 5 6 Central Park North (110 St) 2 3 116 St 4 5 6 116 St 2 3 103 St 4 5 6 favorite stations You haven't added any stations to your favorites.    Press on the station pins to add stations to your list. 1 / 2'; AX.frame={{0, 60}, {375, 542}}; AX.activationPoint={187.5, 331}; AX.traits='UIAccessibilityTraitNone'; AX.focused='N'; frame={{0, 40}, {375, 542}}; opaque; alpha=1>",
      "S":  "notVisible"
    },
    "Error Domain":  "com.google.earlgrey.ElementInteractionErrorDomain",
    "Error Code":  "3",
    "File Name":  "GREYAssertions.m",
    "Function Name":  "+[GREYAssertions grey_createAssertionWithMatcher:]_block_invoke",
    "Line":  "75"
  }
]

 
App Start Up 
 should be able to navigate -- passed in 5775 ms 


Tests passed 1 out of 2

App Start Up 
 should show home screen with weather and transit data -- failed in 889 ms 

App Start Up 
 should be able to navigate -- passed in 5775 ms 
```
