# Change settings via API
1. open firefox
2. open debug console (F12)
3. go to Network
4. open new tab and head to 'Manage home network' on [Telenet](<https://www2.telenet.be/residential/nl/mijn-telenet)
5. go to https://api.prd.telenet.be/ocapi/public/api/resource-service/v1/modems/{your-modem-MAC}/advance-settings where you put the MAC address of your modem
6. look in your debug console for the GET request of 'advanced-settings'
7. right click it and click 'edit and resend'
8. a new window 'new request' will appear on the lefthand side, change GET to PATCH
9. leave everything as is and change the settings in the Body payload
10. to add 2 port forwards, use the following format (edit as needed):
```json
{

"patchModemSettingsOperations":

[

{"op":"replace","path":"/portForwards","value":[{"lanIp":"122","internalPortStart":"5000","externalPort":"5000 - 5003","protocol":"BOTH"},{"lanIp":"99","internalPortStart":"100","externalPort":"100 - 100","protocol":"TCP"}]}

],

"portForwards":

[

{"active":true,"description":null,"internalPortStart":5000,"portStart":5000,"portStop":5003,"protocol":{"value":"BOTH"},"lanIp":"122"},

{"active":true,"description":null,"internalPortStart":100,"portStart":100,"portStop":100,"protocol":{"value":"TCP"},"lanIp":"99"}

]

}
```