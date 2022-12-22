# Python CICFlowMeter + GOOSE

> This project is aimed to the capture of GOOSE (Generic Object Oriented Substation Event) packets detailed by the IEC61850 standard. The basis to build this application is take from this cloned from [Python Wrapper CICflowmeter](https://github.com/datthinh1801/cicflowmeter). Furthermore, the application was modified to custom the needs for the Cibersecurity project from the GITA research group from the University of Antioquia.


### Installation
```sh
https://github.com/SantiagoGuiral/GooseFlowMeter.git
cd cicflowmeter
python3 setup.py install
```

### Usage
```sh
usage: cicflowmeter [-h] (-i INPUT_INTERFACE | -f INPUT_FILE) [-c] [-u URL_MODEL] output

positional arguments:
  output                output file name (in flow mode) or directory (in sequence mode)

optional arguments:
  -h, --help            show this help message and exit
  -i INPUT_INTERFACE    capture online data from INPUT_INTERFACE
  -f INPUT_FILE         capture offline data from INPUT_FILE
  -c, --csv, --flow     output flows as csv
```

Convert pcap file to flow csv:

```
cicflowmeter -f example.pcap -c flows.csv
```

Capture packets real-time from interface to flow csv: (**need root permission**)

```
cicflowmeter -i eth0 -c flows.csv
```

- Reference: https://www.unb.ca/cic/research/applications.html#CICFlowMeter
- Reference: https://github.com/cutaway-security/goosestalker
- Contact: santiago.riosg@udea.edu.co 
