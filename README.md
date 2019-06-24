
# Prometheus playground

This is Prometheus playground. 

Usage:

    vagrant up

check: http://localhost:9100/metrics to see the Prometheus node exporter
check: http://localhost:9090/ to see the Prometheus itself

## Example query

Show CPU usage 

    sum without (cpu) (rate(node_cpu_seconds_total{mode!="idle"}[5m]) * 100)

Check if the scrape of host `default` succeeded

    up{instance="default",job="node"}

Show scrape duration and number of scrapes

    scrape_duration_seconds{instance="default",job="node"}

    scrape_samples_scraped{instance="default",job="node"}

## Disclaimer

This is internal testing host. Use as you need.
