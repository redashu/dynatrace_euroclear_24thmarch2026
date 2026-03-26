# Topic 1: Dynatrace Query Language (DQL)

These tasks test your ability to retrieve and manipulate data from the Grail data lakehouse.

- **Metric Aggregation**: Write a DQL query to fetch the `builtin:host.cpu.usage` metric for the last 2 hours and calculate the average usage grouped by host name.
- **Log Filtering**: Construct a query to fetch logs from the `dt.logs` table where the loglevel is "ERROR" and the message contains the string "timeout".
- **Problem Analysis**: Create a query using the `dt.davis.problems` table to count the total number of active problems in your environment that have an impact level of "SERVICE".
- **Top Consumers**: Write a query to identify the top 5 services based on their request count over the last 24 hours, sorted in descending order.
- **Field Extraction**: Using a sample log record, use the `parse` command to extract a specific JSON field (e.g., `user_id`) into a new column for further analysis.

# Topic 2: Synthetic Monitors

These tasks focus on setting up and tuning simulated user behavior to ensure application health.

- **HTTP Monitor Setup**: Configure a basic HTTP Monitor to check the availability of a specific URL (e.g., `https://example.com`) every 5 minutes from three different global locations.
- **Browser Clickpath**: Create a Browser Clickpath that simulates a login flow: navigate to a URL, enter credentials into specific text fields, and click the "Login" button.
- **Validation Rule**: Add a content validation rule to an existing synthetic monitor to ensure that the text "Welcome" appears on the page after a successful load.
- **Outage Handling**: Configure the outage handling settings for a monitor to only trigger an alert if the monitor fails from at least 2 locations simultaneously.
- **Performance Thresholds**: Set a custom performance threshold for a browser monitor so that a "Slowdown" event is raised if the visually complete time exceeds 3 seconds.

# Topic 3: Dashboards and Notebooks

These tasks test your ability to visualize data and build collaborative reports.

- **Dashboard Tile Creation**: Create a new dashboard and add a Data Explorer tile that charts the "Host Memory Used" for a specific host group over the last 7 days.
- **Notebook Collaboration**: Open a new Notebook, add a DQL block to fetch active problems, and then add a Markdown block below it to explain the findings for a stakeholder.
- **Dynamic Filtering**: Set up a dashboard variable (e.g., for "Management Zone" or "Host Group") so that all tiles on the dashboard update dynamically when the variable is changed.
- **Service Level Visualization**: Add a tile to a dashboard that specifically displays the Apdex score and Failure Rate for a mission-critical web service.
- **SLO Tile Integration**: Configure a Service Level Objective (SLO) for a service (e.g., 99.9% availability) and pin the resulting SLO status tile to a central operations dashboard.
