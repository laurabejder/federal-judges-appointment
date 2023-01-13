## The Federal Courts Project

The ultimate goal of this project is to build a centralized database of the appointed federal judgeships across the 13 district appellate courts during the 107th to 117th congress (2001-2022).

The analysis of the data has been written into the article [Senate confirmations of circuit court judges have become more politically divided](https://laurabejder.github.io/federal_judges_appointment/).

The file `data.csv` contains the full dataset of all confirmed judges, the circuit they were confirmed to and the senate votes. The file includes following variables:

| Header         | Definition |
|----------------|------------|
|`name`|The name of the appointed judge.|
|`circuit`|The circuit the judge was appointed to.|
|`confirmation_date`|The date the judge was confirmed by the senate.|
|`nomination_no`|Unique number for the senate nomination.|
|`congress_no`|The congress that elected the judge. Spans from the 107th to the 117th Congress.|
|`session`|The session within which the judge was elected. Has either the nummeric value of `1` or `2` depending on whether the judge was elected during the first or second session of a congress.|
|`democrats`|The number of democratic senators in the U.S. Senate at the time of the confirmation.|
|`republicans`|The number of republican senators in the U.S. Senate at the time of the confirmation.|
|`independets`|The number of independent senators in the U.S. Senate at the time of the confirmation.|
|`record_vote_number`|Id for the vote by the congress.|
|`yea_votes`|The number of senators that voted 'yea' to the confirmation of the judge. If value is missing, the judge was confirmed by voice vote.|
|`nay_votes`|The number of senators that voted 'nay' to the confirmation of the judge. If value is missing, the judge was confirmed by voice vote.|
|`vote_id`|Unique numerical id for each confirmation vote. |
|`D_yea`|The number of **democratic** senators that voted **'yea'** to the confirmation of the judge.|
|`D_nay`|The number of **democratic** senators that voted **'nay'** to the confirmation of the judge.|
|`D_no_vote`|The number of **democratic** senators that **did not vote** for the confirmation of the judge.|
|`R_yea`|The number of **republican** senators that voted **'yea'** to the confirmation of the judge.|
|`R_nay`|The number of **republican** senators that voted **'nay'** to the confirmation of the judge.|
|`R_no_vote`|The number of **republican** senators that **did not vote** for the confirmation of the judge.|
|`I_yea`|The number of **independent** senators that voted **'yea'** to the confirmation of the judge.|
|`I_nay`|The number of **independent** senators that voted **'nay'** to the confirmation of the judge.|
|`I_no_vote`|The number of **independent** senators that **did not vote** for the confirmation of the judge.|
|`vote`|A list of each senators name and vote|

### Inside the `data` directory:
- `data.csv`: The complete dataset as explained above. 
- `nominations.csv`: This file contains the tabular version of the html scrapes.  
- `party_votes.csv`: The initial dataset of the scrape of the votes of all senators for each nomination.
- `voteinfo.csv`: Contains all the information needed to loop through customized links to each nomination and scrape the votes of all senators for each nomination. 
- `votes.csv`: File containing all judges, their names, circuit number, confirmation date, congress number, nomination number, confirmation date and number of yea and nay votes from the senate confirmation. It is the cleaned and broken down version of `nominations.csv`.

### Inside the `html_scrapes` directory:
- 12 html files containing the original scrape of all individuals confirmed by the judiciary committee in the senate from 2001 to 2022. These files are the basis for the list of all confirmed circuit judges and the yea and nay votes in the Senate. 

### Inside the `map` directory:
- `courts13_join.json`: Geojson shapefile of all 13 district appellate courts.
- `map.html`: HTML code for an interactive map displaying each appellate courts district and the judges confirmed to that district including the partisan votes for each judge. Can be broken down to each congress. 
- `geo-data.js`: The final file combining the data from `data.csv` converted into js and the geojson shapefiles. The basis for the visualization created in `map.html`.
