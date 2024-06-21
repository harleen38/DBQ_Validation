
**Introduction**

This code validates the necessary data for the smooth running of the DBQ algorithm. The data points being validated are:

1. DPF Differential Pressure (3251)
2. DPF In Temperature (3250)
3. Engine RPM (190)
4. SPEED (84)
5. Soot-Load (5466/3719)
6. Engine Load (92)
7. Active Regeneration Signal (3700)

**Conditions for Data Sanity**

The code evaluates the following conditions:

1. Whether the values of each PID data lie within their respective permissible ranges.
2. Whether there is required variance present in each of the PID data.

**Input Format**

To run the code, please specify the following inputs:

1. **vehicle_id**: Unique identifier for the vehicle.
2. **Start_TS**: Start period from which we want the data (Start time should be after the FOTA is being performed).
3. **End_TS**: End period till which we want the data.
4. **country_FLAG**: Specify either "US" for USA vehicles or "IN" for INDIAN vehicles.

**Output**

If all the conditions for data sanity are passed, the output will be:

**PASSED**

If any of the conditions fail, the output will be:

**FAILED**

This README provides a clear overview of the code's purpose, input format, and output.

**Note** 
The algorithm can function even in the absence of Soot-Load and Active Regeneration Signal. If either of these signals is missing, a message will be displayed to inform the validator.


