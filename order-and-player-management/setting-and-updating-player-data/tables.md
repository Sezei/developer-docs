# Tables

Setting values to a table is supported by the Hyra Player Management datastore, but it **must be encoded as a JSON when sent**

## Example

```lua
local db = require(...)
local ReplicatedStorage = game:GetService("ReplicatedStorage")
local http = game:GetService("HttpService")

local event = ReplicatedStorage:WaitForChild("DrinkMade")

event.OnServerEvent:Connect(function(Player, Drink)
    if Drink == "Hot Chocolate" then
        local callback = db.set(Player, {
            property = "made_hot_chocolate",
            value = http:JSONEncode({ made_drink = true }),
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

We are using **:JSONEncode** \(a member of the HttpService\) to encode the table as JSON.

