# Rehid (with turbo)

This is a fork of Rehid which adds turbo. It's a little janky sometimes, but I've been using it a while and it works pretty well.  

Turbo is configured in `rehid.json`. Example configuration:
```json
{
  "turbo": {
    "press": "ZR",
    "mash": "A+B+X+Y",
    "speed": 4
  }
}
```

- Press is the button combo which activate turbo.
- Mash is a list of buttons which turbo is limited to. If omitted, it defaults to every button.
- Speed is the number of polls to wait before changing the button state, i.e. 4 indicates one button press per 8 polls. 4 is the default, and anything below it tends to cause weird behavior. If turbo is janky in a certain game, try messing with this.

If you map the button used for turbo to another key, turbo will still work on that key. For example, with this config:
```json
{
  "keys": [
    { "press": "ZR", "get": "A" }
  ],
  "turbo": {
    "press": "ZR"
  }
}
```
Pressing ZR will mash A, even if you aren't holding A. 
