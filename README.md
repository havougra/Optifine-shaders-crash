# Optifine-shaders-crash
Optifine and all my mods loaded (using forge) on 1.12.1, as soon as I click shaders it either crashes or tells me unrecognized files in the pack.
---- Minecraft Crash Report ----

WARNING: coremods are present:
  llibrary (llibrary-core-1.0.11-1.12.2.jar)
  wings (wings-1.1.6-1.12.2.jar)
  WolfArmorCore (WolfArmorAndStorage-1.12.2-3.8.0-universal-signed.jar)
  XaeroMinimapPlugin (Xaeros_Minimap_23.9.7_Forge_1.12.jar)
  XaeroWorldMapPlugin (XaerosWorldMap_1.37.8_Forge_1.12.jar)
  CTMCorePlugin (CTM-MC1.12.2-1.0.2.31.jar)
Contact their authors BEFORE contacting forge

// Why did you do that?

Time: 3/21/24 4:35 PM
Description: Updating screen events

java.lang.NoSuchFieldError: field_191308_b
	at net.optifine.config.ConnectedParser.parseEntities(ConnectedParser.java:1248)
	at net.optifine.shaders.EntityAliases.loadEntityAliases(EntityAliases.java:164)
	at net.optifine.shaders.EntityAliases.update(EntityAliases.java:89)
	at net.optifine.shaders.Shaders.loadShaderPackProperties(Shaders.java:1086)
	at net.optifine.shaders.Shaders.loadShaderPack(Shaders.java:948)
	at net.optifine.shaders.Shaders.setShaderPack(Shaders.java:871)
	at net.optifine.shaders.gui.GuiSlotShaders.selectIndex(GuiSlotShaders.java:91)
	at net.optifine.shaders.gui.GuiSlotShaders.func_148144_a(GuiSlotShaders.java:81)
	at net.minecraft.client.gui.GuiSlot.func_178039_p(GuiSlot.java:323)
	at net.optifine.shaders.gui.GuiShaders.func_146274_d(GuiShaders.java:117)
	at net.minecraft.client.gui.GuiScreen.func_146269_k(GuiScreen.java:501)
	at net.minecraft.client.Minecraft.func_71407_l(Minecraft.java:1759)
	at net.minecraft.client.Minecraft.func_71411_J(Minecraft.java:1098)
	at net.minecraft.client.Minecraft.func_99999_d(Minecraft.java:398)
	at net.minecraft.client.main.Main.main(SourceFile:123)
	at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
	at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)
	at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.lang.reflect.Method.invoke(Method.java:497)
	at net.minecraft.launchwrapper.Launch.launch(Launch.java:135)
	at net.minecraft.launchwrapper.Launch.main(Launch.java:28)


A detailed walkthrough of the error, its code path and all known details is as follows:
---------------------------------------------------------------------------------------

-- Head --
Thread: Client thread
Stacktrace:
	at net.optifine.config.ConnectedParser.parseEntities(ConnectedParser.java:1248)
	at net.optifine.shaders.EntityAliases.loadEntityAliases(EntityAliases.java:164)
	at net.optifine.shaders.EntityAliases.update(EntityAliases.java:89)
	at net.optifine.shaders.Shaders.loadShaderPackProperties(Shaders.java:1086)
	at net.optifine.shaders.Shaders.loadShaderPack(Shaders.java:948)
	at net.optifine.shaders.Shaders.setShaderPack(Shaders.java:871)
	at net.optifine.shaders.gui.GuiSlotShaders.selectIndex(GuiSlotShaders.java:91)
	at net.optifine.shaders.gui.GuiSlotShaders.func_148144_a(GuiSlotShaders.java:81)
	at net.minecraft.client.gui.GuiSlot.func_178039_p(GuiSlot.java:323)
	at net.optifine.shaders.gui.GuiShaders.func_146274_d(GuiShaders.java:117)
	at net.minecraft.client.gui.GuiScreen.func_146269_k(GuiScreen.java:501)

-- Affected screen --
Details:
	Screen name: net.optifine.shaders.gui.GuiShaders

