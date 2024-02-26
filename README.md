![Grafana Dashboard](/img/Dashboard.png)

# Docker-Prometheus-Blackbox-Exporter
Docker Prometheus Blackbox Exporter Config Example

This repository contains configurations and instructions for setting up Prometheus and Blackbox Exporter to monitor your websites.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Usage](#usage)
- [Configuration](#configuration)
- [Docker Compose](#docker-compose)
- [Additional Information](#additional-information)

## Prerequisites

- Docker installed on your system.
- Basic understanding of Prometheus and Blackbox Exporter concepts.

## Usage

1. Clone this repository:

    ```bash
    git clone https://github.com/taufiqpsumarna/Docker-Prometheus-Blackbox-Exporter.git
    ```

2. Navigate to the project directory:

    ```bash
    cd Docker-Prometheus-Blackbox-Exporter
    ```

3. Update Prometheus configuration (`prometheus.yml`) and Blackbox Exporter configuration (`blackbox.yml`) with your specific settings.

4. Run Docker Compose to start Prometheus and Blackbox Exporter:

    ```bash
    docker-compose up -d
    ```

5. Open Prometheus web interface in your browser: [http://localhost:9090](http://localhost:9090)

6. Explore metrics and set up alerts based on your requirements.

## Configuration

### Prometheus Configuration (`prometheus.yml`)

- Modify `prometheus.yml` to adjust scrape intervals, targets, and other settings.
- Add or modify jobs as needed.

### Blackbox Exporter Configuration (`blackbox.yml`)

- Modify `blackbox.yml` to specify the websites you want to monitor.
- Adjust prober modules and timeouts based on your monitoring requirements.

## Docker Compose

The provided `docker-compose.yml` file sets up Prometheus and Blackbox Exporter containers.

- Adjust port mappings and volumes in `docker-compose.yml` as needed.
- Make sure to replace the example URLs in `blackbox.yml` with the actual websites you want to monitor.

## Grafana Dashboard
- You can use [Grafana Dashboard](https://grafana.com/grafana/dashboards/14928-prometheus-blackbox-exporter/)
- Or Using modified version by me here [Modified Grafana Dashboard](dashboard.json)

## Additional Information

- For more details on Prometheus: [Prometheus Documentation](https://prometheus.io/docs/introduction/overview/)
- For more details on Blackbox Exporter: [Blackbox Exporter GitHub](https://github.com/prometheus/blackbox_exporter)

Feel free to customize the configurations and settings according to your monitoring requirements.


Reference:
- [Grafana Dashboard](https://grafana.com/grafana/dashboards/14928-prometheus-blackbox-exporter/)
- [Medium](https://blog.devops.dev/prometheus-blackbox-exporter-with-kube-prometheus-stack-23a045ccbab2)