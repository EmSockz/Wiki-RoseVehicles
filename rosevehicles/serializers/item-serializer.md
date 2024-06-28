---
description: Item Serializer item from config
---

# Item Serializer

```yaml
Item:
  Material: DIRT
  Name: "<!i>&cExample name"
  Lore:
    - '<!i>&7Example 1'
    - '<!i>&7Example 2'
  Custom_Model_Data: 2
  Unbreakable: true
  Stackable: true
  Hide_Flags: true
```

### Material

The [Material ](https://hub.spigotmc.org/javadocs/spigot/org/bukkit/Material.html)used for the item. For example, `FEATHER`.

### Name

The display name of the item.&#x20;

<details>

<summary>Color codes</summary>

We use[ MiniMessage](https://docs.advntr.dev/minimessage/format.html) to parse messages, a text format that allows colors, links, hoverables, and many other features. MiniMessage also provides an [editor](https://webui.advntr.dev/) for you to build your messages! Check out the default colors below:

![](<../../.gitbook/assets/image (1).png>)

</details>

### Lore

A list of strings to use as the lore of the item.

<details>

<summary>Color codes</summary>

We use[ MiniMessage](https://docs.advntr.dev/minimessage/format.html) to parse messages, a text format that allows colors, links, hoverables, and many other features. MiniMessage also provides an [editor](https://webui.advntr.dev/) for you to build your messages! Check out the default colors below:

![](<../../.gitbook/assets/image (2).png>)

</details>



**Unbreakable**

Use `true` for the item to be unbreakable. Unbreakable items do not show their durability bar, and can never be broken by durability.



**Stackable**

Use `false`so that the item is not stackable. Non-stackable items are not stackable in any way. Note that items cloned in creative will still be able to stack. The items get a unique uuid in NBT, so they cannot be stacked.



**Custom\_Model\_Data**

The [custom model data](https://www.planetminecraft.com/forums/communities/texturing/new-1-14-custom-item-models-tuto-578834/) of the item. Your server must be in MC 1.14.4 or higher.



**Hide\_Flags**

Hides all item flags (Enchantments, Attributes, Unbreakable, Destroys, Placed on, Potion effects, Dye color).
