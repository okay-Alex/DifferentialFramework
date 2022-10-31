# **DifferentialFramework**
Service-Based Roblox game framework || Latest Public Stable Build: v2.13a

Brief guide on using DifferentialFramework within your Roblox projects.

## _Step #1 || Downloading DifferentialFramework_

#### Method #1 Download "_DIFFERENTIAL_FRAMEWORK.rbxm" from the Repository

#### ~~Method #2 Claim the Roblox Model (10576227595)~~ (NOT RECOMMENDED)


## _Step #2 || Installing DifferentialFramework_

1. -> Drag "_DIFFERENTIAL_FRAMEWORK.rbxm" file // "Differential Framework" model into Studio Instance
2. -> Drag the contents of "_DIFFERENTIAL_FRAMEWORK" into their respective Services

![image](https://user-images.githubusercontent.com/108566298/198916462-ca6dee64-930a-4c1d-9d10-c73be494922b.png)

## _Step #3 || Creating a Service_

#### Whenever creating a Service Module Script, copy the following "Skeleton Code" into your module:
```lua
local NewService = {}

function NewService.init() -- ALL valid DifferentialFramework Services require an .i/Init or .Initialize function
	-- Insert Code Here
	script:SetAttribute("Loaded", true) -- This allows for the Service to be accessed
end

return NewService
```

## _Step #4 || Using a Service_

#### Services may be required by other Services and normal Scripts, although whenever using a normal Script with DifferentialFrame, ensure that you put the following statement on the first line:
```lua
require(workspace.LoadScript)() -- Ensures that DifferentialFramework has loaded before Script's contents are executed
```

#### To require & use a Service in both, Services and normal Scripts you require it via _G:
```lua
local NewService = _G:GetService("NewService")
```
#### Once required, you can use the Service like you would a normal module script, do note that _G:GetService will actually yield until the module is fully initialized.

## _Step #5 || Using Bundled Libraries_

#### DifferentialFramework comes bundled with a couple light-weight libraries, to include a library you must include the following statement:
```lua
local stdLib = _G["#include"]("stdLib") -- Exchange stdLib for a different library if you want to include a different one
```
