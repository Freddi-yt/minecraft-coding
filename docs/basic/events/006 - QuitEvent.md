### Register Listener
``` java
package xyz.freddi.tutorial;

import org.bukkit.Bukkit;
import org.bukkit.event.Listener;
import org.bukkit.plugin.java.JavaPlugin;

public class Tutorial extends JavaPlugin {

	@Override
	public void onEnable() {
		Bukkit.getPluginManager().registerEvents(new Listener() {
            

		}, this);
	}

}
```
### add EventHendler
``` java
package xyz.freddi.tutorial;

import org.bukkit.Bukkit;
import org.bukkit.ChatColor;
import org.bukkit.entity.Player;
import org.bukkit.event.EventHandler;
import org.bukkit.event.Listener;
import org.bukkit.event.player.PlayerQuitEvent;
import org.bukkit.plugin.java.JavaPlugin;

public class Tutorial extends JavaPlugin {

	@Override
	public void onEnable() {
		Bukkit.getPluginManager().registerEvents(new Listener() {

			@EventHandler
			public void onQuit(PlayerQuitEvent event) {
				Player player = event.getPlayer();
				event.setQuitMessage(ChatColor.translateAlternateColorCodes('&', "&7[&c-&7] &7" + player.getName()));
			}

		}, this);
	}

}
```