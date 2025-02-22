# Test data

## Overview

This folder contains some tarballs that have been generated by the 'generate_sample_tarballs.sh' script
and that allow to reproduce almost-perfectly the /proc and /sys/fs/cgroup hierarchies generated by the
Centos7 Linux 3.10.0 kernel on x86_64 platforms.
This is used for unit-testing the cmonitor_collector source code and verify that no regressions are
ever introduced in the handling of such file hierarchies.

## About sampled process

In this test the /proc and /sys/fs/cgroup hierarchies generated for a Redis server running inside a Docker
container have been "frozen" into the sampleXYZ.tar.gz files.

## About each sample

Sample#1: 
 initialization sample, with redis-server idle

Sample#2: 
 another sample with redis-server idle; this will trigger first cmonitor_collector output with CPU usages close to 0%.
 Immediately after this sample is produced, Redis server is loaded with a lot of commands to increase its CPU usage

Sample#3: 
 this sample will reveal that since last sample Redis has used close to 90% CPU usage in user/kernel space (90% being
 the max allowed cpu usage in its cpuacct cgroup).
 Immediately after this sample is produced, Redis server load is removed.

Sample#4: 
 this sample will show again close to 0% CPU usage

