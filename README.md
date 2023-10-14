The 2020 Presidential race mapped out in Texas (using two party vote share, minor parties dropped)

This map uses data from Harvard VEST, who compile election results in a database for easy useage, in particular for mapping purposes
https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/K7760H

I created this map to show which candidate won which precincts in Texas in 2020. Texas is expected to be competitive federally in 2024, so understanding the previous election's results and coalitions is informative to how it might vote in 2024 and after. Also, I have had family members live in Williamson and Zapata counties, so I was naturally a bit curious, having not made many Texas maps previously

This map was made in QGIS using Harvard VEST's shapefile and data. To simplify the process, I made my own spreadsheet based on the one provided by VEST (included in the above folder), but only using 5 of their original fields (CNTY, PREC, PCTKEY, and Trump and Biden numbers). I also made 4 of my own fields, ones representing the two party vote total, Trump and Biden's share of the two party vote (so Trump votes / total votes, then -1 to get Biden's %), and R-D PCT, which shows their margins of victory. I calculated R-D PCT by adding Biden and Trump's votes together, with positive values coloring in red for Trump, and negative values coloring in shades of blue for Biden. Tied precincts would end up as a 0, and show as light gray, and precincts with no votes had to be manually re-input as 10 to color as dark gray (easily done by sorting the R-D PCT values large to small). +/- 1's also have to be manually changed to a +/- .99, since my color scheme doesn't account for those values

Link to my color scheme files in Google Drive below (since they're massive). The Clear Prev.qml file is the one that I used, but New Partisan Rev.qml should also work if you'd like the borders to show up (though it makes the urban areas hard to see)

https://drive.google.com/drive/folders/1KUlv8GUj19tw2UnHDgtDa3VFztKe6__c?usp=sharing

I then changed the projection on their shapefile, added my spreadsheet, created a join layer between the shapefile and spreadsheet's and PCTKEY fields, and used my pre-made color scheme to color precincts based on the R-D PCT field, and viola. If this method doesn't recreate the map at first, try copying just the filled cells in the spreadsheet and pasting them to a new page. Sometimes excel and QGIS like to think there's an extra row or column that isn't there

I changed the original projection of the data since it was to the US at-large. It is now ESPG: 3081 since its a Texas-specific projection labeled as "Texas State Mapping System"

What this map shows us is that 1) the urban and suburban areas of the state voted heavily Democratic, 2) the rural and exurban areas voted heavily Republican, and 3) that the areas along the border were Democratic leaning despite some of the more rural character of the precincts due to the large Hispanic population. The small blue dots throughout the state indicate minority populations (predominantly African Americans in the East, Hispanics elsewhere) and/or small towns
