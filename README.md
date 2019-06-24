
# Prometheus playground

This is Prometheus playground. 

Usage:

    vagrant up

check: http://localhost:9100/metrics to see the Prometheus node exporter
check: http://localhost:9090/ to see the Prometheus itself

## Example query

Show CPU usage 

    sum without (cpu) (rate(node_cpu_seconds_total{mode!="idle"}[5m]) * 100)

## Disclaimer

This is internal testing host. Use as you need.