-- Affected level --
Details:
	Level name: MpServer
	All players: 1 total; [EntityPlayerSP['Hampsterwisdom'/9985, l='MpServer', x=-84.27, y=67.00, z=-1.12]]
	Chunk stats: MultiplayerChunkCache: 439, 439
	Level seed: 0
	Level generator: ID 00 - default, ver 1. Features enabled: false
	Level generator options: 
	Level spawn location: World: (-132,64,44), Chunk: (at 12,4,12 in -9,2; contains blocks -144,0,32 to -129,255,47), Region: (-1,0; contains chunks -32,0 to -1,31, blocks -512,0,0 to -1,255,511)
	Level time: 65101 game time, 65101 day time
	Level dimension: 0
	Level storage version: 0x00000 - Unknown?
	Level weather: Rain time: 0 (now: false), thunder time: 0 (now: false)
	Level game mode: Game mode: survival (ID 0). Hardcore: false. Cheats: false
	Forced entities: 166 total; [EntityHat['unknown'/1538, l='MpServer', x=-73.25, y=49.00, z=-14.48], EntityHat['unknown'/1539, l='MpServer', x=-62.51, y=53.00, z=-4.81], EntityBat['Bat'/21009, l='MpServer', x=-92.00, y=25.13, z=-79.36], EntityItem['item.item.egg'/17950, l='MpServer', x=-73.23, y=78.00, z=5.54], EntityItem['item.item.egg'/20528, l='MpServer', x=-72.55, y=81.00, z=8.83], EntitySpider['Spider'/21044, l='MpServer', x=-145.50, y=72.00, z=22.50], EntitySpider['Spider'/21056, l='MpServer', x=-107.50, y=75.00, z=-63.50], EntityCreeper['Creeper'/21057, l='MpServer', x=-117.44, y=74.00, z=-73.20], EntitySpider['Spider'/21059, l='MpServer', x=-20.50, y=67.00, z=-52.50], EntityHat['unknown'/1617, l='MpServer', x=-61.40, y=62.00, z=-11.65], EntityBat['Bat'/21076, l='MpServer', x=-149.24, y=38.61, z=43.54], EntityBat['Bat'/21077, l='MpServer', x=-152.52, y=34.03, z=29.76], EntityCow['Cow'/99, l='MpServer', x=-160.41, y=65.00, z=-29.45], EntityCow['Cow'/100, l='MpServer', x=-161.71, y=65.00, z=-32.84], EntityChicken['Chicken'/104, l='MpServer', x=-124.86, y=64.00, z=-50.48], EntitySkeleton['Skeleton'/20072, l='MpServer', x=-47.50, y=29.00, z=10.50], EntityChicken['Chicken'/105, l='MpServer', x=-130.60, y=63.00, z=-48.11], EntitySkeleton['Skeleton'/21097, l='MpServer', x=-10.50, y=65.00, z=41.50], EntitySquid['Squid'/19562, l='MpServer', x=-76.64, y=61.92, z=-13.40], EntityChicken['Chicken'/106, l='MpServer', x=-129.50, y=63.00, z=-49.50], EntityChicken['Chicken'/107, l='MpServer', x=-130.86, y=66.00, z=-40.03], EntitySquid['Squid'/19563, l='MpServer', x=-67.28, y=59.17, z=-7.69], EntitySquid['Squid'/19564, l='MpServer', x=-63.31, y=61.46, z=-4.24], EntityHusk['Husk'/20083, l='MpServer', x=-46.81, y=65.00, z=7.49], EntitySkeleton['Skeleton'/20086, l='MpServer', x=-21.45, y=67.00, z=1.78], EntityItem['item.item.egg'/20599, l='MpServer', x=-78.41, y=64.00, z=-6.63], EntityChicken['Chicken'/120, l='MpServer', x=-106.22, y=68.00, z=-13.53], EntityChicken['Chicken'/121, l='MpServer', x=-90.39, y=71.00, z=-19.83], EntityChicken['Chicken'/122, l='MpServer', x=-101.46, y=74.00, z=-33.12], EntityChicken['Chicken'/123, l='MpServer', x=-83.87, y=64.00, z=-34.87], EntityChicken['Chicken'/124, l='MpServer', x=-91.48, y=64.00, z=-36.23], EntityChicken['Chicken'/125, l='MpServer', x=-89.37, y=67.00, z=1.91], EntityChicken['Chicken'/126, l='MpServer', x=-109.55, y=73.00, z=-32.20], EntityChicken['Chicken'/127, l='MpServer', x=-82.48, y=72.00, z=6.20], EntityHat['unknown'/640, l='MpServer', x=-83.87, y=64.00, z=-34.87], EntityChicken['Chicken'/128, l='MpServer', x=-80.11, y=80.00, z=9.31], EntityChicken['Chicken'/129, l='MpServer', x=-73.79, y=82.00, z=8.46], EntityChicken['Chicken'/130, l='MpServer', x=-73.19, y=82.00, z=8.02], EntityItem['item.item.egg'/20098, l='MpServer', x=-82.46, y=67.00, z=-21.28], EntityChicken['Chicken'/131, l='MpServer', x=-67.50, y=80.00, z=16.13], EntityHat['unknown'/1677, l='MpServer', x=-130.86, y=66.00, z=-40.03], EntitySpider['Spider'/20621, l='MpServer', x=-51.50, y=73.00, z=-67.50], EntityRabbit['Rabbit'/151, l='MpServer', x=-46.50, y=67.00, z=-5.50], EntityRabbit['Rabbit'/152, l='MpServer', x=-48.50, y=63.00, z=-14.99], EntityRabbit['Rabbit'/153, l='MpServer', x=-33.89, y=68.00, z=17.57], EntityRabbit['Rabbit'/154, l='MpServer', x=-23.40, y=67.00, z=7.46], EntityRabbit['Rabbit'/155, l='MpServer', x=-58.52, y=63.06, z=4.71], EntityRabbit['Rabbit'/156, l='MpServer', x=-50.60, y=66.00, z=-8.51], EntityRabbit['Rabbit'/157, l='MpServer', x=-50.50, y=67.00, z=-5.50], EntityItem['item.item.egg'/16029, l='MpServer', x=-125.64, y=64.00, z=-50.80], EntityRabbit['Rabbit'/158, l='MpServer', x=-51.50, y=67.00, z=-5.50], EntityHat['unknown'/675, l='MpServer', x=-90.39, y=71.00, z=-19.83], EntityHat['unknown'/680, l='MpServer', x=-101.46, y=74.00, z=-33.12], EntityHat['unknown'/1707, l='MpServer', x=-76.64, y=61.92, z=-13.40], EntityHat['unknown'/1708, l='MpServer', x=-67.28, y=59.17, z=-7.69], EntityHat['unknown'/1709, l='MpServer', x=-63.31, y=61.46, z=-4.24], EntityHat['unknown'/687, l='MpServer', x=-106.22, y=68.00, z=-13.53], EntityZombie['Zombie'/20655, l='MpServer', x=-124.50, y=66.00, z=-17.50], EntitySpider['Spider'/21169, l='MpServer', x=-47.01, y=67.00, z=4.00], EntitySquid['Squid'/20146, l='MpServer', x=-48.57, y=61.00, z=-34.60], EntitySkeleton['Skeleton'/21171, l='MpServer', x=-44.81, y=66.00, z=11.51], EntityHat['unknown'/693, l='MpServer', x=-91.48, y=64.00, z=-36.23], EntityCreeper['Creeper'/20662, l='MpServer', x=-121.50, y=71.00, z=21.50], EntitySkeleton['Skeleton'/20665, l='MpServer', x=-53.50, y=33.00, z=-80.50], EntityHat['unknown'/700, l='MpServer', x=-89.37, y=67.00, z=1.91], EntityHat['unknown'/701, l='MpServer', x=-109.55, y=73.00, z=-32.20], EntitySkeleton['Skeleton'/21184, l='MpServer', x=-163.50, y=93.00, z=69.50], EntityHat['unknown'/1739, l='MpServer', x=-130.60, y=63.00, z=-48.11], EntityBat['Bat'/21202, l='MpServer', x=-42.23, y=34.13, z=17.88], EntityHat['unknown'/1750, l='MpServer', x=-124.86, y=64.00, z=-50.48], EntityHat['unknown'/1751, l='MpServer', x=-129.50, y=63.00, z=-49.50], EntityHat['unknown'/734, l='MpServer', x=-82.48, y=72.00, z=6.20], EntityCreeper['Creeper'/20204, l='MpServer', x=-113.50, y=73.00, z=-41.50], EntityPlayerSP['Hampsterwisdom'/9985, l='MpServer', x=-84.27, y=67.00, z=-1.12], EntityHat['unknown'/1782, l='MpServer', x=-151.50, y=81.00, z=-65.50], EntityHat['unknown'/1785, l='MpServer', x=-162.50, y=66.00, z=-23.50], EntityHat['unknown'/1301, l='MpServer', x=-160.41, y=65.00, z=-29.45], EntityBat['Bat'/21269, l='MpServer', x=-22.21, y=51.00, z=14.40], EntityHat['unknown'/790, l='MpServer', x=-80.11, y=80.00, z=9.31], EntityHat['unknown'/791, l='MpServer', x=-73.79, y=82.00, z=8.46], EntityHat['unknown'/792, l='MpServer', x=-73.19, y=82.00, z=8.02], EntityBat['Bat'/21272, l='MpServer', x=-148.39, y=34.53, z=46.64], EntityBat['Bat'/21273, l='MpServer', x=-57.15, y=56.99, z=31.32], EntityHat['unknown'/795, l='MpServer', x=-50.60, y=66.00, z=-8.51], EntityHat['unknown'/1307, l='MpServer', x=-161.71, y=65.00, z=-32.84], EntityItem['item.item.egg'/20765, l='MpServer', x=-130.88, y=63.00, z=-47.41], EntityHat['unknown'/798, l='MpServer', x=-67.50, y=80.00, z=16.13], EntityZombie['Zombie'/20254, l='MpServer', x=-109.50, y=88.00, z=33.50], EntityItem['item.tile.sapling.acacia'/21284, l='MpServer', x=-114.13, y=87.00, z=38.53], EntityItem['item.tile.sapling.acacia'/20779, l='MpServer', x=-116.40, y=86.00, z=41.13], EntityHat['unknown'/813, l='MpServer', x=-46.50, y=67.00, z=-5.50], EntityHat['unknown'/814, l='MpServer', x=-33.89, y=68.00, z=17.57], EntityCreeper['Creeper'/21296, l='MpServer', x=-34.67, y=67.00, z=-6.91], EntitySquid['Squid'/19257, l='MpServer', x=-61.40, y=62.00, z=-11.65], EntityCreeper['Creeper'/21306, l='MpServer', x=-153.50, y=32.00, z=21.50], EntityCreeper['Creeper'/21307, l='MpServer', x=-153.50, y=32.00, z=20.50], EntityItem['item.item.egg'/15676, l='MpServer', x=-79.79, y=66.00, z=-11.81], EntityItem['item.item.egg'/16701, l='MpServer', x=-80.08, y=66.00, z=-12.73], EntitySkeleton['Skeleton'/21316, l='MpServer', x=-87.50, y=99.00, z=19.50], EntityHat['unknown'/1865, l='MpServer', x=-47.50, y=29.00, z=10.50], EntitySkeleton['Skeleton'/20297, l='MpServer', x=-15.49, y=70.00, z=-33.25], EntityHat['unknown'/1867, l='MpServer', x=-46.81, y=65.00, z=7.49], EntityHat['unknown'/1868, l='MpServer', x=-21.45, y=67.00, z=1.78], EntityZombie['Zombie'/19789, l='MpServer', x=-162.50, y=66.00, z=-23.50], EntityHat['unknown'/355, l='MpServer', x=-84.27, y=67.00, z=-1.12], EntityHat['unknown'/1892, l='MpServer', x=-48.57, y=61.00, z=-34.60], EntityCreeper['Creeper'/21349, l='MpServer', x=-131.50, y=20.00, z=39.50], EntityCreeper['Creeper'/19302, l='MpServer', x=-151.50, y=81.00, z=-65.50], EntityHat['unknown'/1901, l='MpServer', x=-113.50, y=73.00, z=-41.50], EntityHusk['Husk'/21357, l='MpServer', x=-10.50, y=69.00, z=-65.50], EntityHat['unknown'/1904, l='MpServer', x=-109.50, y=88.00, z=33.50], EntityItem['item.item.egg'/20851, l='MpServer', x=-83.45, y=64.00, z=-34.39], EntitySkeleton['Skeleton'/20859, l='MpServer', x=-157.24, y=72.00, z=22.69], EntityHat['unknown'/1918, l='MpServer', x=-15.49, y=70.00, z=-33.25], EntityCreeper['Creeper'/20880, l='MpServer', x=-38.50, y=36.00, z=-7.50], EntityHat['unknown'/1937, l='MpServer', x=-51.50, y=73.00, z=-67.50], EntityCreeper['Creeper'/20881, l='MpServer', x=-40.50, y=36.00, z=-8.50], EntityHat['unknown'/1943, l='MpServer', x=-124.50, y=66.00, z=-17.50], EntityHat['unknown'/1946, l='MpServer', x=-121.50, y=71.00, z=21.50], EntityHat['unknown'/1947, l='MpServer', x=-53.50, y=33.00, z=-80.50], EntitySkeleton['Skeleton'/20895, l='MpServer', x=-77.50, y=100.00, z=34.50], EntityItem['item.item.egg'/19872, l='MpServer', x=-131.78, y=66.00, z=-39.93], EntityItem['item.item.egg'/19874, l='MpServer', x=-129.68, y=63.00, z=-49.49], EntityBat['Bat'/20397, l='MpServer', x=-161.21, y=16.01, z=22.92], EntityItem['item.item.egg'/18350, l='MpServer', x=-102.41, y=74.00, z=-33.79], EntityItem['item.item.egg'/18351, l='MpServer', x=-73.76, y=82.00, z=8.88], EntityHat['unknown'/1969, l='MpServer', x=-157.24, y=72.00, z=22.69], EntityHat['unknown'/1970, l='MpServer', x=-38.50, y=36.00, z=-7.50], EntityHat['unknown'/1971, l='MpServer', x=-40.50, y=36.00, z=-8.50], EntityItem['item.tile.sapling.acacia'/20405, l='MpServer', x=-112.17, y=90.00, z=40.07], EntityHat['unknown'/1973, l='MpServer', x=-77.50, y=100.00, z=34.50], EntityHat['unknown'/1974, l='MpServer', x=-139.70, y=23.52, z=-63.56], EntityHat['unknown'/1978, l='MpServer', x=-136.50, y=69.00, z=-9.50], EntityHat['unknown'/1979, l='MpServer', x=-52.50, y=89.00, z=62.50], EntityHat['unknown'/1982, l='MpServer', x=-62.78, y=74.00, z=-69.30], EntityHat['unknown'/1983, l='MpServer', x=-26.50, y=64.00, z=46.50], EntityHat['unknown'/1990, l='MpServer', x=-145.50, y=72.00, z=22.50], EntityHat['unknown'/1991, l='MpServer', x=-107.50, y=75.00, z=-63.50], EntityHat['unknown'/1992, l='MpServer', x=-117.44, y=74.00, z=-73.20], EntityHat['unknown'/1993, l='MpServer', x=-20.50, y=67.00, z=-52.50], EntityHat['unknown'/1996, l='MpServer', x=-149.24, y=38.61, z=43.54], EntityHat['unknown'/1997, l='MpServer', x=-152.52, y=34.03, z=29.76], EntityHat['unknown'/2001, l='MpServer', x=-10.50, y=65.00, z=41.50], EntityHat['unknown'/2005, l='MpServer', x=-47.01, y=67.00, z=4.00], EntityHat['unknown'/2006, l='MpServer', x=-44.81, y=66.00, z=11.51], EntityHat['unknown'/2007, l='MpServer', x=-163.50, y=93.00, z=69.50], EntityHat['unknown'/2009, l='MpServer', x=-42.23, y=34.13, z=17.88], EntityHat['unknown'/2013, l='MpServer', x=-22.21, y=51.00, z=14.40], EntityBat['Bat'/20958, l='MpServer', x=-139.70, y=23.52, z=-63.56], EntityHat['unknown'/2014, l='MpServer', x=-148.39, y=34.53, z=46.64], EntityHat['unknown'/2015, l='MpServer', x=-57.15, y=56.99, z=31.32], EntityItem['item.tile.sapling.acacia'/20963, l='MpServer', x=-119.72, y=94.00, z=37.30], EntityHat['unknown'/2020, l='MpServer', x=-34.67, y=67.00, z=-6.91], EntityZombie['Zombie'/18405, l='MpServer', x=-73.25, y=49.00, z=-14.48], EntitySkeleton['Skeleton'/20965, l='MpServer', x=-136.50, y=69.00, z=-9.50], EntityZombie['Zombie'/18406, l='MpServer', x=-62.51, y=53.00, z=-4.81], EntityZombie['Zombie'/20967, l='MpServer', x=-52.50, y=89.00, z=62.50], EntityHat['unknown'/2023, l='MpServer', x=-153.50, y=32.00, z=21.50], EntityHat['unknown'/2024, l='MpServer', x=-153.50, y=32.00, z=20.50], EntityHat['unknown'/2026, l='MpServer', x=-87.50, y=99.00, z=19.50], EntityHat['unknown'/2028, l='MpServer', x=-131.50, y=20.00, z=39.50], EntityHat['unknown'/2030, l='MpServer', x=-92.00, y=25.13, z=-79.36], EntityHat['unknown'/2032, l='MpServer', x=-161.21, y=16.01, z=22.92], EntityHat['unknown'/2034, l='MpServer', x=-10.50, y=69.00, z=-65.50], EntityHusk['Husk'/20982, l='MpServer', x=-62.78, y=74.00, z=-69.30], EntitySpider['Spider'/20989, l='MpServer', x=-26.50, y=64.00, z=46.50]]
	Retry entities: 0 total; []
	Server brand: fml,forge
	Server type: Non-integrated multiplayer server
