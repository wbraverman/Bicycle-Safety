# EDAs

## Columns Removed

The following columns were removed for the reasons listed:

### Num columns

These columns represent how many cyclists were involved in an accident and how many received each injury type. We only care about the most severe injury, so this data was not needed.

- 'NumBicsAin'
- 'NumBicsBin'
- 'NumBicsCin'
- 'NumBicsKil'
- 'NumBicsNoi'
- 'NumBicsTot'
- 'NumBicsUin'
- 'NumUnits'

### Drvr columns

These columns include data about the driver involved in the accident, not the cyclist. Since our KPIs focus more on what the cyclists can do avoid serious injuries, we're removing all driver columns which they can't control (except 'DrvrVehTyp')

- 'DrvrAge'
- 'DrvrAgeGrp'
- 'DrvrAlcDrg'
- 'DrvrAlcFlg'
- 'DrvrInjury'
- 'DrvrRace'
- 'DrvrSex'

### Other columns

- 'X'
- 'Y'
- 'OBJECTID'
- 'AmbulanceR'
- 'BikeAgeGrp' 
- 'BikeAlcDrg'
- 'BikeAlcFlg'
- 'City'
- 'County'
- 'CrashAlcoh'
- 'CrashSevr'
- 'CrashType'
- 'CrashYear'
- 'Developmen'
- 'HitRun'
- 'Latitude'
- 'Longitude'
- 'RdDefects'
- 'RuralUrban'