# EDAs

## Columns Removed

Apart from removing OBJECTID, as this column is just an ID column that doesn't bring information about the accident, the following columns were also removed for the reasons listed:

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

### Driver columns

These columns include data about the driver involved in the accident, not the cyclist. Since our KPIs focus more on what the cyclists can do avoid serious injuries, we're removing all driver columns which they can't control (except 'DrvrVehTyp').

- 'DrvrAge'
- 'DrvrAgeGrp'
- 'DrvrAlcDrg'
- 'DrvrAlcFlg'
- 'DrvrInjury'
- 'DrvrRace'
- 'DrvrSex'

### Location columns

These columns represent some kind of location, either as longitude and latitude, or as a city or county. Since our KPIs include using this in a general case regardless of location, we remove these columns. For the future, if we obtain data from more places, city and county could be relevant.

- 'X'
- 'Y'
- 'City'
- 'County'
- 'Latitude'
- 'Longitude'

### Not relevant to KPIs columns

The first columns refer to whether there was alcohol involved in the accident. As we would not have this data in our KPI scenarios, they are not relevant. Same case for the other columns, as we can't control the year or the hit and run situation. Lastly, CrashType is removed since there's too many details and can't be used effectively in a model.

- 'BikeAlcDrg'
- 'BikeAlcFlg'
- 'CrashAlcoh'
- 'CrashType'
- 'CrashYear'
- 'HitRun'

### Similar columns

- 'BikeAgeGrp': Similar values to BikeAge, just grouped together.
- 'CrashSevr': Mostly the same as BikeInjury, but care mostly about the injury type of the cyclist.
- 'Developmen': A bit similar to Locality, but could still bring it back.
- 'RuralUrban': Similar values to Locality, which also classifies as Rural or Urban

### Mostly constant columns

These columns have >99% of their values be the exact same value, so we're removing them as they don't bring much value to the model.

- 'RdDefects'
- 'Workzone'