Stacktrace:
	at net.minecraft.client.multiplayer.WorldClient.func_72914_a(WorldClient.java:532)
	at net.minecraft.client.Minecraft.func_71396_d(Minecraft.java:2741)
	at net.minecraft.client.Minecraft.func_99999_d(Minecraft.java:419)
	at net.minecraft.client.main.Main.main(SourceFile:123)
	at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
	at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)
	at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.lang.reflect.Method.invoke(Method.java:497)
	at net.minecraft.launchwrapper.Launch.launch(Launch.java:135)
	at net.minecraft.launchwrapper.Launch.main(Launch.java:28)

-- System Details --
Details:
	Minecraft Version: 1.12.2
	Operating System: Windows 10 (amd64) version 10.0
	Java Version: 1.8.0_51, Oracle Corporation
	Java VM Version: Java HotSpot(TM) 64-Bit Server VM (mixed mode), Oracle Corporation
	Memory: 2497983128 bytes (2382 MB) / 6442450944 bytes (6144 MB) up to 6442450944 bytes (6144 MB)
	JVM Flags: 8 total; -XX:HeapDumpPath=MojangTricksIntelDriversForPerformance_javaw.exe_minecraft.exe.heapdump -Xmx6G -XX:+UnlockExperimentalVMOptions -XX:+UseG1GC -XX:G1NewSizePercent=20 -XX:G1ReservePercent=20 -XX:MaxGCPauseMillis=50 -XX:G1HeapRegionSize=64M
	IntCache: cache: 0, tcache: 0, allocated: 0, tallocated: 0
	FML: MCP 9.42 Powered by Forge 14.23.5.2859 Optifine OptiFine_1.12.2_HD_U_F5 71 mods loaded, 69 mods active
	States: 'U' = Unloaded 'L' = Loaded 'C' = Constructed 'H' = Pre-initialized 'I' = Initialized 'J' = Post-initialized 'A' = Available 'D' = Disabled 'E' = Errored

	| State  | ID                  | Version           | Source                                                | Signature                                |
	|:------ |:------------------- |:----------------- |:----------------------------------------------------- |:---------------------------------------- |
	| LCHIJA | minecraft           | 1.12.2            | minecraft.jar                                         | None                                     |
	| LCHIJA | mcp                 | 9.42              | minecraft.jar                                         | None                                     |
	| LCHIJA | FML                 | 8.0.99.99         | forge-1.12.2-14.23.5.2859.jar                         | e3c3d50c7c986df74c645c0ac54639741c90a557 |
	| LCHIJA | forge               | 14.23.5.2859      | forge-1.12.2-14.23.5.2859.jar                         | e3c3d50c7c986df74c645c0ac54639741c90a557 |
	| LCHIJA | xaerominimap_core   | 1.12.2-1.0        | minecraft.jar                                         | None                                     |
	| LCHIJA | xaeroworldmap_core  | 1.12.2-1.0        | minecraft.jar                                         | None                                     |
	| LCHIJA | movillages          | 1.5.4             | [1.12]MoVillages-1.5.4.jar                            | None                                     |
	| LCHIJA | aether_legacy       | 1.5.3.2           | aether-1.12.2-v1.5.4.0.jar                            | None                                     |
	| LCHIJA | animalbikes         | 1.11.2            | AnimalBikes_1.12.2(13Jan19).jar                       | None                                     |
	| LCHIJA | biomesoplenty       | 7.0.1.2445        | BiomesOPlenty-1.12.2-7.0.1.2445-universal.jar         | None                                     |
	| LCHIJA | craftstudioapi      | 1.0.0             | CraftStudioAPI-universal-1.0.1.95-mc1.12-alpha.jar    | None                                     |
	| LCHIJA | mantle              | 1.12-1.3.3.55     | Mantle-1.12-1.3.3.55.jar                              | None                                     |
	| LCHIJA | natura              | 1.12.2-4.3.2.69   | natura-1.12.2-4.3.2.69.jar                            | None                                     |
	| LCHIJA | harvestcraft        | 1.12.2zb          | Pam's HarvestCraft 1.12.2zg.jar                       | None                                     |
	| LCHIJA | ctm                 | MC1.12.2-1.0.2.31 | CTM-MC1.12.2-1.0.2.31.jar                             | None                                     |
	| LCHIJA | twilightforest      | 3.11.1021         | twilightforest-1.12.2-3.11.1021-universal.jar         | None                                     |
	| LCHIJA | animania            | 2.0.3.28          | animania-1.12.2-base-2.0.3.28.jar                     | None                                     |
	| LCHIJA | antiqueatlas        | 4.5.1             | antiqueatlas-1.12.2-4.5.1.jar                         | e631d7254e451d0360d0148cb21407d5511d45e9 |
	| LCHIJA | antiqueatlasoverlay | 1.2               | antiqueatlas-1.12.2-4.5.1.jar                         | e631d7254e451d0360d0148cb21407d5511d45e9 |
	| LCHIJA | autoreglib          | 1.3-32            | AutoRegLib-1.3-32.jar                                 | None                                     |
	| LCHIJA | ichunutil           | 7.2.2             | iChunUtil-1.12.2-7.2.2.jar                            | 4db5c2bd1b556f252a5b8b54b256d381b2a0a6b8 |
	| LCHIJA | backtools           | 7.0.1             | BackTools-1.12.2-7.0.1.jar                            | 4db5c2bd1b556f252a5b8b54b256d381b2a0a6b8 |
	| LCHIJA | baubles             | 1.5.2             | Baubles-1.12-1.5.2.jar                                | None                                     |
	| LCHIJA | bettercaves         | 1.12.2            | bettercaves-1.12.2-2.0.2 (1).jar                      | None                                     |
	| LCHIJA | bibliocraft         | 2.4.6             | BiblioCraft[v2.4.6][MC1.12.2].jar                     | None                                     |
	| LCHIJA | jei                 | 4.16.1.301        | jei_1.12.2-4.16.1.301.jar                             | None                                     |
	| LCHIJA | chisel              | MC1.12.2-1.0.2.45 | Chisel-MC1.12.2-1.0.2.45.jar                          | None                                     |
	| LCHIJA | clumps              | 3.1.2             | Clumps-3.1.2.jar                                      | None                                     |
	| LCHIJA | codechickenlib      | 3.2.3.358         | CodeChickenLib-1.12.2-3.2.3.358-universal.jar         | f1850c39b2516232a2108a7bd84d1cb5df93b261 |
	| LCHIJA | corpse              | 1.12.2-1.0.8      | corpse-1.12.2-1.0.8.jar                               | None                                     |
	| LCHIJA | customspawner       | 3.11.4            | CustomMobSpawner-3.11.5.jar                           | None                                     |
	| LCHIJA | ptrmodellib         | 1.0.5             | PTRLib-1.0.5.jar                                      | None                                     |
	| LCHIJA | props               | 2.6.3.7           | Decocraft-2.6.3.7_1.12.2.jar                          | None                                     |
	| LCHIJA | doggytalents        | 1.15.1.6          | DoggyTalents-1.12.2-1.15.1.6.jar                      | None                                     |
	| LCHIJA | mocreatures         | 12.0.5            | DrZharks MoCreatures Mod-12.0.5.jar                   | None                                     |
	| LCHIJA | fairylights         | 2.1.10            | fairylights-2.2.0-1.12.2.jar                          | None                                     |
	| LCHIJA | familiarfauna       | 1.0.11            | FamiliarFauna-1.12.2-1.0.11.jar                       | None                                     |
	| LCHIJA | fenceoverhaul       | 1.3.4             | FenceOverhaul-1.3.4.jar                               | None                                     |
	| LCHIJA | llibrary            | 1.7.20            | llibrary-1.7.20-1.12.2.jar                            | b9f30a813bee3b9dd5652c460310cfcd54f6b7ec |
	| LCHIJA | fossil              | 8.0.5             | fossilsarcheology-8.0.6.jar                           | None                                     |
	| LCHIJA | cfm                 | 6.3.0             | furniture-6.3.2-1.12.2.jar                            | None                                     |
	| LCHIJA | hats                | 7.1.1             | Hats-1.12.2-7.1.1.jar                                 | 4db5c2bd1b556f252a5b8b54b256d381b2a0a6b8 |
	| LCHIJA | hatstand            | 7.1.0             | HatStand-1.12.2-7.1.0.jar                             | None                                     |
	| LCHIJA | waila               | 1.8.26            | Hwyla-1.8.26-B41_1.12.2.jar                           | None                                     |
	| LCHIJA | inspirations        | 1.12.2-0.2.9      | Inspirations-1.12.2-0.2.9.jar                         | None                                     |
	| LCHIJA | inventorypets       | 2.0.15            | inventorypets-1.12-2.0.15.jar                         | None                                     |
	| LCHIJA | ironchest           | 1.12.2-7.0.67.844 | ironchest-1.12.2-7.0.72.847.jar                       | None                                     |
	| LCHIJA | jeresources         | 0.9.2.60          | JustEnoughResources-1.12.2-0.9.2.60.jar               | None                                     |
	| LCHIJA | mcwdoors            | 1.3               | mcw-doors-1.0.3-mc1.12.2.jar                          | None                                     |
	| LCHIJA | mcwfences           | 1.0.0             | mcw-fences-1.0.0-mc1.12.2.jar                         | None                                     |
	| LCHIJA | mcwwindows          | 1.0               | mcw-windows-1.0.0-mc1.12.2.jar                        | None                                     |
	| LCHIJA | morph               | 7.2.0             | Morph-1.12.2-7.2.1.jar                                | 4db5c2bd1b556f252a5b8b54b256d381b2a0a6b8 |
	| LCHIJA | morpheus            | 1.12.2-3.5.106    | Morpheus-1.12.2-3.5.106.jar                           | None                                     |
	| LCHIJA | naturescompass      | 1.8.5             | NaturesCompass-1.12.2-1.8.5.jar                       | None                                     |
	| LCHIJA | netherportalfix     | 5.3.17            | NetherPortalFix_1.12.1-5.3.17.jar                     | None                                     |
	| LCHIJA | nei                 | 2.4.3             | NotEnoughItems-1.12.2-2.4.3.245-universal.jar         | f1850c39b2516232a2108a7bd84d1cb5df93b261 |
	| LCHIJA | patchouli           | 1.0-23.6          | Patchouli-1.0-23.6.jar                                | None                                     |
	| LCHIJA | placeableitems      | 3.3               | placeableitems-3.3.jar                                | None                                     |
	| LCHIJA | pvj                 | 1.6.4             | ProjectVibrantJourneys-1.12.2-1.6.4.jar               | None                                     |
	| LCHIJA | statues             | 0.8.10            | statues-1.12.2-0.8.11.jar                             | None                                     |
	| LCHIJA | timber              | 1.2.0             | timber-1.12.2-1.2.0.jar                               | None                                     |
	| LCHIJA | torchmaster         | 1.8.5.0           | torchmaster_1.12.2-1.8.5.0.jar                        | None                                     |
	| LCHIJA | wearablebackpacks   | 3.1.4             | Wearable-Backpacks-Mod-1.12.2.jar                     | None                                     |
	| LCHIJA | wings               | 1.1.6             | wings-1.1.6-1.12.2.jar                                | None                                     |
	| LCHIJA | bauble_wings        | 1.0.0             | wings-1.1.6-1.12.2.jar                                | None                                     |
	| LCHIJA | wolfarmor           | 3.8.0             | WolfArmorAndStorage-1.12.2-3.8.0-universal-signed.jar | e94e38a605842477f3ec218e6fcf781f6b3f7f89 |
	| LCHIJA | xaerominimap        | 23.9.7            | Xaeros_Minimap_23.9.7_Forge_1.12.jar                  | None                                     |
	| LCHIJA | xaeroworldmap       | 1.37.8            | XaerosWorldMap_1.37.8_Forge_1.12.jar                  | None                                     |
	| LCHIJA | totemexpansion      | 1.2.2             | totemexpansion-1.2.2-1.12.2.jar                       | None                                     |
	| UD     | mowzies_wings       | 1.0.0             | wings-1.1.6-1.12.2.jar                                | None                                     |
	| UD     | mobends_wings       | 1.0.0             | wings-1.1.6-1.12.2.jar                                | None                                     |

	Loaded coremods (and transformers): 
