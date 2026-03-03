SELECT b.city, b.state,
a."2014_murders" AS "2014_murders",
a."2015_murders" AS "2015_murders",
b."2016_murders" AS "2016_murders"
FROM murder_2015_final a
JOIN murder_2016_prelim b
ON a.city=b.city AND a.state=b.state
ORDER BY b."2016_murders" DESC;


[Baltimore](https://www.cbsnews.com/baltimore/news/baltimore-city-records-344-homicides-in-2015/) and [Washington, D.C.](https://www.fox5dc.com/news/dc-ends-2015-with-54-percent-homicide-spike) in murder_2015_final match reported 2015 year-end homicide totals, while [Chicago’s](https://www.wbez.org/news/2016/01/01/chicago-homicides-up-during-tumultuous-2015-for-police) murder_2015_final value is at least in the right range compared to commonly reported year-end figures. However, murder_2016_prelim lists Chicago’s 2015 murders as 378, which is far enough off that it suggests incomplete or inconsistent counting. So for the joined table, I kept the 2015 column from murder_2015_final because it aligns better with published year-end totals across cities.


city,state,2014_murders,2015_murders,2016_murders
Chicago,Illinois,411,478,536
New York,New York,333,352,252
Baltimore,Maryland,211,344,230
Detroit,Michigan,298,295,221
Philadelphia,Pennsylvania,248,280,213
Houston,Texas,242,303,212
Los Angeles,California,260,282,205
Memphis,Tennessee,140,135,158
St. Louis,Missouri,159,188,133
New Orleans,Louisiana,150,164,127
Las Vegas,Nevada,122,127,125
Dallas,Texas,116,136,118
Indianapolis,Indiana,136,148,117
Phoenix,Arizona,114,112,111
San Antonio,Texas,103,94,111
Washington,D.C.,105,162,105
Kansas City,Missouri,78,109,90
Cleveland,Ohio,63,120,89
Atlanta,Georgia,93,94,85
Milwaukee,Wisconsin,90,145,84
Louisville,Kentucky,56,81,79
Jacksonville,Florida,96,97,78
Orlando,Florida,15,32,73
Newark,New Jersey,93,104,72
Columbus,Ohio,83,77,70
Tulsa,Oklahoma,46,55,52
Oakland,California,80,85,52
Cincinnati,Ohio,60,66,50
Nashville,Tennessee,41,72,49
Fort Worth,Texas,54,56,49
Albuquerque,New Mexico,30,43,46
Pittsburgh,Pennsylvania,69,57,46
Miami,Florida,81,75,45
Stockton,California,49,49,38
Buffalo,New York,60,41,38
San Jose,California,32,30,35
Fort Wayne,Indiana,12,25,34
Denver,Colorado,31,53,33
San Francisco,California,45,53,32
Oklahoma City,Oklahoma,45,73,30
Durham,North Carolina,21,34,30
San Diego,California,32,37,30
Long Beach,California,23,36,29
Austin,Texas,32,23,28
Boston,Massachusetts,53,38,28
Minneapolis,Minnesota,31,47,26
Anchorage,Alaska,12,26,26
Charlotte-Mecklenburg,North Carolina,47,61,25
Bakersfield,California,17,22,22
Sacramento,California,28,43,21
Omaha,Nebraska,32,48,20
Greensboro,North Carolina,23,26,20
Santa Ana,California,18,12,20
Fresno,California,47,39,19
Tucson,Arizona,35,31,18
Arlington,Texas,13,8,17
Aurora,Colorado,11,24,16
Lexington,Kentucky,20,15,16
Colorado Springs,Colorado,20,25,15
Portland,Oregon,26,34,14
Jersey City,New Jersey,24,27,14
Seattle,Washington,26,23,14
El Paso,Texas,21,17,14
St. Petersburg,Florida,19,14,14
Virginia Beach,Virginia,17,19,13
Mobile,Alabama,31,24,12
Wichita,Kansas,26,27,10
Honolulu,Hawaii,21,15,9
Laredo,Texas,14,8,9
Lincoln,Nebraska,7,1,9
Corpus Christi,Texas,27,17,9
Toledo,Ohio,24,24,8
Raleigh,North Carolina,16,17,7
Riverside,California,12,10,7
Plano,Texas,4,4,5
Anaheim,California,14,18,4
Henderson,Nevada,3,4,3
Chandler,Arizona,1,1,3
Chula Vista,California,7,6,1
Load SQLite DB by URL Load CSV Load JSON Load Parquet Load SQL Documentation
