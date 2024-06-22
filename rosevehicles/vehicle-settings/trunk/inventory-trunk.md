---
description: Setting inventory
---

# Inventory Trunk

```yaml
Inventory:
  Title: "&0Trunk | 20 Slots"
  Barriers:
    Enable: true
    Item:
      Material: BARRIER
      Name: "&7Unavailable slot"
      Lore: []
      Hide_Flags: true
      Stackable: true
```

## Title

Trunk inventory title.

<details>

<summary>Color codes</summary>

We use[ MiniMessage](https://docs.advntr.dev/minimessage/format.html) to parse messages, a text format that allows colors, links, hoverables, and many other features. MiniMessage also provides an [editor](https://webui.advntr.dev/) for you to build your messages! Check out the default colors below:

![](https://cjcrafter.gitbook.io/\~gitbook/image?url=https%3A%2F%2F3986652622-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FIIUkVnlH40vVBzLhWWQ8%252Fuploads%252FKGRabEyd4A8CuFORQtzj%252F181638380-921e157d-15d2-46ab-abe6-189ce1795b9b.png%3Falt%3Dmedia%26token%3D4a5b014b-f136-4833-8065-277926d8bfa3\&width=300\&dpr=4\&quality=100\&sign=cb0fd7d095a6f664f1547a837cc5bcd442f103878855df0d62d13261151a4d25)

</details>

## Barriers

* Enable -> Enable/Disable use barriers for block unused slots
* Item -> <[Item Serializer](../../item-serializer.md)> Settings barrier item.&#x20;
