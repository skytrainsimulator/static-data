# Skytrain Technical Map - Data

This is the data for the schema contained in [the SkytrainSim schema](https://github.com/skytrainsimulator/schema). These 
csv files should be able to be imported into PostgreSQL using `\copy` or similar utilities.

## Dataset notes
### Maps
- `geo`: Georeferenced track data. Accuracy is iffy but should be within a few meters
- `trace-OMC1`: Map of OMC1 traced from a TransLink drawing dated `24-02-26`
- `trace-OMC3`: Map of OMC3 traced from a TransLink drawing dated `20-11-30`
- `trace-VCC1-*` & `trace-VCC2-*`: Maps of Mainline 1 traced from TransLink drawings dated `24-12-11`
- `trace-VCC4-*`: Maps of Mainline 2 traced from TransLink drawing dated `16-02-10`
- `trace-VCC5-*`: Maps of Mainline 3 traced from TransLink drawing dated `2015/06/11`. This drawing is a draft and thus 
not particularly accurate.

### Other notes
Track fragment lengths are currently derived from the `geo` map, which means they inherit the iffy accuracy. Should be 
accurate enough for simulation purposes, but should not be used for anything critical.
