# Default Filter Settings:

## Pupil range filter criteria:
Maximum pupil size = 9mm
Minimum pupil size = 1.5mm 

If your eyetracker does not record in mm, then the following are recommended:
Maximum pupil size = np.Inf
Minimum pupil size = 0.1

## Isolated sample filter criteria:
The minimum temporal distance (in ms) between two clusters of samples for them to be considered separated is 40. 

Each separated cluster must be at least 50ms in temporal length to be considered valid. 

## Dilation speed filter criteria: 
The number of medians to use as the cutoff threshold when applying the speed filter is set at 16. 

Only calculate the speed when the gap between samples is smaller than 200ms. 

## Edge removal filter criteria: 
A section of missing data is considered a gap if it is between 75-2000ms long. 

We have indicated 50ms before and after a gap to be "padding."

## Deviation filter criteria:
The deviation filter passes four times over the data marked as valid by all filters above.
Filters outliers, indicated by 16 MADs
