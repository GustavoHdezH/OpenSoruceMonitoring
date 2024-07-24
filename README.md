<div align="center">
    <img  width="200" height="200" src="/docs/Monitoring.png">
</div>
<div> 
  <h1 align="center">Open Source Monitoring</h1>
  <p>
    Free and Open source monitoring configuration template for setting up Prometheus, Node Exporter, PostgreSQL Exporter,
    Windows Exporte, Grafana, and cAdvisor using Docker Compose.
  </p>
</div>

## Steps to create 

* You will need install Docker and docker-compose in your environment
* Also, install necessary dependencies

*Note: this document explains how to configure grafana on a master server and prometheus, node-exporter on servers to 
observe*

## Master Server

This server will be hosted grafana and tools, and we will assign it any IP for this example, in this case it will be 
assigned IP **10.10.10.3**.

* Grafana deployment on port 8010
* Prometheus deployment on port 8011
* Node-Exporter deployment on port 8012
* Cadvisor deployment on port 8013
* PostgreSQL Exporter deployment on port 8014

*Note: Replace the IP and ports with those available in your environment*

## Target Server

This server will be hosted node-exporter cadvisor, and we will assign it any IP for this example, in this case it will
be assigned IP **10.10.10.4**.

* Prometheus deployment on port 8011
* Node-Exporter deployment on port 8012

*Note: Replace the IP and ports with those available in your environment*

## Windows Server

This server will be hosted windows exporter, and we will assign it any IP for this example, in this case it will
be assigned IP **10.10.10.5**.

* [Download windows exporter][windows]

*Note: Make sure the windows exporter service is running on your server*

---

## Fire it up

1. Clone down the example files
2. Create directories for the tools.
3. Replace ports, networks and IPs with those available in your environment
4. Navegate to the apps folder and issue the command docker-compose up -d

---

<div align="center"> 
  <p>
    Made with &hearts; by ghernandez  |   2020-2024
  </p>
</div>

<!-- Home links for this document -->
[windows]: https://github.com/prometheus-community/windows_exporter?tab=readme-ov-file
<!-- End of links for this document -->
