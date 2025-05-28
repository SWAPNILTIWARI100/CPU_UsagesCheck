# System Monitor


## Overview

This application is a cross-platform desktop system monitoring tool built using C#. It tracks CPU usage, memory usage, and disk space in real-time. It includes plugin support for integrations such as logging to a file and exposing a REST API for external access.
It can also be used to send alerts via email or Telegram if the usage exceeds the upper limit set by the us.(Will add this later)

### 🔗 Executable

The binary of the solution is available [here](https://github.com/pooooo976/Assesment/blob/main/Assesment_Soroco/bin/Debug/net8.0), and you can directly run the application using this [executable](https://github.com/pooooo976/Assesment/blob/main/Assesment_Soroco/bin/Debug/net8.0/Assesment_Soroco.exe).



## Configuration

All application settings are defined in the configuration file:

```xml
<add key="MonitoringInterval" value="3000" />
<add key="HostUrl" value="http://localhost:5000" />
<add key="EnableFileLogging" value="true" />
<add key="EnableApiIntegration" value="true" />
<add key="LogFilePath" value="C:\\QT\\Resource.log" />
```

## Console Output

The application prints system metrics to the console at regular intervals:

```
DateTime CPU: %, Disk: used/total(%), RAM: used/total(%)
2025-05-06 02:16:23 CPU: 8.94%, Disk: 164413.52/187055.2 (87.90%), RAM: 13824/16125 (85.73%)
```

## API Output

When the API endpoint is hit, the following JSON response is returned:

```json
{
  "cpu": "3.41%",
  "ram_used": "13839 MB",
  "disk_used": "164416.25 MB"
}
```

## Log File

The plugin system supports file logging. The log entries are stored in the path defined by the `LogFilePath` key in the configuration:

```
C:\QT\Resource.log
```

## Screenshots

Console Output:

![Console Output] 


![Screenshot 2025-05-06 021408](https://github.com/user-attachments/assets/445c6fa8-d8f5-40b1-b947-aadac7d93cf7)
![Screenshot 2025-05-06 020725](https://github.com/user-attachments/assets/d44177bf-580d-4b63-bc9a-03bf9e3959d8)



![Screenshot 2025-05-06 021821](https://github.com/user-attachments/assets/00e4ae83-a6a3-4996-bece-3a2149a71c61)
![Screenshot 2025-05-06 021812](https://github.com/user-attachments/assets/a7750b5a-62e4-4760-a0c5-b6de2af15ef6)
![Screenshot 2025-05-06 021601](https://github.com/user-attachments/assets/8bef76f2-5948-45cb-b237-c057f4264a0e)



For any additional details, refer to the code or contact me via Linkdin @tiwariswapnil100 (https://www.linkedin.com/in/tiwariswapnil100/)


