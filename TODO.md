## TODO collector-side

- Add 'blkio' cgroup data collection
- Add benchmarks to see if fscanf() is actually slower compared to string2int() to optimize CPU usage
- Add support for UDP data tx to InfluxDB

## TODO chart-side

- Add javascript buttons to toggle graphs for e.g. disks/networks/cpus
- Add 'blkio' cgroup data plotting
- Plot CPU "counters" JSON section

## TODO testing/documentation

- Add tests on:
   CMonitorSystem
   -> challenge is it uses "lsblk" and "ifconfig" utilities, does not just read the filesystem!
   CMonitorHeaderInfo

- add more sampled data for CMonitorCGroup, for several kernels
- test more configurations for CMonitorCGroup
- Test deployment on supported Linux distributions
- Add LXC examples

## TODO influxdb/grafana

- Provide a nice dashboard to get started
