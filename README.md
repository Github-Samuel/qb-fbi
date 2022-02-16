# qb-fbi

This is a modified qb-policejob, just rewritten to use a different job and everything is set to use qb-target, this is a fork from another developer, who had it unmaintained.


## Dependencies 

* [PolyZone](https://github.com/mkafrin/PolyZone)
* [QBCore](https://github.com/qbcore-framework/qb-core)
* [QB-Target](https://github.com/Github-Samuel/qb-target)

& everything used in the [qb-policejob]

## Optional Installation

If you're using lj-fuel rather than LegacyFuel, you have to change 4 lines in qb-fbi/client/job.lua
Line 131, Line 699, Line 350 & 150
 

## Installation
Add this to the qb-target Config.BoxZones
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


```

Add this to your qbcore/shared/jobs.lua

```['fbi'] = {
        label = 'Federal Investigation Bureau',
        defaultDuty = true,
        offDutyPay = false,
        grades = {
            ['0'] = {
                name = 'Trainee',
                payment = 50
            },
            ['1'] = {
                name = 'Agent',
                payment = 75
            },
            ['2'] = {
                name = 'Field Agent',
                payment = 100
            },
            ['3'] = {
                name = 'Special Agent',
                payment = 125
            },
            ['4'] = {
                name = 'Director',
                isboss = true,
                payment = 150
            },
        },
    },
```
