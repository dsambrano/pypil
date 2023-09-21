# Pypil 

Pypil is a Python-based package for preprocessing timeseries pupil data. It follows the best practices for smoothing pupil data and managing eye blinks for arbrirtrary timelengths, as described in Kret & Sjak-Shie (2018).

## Installing Pypil

## Workflow

After inputting the pupil dataframe, Pypil runs through three phases:

1. pypil.prepare_phase(): This method organizes the data into a managable format, removing all the unnecessary components produced by the eyetracker.

2. pypil.filter_phase(): This method performs a series of filters on the data to smooth the data and start filtering out the bad data points. 

3. pypil.process_valid_samples(): The final method uses the filtered data to make inferences about which data points are likely due to noise (based on either physical impossibilities or logic; see Kret & Sjak-Shie, 2018, see Figure 2 and 4). It then removes these values and imputes the value given the autocorrelation and overall path trajectory.  

## Dependencies
1. pandas
2. numpy
3. os
4. from scipy, signal
5. re
6. from io, StringIO
7. warnings 