llibrary (llibrary-core-1.0.11-1.12.2.jar)
  net.ilexiconn.llibrary.server.core.plugin.LLibraryTransformer
  net.ilexiconn.llibrary.server.core.patcher.LLibraryRuntimePatcher
wings (wings-1.1.6-1.12.2.jar)
  me.paulf.wings.server.asm.WingsRuntimePatcher
  me.paulf.wings.server.asm.mobends.WingsMoBendsRuntimePatcher
WolfArmorCore (WolfArmorAndStorage-1.12.2-3.8.0-universal-signed.jar)
  
XaeroMinimapPlugin (Xaeros_Minimap_23.9.7_Forge_1.12.jar)
  xaero.common.core.transformer.ChunkTransformer
  xaero.common.core.transformer.NetHandlerPlayClientTransformer
  xaero.common.core.transformer.EntityPlayerTransformer
  xaero.common.core.transformer.AbstractClientPlayerTransformer
  xaero.common.core.transformer.WorldClientTransformer
  xaero.common.core.transformer.EntityPlayerMPTransformer
  xaero.common.core.transformer.EntityPlayerSPTransformer
  xaero.common.core.transformer.PlayerListTransformer
  xaero.common.core.transformer.SaveFormatTransformer
  xaero.common.core.transformer.GuiIngameForgeTransformer
  xaero.common.core.transformer.MinecraftServerTransformer
  xaero.common.core.transformer.GuiBossOverlayTransformer
  xaero.common.core.transformer.ModelRendererTransformer
