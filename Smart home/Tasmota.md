| Device            | web interface                          |
|:----------------- |:-------------------------------------- |
| TasmotaServer1    | [192.168.0.210](http://192.168.0.210/) |
| TasmotaServer2    | [192.168.0.211](http://192.168.0.211/) |
| TasmotaDesk       | [192.168.0.212](http://192.168.0.212/) |
| TasmotaWindow     | [192.168.0.213](http://192.168.0.213/) |
| TasmotaPowerstrip | [192.168.0.214](http://192.168.0.214/) |

# change Tasmota device ip
1. go to device web interface
2. open console
3. ipaddress1 {ip}
4. SetOption19 1

# configure mqtt
1. go to device web interface > configuration > configure mqtt
2. host: {ip of [[homeassistant]] vm}
3. user + password: creds of user configured in [[homeassistant]]
4. keep the rest default