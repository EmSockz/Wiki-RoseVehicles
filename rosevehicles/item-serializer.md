---
description: Irtem Serializer item from config
---

# 🗜️ Item Serializer

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

![](https://cjcrafter.gitbook.io/\~gitbook/image?url=https%3A%2F%2F3986652622-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FIIUkVnlH40vVBzLhWWQ8%252Fuploads%252FKGRabEyd4A8CuFORQtzj%252F181638380-921e157d-15d2-46ab-abe6-189ce1795b9b.png%3Falt%3Dmedia%26token%3D4a5b014b-f136-4833-8065-277926d8bfa3\&width=300\&dpr=4\&quality=100\&sign=cb0fd7d095a6f664f1547a837cc5bcd442f103878855df0d62d13261151a4d25)

</details>

### Lore

A list of strings to use as the lore of the item.

<details>

<summary>Color codes</summary>

We use[ MiniMessage](https://docs.advntr.dev/minimessage/format.html) to parse messages, a text format that allows colors, links, hoverables, and many other features. MiniMessage also provides an [editor](https://webui.advntr.dev/) for you to build your messages! Check out the default colors below:

![](https://cjcrafter.gitbook.io/\~gitbook/image?url=https%3A%2F%2F3986652622-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FIIUkVnlH40vVBzLhWWQ8%252Fuploads%252FKGRabEyd4A8CuFORQtzj%252F181638380-921e157d-15d2-46ab-abe6-189ce1795b9b.png%3Falt%3Dmedia%26token%3D4a5b014b-f136-4833-8065-277926d8bfa3\&width=300\&dpr=4\&quality=100\&sign=cb0fd7d095a6f664f1547a837cc5bcd442f103878855df0d62d13261151a4d25)

</details>



**Unbreakable**

Use `true` for the item to be unbreakable. Unbreakable items do not show their durability bar, and can never be broken by durability.



**Stackable**

Use `false`so that the item is not stackable. Non-stackable items are not stackable in any way. Note that items cloned in creative will still be able to stack. The items get a unique uuid in NBT, so they cannot be stacked.



**Custom\_Model\_Data**

The [custom model data](https://www.planetminecraft.com/forums/communities/texturing/new-1-14-custom-item-models-tuto-578834/) of the item. Your server must be in MC 1.14.4 or higher.



**Hide\_Flags**

Hides all item flags (Enchantments, Attributes, Unbreakable, Destroys, Placed on, Potion effects, Dye color).
