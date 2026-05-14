# datalogviewer

> 日本語のREADMEはこちらです: [README.ja.md](README.ja.md)

A web-based viewer that generates interactive, dual-axis line charts from time-series data in CSV files. Simply drag and drop a file to visualize it.

## Live Demo

This viewer was created for the blog post: **[data log viewer for iOS App of Barometer](https://fukuno.jig.jp/4795)**


![datalogviewer screenshot showing a dual-axis line chart with pressure on the left y-axis and relative altitude on the right y-axis, plotted against a time-based x-axis.](https://fukuno.jig.jp/img/datalogviewer.png)


## Features

-   **Instant Visualization:** Drag and drop a CSV file to automatically generate a chart.
-   **Multi-Series Plotting:** Automatically plots all numeric columns from the CSV against the `timestamp` column.
-   **Dual Y-Axis:** Renders a dual-axis chart when two data columns are present (e.g., pressure and altitude), with each series getting its own independent y-axis.
-   **Gap Detection:** Intelligently identifies time gaps greater than 10 seconds in the data and displays them as breaks in the line chart.
-   **Interactive Tooltips:** Hover over data points to see precise timestamp and value information.
-   **Smart Scaling:** Automatically adjusts y-axis ranges to fit the data and uses clean, readable scales.

## Usage

1.  Clone the repository:
    ```bash
    git clone https://github.com/code4fukui/datalogviewer.git
    ```
2.  Open the `index.html` file in a web browser.
3.  Drag and drop your CSV file onto the page.

The viewer loads with the sample `Barolog-2025-09-10.csv` by default.

### CSV File Format

The CSV file must contain a header row with the following structure:

-   One column must be named `timestamp` and contain ISO 8601 formatted strings (e.g., `2025-09-10T06:58:05Z`).
-   All other columns should contain numeric data.

**Example:**
```csv
timestamp,pressure_hPa,relative_altitude_m
2025-09-10T06:58:05Z,1010.2,0.000
2025-09-10T06:58:06Z,1010.2,-0.127
...
```

## Dependencies

-   [ApexCharts.js](https://github.com/apexcharts/apexcharts.js) for creating interactive charts.
-   [CSV.js](https://js.sabae.cc/CSV.js) for parsing CSV files in the browser.
-   [DateTime.js](https://github.com/code4fukui/DateTime.js) for date and time manipulation in tooltips.

## License

[MIT](LICENSE)