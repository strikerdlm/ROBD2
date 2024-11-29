# ROBD2
Repo to get data from the ROBD2 device through serial port

# ROBD2 Command Interface

A Python-based command-line interface for controlling and monitoring ROBD2 (Reduced Oxygen Breathing Device) systems. This application provides comprehensive functionality for calibration, performance monitoring, and flight data logging.

## Features

- **O2 Sensor Calibration**: Calibrate oxygen sensors with room air and 100% O2
- **Performance Monitoring**: Real-time monitoring of O2 concentrations and system performance
- **Flight Data Logging**: Record and save flight simulation data
- **Operating Commands**: Direct control of ROBD2 operations
- **Programming & Configuration**: Create and manage flight profiles
- **Diagnostics**: System status and troubleshooting tools

## Requirements

- Python 3.7+
- pyserial
- rich

## Installation

1. Clone the repository:

`git clone https://github.com/strikerdlm/ROBD2.git`

2. Create a virtual env with conda

  ```bash                                                                                │
  conda create -n myenv python=3.12                                                                 │
  ```  
  ```bash
  conda activate <myvenv>`
  ```

4. Install required packages

 ```bash
`pip install pyserial rich`
 ```

## Usage

Run the application with default settings:

 ```bash
`python COM_serial.py`
 ```

### Command Line Options

- `--port`: Specify COM port (default: COM12)
- `--baudrate`: Set baudrate (default: 9600)
- `--timeout`: Set serial timeout in seconds (default: 1)
- `--debug`: Enable debug logging

Example:

`python COM_serial.py --port COM3 --baudrate 9600 --debug`


## Menu Structure

1. O2 Sensor Calibration
2. Performance Monitoring
3. Flight Data Log
4. Operating Commands
5. Programming & Configuration
6. Diagnostics

## Device Support

Compatible with ROBD2 devices:
- ROBD2-9515
- ROBD2-9516
- ROBD2-9471

## Data Logging

- Performance logs are saved in `performance_logs/`
- Flight data logs are saved in `logs/`
- Debug logs are available when running in debug mode

## Troubleshooting

If you encounter COM port issues:
1. Ensure device is properly connected
2. Verify device drivers are installed
3. Check port permissions
4. Try disconnecting and reconnecting the device
5. Run the program as administrator if necessary

## License

MIT License

## Author

Diego Malpica MD
Aerospace Medicine
