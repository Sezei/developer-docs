# Setting a property

Setting a property allows you to set the value of a property to the provided value. This creates the property and sets the value if it does not exist, or updates the value of the property if the property already existed.

## Examples

### Setting last played date

A last played date can be achieved by using the set option. This will replace the old date property value or create the property if it does not exist.

#### Roblox Module Example

```lua
local db = require(...)
local Players = game:GetService("Players")

Players.PlayerAdded:Connect(function(Player)
    local callback = db.set(Player, {
        property = "last_seen",
        value = os.time(),
        reason = "Setting last seen"
    })
    
    if callback == true then
        -- Property set successfully
    else
        -- Property failed, the error is available on the callback propety
    end
end)
```

### Achievements

You can mark off achievements by players, i.e. making a hot chocolate by using the set method.

#### Roblox Module Example

```lua
local db = require(...)
local ReplicatedStorage = game:GetService("ReplicatedStorage")

local event = ReplicatedStorage:WaitForChild("DrinkMade")

event.OnServerEvent:Connect(function(Player, Drink)
    if Drink == "Hot Chocolate" then
        local callback = db.set(Player, {
            property = "made_hot_chocolate",
            value = true,
            reason = "Player has made a hot chocolate"
        })
        
        if callback == true then
            -- Property set successfully
        else
            -- Property failed, the error is available on the callback propety
        end
    end
end)
```

