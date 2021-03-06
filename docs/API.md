   
# Module `tuyaface` {#tuyaface}

Functionality for communicating with a Tuya device.


    
## Sub-modules

* [tuyaface.aescipher](#tuyaface.aescipher)
* [tuyaface.const](#tuyaface.const)
* [tuyaface.helper](#tuyaface.helper)
* [tuyaface.tuyaclient](#tuyaface.tuyaclient)



    
## Functions


    
### Function `set_state` {#tuyaface.set_state}



    
> `def set_state(device: dict, value, idx: int = 1) -> bool`


Send status update request for one dps value to the tuya device.

returns bool

    
### Function `set_status` {#tuyaface.set_status}



    
> `def set_status(device: dict, dps: dict) -> bool`


Send state update request to the tuya device and waits for response.

returns bool

    
### Function `status` {#tuyaface.status}



    
> `def status(device: dict) -> dict`


Request status of the tuya device.

returns dict




    
# Module `tuyaface.aescipher` {#tuyaface.aescipher}

Helpers for AES crypto.




    
## Functions


    
### Function `decrypt` {#tuyaface.aescipher.decrypt}



    
> `def decrypt(key, enc, use_base64=True)`


Optionally base64-decode and decrypt.

    
### Function `encrypt` {#tuyaface.aescipher.encrypt}



    
> `def encrypt(key, raw, use_base64=True)`


Encrypt and optionally base64-encode.




    
# Module `tuyaface.const` {#tuyaface.const}

Tuya constants.





    
## Classes


    
### Class `CMD_TYPE` {#tuyaface.const.CMD_TYPE}



> `class CMD_TYPE(value, names=None, *, module=None, qualname=None, type=None, start=1)`


Tuya message types.


    
#### Ancestors (in MRO)

* [enum.IntEnum](#enum.IntEnum)
* [builtins.int](#builtins.int)
* [enum.Enum](#enum.Enum)



    
#### Class variables


    
##### Variable `ACTIVE` {#tuyaface.const.CMD_TYPE.ACTIVE}



    
##### Variable `AP_CONFIG` {#tuyaface.const.CMD_TYPE.AP_CONFIG}



    
##### Variable `AP_CONFIG_NEW` {#tuyaface.const.CMD_TYPE.AP_CONFIG_NEW}



    
##### Variable `BIND` {#tuyaface.const.CMD_TYPE.BIND}



    
##### Variable `CONTROL` {#tuyaface.const.CMD_TYPE.CONTROL}



    
##### Variable `CONTROL_NEW` {#tuyaface.const.CMD_TYPE.CONTROL_NEW}



    
##### Variable `DP_QUERY` {#tuyaface.const.CMD_TYPE.DP_QUERY}



    
##### Variable `DP_QUERY_NEW` {#tuyaface.const.CMD_TYPE.DP_QUERY_NEW}



    
##### Variable `ENABLE_WIFI` {#tuyaface.const.CMD_TYPE.ENABLE_WIFI}



    
##### Variable `HEART_BEAT` {#tuyaface.const.CMD_TYPE.HEART_BEAT}



    
##### Variable `LAN_CHECK_GW_UPDATE` {#tuyaface.const.CMD_TYPE.LAN_CHECK_GW_UPDATE}



    
##### Variable `LAN_DELETE_SUB_DEV` {#tuyaface.const.CMD_TYPE.LAN_DELETE_SUB_DEV}



    
##### Variable `LAN_EXPORT_APP_CONFIG` {#tuyaface.const.CMD_TYPE.LAN_EXPORT_APP_CONFIG}



    
##### Variable `LAN_GW_ACTIVE` {#tuyaface.const.CMD_TYPE.LAN_GW_ACTIVE}



    
##### Variable `LAN_GW_UPDATE` {#tuyaface.const.CMD_TYPE.LAN_GW_UPDATE}



    
##### Variable `LAN_PUBLISH_APP_CONFIG` {#tuyaface.const.CMD_TYPE.LAN_PUBLISH_APP_CONFIG}



    
##### Variable `LAN_PUBLISH_CLOUD_CONFIG` {#tuyaface.const.CMD_TYPE.LAN_PUBLISH_CLOUD_CONFIG}



    
##### Variable `LAN_PUBLISH_SCENE_PANEL` {#tuyaface.const.CMD_TYPE.LAN_PUBLISH_SCENE_PANEL}



    
##### Variable `LAN_REMOVE_GW` {#tuyaface.const.CMD_TYPE.LAN_REMOVE_GW}



    
##### Variable `LAN_REPORT_SUB_DEV` {#tuyaface.const.CMD_TYPE.LAN_REPORT_SUB_DEV}



    
##### Variable `LAN_SCENE` {#tuyaface.const.CMD_TYPE.LAN_SCENE}



    
##### Variable `LAN_SET_GW_CHANNEL` {#tuyaface.const.CMD_TYPE.LAN_SET_GW_CHANNEL}



    
##### Variable `LAN_SUB_DEV_REQUEST` {#tuyaface.const.CMD_TYPE.LAN_SUB_DEV_REQUEST}



    
##### Variable `QUERY_WIFI` {#tuyaface.const.CMD_TYPE.QUERY_WIFI}



    
##### Variable `RENAME_DEVICE` {#tuyaface.const.CMD_TYPE.RENAME_DEVICE}



    
##### Variable `RENAME_GW` {#tuyaface.const.CMD_TYPE.RENAME_GW}



    
##### Variable `SCENE_EXECUTE` {#tuyaface.const.CMD_TYPE.SCENE_EXECUTE}



    
##### Variable `STATUS` {#tuyaface.const.CMD_TYPE.STATUS}



    
##### Variable `TOKEN_BIND` {#tuyaface.const.CMD_TYPE.TOKEN_BIND}



    
##### Variable `UDP` {#tuyaface.const.CMD_TYPE.UDP}



    
##### Variable `UDP_NEW` {#tuyaface.const.CMD_TYPE.UDP_NEW}



    
##### Variable `UNBIND` {#tuyaface.const.CMD_TYPE.UNBIND}



    
##### Variable `UNKNOWN` {#tuyaface.const.CMD_TYPE.UNKNOWN}








    
# Module `tuyaface.helper` {#tuyaface.helper}

Helpers.




    
## Functions


    
### Function `bytes2hex` {#tuyaface.helper.bytes2hex}



    
> `def bytes2hex(data: bytes, pretty: bool = False)`


Render hexstring from bytes.

    
### Function `hex2bytes` {#tuyaface.helper.hex2bytes}



    
> `def hex2bytes(data: str)`


Parse hexstring to bytes.




    
# Module `tuyaface.tuyaclient` {#tuyaface.tuyaclient}

Helper to maintain a connection to and serialize access to a Tuya device.





    
## Classes


    
### Class `TuyaClient` {#tuyaface.tuyaclient.TuyaClient}



> `class TuyaClient(device: dict, on_status: <built-in function callable> = None, on_connection: <built-in function callable> = None)`


Helper class to maintain a connection to and serialize access to a Tuya device.

Initialize the Tuya client.


    
#### Ancestors (in MRO)

* [threading.Thread](#threading.Thread)






    
#### Methods


    
##### Method `run` {#tuyaface.tuyaclient.TuyaClient.run}



    
> `def run(self)`


Tuya client main loop.

    
##### Method `set_state` {#tuyaface.tuyaclient.TuyaClient.set_state}



    
> `def set_state(self, value, idx: int = 1) -> dict`


Set state.

    
##### Method `set_status` {#tuyaface.tuyaclient.TuyaClient.set_status}



    
> `def set_status(self, value: dict) -> dict`


Set status.

    
##### Method `status` {#tuyaface.tuyaclient.TuyaClient.status}



    
> `def status(self) -> dict`


Request status.

    
##### Method `stop_client` {#tuyaface.tuyaclient.TuyaClient.stop_client}



    
> `def stop_client(self)`


Close the connection and stop the worker thread.


-----
Generated by *pdoc* 0.8.1 (<https://pdoc3.github.io>).
