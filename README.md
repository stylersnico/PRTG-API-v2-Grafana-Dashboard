# Grafana dashboard for PRTG API v2
The goal of this repository is to provide instruction to link your Grafana server and your PRTG monitoring server with the new V2 rest API.
It will provide some dashboard to start with.

# Experimental support
Some of the parts of this API are still experimental.
Also, the new PRTG api is available on port 1616 by default and must be enabled.

# Prerequisites
You need to install the Infinity datasource in Grafana.
Please find the latest installation instructions directly on their website: https://grafana.com/grafana/plugins/yesoreyeram-infinity-datasource/?tab=installation

# Configuring the datasource

Create a new datasource "prtg-v2" using the Infinity plugin.
Don't configure the base URL. We will do it on each dashboard.

Configure the **Bearer Token** using a PRTG Api key in read-only.
Then, configure the allowed hosts using your PRTG base URL with port:
<img width="1402" height="928" alt="apiv2-1" src="https://github.com/user-attachments/assets/ddc8bd2b-6db7-43c3-b22a-a45b27014e3f" />

After that, you can configure your Dashboard using this datasource like this example for showing all objects that are down on PRTG with only showing a subset of collumns:
<img width="1775" height="789" alt="apiv2-2" src="https://github.com/user-attachments/assets/402c6cf4-078d-4b50-b295-8152852e51e9" />

You can have the full dashboard in the samples folder for showing current alerts, for example:
<img width="1790" height="768" alt="currents-alerts" src="https://github.com/user-attachments/assets/b8b83a97-7f5e-49cf-90b7-434f4855a0e1" />
