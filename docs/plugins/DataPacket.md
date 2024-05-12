# Data Packet

Are you looking for a way to send data from the client to Nexus? We've integrated a feature called cron to perform that task. You can enable this feature in the `nexus.properties` file.

Ex:
```js
client.connect(port, ip, () => {
    client.write(data);
});
```