XaeroWorldMapPlugin (XaerosWorldMap_1.37.8_Forge_1.12.jar)
  xaero.map.core.transformer.ChunkTransformer
  xaero.map.core.transformer.NetHandlerPlayClientTransformer
  xaero.map.core.transformer.EntityPlayerTransformer
  xaero.map.core.transformer.AbstractClientPlayerTransformer
  xaero.map.core.transformer.WorldClientTransformer
  xaero.map.core.transformer.EntityPlayerMPTransformer
  xaero.map.core.transformer.PlayerListTransformer
  xaero.map.core.transformer.SaveFormatTransformer
  xaero.map.core.transformer.BiomeColorHelperTransformer
  xaero.map.core.transformer.MinecraftServerTransformer
  xaero.map.core.transformer.MinecraftTransformer
CTMCorePlugin (CTM-MC1.12.2-1.0.2.31.jar)
  team.chisel.ctm.client.asm.CTMTransformer
	GL info: ' Vendor: 'ATI Technologies Inc.' Version: '4.6.0 Compatibility Profile Context 22.40.52.07.231123' Renderer: 'AMD Radeon RX 5500'
	Pulsar/natura loaded Pulses: 
		- NaturaCommons (Enabled/Forced)
		- NaturaOverworld (Enabled/Not Forced)
		- NaturaNether (Enabled/Not Forced)
		- NaturaDecorative (Enabled/Not Forced)
		- NaturaTools (Enabled/Not Forced)
		- NaturaEntities (Enabled/Not Forced)
		- NaturaOredict (Enabled/Forced)
		- NaturaWorld (Enabled/Not Forced)

	Pulsar/inspirations loaded Pulses: 
		- InspirationsShared (Enabled/Forced)
		- InspirationsBuilding (Enabled/Not Forced)
		- InspirationsUtility (Enabled/Not Forced)
		- InspirationsTools (Enabled/Not Forced)
		- InspirationsRecipes (Enabled/Not Forced)
		- InspirationsTweaks (Enabled/Not Forced)
		- InspirationsShared (Enabled/Forced)
		- WailaPlugin (Enabled/Not Forced)
		- TwilightForestPlugin (Enabled/Not Forced)

	Patchouli open book context: n/a
	Launched Version: 1.12.2-forge-14.23.5.2859
	LWJGL: 2.9.4
	OpenGL: AMD Radeon RX 5500 GL version 4.6.0 Compatibility Profile Context 22.40.52.07.231123, ATI Technologies Inc.
	GL Caps: Using GL 1.3 multitexturing.
