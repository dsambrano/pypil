# Meaning of advanced preprocessing functions in Pypil

## read_merged_and_task(self, task_df_name=None, overwrite=False)
Reads preprocessed pupil data (the dataframe outputted from running the standard preprocessing functions) 
Reads task data (a separate dataframe from the pupil data)
Reads in merged_pupil_first_row dataframe if it exists

When running:
1. task_df_name should be a string specifying the appropriate directory and file name
2. if overwrite=True, existing files in the appropriate directory will be overwritten

## add_first_row_pupil(self)
Uses the merged_pupil.csv dataframe to generate a datafile with one row for each trial
Call this function after irrelevant columns and events are removed

## drop_redundant_column(self, for_first_row=False)
If for_first_row=False: Drops redundant columns from merged data as defined in self.redundant_col

If for_first_row=True: Drops redundant columns from merged data first row as defined in self.redundant_col_first_row (this is run in add_first_row_pupil)

## add_identifier(self)
Adds a unique subjectID-block-trial identifier to both merged and task data to facilitate future mapping
Before adding the unique identifier, it makes sure that the merged and task data are of the same data type 

## add_timestamp(self)
Calculates timestamp based on column event for each trial
Disclaimer: If each block/trial lacks at least one event, then there may not be column names for each event. 

## avg_within_timewindow(self, timestamp_col='X', y_col='Y', timestamp_range=[q,r], new_x_col='avg')
Calculates the specified y_col average within the specified timestamp_range for the specified timestamp_col. 

When running:
1. timestamp_col and y_col should both be strings which specify columns in the merged dataframe
2. timestamp_range should be a list of float time values

## percent_miss(self, new_x_col='percent_miss')
Calculates the percentage of missing data for each trial based on whether pupil size is zero

## write_merged_and_task(self, overwrite=False)
Writes preprocessed merged data, merged_data_first_row, and task_df

## read_data_ready2use(self)
Reads in merged pupil and task data that is ready to use downstream in the exp

## choice_msgpupil_merge(self, task_df=None, overwrite=False)
Merges task and choice data with pupil and msg (pupil and msg should be merged in mess_pupil_merge)

When running:
1. run this function after preprocess, filter and valid has all been done
2. task_df should be of the form self.task_df





