# Complication

Syntactic sugar in Swift for WatchKit Complications.

**Complication** sugar looks like this:
```swift
let template = CLKComplicationTemplate.Modular.Small.stackText()
```
Instead of the not yet fimiliar:
```swift
let template = CLKComplicationTemplateModularSmallStackText()
```

It also allows you to get a sub-type matching a `CLKComplicationFamily`:
```swift
let template = CLKComplicationTemplate.subType(forFamily: complication.family) as! CLKComplicationTemplate.Modular.Small.Type
if true {
  return template.stackText()
} else {
  return template.simpleImage()
}
```
