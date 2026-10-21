# Search operators
Splunk's Search Processing Language (SPL) is behind every search in Splunk. It combines commands, functions, and operators that allow you to filter, transform, and analyze data from your logs.

---

## Relational operators
These operators are used to filter, remove, and refine your search results based on the specified criteria. Below, are examples of relational operators:
- Equals (=): e.g., **UserName=Mark**, Searches all the events in which **UserName** field is equal to **Mark**
- Not Equal To (!=): e.g., **UserName!=Mark**, Finds all the events in which **UserName** is not equal to **Mark**
- Less Than (<): e.g., **Age<12**, All the events where **Age** is less than **12**
- Less Than or Equal To (<=): e.g., **Age<=12**, Searches all events where **Age** is less than or equal to **12**
- Greater Than (>): e.g., **Outbound_Traffic>50**, Events with **Outbound_Traffic** greater than **50**
- Greater Than or Equal To (>=): e.g., **Outbound_Traffic>=50**, All the events with **Outbound_Traffic** is greater than or equal to **50**

- <img width="1917" height="902" alt="3" src="https://github.com/user-attachments/assets/38ee513f-8c9c-4bfd-9e7d-5e31082381bf" />

---

## Logical operators
Logical operators can be used to connect or modify conditions and can operate on Boolean values. Below, are examples of logical operators:
- NOT: e.g., **NOT UserName=\***, Returns events where **Username** is not present
- AND: e.g., **UserName=David AND IPAddress=10.10.10.10**, Returns events with **UserName** equal to **David** and **IPAddress** equal to **10.10.10.10**
- OR: e.g., **UserName=David OR UserName=John**, Returns all the events which has **UserName** equal to **David** or **UserName** equal to **John**
- IN: e.g., **UserName IN(David,John)**, This operator is an **alternative** of **OR** operator

<img width="1915" height="877" alt="4" src="https://github.com/user-attachments/assets/32b5688e-8a7b-41a0-9ed5-14630b4062b3" />

---

---

## Wildcards operators
In Splunk, a wildcard is a special character (*) used to match multiple characters in a search. It helps to find events without knowing the values. Some examples are drawn below:
- status=\*fail\*: This will return all events that have status field set to failed, failure, appfail, etc.
- DestinationIp=172.*: This will return all events that contain values like DestinationIp=172.90.0.1 or DestinationIp=172.18.5.22
- file=*.log: Matches log files (e.g., access.log, error.log, etc.)
- host=web*: Matches host machines (e.g., web01, webserver, etc.)

<img width="1917" height="891" alt="5" src="https://github.com/user-attachments/assets/86920223-bcf9-4651-a439-9d5ede9848c1" />

---

<img width="1913" height="897" alt="6" src="https://github.com/user-attachments/assets/b88f4f65-902b-4949-86fc-650e671c4b7c" />

---
