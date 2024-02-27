# Meaning of self.X parameters in __init__(self, filename)

## self.filename:
The name of the file you wish to preprocess, including the directory it is located in.

## self.subjectid:
Line of code identifying the subject ID in the file name.

## self.sf:
Sampling frequency (aka Hz) that you want to be sampled at (if downsampling).

## self.include_pupil:
This should be False. It indicates that no pupil data will be included unless it meets the conditions.

## self.data_dir:
The directory your file is located in. This should be in self.filename.

## self.event_list:
A list of all event names in your experiment data. Each element in the list should be written as a string. Some events you may have are: fixation, stimulus, key press, reward.

## self.relevant_list:
A list of event names (strings) in your experiment data that you want to include in your final, cleaned dataframe.

## self.bad_strings:
A list of strings in your experiment data that you do not want to include in your final, cleaned dataframe. An example may be strings indicating eye saccades or blinks. 
  
## self.start_baseline_str:
Name (string) indicating the beginning of the baseline period in your data, if applicable. This may be something like 'baseline_onset'

## self.end_baseline_str:
Name (string) indicating the end of the baseline period in your data, if applicable. This may be something like 'baseline_end'

## self.start_blocks_str:
Name indicating the first block in your data. This should be a string. It may be something like 'BLOCKID 1'

## self.end_blocks_str:
Name indicating the last block in your data. This should be a string. It may be something like 'BLOCKID 16'

## self.redundant_col:
Array of column names (string) for long pupil data (i.e. pupil data with multiple rows for each trial) 

## self.redundant_col_first_row:
Array of column names (string) of first row of pupil data for each trial (i.e. pupil data with one row for each trial).

## self.event_str:
Name (string) of the column which lists each event in your experiment data. 

## self.block_str:
Name (string) of a word found in all block names in your experiment data. This may be something like 'BLOCKID'

## self.trial_str:
Name (string) of a word found in all trial names in your experiment data. This may be something like 'TRIALID'

## BLOCKID_999 and TRIALID_999:
The code includes these strings as placeholder block and trial IDs. Please ensure that you do not have any block or trial IDs labeled as 999 in your data. 

## self.number_of_columns_for_messages:
Array of column names (string) you would like to have in your dataframe, including placeholder strings for extra columns. 

## self.separation_rule:
String indicating the delimiter in your data. Example could be ' |\t'

## self.start_fixation_str:
Name (string) indicating the start of the fixation period in your data, if applicable. This may be something like 'fixation_onset'

## self.merged_data_columns:
Array of column names (string) in the merged data. We have provided a default list for columns to include in the tidy dataframe.

## self.time_str:
Name (string) of the column which lists the time series data in your experiment data.

## self.fraction_of_sampling_rate
Fraction of the sampling rate to scale the closeness of samples to the raw samples (default is set at 0.5)
