# 01. Splunk Fundamentals

## 1. What is Splunk?
Splunk is a data analytics platform primarily used for searching, monitoring, and analyzing machine-generated big data via a web-style interface. In security operations (SOC), it serves as a central SIEM (Security Information and Event Management) platform.

---

## 2. Core Architecture
- **Forwarder:** Collects and forwards data from remote systems (Universal Forwarder or Heavy Forwarder).
- **Indexer:** Parses, formats, indexes, and stores raw data on disk.
- **Search Head:** Provides the UI for querying, visualizing data, and managing alerts.

---

## 3. The 4 Essential Metadata Fields
Every event indexed in Splunk is tagged with:
- `index`: Storage repository for the data (e.g., `index=security`).
- `sourcetype`: Structure/format definition of the data (e.g., `sourcetype=syslog`).
- `source`: The physical location or port from which data originated (e.g., `/var/log/auth.log`).
- `host`: The machine name or IP that generated the event.

---

## 4. Search Best Practices for Beginners
1. **Always specify an index:** Avoid running blind searches across all data; use `index=<target_index>`.
2. **Filter early:** Place filters at the beginning of the search pipeline before piping (`|`) to commands.
3. **Control your time range:** Never search `All Time` in production environments; constrain queries to the minimum window needed.
