# PerfMonCollectorLua
Server side mode to collect Performance Monitoring log lines and submit to a Collector service

## Tasks
* Investigate size of log files
  * Bots
  * Live players
* Dump PerfMon lines to a separate log file (shine does this)
* On round end
  * Rotate log file
  * Compress the file in memory (zip vs gzip)
  * Submit to PerfMonCollectorAPI
    * With credentials from some server.json
  * On successful response
    * Cleanup raw logfile
  * On fail response
    * Write zip to disk
    * Cleanup raw file
