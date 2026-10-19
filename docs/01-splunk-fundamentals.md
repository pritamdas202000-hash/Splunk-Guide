#  Splunk Fundamentals

## What is Splunk?
Splunk is a SIEM platform primarily used for searching, monitoring, and analyzing machine-generated logs and activities via a web interface. In security operations (SOC), it serves as a central SIEM (Security Information and Event Management) platform.

---

## Splunk Architecture
- **Forwarder:** Collects and forwards data or logs from remote systems which are working within the organizations network. Forwarder are of two types: Universal Forwarder (lightweight agent) and Heavy forwarder (can parse data before forwarding).
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

---

## Splunk search and reporting
Splunk search and reporting is a default interface used for searching and analyzing data on the Splunk home page. It has various functionalities which asssist analysts in improving search experience. Key functionalities are described below:
- Search Head: Where analysts put the queies to filter and aggregate log data
- Time Picker: Multiple options to select the timeframe of your search
- Search History: Saves Splunk's search queries that was previously used
- Data Summary: Provides a summary of the hosts, sources, and sourcetypes

<img width="1901" height="716" alt="1" src="https://github.com/user-attachments/assets/87c3ae73-c896-444d-8692-59c09f856ba1" />

---

--- 

## First search and Field sidebar
In splunk index is the database or container for organizing the data. So here our index which stores all the data is 'windowslogs'. And Field sidebar is present in the left panel of the splunk search. The sidebar provides various sections, which are described below: - Selected Fields: The default selected fields. We can select all other fields by clicking on them
- Interesting Fields: Extract all the interesting fields (e.g., Application, AccountName, and many more)
- Numeric Fields (#): This symbol represents fields that contain numerical values
- Alpha-numeric Fields (α): The alpha symbol represents fields that contain strings
- Count: Counts the number of events containing the listed field
You can explore more to extract more fields

<img width="1900" height="880" alt="2" src="https://github.com/user-attachments/assets/06c95c79-18b9-499d-b6b5-171081fb0d59" />
