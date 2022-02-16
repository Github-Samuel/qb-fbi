# qb-fbi




# Add this to the qb-target Config.BoxZones
```
["FIBArmory"] = {
        name = "FIBArmory",
        coords = vector3(118.09197998047,-728.92181396484,242.61134338379),
        length = 2.0,
        width = 3.4,
        heading = 0,
        debugPoly = false,
        minZ=239.69,
        maxZ=243.29,
        options = {
            {
                type = "client",
                event = "fbi:client:armory",
                icon = "fas fa-clipboard",
                label = "Access Armory",
                job = "fbi"
            }
        },
        distance = 3.5
    },

    ["FIBDuty2"] = {
        name = "FIBDuty2",
        coords = vector3(125.29919433594,-733.60913085938,242.12716674805),
        length = 1.5,
        width = 1.5,
        heading = 31.27,
        debugPoly = false,
        minZ = 241.22,
        maxZ = 244.22,
        options = {
            {
                type = "client",
                event = "Toggle:Duty",
                icon = "fas fa-sign-in-alt",
                label = "Sign In / Out",
                job = "fbi",
            },
        },
        distance = 2.0
    },
