# Web API

The plugin can use the camera's Web API (http\://localhost:8080/). When using the Web API from the plugin, digest authentication is not required regardless of the wireless LAN mode. (NOTE: Since bugs are found in this part, digest authentication is required for RICOH THETA V firmware v2.50.1 or earlier.) For detailed specifications of the WebAPI, please refer [here](../core/products/theta-api.md)

The Web API can not be used when the plugin controls the camera device using the [Camera API](camera-api.md).

The following are restricted for "RICOH THETA Z1 51GB", "RICOH THETA X" sold in Japan.
* Plugins operation in the client mode
* Developing plugins

For more details see [here](https://topics.theta360.com/en/news/2021-04-28/)

If you are Japan residence and would like to develop plugin using RICOH THETA Z1 51GB or RICOH THETA X, please see [here](https://webform.ricoh.com/form/pub/e00101/support51gb)
