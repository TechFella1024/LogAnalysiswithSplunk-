# Log Analysis with Splunk

## Overview
This project demonstrates log analysis using Splunk to identify login failures, suspicious IP addresses, and error patterns. It includes ingesting logs, creating queries, and visualizing the data with Splunk dashboards.

## Tools Used
- [Splunk Enterprise Free](https://www.splunk.com/)
- Sample Syslog Logs

## Steps
1. Installed and configured Splunk.
2. Uploaded sample log files for analysis.
3. Created queries to identify failed logins, suspicious IP addresses, and error patterns.
4. Visualized results using dashboards.

## Example Queries
- **Failed Login Attempts**:
  ```plaintext
  index="sample_logs" "failed login"
  ```

- **Top IP Addresses with Failed Logins**:
  ```plaintext
  index="sample_logs" "failed login" | stats count by src_ip
  ```

- **Search for Error Patterns**:
  ```plaintext
  index="sample_logs" "error" OR "exception"
  ```

## Screenshots
This section includes visual documentation of the project:

1. **Query in Action**:
   - Shows a Splunk query running and displaying results.
   - Filename: `query_in_action.png`(https://github.com/TechFella1024/LogAnalysiswithSplunk-/blob/main/query_in_action.png)

2. **Failed Login Results**:
   - Highlights failed login attempts and suspicious IP addresses.
   - Filename: `failed_login_results.png`

3. **Dashboard Visualization**:
   - Displays a dashboard showing login trends and top offending IPs.
   - Filename: `dashboard_visualization.png`

## Lessons Learned
- **Log Ingestion**: Learned how to upload and index logs in Splunk.
- **Query Building**: Developed skills to write Splunk queries for analyzing log data.
- **Visualization**: Gained experience creating dashboards for identifying patterns and trends.

## Next Steps
- Analyze more diverse log data sets, such as firewall or application logs.
- Automate log ingestion and analysis using Splunk forwarders.
- Expand dashboards to include alerts for suspicious activity.