Using GL 1.3 texture combiners.
Using framebuffer objects because OpenGL 3.0 is supported and separate blending is supported.
Shaders are available because OpenGL 2.1 is supported.
VBOs are available because OpenGL 1.5 is supported.

	Using VBOs: Yes
	Is Modded: Definitely; Client brand changed to 'fml,forge'
	Type: Client (map_client.txt)
	Resource Packs: Better-Leaves-7.2-1.19+.zip (incompatible), CFM Model Backport mc1.12.2-v1.2.zip (incompatible), Clear Glass Pack 1.11 or 1.12.zip, NightVision_1.7-1.12.zip, Vanilla_Future_Texture_optifine.zip, MandalasGUI_Dakmode_Vanilla1.20.4.zip (incompatible)
	Current Language: English (US)
	Profiler Position: N/A (disabled)
	CPU: 8x AMD Ryzen 3 5300G with Radeon Graphics 
	OptiFine Version: OptiFine_1.12.2_HD_U_F5
	OptiFine Build: 20191204-141934
	Render Distance Chunks: 12
	Mipmaps: 4
	Anisotropic Filtering: 1
	Antialiasing: 0
	Multitexture: false
	Shaders: Sildur's Vibrant Shaders v1.51 Extreme-VL.zip
	OpenGlVersion: 4.6.0 Compatibility Profile Context 22.40.52.07.231123
	OpenGlRenderer: AMD Radeon RX 5500
	OpenGlVendor: ATI Technologies Inc.
	CpuCount: 8
 
