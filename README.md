## HOMER+

The [Household Object Movements from Everyday Routines dataset](https://github.com/GT-RAIL/rail_tasksim/blob/homer/routines/README.md) contains a longitudinal data of simulated user behavior over several weeks with an object interaction level detail. While it shows natural variations in activity times, it assumes the same objects are used in every occurence of an activity (e.g. eating cereal for breakfast every time).

In HOMER+, we manually introduce 1-3 variations for 17 out of 24 activities to better emulate how humans perform the same activity in various ways, eg. sometimes having cereal, and other times having oatmeal for breakfast. This repository hosts the resulting dataset with Household A, B, C depicting each household. Each household contains 65 days of training data and 10 days of test data with the following information
- The `scripts_train` and `scripts_test` directories contain human-readable and VirtualHome executable script for each day. The script header outlines the schedule of that day with activity names, and the rest of the script provides timestamped atomic actions performed through the day.
- The `routines_train` and `routines_test` directories contain the full object arrangement sequences, alongwith the corresponding timestamps. Parsing each file will result in a dictionary containing lists of (1) 'graphs' representing object arrangements, (2) 'times' in minutes from midnight of the graphs, (3) 'activities' and 'activities_coarse' representing the activity being performed by the user at two different levels of granularity

If uoi find this dataset useful in your work, consider citing us as

```
@inproceedings{
patel2023predicting,
title={Predicting Routine Object Usage for Proactive Robot Assistance},
author={Maithili Patel and Aswin Gururaj Prakash and Sonia Chernova},
booktitle={7th Annual Conference on Robot Learning},
year={2023},
url={https://openreview.net/forum?id=rvh0vkwKUM}
}
```