
# Shelly Plug Wi-Fi Connection Manager

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Windows](https://img.shields.io/badge/Windows-0078D6?style=for-the-badge&logo=windows&logoColor=white)
![PyCharm](https://img.shields.io/badge/pycharm-143?style=for-the-badge&logo=pycharm&logoColor=black&color=black&labelColor=green)

This utility streamlines the process of connecting multiple devices to Wi-Fi by automating the entry of network credentials. It scans for Wi-Fi networks, connects devices, and logs the status of each connection attempt into a CSV file.

## Highlight

- **Features**: Automating Wi-Fi connections and generating reports.
- **Installation**: Steps to set up the necessary environment.
- **Getting Started**: Initial configuration before running the program.
- **Usage**: Guidelines on how to use the program.
- **Execution**: The workflow from start to finish.
- **Error Handling**: How the program deals with potential issues.
- **Maintenance**: Information about software maintenance.
- **Testing**: Instructions for running unit tests.

## Features

- Batch process Wi-Fi connections for multiple devices.
- Auto-retry mechanism for devices that fail to connect on the first attempt.
- Generates a CSV report detailing the connection status of each device.

## Installation

To set up the necessary environment for the program, install the following packages using pip:

```sh
pip install requests pandas
```

## Getting Started

Before running the program, ensure the `connect_device_to_wifi("device_name")` function is invoked in the main routine.

### Usage

1. Provide the customer name and workspace ID when prompted.
2. All input is treated as strings, even numerical values.

### Execution

The program follows these steps:

1. Retrieves Wi-Fi credentials via a GET request to the workspace server.
2. Attempts to connect to the device twice if the first attempt fails.
3. Posts updated device configurations to the server.
4. Generates a CSV report with the outcomes of the connection attempts.

## Error Handling

The program includes exception handling for various potential issues, such as:

- Wi-Fi list access errors.
- Connection failures to devices or servers.
- Fallback to a backup Wi-Fi network if the primary credentials are not provided.

## Maintenance

This software is maintained by NNE. All rights reserved.

## Testing

Unit tests are provided to ensure the functionality works as expected. Run the tests using the following command:

```sh
python -m unittest discover
```

## Program Entry Point

The main program is designed to be user-friendly. Invoke the `connect_device_to_wifi` function with the appropriate parameters to start the process.

```python
# Main execution
if __name__ == '__main__':
    connect_device_to_wifi("shelly")
```
