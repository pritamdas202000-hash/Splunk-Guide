# Filtering commands
A network may generate thousands of logs every minute, and all of which are ingested into your SIEM solution. Searching for anomalies can become overwhelming. Splunk's SPL(Search Processing Language) enables analysts to apply filters using search commands to narrow down search results and focus on relevant results. Here are some of the useful filtering commands that organise search results.

---

## Fields
The **fields** commands is used to include or exclude specific fields from your search results. To exclude a fields you can use a minus sign - before the field name.

index=windowslogs | fields host User SourceIp 

<img width="1912" height="888" alt="7" src="https://github.com/user-attachments/assets/58d74fb1-ea64-4541-bb85-4319f57357d9" />

---

---

## Dedup
The **dedup** command is used to remove duplicate values from the search results. For example if logs contains seven distinct Ip addresses in the **SourceIp** field, the results will return seven events, one for each unique IP. This command is useful for identical events.

index=windowslogs | fields Hostname User Image EventID SourceIp | dedup SourceIp

<img width="1915" height="908" alt="8" src="https://github.com/user-attachments/assets/8d5923c5-b65b-4422-97ce-0e9e452408f8" />

---

---

## Rename
The **rename** command allows you to change the name of the fields in your search results. This helps to improve the readability of your search results, especially if the original field name is too long or not suitable.

index = windowslogs | fields EventID User Image Hostname SourceIp | rename User as Employee

<img width="1913" height="893" alt="9" src="https://github.com/user-attachments/assets/c678be82-8d94-4e80-84fc-3435049235f3" />

---

---

## Regex
The **regex** command allows you to filter search results using regular expressions, which match specific text patterns in field values. This is useful when you need to find events that follow a specific format. 

index = windowslogs | regex Image = "\.exe$"

The query above applies a regular expression to the **Image** field, will return only events where the field value ends with .exe. The **$** symbol specifies that the match must occur at the end of the string.

<img width="1917" height="890" alt="10" src="https://github.com/user-attachments/assets/a37de0a2-4af5-4ff4-9152-14fd3ca45bd7" />
