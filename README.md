# solaxInverter
Pulls info from Solar inverter over local http. Does not require an internet connection.
There are two strings that can be pulled form the inverter. History and Realtime.

## Files
These are flow files for node-red. Either copy the file to your Node-Red Directory or copy the contetns and then Import>From Clipboard to import into your flow.

`history.json` is a small summary.
`realtimeData.json` has much more detail, states, values and alarms.

## Instructions

1. Put Inverter on your network (Ethernet or Wifi). Use either a DHCP Reservation, Static IP or configure your DNS and give your inverter a name.
1. Install an MQTT Broker (if you do not already have one)
3. Install Node-red (google instructions, it’s not hard).
4. Install the following nodes in Node-red: node-red-dashboard, node-red-contrib-string
5. Copy code below
6. In your Node-red installation <<IP_of_Node-red>>:1880
7. Click menu in top right corner>Import>From Clipboard
8. Paste the code below into that space
9. Read the readme
10. Put Inverter IP/Name in the “Inverter IP Here” node (replace the IP address that is there, leave the rest of the address as is).
11. Hit Deploy
12. Click square to the left of “Make Request”
13. Go to <<IP_of_Node-red>>:1880/ui
14. You should see values in the Dashboard under the IP in Step 13. If you do, the connection from the Inverter to Node-red is good.
15. Configure MQTT broker in the “Configure MQTT here” node. Click the pencil next to the server. Remember authentication if you have it on your MQTT server. Leave topic blank (it’s configured in the large function).
16. Hit Deploy.
17. Check values at your MQTT server (you can google this as each server is different).
18. Configure sensors in HASS as per sensor code below.
19. Voila!
