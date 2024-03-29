![Grafana Dashboard](/img/Dashboard.png)

# Docker Prometheus Blackbox Exporter Config Example
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

    ```
    git clone https://github.com/taufiqpsumarna/Docker-Prometheus-Blackbox-Exporter.git
    ```

2. Navigate to the project directory:

    ```
    cd Docker-Prometheus-Blackbox-Exporter
    ```

3. Update Prometheus configuration (`prometheus.yml`) and Blackbox Exporter configuration (`blackbox.yml`) with your specific settings.

4. Create persistent data volume for storing prometheus data

    First create a folder for the volume on the host machine, e.g.:

    ```
    mkdir ./data/prometheus
    ```

    Then change the folder owner to nobody, like (use sudo if needed):
    ```
    chown 65534:65534 ./data/prometheus
    ```

4. Run Docker Compose to start Prometheus and Blackbox Exporter:

    ```
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
- You can use Dashboard below:
    - # Blackbox Exporter (HTTP prober)
      ![Blackbox Exporter (HTTP prober](/img/Dashboard_1.png)
       - [Blackbox Exporter (HTTP prober)](https://grafana.com/grafana/dashboards/13659-blackbox-exporter-http-prober/)
    
    - # Prometheus Blackbox Exporter
      ![Prometheus Blackbox Exporter](/img/Dashboard_2.png)
        - [Prometheus Blackbox Exporter](https://grafana.com/grafana/dashboards/14928-prometheus-blackbox-exporter/)
    
    - # Prometheus Blackbox Exporter
      ![Prometheus Blackbox Exporter](/img/Dashboard_3.png)
       - [Prometheus Blackbox Exporter](https://grafana.com/grafana/dashboards/7587-prometheus-blackbox-exporter/)
- Or Using modified version by me here [Modified Grafana Dashboard](dashboard.json)

## Additional Information

- For more details on Prometheus: [Prometheus Documentation](https://prometheus.io/docs/introduction/overview/)
- For more details on Blackbox Exporter: [Blackbox Exporter GitHub](https://github.com/prometheus/blackbox_exporter)

Feel free to customize the configurations and settings according to your monitoring requirements.


Reference:
- [Grafana Dashboard](https://grafana.com/grafana/dashboards/14928-prometheus-blackbox-exporter/)
- [Medium](https://blog.devops.dev/prometheus-blackbox-exporter-with-kube-prometheus-stack-23a045ccbab2)