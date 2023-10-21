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
A list of event names in your experiment data that you want to include in your final, cleaned dataframe.

## self.bad_strings:
List
  
## self.start_baseline_str:
Name indicating the beginning of the baseline period in your data, if applicable. Each element in the list should be written as a string. This may be something like 'baseline_onset'

## self.end_baseline_str:
Name indicating the end of the baseline period in your data, if applicable. Each element in the list should be written as a string. This may be something like 'baseline_end'

## self.start_blocks_str:
Name indicating the first block in your data. This should be a string. It may be something like 'BLOCKID 1'

## self.end_blocks_str:
Name indicating the last block in your data. This should be a string. It may be something like 'BLOCKID 16'

## self.redundant_col:
List of column names. 

## self.redundant_col_first_row:
List of column names.