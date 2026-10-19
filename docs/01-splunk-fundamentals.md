#  Splunk Fundamentals

## What is Splunk?
Splunk is a SIEM platform primarily used for searching, monitoring, and analyzing machine-generated logs and activities via a web interface. In security operations (SOC), it serves as a central SIEM (Security Information and Event Management) platform.

---

## Splunk Architecture
- **Forwarder:** Collects and forwards data or logs from remote systems which are working within the organizations network. Fprwarder are of two types: Universal Forwarder, lightweight agent and heavy forwarder, this can parse data before forwarding.
- **Indexer:** Indexer receives forwarded logs, parses and process them, convert into standard format so that analyst can analyse it and troubleshoot the problem.
- **Search Head:** Search Head is the UI where analyst put the queries to filter and visualise the log data.

---

## The Metadata Fields
Every event indexed in Splunk is tagged with:
- `index`: Act as a storage container for the data/logs (e.g., `index=windowslog`).
- `sourcetype`: Tells what kind of data splunk is receiving (e.g., `sourcetype=syslog`).
- `source`: The location or port from which data is originated (e.g., `/var/log/auth.log`).
- `host`: The machine name or IP that generated the logs.

---
