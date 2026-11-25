# 雇员同类物品存取 · Retainer Item Transfers

每个版本的改动均以中文和英文记录。日期按北京时间（UTC+8）。1.0.0 至 1.1.0 的记录根据保留的本地构建和测试整理；GitHub 订阅库从 1.1.1 开始提供下载。

Each entry is maintained in Chinese and English. Dates use Beijing time (UTC+8). The entries from 1.0.0 through 1.1.0 are based on archived local builds and tests. The first version available through the GitHub feeds was 1.1.1.

## 1.3.0 · 陆行鸟鞍囊存取 / Chocobo saddlebag transfers

2026-11-25 · 橙月独立版与 Omni 模块 / Standalone Dalamud plugin and Omni module

打开陆行鸟鞍囊，右键自己背包里的物品，选择「将同类物品存入鞍囊」。要取回时，右键鞍囊里的物品，选择「从鞍囊取出同类物品」。鞍囊与雇员道具栏同时打开时，玩家背包会显示两个存入目标，各自带有粉色 OT 标记。

With the chocobo saddlebag open, right-click an item in your inventory to deposit its family, or right-click an item in the saddlebag to retrieve its family. If a retainer’s inventory is also open, the player inventory menu shows both deposit destinations, each with its own pink OT badge.

- 普通鞍囊与已解锁且加载完成的扩容鞍囊共用一次预览和存取范围。存取两向都先补目标背包里同物品、同品质的未满堆，再使用空格。空间只够装下一部分时，其余物品留在原背包。

  The preview and transfer cover the standard saddlebag and any unlocked, loaded expansion. Deposits and withdrawals fill compatible partial stacks before using an empty slot. If only part of a stack fits, the remainder stays in its original inventory.

- 关闭当前存取窗口或切换角色会停止后续移动。雇员存取时切换雇员、鞍囊存取时可用页发生变化，也会中止。聊天栏只统计两侧都确认的数量。已提交的移动若仍未确认，会提示核对两侧背包。

  Further moves stop when the active storage window closes or the player switches characters. A retainer transfer also stops if the retainer changes, and a saddlebag transfer stops if its accessible pages change. Chat counts items confirmed in both inventories and flags any submitted moves still awaiting confirmation.

国服实测在鞍囊中分别存入并取回 5 张九宫幻卡、317 件料理和 8 份乐谱，三次往返的数量均已确认。93 项菜单与转移检查、500 组随机背包模拟均通过。普通与扩容鞍囊之间的跨页行为通过离线回归验证。

In the Chinese client, three saddlebag round trips confirmed all 5 Triple Triad cards, 317 food items and 8 orchestrion rolls on both deposit and withdrawal. All 93 menu and transfer checks and 500 randomized inventory simulations passed. Offline tests covered transfers spanning the standard and expanded saddlebag pages.

## 1.2.0 · 重整六类物品 / Six revised item families

2026-11-25 · 橙月独立版与 Omni 模块同步发布 / Standalone Dalamud plugin and Omni module

旧版把 3 级刚力之灵水和普通炼金原料放在一起，却把部分纺织用棉麻分到了木材花草里。传送券和惰性水晶也常常只能逐种存取。根据国服物品表、制作配方、钓鱼笔记和商店兑换记录重新划分后，右键预览、存入和取出都使用下表的范围。

Grade 3 strength reagents used to share a family with general alchemy materials, while some textile fibers ended up with lumber and flowers. Travel tickets and cracked materia tokens also had to be transferred one type at a time. The revised families use the Chinese client’s item data, recipes, fishing records and shop exchanges. The menu preview, deposits and withdrawals all use the same membership.

| 类别 / Family | 国服物品数 / Items | 存取范围 / What moves together |
| --- | ---: | --- |
| 鱼和水产品 / Fish and seafood | 2,822 | 含刺鱼、可收藏鱼、重建水产、贝虾，以及能作活饵的真鱼。专用鱼饵和鱼料理另分。<br>Includes spearfishing catches, collectable fish, Restoration catches, shellfish and fish used for mooching. Fishing tackle and prepared meals stay in their own families. |
| 传送券 / Teleport tickets | 9 | 通用传送券、7 种定点券和传送网使用优惠券。<br>The standard aetheryte ticket, seven destination-specific tickets and the teleport discount voucher. |
| 魔晶石兑换物 / Materia exchange tokens | 16 | 惰性炸裂状水晶可与其他兑换用水晶、晶簇及两种玛哈物质一起搬运。成品魔晶石和元素水晶另分。<br>Cracked crystals and clusters group with the two Mhachi tokens used to obtain materia. Finished materia and elemental crystals stay in separate families. |
| 灵水、幻水和宝水 / Crafting reagents | 85 | 含各属性、各等级的灵水、幻水、宝水及相应的工匠款和收藏品。战斗药单独归类。<br>Groups the reisui, alkahest and gemsap series across attributes and grades, including their artisan and collectable variants. Consumable stat potions are handled separately. |
| 布匹和纤维 / Cloth and fibers | 314 | 阿拉米格纤维与布、纱线、棉麻、毛和茧归在一起。65 种原先划进木材花草的纺织原料已归回。<br>Ala Mhigan Fiber now groups with cloth, yarn, cotton, flax, wool and cocoons. This brings 65 textile materials back from the lumber and flowers family. |
| 藏宝图 / Treasure maps | 27 | 按游戏寻宝表归类，包含隐藏地图和深层传送魔纹的地图。<br>Follows the game’s treasure-hunt data, including hidden maps and maps that lead to deeper treasure chambers. |

