# Slash Command

The commands you register to Nexus it can be used on both console and discord.
To register a command use the `register` method

Ex:
```js
this.getNexus().getCommandMap().register(new PingCommand());
```

To handle when the command is called, create an `execute` method
```{important}
The `execute` method must be created when registering a command
```
For `PingCommand.js`
```js
import { BaseInteraction, SlashCommandBuilder, User } from "discord.js";

export class PingCommand extends Command {

    constructor() {
        super(
            new SlashCommandBuilder()
                .setName("ping")
                .setDescription("ping commannd")
        )
    }

     /**
     * Execute the command
     * @param {User|ConsoleCommandSender} sender 
     * @param {BaseInteraction|undefined} interaction
     * @param {Object|undefined} args
     */
    async execute(sender, interaction, args) {
        if (sender instanceof ConsoleCommandSender) {
            return sender.reply("This command only can use in-discord.")
        }
        interaction.reply("Pong");
    }
}
```

Tutorial Video:
<iframe width="480" height="315"
src="https://www.youtube.com/embed/1X50uB6iLRs">
</iframe>
