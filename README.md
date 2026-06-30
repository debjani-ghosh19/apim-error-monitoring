API Error Monitoring with Databricks

Automated daily pipeline that queries Azure Application Insights for API errors (via Azure APIM) and reports failure rates, error counts, and error messages — no manual checking required.

What It Does:

a) Queries AppRequests and AppExceptions tables in Log Analytics via KQL
b) Calculates error counts, failure rates, and average response times per API
c) Saves results to a Delta Lake table in Unity Catalog for historical tracking
d) Runs automatically every day via a scheduled Databricks Job
e) Team queries the table directly in Databricks (read access via Unity Catalog grants)

Job Parameter:
The job takes the run date as a parameter. You can set it as {{job.start_time.iso_date}}

Schedule:
You can schedule it at anytime as per business requirement.
