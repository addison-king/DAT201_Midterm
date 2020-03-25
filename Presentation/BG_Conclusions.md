# Conclusions:
* Based on the data about SO2 and 2.5mm particulates, the area SouthEast of downtown Pittsburgh has a higher concentration of pollution than the rest of the city & county.
* This area (Homestead, North Braddock, West Mifflin, Liberty, Clarion, McKeesport, Brentwood, Pleasant Hills), has high pockets of SO2 and overall has more 2.5mm particulates than the rest of the county.

## Specific Pollution Conclusions:
* SO2: The worst location (Liberty, 3.328ppb) is 2 times worse than the next most polluted area (North Braddock, 1.578ppb) and compared to the least polluted location (Avalon, 0.0187ppb) Liberty is 17,800% more polluted.
	
* 2.5mm Particulates: The worst location (Census Tract 310200, Lincoln Place, 12.456 microgram/m3) is 111% more polluted than the cleanest area (Census Tract 401100, Harrison Twp, 11.251 microgram/m3).



# BG - My Workflow:
### How I created the SO2 map:

1. Imported all PA counties on top of the open street maps
2. Removed all county entries from the attributes table except for Allegheny
3. Imported the layer of all Air emission plants for all of PA
	* Using the Allegheny county layer, I could "clip" everything that was outside of the county
5. Added the layer of sensor locations in Allegheny county
6. Created a "screen" layer that contained the surrounding area (enough to make a map) that would be colored grey with light opacity (help focus attention to Allegheny county)
	* Again using the Allegheny county layer to do this
7. Added the .csv SO2 data
8. Formatted the data to be in ppb
9. Formatted the data points to be a heat points (bigger and darker for larger numbers)
10. Formatted the data callouts to read the location and the measure in ppb

### Printing the map:
	Placed the Title using html to get it centered vertically and horizontally
		<h4 style="line-height: 160px;">Allegheny County: Measure of SO<sub>2</sub> parts per billion</h4>
	Placed the data source
	Wind Rose:
		Using data from the past year, a wind rose was created from the average wind direction
	Scale:
		15 mile bar split into 5 mile increments
	Legend:
		labels for the air emission plants and sensor locations
		
		
### How I created the 2.5mm particulate map:
1. Imported all PA counties on top of the open street maps
1. Removed all county entries from the attributes table except for Allegheny
1. Imported the layer of all Air emission plants for all of PA
	*	Using the Allegheny county layer, I could "clip" everything that was outside of the county
1. Created a "screen" layer that contained the surrounding area (enough to make a map) that would be colored grey with light opacity (help focus attention to Allegheny county)
	*	Again using the Allegheny county layer to do this
1. Added the 2.5mm particulate data
	*	Formatted the data to display 10 color buckets
	*	Formatted the data callouts to only show names for locations that are not in compliance 

### Printing the map:
	Placed the Title using html to get it centered vertically and horizontally
	Placed the data source
	Wind Rose:
		Using data from the past year, a wind rose was created from the average wind direction
	Scale:
		15 mile bar split into 5 mile increments
	Legend:
		labels for the air emission plants and the Particulate 2.5mm buckets
