# Dynatrace Exam Tips - Lab 2

## 1. Dynatrace Query Language (DQL)

**Focus:** Fetching logs/events, filtering, and basic aggregation in Logs and Grails.

- **Filtering by Level:** Write a query to fetch all logs from the last 2 hours where the status is ERROR, then sort them by the most recent timestamp.
- **Counting Records:** Fetch logs for a specific process group and use the `summarize` command to count the number of log entries per loglevel.
- **Pattern Matching:** Query logs to find all entries containing the string "timeout" within the content field, excluding any logs from the "Production" environment tag.
- **Parsing Data:** Fetch a log stream and use the `parse` command to extract a specific IP address from a raw log message into a new column named `client_ip`.
- **Field Selection:** Fetch entries from the `dt.entity.host` table and display only the `display_name`, `cpu_cores`, and `memory_total` columns.

## 2. Synthetic Monitoring

**Focus:** Creating monitors that simulate user behavior and checking availability.

- **HTTP Monitor Setup:** Create an HTTP monitor for `https://example.com`. Set the frequency to 5 minutes and ensure it triggers an alert if the response code is anything other than 200.
- **Browser Clickpath:** Record or script a 3-step clickpath: Navigate to a URL, click a "Login" button (by CSS selector), and validate that the text "Welcome" appears on the final page.
- **Performance Thresholds:** Configure an existing Synthetic monitor to fail if the "Total duration" of the page load exceeds 3 seconds for three consecutive runs.
- **Private Synthetic Locations:** Set up a monitor that executes only from a specific "Private Location" (ActiveGate) rather than a public Dynatrace cloud location.
- **Header Configuration:** Create an HTTP request monitor that passes a custom Authorization header and validates a specific JSON property in the response body.

## 3. Dashboards & Notebooks

**Focus:** Data visualization, sharing, and troubleshooting layouts.

- **Data Explorer Visualization:** Create a dashboard tile that shows the "Host CPU Usage %" for all hosts tagged with `Environment:Dev`. Change the visualization type to a Top List.
- **Dynamic Filtering:** Create a Dashboard with a "Variable" (Filter) that allows a user to switch between different Services and have all tiles on the dashboard update automatically.
- **Notebook Documentation:** Create a Notebook that includes a Markdown cell explaining a service's health, followed by a DQL cell that pulls that service's error rate for the last 24 hours.
- **SLA Reporting:** Build a dashboard tile using the "Service Availability" metric and display it as a Big Number for the last 7 days.
- **Sharing & Permissions:** Configure a Dashboard so it is "Visible to everyone" in the environment but "Editable" only by the Admin group.

### Pro-Tip for the Exam

> The hands-on environment is often a live, sandboxed tenant. Make sure you are comfortable using the Global Search (<kbd>Cmd</kbd>+<kbd>K</kbd> or <kbd>Ctrl</kbd>+<kbd>K</kbd>); it is the fastest way to find specific hosts, services, or settings without clicking through the sidebar.
