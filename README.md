# Advanced Spring
Advanced Spring lets you create spring class for every major Roblox & Luau datatype

## About
Supported datatypes:  `boolean`, `number`, `BrickColor`, `CFrame`, `Color3`, `ColorSequence`, `NumberRange`, `NumberSequence`, `Rect`, `UDim`, `UDim2`, `Vector2`, `Vector3`. You can set **initial position**, **damping ratio** and **frequency** when creating new spring instance or by creating config file or by changing `DEFAULT_SETTINGS`.

## API Usage
```lua
local Spring = require(path.to.this.module)

-- Creates new spring class with optional initial position and settings
local spring = Spring.new(Vector3.new())

-- Sets new spring goal
spring:Set(Vector3.new(4, 2, 0))

-- Updates spring by delta seconds
spring:Step(delta)

-- Returns current spring position
part.Position = spring:Get()

-- Sets new goal, updates spring and returns current position
part.Position = spring:All(Vector3.new(4, 2, 0), delta)
```

## Limitations
* CFrame - only position is supported (it may change in the future)
* ColorSequence & NumberSequence - only first and last keypoints are supported

## Credits
Part of this code was written by @Fraktality