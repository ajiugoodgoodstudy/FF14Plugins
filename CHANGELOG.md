# 雇员同类物品存取 · Retainer Item Transfers

每个版本的改动均以中文和英文记录。日期按北京时间（UTC+8）。1.0.0 至 1.1.0 的记录根据保留的本地构建和测试整理；GitHub 订阅库从 1.1.1 开始提供下载。

Each entry is maintained in Chinese and English. Dates use Beijing time (UTC+8). The entries from 1.0.0 through 1.1.0 are based on archived local builds and tests. The first version available through the GitHub feeds was 1.1.1.

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
