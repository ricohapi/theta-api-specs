# Get Options

### Service

b6ac7a7e-8c01-4a52-b188-68d53df53ea2

### Characteristic

7cffaae3-8467-4d0c-a9dd-7f70b4f52863

### Format

utf8s

### Overview

Acquires current settings of Theta.

### Properties

| Property | Requirement |
|:--|:--|
| Read | true |
| Write | true |
| Notify | true for THETA X<br>false for THETA Z1 |

### How to Use

1. Write a request like following.

    ```
    {
        "optionNames": [
            "_camerPower",
            "captureMode"
        ]
    }
    ```

    ```
    {
        "optionNames": [
            "_defaultWifiPassword"
        ]
    }
    ```

2. Read or Receive notify a response like following.

    ```
    {
        "userName": "THETAYR12345678",
        "captureMode": "image"
    }
    ```

    ```
    {
        "_defaultWifiPassword": "abcd1234"
    }
    ```