本版对照国服数据检查了 51,228 条有名称的物品。65 项菜单及转移模拟检查通过，覆盖六个新类别的存取两向。上表数字为物品种数，实际右键菜单显示当前背包匹配的格数。

The category checks covered 51,228 named items in the Chinese client data. All 65 menu and transfer simulation checks passed, including deposits and withdrawals for each revised family. The table counts item types. The in-game menu shows how many slots match in the current inventory.

## 1.1.1 · 菜单对齐，首次公开订阅 / Menu alignment and first public release

2026-11-24 本地构建 / Local build · 2026-11-25 公开发布 / Public release

修正「存入同类物品」和「取出同类物品」比其他 Omni 菜单项靠右的问题。移除了粉色 OT 前的空白，保留两个相邻的方框字母和正文前的一个空格。次日将橙月独立版和 Omni 在线模块一同上架。[首次公开发布](https://github.com/ajiugoodgoodstudy/FF14Plugins/commit/58b617a531dcb297f34230a07b0cbe571bfeb68a)

Both transfer commands were indented farther than the other Omni menu entries. Removing the leading space aligned the pink OT badge with its neighbors. The boxed letters sit together, with one space before the command. The standalone Dalamud plugin and the Omni module went live together the following day. [First public release](https://github.com/ajiugoodgoodstudy/FF14Plugins/commit/58b617a531dcb297f34230a07b0cbe571bfeb68a)

## 1.1.0 · 批量存取提速 / Faster batch transfers

2026-11-24 · 本地构建 / Local build

逐格等回执会拖慢整批操作。这个版本按游戏库存队列的剩余容量，在同一帧提交多笔移动，并为每笔预留来源格和目标格。需要复用格位时再分批。一次实际存取中，26 格料理共 272 件，存入和取出各用一帧提交，两边均确认到账。右键菜单也换成了粉色 OT 标记。

Waiting for each stack to arrive slowed down larger transfers. This version submits multiple moves in one frame, up to the inventory queue’s available capacity. Each move reserves its source and destination slots. Moves that need to reuse a slot wait for the next batch. In one in-game round trip, 272 food items across 26 slots were deposited and retrieved. Each direction took one frame to submit, and all 272 items were confirmed on arrival. The menu also gained the pink OT badge.

## 1.0.2 · 修复连续搬运卡住 / Fixed stalled transfers

2026-11-24 · 本地构建 / Local build

针对连续搬运料理时中途卡住的问题，存取改用游戏的 `MoveItemSlot`。发送前重新检查来源格和目标格，优先使用可合堆的位置。若等待 8 秒后双方数量都没变、库存队列也已空闲，就跳过这一格继续。若只看到一侧变化，则停止并提示玩家核对。

Transfers could stall partway through a run of food stacks. The plugin switched to the game’s `MoveItemSlot` operation, rechecks both slots before each move, and prefers a compatible partial stack. After eight seconds, it can skip an unchanged stack if the queue is idle. If only one inventory has changed, it stops and asks the player to check.

## 1.0.1 · 分类与预览 / Category fixes and menu preview

2026-11-24 · 中间测试版 / Local test build

根据「部分幻卡和料理分不到一起、乐谱存取不全」的反馈，重新核对了单卡和卡包、成品和陈旧乐谱、空白谱、可兑换乐谱的破旧乐章，以及收藏料理和节日点心。右键菜单开始显示类别和来源格数，方便点击前核对范围。目标已有相同珍稀物品时会跳过，超时提示会指出具体物品。

Reports of missing cards, rolls and food led to a review of Triple Triad cards and packs, finished and faded orchestrion rolls, blank rolls, fragments exchangeable for rolls, collectable dishes and seasonal sweets. The menu began showing the family and the number of matching source slots before the player clicked. The plugin also skips a unique item if the destination already holds one and names the item when a transfer times out.

## 1.0.0 · 首个可用版本 / First working version

2026-11-24 · 本地构建 / Local build

打开雇员道具栏后，右键玩家背包可存入同类物品，右键雇员背包可取出同类物品。首版支持矿产和金属、木材和花草、染料、魔晶石、装备及游戏的乐谱类别。保留物品品质，每次处理一格，核对双方数量后继续。首版已提供橙月独立插件和 Omni 模块两种入口。

With a retainer’s inventory open, players could right-click their own inventory to deposit a family of items, or the retainer’s inventory to retrieve it. Initial families included ores and metals, lumber and flowers, dyes, materia, equipment and the game’s orchestrion roll category. The plugin preserved item quality and checked both inventories before moving the next stack. Both a standalone Dalamud plugin and an Omni module were available in this local build.
