## The Federal Courts Project

The ultimate goal of this project is to build a centralized database of the appointed federal judgeships across the 13 district appellate courts since 2001.

The file `data.csv` contains....



| Header         | Definition |
|----------------|------------|
|`name`|The name of the appointed judge.|
|`circuit`  |The circuit the judge was appointed to.|
|`confirmation_date`   |The date the judge was confirmed by the senate.|
|`nomination_no`   |Unique number for the senate nomination.|
|`congress_no`      ||
|`session`      ||
|`democrats`|The number of democratic senators at the time of the confirmation.|
|`republicans`|The number of republican senators at the time of the confirmation.|
|`independets`|The number of independent senators at the time of the confirmation.|
|`record_vote_number`||
|`yea_votes`    |The number of senators that voted 'yea' to the confirmation of the judge.|
|`nay_votes`|The number of senators that voted 'nay' to the confirmation of the judge.|
|`vote_id`|Unique numerical id for each confirmation vote. |
|`D_yea`|The number of **democratic** senators that voted **'yea'** to the confirmation of the judge.|
|`D_nay`|The number of *democratic* senators that voted 'nay' to the confirmation of the judge.|
|`D_no_vote`|The number of *democratic* senators that did not vote for the confirmation of the judge.|
|`R_yea`|The number of *republican* senators that voted 'yea' to the confirmation of the judge.|
|`R_nay`|The number of republican senators that voted 'nay' to the confirmation of the judge.|
|`R_no_vote`|The number of republican senators that did not vote for the confirmation of the judge.|
|`I_yea`|The number of independent senators that voted 'yea' to the confirmation of the judge.|
|`I_nay`|The number of independent senators that voted 'nay' to the confirmation of the judge.|
|`I_no_vote`|The number of independent senators that did not vote for the confirmation of the judge.|
|`vote`|A list of each senators name and vote|

