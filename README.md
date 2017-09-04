# Set-top Box Health Monitor

STB Health Monitor is an automated system to monitor the health of STB's installed in the field in the least intrusive way. It can generate an automatic alert system, which can detect anomalies in the logs and anticipate failures, remedies resulting great reduction in the feedback loop between field and Engineering teams.


## Watchdog Monitor

Monitor component is a part of STB Health Monitor which is responsible for interfacing with Prime Home, Alerter or any other Error-Reporting system to find any unusual activities per CPE. The Monitor shall interface with Rule Engine to retrieve the CPE ID to be monitored and make a connection with Prime Home or Alerter to get the OSD raised since the last request made. All the required data is sterilized in a json object and is passed to Analyser module for further processing

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

* Linux (Ubuntu/ Redhat) 
* Python 3.0 or Above
* SQLite


### Installing Dependencies

```
 cd Monitor/
 pip install install -r dependencies.txt
 
```

### Starting Monitor

```
python monitor_main.py

```

### TODO

Extensive error handling
Remaining Use Cases
More Pythonic Way
Run as a service
Code cleanup and optimization
