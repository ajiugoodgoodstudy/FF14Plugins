# FF14Plugins
FF14Plugins

## 雇员同类物品存取

打开雇员道具栏或陆行鸟鞍囊后，右键自己背包中的物品，可按类别批量存入。右键雇员或鞍囊中的物品，可将同类物品取回自己的背包。菜单括号会显示类别和来源背包中匹配的格数。

Open a retainer’s inventory or your chocobo saddlebag. Right-click an item in your inventory to deposit items of the same family. To bring them back, right-click an item in the retainer’s inventory or saddlebag. The menu shows the family and how many source slots match.

**当前版本 / Current version 1.3.0** · 2026-11-25

两个窗口同时打开时，玩家背包的右键菜单会列出「将同类物品交给雇员」和「将同类物品存入鞍囊」。鞍囊存取会优先补满目标背包中同物品、同品质的已有堆叠。已解锁且加载完成的扩容鞍囊与普通鞍囊合并计算。

With both windows open, your inventory menu offers separate commands to send matching items to the retainer or the saddlebag. Saddlebag transfers fill existing stacks of the same item and quality first. The standard and expanded saddlebags count as one inventory when the expansion is unlocked and loaded.

[查看从 1.0.0 开始的中英更新记录 / Read the bilingual changelog from 1.0.0](CHANGELOG.md)

### 橙月独立版 / Standalone Dalamud plugin

在 Dalamud 设置的「自定义插件仓库」添加下面的地址并保存，然后在插件安装器搜索「雇员同类物品存取」。

Add the address below to Dalamud’s custom plugin repositories and save. Search the installer for `雇员同类物品存取`.

```text
https://raw.githubusercontent.com/ajiugoodgoodstudy/FF14Plugins/main/repo.json
```

### Omni 在线模块版 / Omni online module

在 Omni 的「插件设置 → 在线模块」添加下面的仓库地址，安装后到「树树妙妙屋 → 在线」启用。此模块需要 Omni 1.2.0.9 或更高版本。

In Omni Toolbox, add the repository under **插件设置 → 在线模块** (plugin settings → online modules). After installing, enable the module under **树树妙妙屋 → 在线**. Requires Omni 1.2.0.9 or later.

```text
https://github.com/ajiugoodgoodstudy/FF14Plugins
```

两种安装方式提供相同的存取功能，选一种启用即可。

Both editions provide the same transfer commands. Enable one of them.
