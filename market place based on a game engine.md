An fps focused quake like game engine with built in map editor. Runs in web browser.

Goals:
- Focus on FPS rather than general game engine to make content creation simpler.
- Focus on low poly map geometry that can all be created inside the game editor rather than imported from a 3D modelling package. Quake engine's BSP brushes seem to be a sweet spot between Doom's 2.5D geometry or Minecraft like voxel worlds and unrestricted meshes used in Unity and Unreal. We aim to strike balance of expressivity and simplicity. Doom is still more popular than Quake among mappers because of how easy it is to make 2D sector based Doom maps, but similar tools could be brought to BSP like geometry, while still allowing true 3D geometry when needed. BSP:s are not required anymore for performance reasons, but restricting to convex blocks seems to make it easier to manage geometry compared to unrestricted triangle based meshes. There may be other geometry paradigms still undiscovered that would combine easiness and expressivity even better.
- Basic map editing should be as simple as playing Minecraft. Editing could be gamified by mapping challenges that ask the user to complete map geometry to learn the mapping tools.
- Multiplayer map editing: friends can play or edit the map while you edit it. Like [Reflex arena](https://www.reflexarena.com/) and [Diabotical](https://www.diabotical.com/) .
- Longetivity guarantee: engine is open source. Content creators should be assured that their creations can be experienced on the decades to come. The active Doom and Quake mapping communities show that game engines can live for decades even if content creation tools are made by hobbyists and lack in comparison to professionally developed tools
- content creators can earn money: maps, assets and editor plugins can be sold with micro transactions.
- Game logic is programmable with clojurescript.
- Development workflow should be fully interactive. Editor and the game share the same engine. Lightmaps for global illumination are ray traced in realtime with GPU.
- Easy to setup multiplayer servers financed with monthly subscription.
- Version control for maps that allow pull requests and visual diffs.
- Runs in browser. Maps should be playable just by clicking a link.

Non goals:
- Generic game engine for non FPS games
- High fidelity map geometry that requires dedicated 3D modelling software. All map geometry is encouraged to be created in the build in editor. The game engine may not be powerful enough to support huge polygon counts. Game entities such as enemies or items can still be modelled and animated in external software such as Blender. Also using an external image editor should be fully supported for creating textures.
- Arena shooter focus. Arena shooters require active community so that people have players to play with. They do not encourage making new maps since each map is it's own game that requires years of practice to master.
- Obscure game currency such like Robux that makes it hard to understand the real price of content.

Competitors:
- [Prodeus](https://store.steampowered.com/app/964800/Prodeus/)
- [Roblox](https://www.roblox.com/)
- [Krunker](https://krunker.io/)
- [Reflex arena](https://www.reflexarena.com/)
- [Diabotical](https://www.diabotical.com/)
- [Unity](https://unity.com/)
- [Unreal](https://www.unrealengine.com/)