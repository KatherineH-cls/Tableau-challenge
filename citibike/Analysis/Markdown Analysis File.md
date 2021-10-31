### Citibike Data Analysis

## Approach for data analysis

The citibike program has been running for a number of years now, so It was decided to analyse the data from the point of view of information that would be useful for operation of the program.  Two key aspects to operations are the rebalancing of bikes between stations and bike maintenance.  Dashboards were developed with view to present monthly performance metrics in each of these areas.

## Clean data
-	Drop duplicates
-	Drop electric bikes as information for this group does not appear correct
-	Drop rows with null values
-	Drop rows with start time later than end time
-	Convert time to datetime
-	End station ids are a mix of numeric and string.  Convert all to string.
-	Unique set of stations – drop duplicates based on subset of station_id, then use station_id to connect tables

## Manipulate Data
-	Calculate trip duration
-	Calculate trip distance
-	Separate into classic bike and docked bike, so that smaller files can be exported to tableau for visualisation of maintenance
-	Group by station and count number of starts and ends for each day, and combine to calculate number of rebalances required

## Analysis Findings (September 2021)

1.	 Rebalances – rebalances were calculated for each station.  This allows the stations with accumulations / depletions to be readily identified (both as a list or on a map).  The number of rebalances required in a given week would determine whether rebalances need to be undertaken daily, weekly or less frequently.  This would improve planning of routes and number of trucks / amount of labour to be allocated to rebalances.

2.	Maintenance.  The total time bikes were docked for maintenance was calculated.  The median repair time was calculated and compared to performance targets.  The target was met for September 2021.  Closer inspection of the data shows that more bikes require maintenance on weekends, and the median maintenance time on weekends is higher than for weekdays.  Performance outcomes could be improved by allocating more maintenance staff to weekends and less to weekdays.
