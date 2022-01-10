---
title: InfluxDB (Database service)
slug: influxdb
section: Services
---

**Last updated 7th January 2022**


## Objective  

InfluxDB is a time series database optimized for high-write-volume use cases such as logs, sensor data, and real-time analytics.


It exposes an HTTP API for client interaction. See the [InfluxDB documentation](https://docs.influxdata.com/influxdb) for more information.

## Supported versions

| **Grid** |  **Dedicated Generation 3** |
|----------------------------------|  
|  1.2 |  
|  1.3 |  
|  1.7 |  
|  1.8 |  

## Relationship

The format exposed in the ``$PLATFORM_RELATIONSHIPS`` [environment variable](../../development-variables#platformsh-provided-variables):

```json  
{
    "service": "influxdb18",
    "ip": "169.254.229.191",
    "hostname": "duqbjfn7t4dwr2fi2o7bsvqafy.influxdb18.service._.eu-3.platformsh.site",
    "cluster": "rjify4yjcwxaa-master-7rqtwti",
    "host": "influxdb.internal",
    "rel": "influxdb",
    "scheme": "http",
    "type": "influxdb:1.8",
    "port": 8086
}
```  

## Usage example

In your `.platform/services.yaml`:


```yaml   
timedb:
    type: influxdb:1.8
    disk: 256
```  


In your `.platform.app.yaml`:


```yaml   
relationships:
    influxtimedb: "timedb:influxdb"
```  




You can then use the service in a configuration file of your application with something like:

```php
<?php
// This assumes a fictional application with an array named $settings.
if (getenv('PLATFORM_RELATIONSHIPS')) {
	$relationships = json_decode(base64_decode($relationships), TRUE);

	// For a relationship named 'influxtimedb' referring to one endpoint.
	if (!empty($relationships['influxtimedb'])) {
		foreach ($relationships['influxtimedb'] as $endpoint) {
			$settings['influxdb_host'] = $endpoint['host'];
			$settings['influxdb_port'] = $endpoint['port'];
			break;
		}
	}
}
```

## Exporting data

InfluxDB includes its own [export mechanism](https://docs.influxdata.com/influxdb/v1.2/tools/influx_inspect/).  To gain access to the server from your local machine open an SSH tunnel with the Web PaaS CLI:

```bash
webpaas tunnel:open
```

That opens an SSH tunnel to all services on your current environment and produce output like the following:

```bash
SSH tunnel opened on port 30000 to relationship: influxtimedb
```

The port may vary in your case.  Then, simply run InfluxDB's export commands as desired.

```bash
influx_inspect export -compress
```
