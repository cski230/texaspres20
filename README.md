# The 2020 Presidential race mapped out in Texas (using two party vote share, minor parties dropped)

#This map uses data from Harvard VEST, who compile election results in a database for easy useage, in particular for mapping purposes
#https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/K7760H

#I created this map to show which candidate won which precincts in Texas in 2020. Texas is expected to be competitive federally in 2024, so understanding the previous election's results and coalitions is informative to how it might vote in 2024 and after

#This map was made in QGIS using VEST's shapefile and data. To simplify the process, I made my own spreadsheet based on the one provided by VEST, but only using 5 of their original fields (CNTY, PREC, PCTKEY, and Trump and Biden numbers). I also made 4 of my own fields, ones representing Trump and Biden's share of the two party vote, the two party vote total, and R-D PCT, which shows their margins of victory. I then changed the projection on their shapefile, added my spreadsheet, created a join layer between the shapefile and the PCTKEY fields, and used my pre-made color scheme to color precincts based on the R-D PCT field, and viola

#I changed the original projection of the data since it was to the US at-large. It is now ESPG: 3081 since its a Texas-specific projection labeled as "Texas State Mapping System"
