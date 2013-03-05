       ___                 _____ ____  ____  ____
      / _ \ _ __   ___ _ _|_   _/ ___||  _ \| __ )
     | | | | '_ \ / _ \ '_ \| | \___ \| | | |  _ \
     | |_| | |_) |  __/ | | | |  ___) | |_| | |_) |
      \___/| .__/ \___|_| |_|_| |____/|____/|____/
           |_|    The modern time series database.

OpenTSDB is a distributed, scalable Time Series Database (TSDB) written on
top of HBase.  OpenTSDB was written to address a common need: store, index
and serve metrics collected from computer systems (network gear, operating
systems, applications) at a large scale, and make this data easily accessible
and graphable.

Thanks to HBase's scalability, OpenTSDB allows you to collect thousands of
metrics from tens of thousands of hosts and applications,  at a high rate
(every few seconds). OpenTSDB will never delete or downsample data and can
easily store hundreds of billions of data points.

OpenTSDB is free software and is available under both LGPLv2.1+ and GPLv3+.
Find more about OpenTSDB at http://opentsdb.net


# Changes
The following changes have been committed to this fork.

* Atomic Increment functionality enabled via an "inc" command.
  * This requires my fork of aysnchbase
* Adding TsdApi class to expose OpenTSDB internals
  * Currently only "Query" functionality exposed
* Maximum # of tags for 1 datapoint has been incresed from 8 to 16
* &ascii queries will return datapoints in the exact timeframe requested, with no padding
  * Thanks to manolama
* Increased scan size to (1024 * 10)
  * Thanks to Brian Hawkins

