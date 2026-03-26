# Advanced DQL (Dynatrace Query Language)

**Focus:** Data manipulation and specific entity relationships.

- **Averaging Metrics:** Write a DQL query to calculate the average `cpu.usage` for all hosts, grouped by `dt.entity.host`, and filter for only those where the average is greater than 70%.
- **Log Expansion:** Fetch logs from the legacy bucket, find entries where the status is "failed," and use the `expand` command to flatten a nested JSON field (if present) into individual columns.
- **Time Series Analysis:** Create a query that fetches `builtin:service.response.time` and displays it as a time series with 5-minute bins for the last 6 hours.
- **Combining Filters:** Write a query that fetches logs where `dt.process_group.name` contains "Java" AND the log message does NOT contain the word "ignore."
- **Entity Mapping:** Query the `dt.entity.service` table to list all services that have a `software_technology` of "Spring Boot."

# Synthetic Monitoring (Advanced Scenarios)

**Focus:** Troubleshooting and specific configuration tweaks.

- **Maintenance Windows:** Create a Synthetic monitor for a test URL, then navigate to Settings and configure a "Maintenance Window" that suppresses alerts every Sunday from 2:00 AM to 4:00 AM.
- **Content Validation (Regex):** Set up an HTTP monitor that checks a specific page and fails if the text "System Online" is not found using a Regular Expression match.
- **Cookie Handling:** Configure a Browser monitor that requires a specific cookie (Name: `exam_user`, Value: `certified`) to be injected before the page loads.
- **Retry Logic:** Modify an existing monitor's settings so that it only generates a problem ticket if the monitor fails from all assigned locations simultaneously.
- **Request Timeout:** Create an HTTP monitor and set a custom "Request timeout" of 10,000ms (10 seconds) instead of using the default value.

# Dashboards & Notebooks (Analysis & Sharing)

**Focus:** Advanced visualization and root cause layout.

- **Honeycombs for Health:** Build a Dashboard tile using the Honeycomb visualization to show the "Availability" of all Applications. Color-code it so that 100% is green and anything less is red.
- **Markdown with Links:** In a Notebook, add a Markdown cell that contains a functional hyperlink to the "Problems" feed filtered by "Critical" severity.
- **Multi-Metric Charts:** Create a single Dashboard chart that overlays two different metrics: Service Request Count and Service Error Count to visualize their correlation.
- **Top List Filtering:** Create a "Top List" tile that shows the top 5 Processes consuming the most memory, filtered to only include processes running on "Linux" hosts.
- **USQL to DQL Migration:** Take a simple User Session Query like `SELECT count(*) FROM usersession` and recreate the equivalent visualization in a Notebook using a DQL query on the `user_sessions` table.
