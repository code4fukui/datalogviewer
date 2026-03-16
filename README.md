# datalogviewer

> 日本語のREADMEはこちらです: [README.ja.md](README.ja.md)

A web-based data log viewer for visualizing pressure and relative altitude data.

## Features
- Displays pressure and relative altitude data in a line chart
- Supports loading CSV files with timestamp, pressure, and relative altitude data
- Automatically adjusts the y-axis scales for each data series
- Provides tooltips with date/time information when hovering over data points

## Requirements
This project uses the following external libraries:
- [ApexCharts.js](https://github.com/apexcharts/apexcharts.js) for creating the line chart
- [DateTime.js](https://github.com/code4fukui/DateTime.js) for date/time manipulation

## Usage
To run the project locally:

1. Clone the repository:
   ```
   git clone https://github.com/code4fukui/datalogviewer.git
   ```
2. Open the `index.html` file in your web browser.
3. Drag and drop a CSV file with timestamp, pressure, and relative altitude data into the browser window.

## Data / API
The project includes a sample CSV file (`Barolog-2025-09-10.csv`) that contains simulated pressure and relative altitude data.

## License
MIT License — see [LICENSE](LICENSE).