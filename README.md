# Project Overview
Ve.Direct.InfluxDB.Collector is a dedicated data collector that bridges the gap between Victron SmartSolar MPPT devices and InfluxDB. The primary aim of this project is to collect, process, and store data from Victron SmartSolar MPPT devices using the Ve.Direct protocol into an InfluxDB database. The resulting dataset can then be visualized using a Grafana dashboard, providing users with a detailed, real-time overview of their solar energy system's performance.

[![Maintainability Rating](https://sonarcloud.io/api/project_badges/measure?project=DocBrown101_Ve.Direct.InfluxDB.Collector&metric=sqale_rating)](https://sonarcloud.io/dashboard?id=DocBrown101_Ve.Direct.InfluxDB.Collector)
[![Lines of Code](https://sonarcloud.io/api/project_badges/measure?project=DocBrown101_Ve.Direct.InfluxDB.Collector&metric=ncloc)](https://sonarcloud.io/dashboard?id=DocBrown101_Ve.Direct.InfluxDB.Collector)
[![Security Rating](https://sonarcloud.io/api/project_badges/measure?project=DocBrown101_Ve.Direct.InfluxDB.Collector&metric=security_rating)](https://sonarcloud.io/dashboard?id=DocBrown101_Ve.Direct.InfluxDB.Collector)

![Preview](https://github.com/DocBrown101/Ve.Direct.InfluxDB.Collector/blob/main/docs/image1.jpg)

![Preview](https://github.com/DocBrown101/Ve.Direct.InfluxDB.Collector/blob/main/docs/image2.jpg)

## Requirements
To run the Ve.Direct.InfluxDB.Collector, you will need:
* Grafana and InfluxDB docker images
* [The matching Grafana Dashboard](https://grafana.com/grafana/dashboards/14597)
* [A Victron SmartSolar charge controller](https://www.victronenergy.com/solar-charge-controllers)
* A Raspberry Pi or a 24/7 running PC with .NET or MONO and a serial port
* A Ve.Direct cable for connecting the Victron device to the Raspberry Pi or PC

If there are only a few centimeters between the MPPT and the Raspberry Pi, no USB adapter from Victron is needed!

![Preview](https://github.com/DocBrown101/Ve.Direct.InfluxDB.Collector/blob/main/docs/No-VEDirect-USB.jpg)

![Preview](https://github.com/DocBrown101/Ve.Direct.InfluxDB.Collector/blob/main/docs/Connect-VEDirect-To-RPi.jpg)

## Example Usage
```
/path/to/Ve.Direct.InfluxDB.Collector.exe -o Influx
```

You can alternatively run this as a crontab.
```
@reboot /usr/bin/mono -- /path/to/Ve.Direct.InfluxDB.Collector.exe -o Influx >> /var/log/cron.log 2>&1
```

## Future Plans
I am always working on improving Ve.Direct.InfluxDB.Collector and adding more features, so I welcome contributions and suggestions from the community to improve the functionality of this tool and make it even more useful for all users.

Inspired by https://github.com/oyebayo/vedirect
