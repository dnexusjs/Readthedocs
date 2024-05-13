# Event Handling

To consume events from Nexus and Client you can register using the `registerEvents` method

Ex:
```js
this.getNexus().getPluginManager().registerEvents(new EventListener())
```

To use any event, create a function with the function name being the name of the event to use

You can see the event names [here](https://github.com/dnexusjs/DiscordNexus/blob/master/src/event/Events.js)

Ex:
```js
export class EventListener extends Listener {

    /**
     * @param {MessageCreateEvent} event 
     */
    async messageCreate(event) {
        const message = event.getMessage();
    }
}
```

Tutorial Video:
<iframe width="480" height="315"
src="https://www.youtube.com/embed/BmHmnSikl50">
</iframe>
