# Set-top Box Health Monitor

STB Health Monitor is an automated system to monitor the health of STB's installed in the field in the least intrusive way. It can generate an automatic alert system, which can detect anomalies in the logs and anticipate failures, remedies resulting great reduction in the feedback loop between field and Engineering teams.


## Watchdog Monitor

Monitor component is a part of STB Health Monitor which is responsible for interfacing with Prime Home, Alerter or any other Error-Reporting system to find any unusual activities per CPE. The Monitor shall interface with Rule Engine to retrieve the CPE ID to be monitored and make a connection with Prime Home or Alerter to get the OSD raised since the last request made. All the required data is sterilized in a json object and is passed to Analyser module for further processing

### Directory Structure

```
.
`-- Monitor
    |-- dependency.txt
    |-- logs
    |   `-- monitor.log
    |-- README.md
    |-- src
    |   |-- db
    |   |   |-- cpe-status.db
    |   |   |-- cpe_status.py
    |   |   `-- __init__.py
    |   |-- __init__.py
    |   |-- interface
    |   |   |-- analyser
    |   |   |   |-- analyser.py
    |   |   |   `-- __init__.py
    |   |   |-- http_request.py
    |   |   |-- __init__.py
    |   |   |-- logs_db
    |   |   |   |-- __init__.py
    |   |   |   `-- logs_db.py
    |   |   |-- ph_proxy
    |   |   |   |-- __init__.py
    |   |   |   |-- ph.cfg
    |   |   |   `-- ph_proxy.py
    |   |   `-- rule_engine
    |   |       |-- __init__.py
    |   |       |-- rule_engine.cfg
    |   |       `-- rule_engine.py
    |   |-- logger.conf
    |   |-- monitor.json
    |   `-- monitor_main.py
    `-- unit_tests
        `-- test_rules_engine.py
```
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
