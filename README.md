# name_clusters
Script to disambiguate names in the database, so similar names can be grouped together. This is to identify same firm/individual with different names in the database.

To identify the same firm/person in the database with different naming is challenging. People may have typos, putting different abbreviations and/or putting the words in different orders etc. This script provides a way to group similar names together, so that they can point to the same firm/person rather than counting them more than once, making the work with database without common entity identifier easier.

It has three steps.

1. pre-process the names: disambiguate some common abbreviations and basic disambiguition.
2. Assign names into clusters (to reduce the run time) and calculate similarity scores and keep names with high similarity scores.
3. post-process the matched pairs, so that final pairs are the same entity.
4. Give original names a identfier to indicate they are the same entity.

Requirements:
- POSIX compliant shells
- python3.6+, pandas, fuzzuwuzzy, python-levenshtein
- GNU parallel
