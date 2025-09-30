# Web API

The plugin can access the [THETA Web API v2.1](../theta-web-api-v2.1/README.md) via `http://localhost:8080/`.  
When the plugin uses the Web API to communicate with localhost, digest authentication is not required, regardless of the wireless LAN mode.  

> [!IMPORTANT]  
> Due to known bugs, digest authentication is required on RICOH THETA V with firmware version 2.50.1 and earlier.  

> [!NOTE]
> Some Web API functions cannot be used while the plugin has control of the camera resources via the [Camera API](camera-api.md).    

> [!NOTE]
> Some Web API functions e.g. video recording cannot be used by plugin for THETA X.  

> [!WARNING]  
> The following features are restricted on the "RICOH THETA Z1 51GB" and "RICOH THETA X" models sold in Japan:  
> 
> * Plugin operation in WLAN client mode  
> * Plugin development  
> 
> For more details, please see [here](https://topics.theta360.com/en/news/2021-04-28/).  
> If you reside in Japan and would like to develop plugins using the RICOH THETA Z1 51GB or RICOH THETA X, please see [here](https://webform.ricoh.com/form/pub/e00101/support51gb).  
