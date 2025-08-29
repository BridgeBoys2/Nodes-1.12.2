# High level
-   The async tasks do not have proper synchronization. There isn't
    proper locking to make sure async stuff runs properly, TODO.
    Check filesystem saving sync as well.
-   No real API. Most functionality is attached to the Nodes object
    with intent that this basically acts as API. But not well defined
    and subject to change.
-   Nodes world state is global variable, so only supports single world.
    E.g. no separate nodes map for overworld + nether.
    This is likely not to change since goal is only single map/world.
-   No API for custom node/territory properties.
-   Cannot `/nodes reload` world. Inconvenient. TODO.
-   Get rid of java.io.File, swap to nio


# Nodes
-   Fix moving stuff back into town nodes income inventory with shift click

# Minimap
-   Port indicator on chunk. Would require a minimap api though since ports
    are intended to be a plugin...?
-   Chunks with war flags indicator, e.g. flashing or separate minimap symbol

# War
-   Indicator above war claim flag showing enemy/ally owner whos attacking
-   Claiming incontiguous territories short distance across seazone/wasteland
-   Seazone border claiming penalty only on edge chunks not bordering friendly land
-   Make it take longer to break claims flags so players cant naked greek
    with sheers.
    https://www.spigotmc.org/threads/why-custom-block-breaking-change-block-hardness.531825/#post-4291982
    https://www.spigotmc.org/resources/breaker-2-configurable-breaking-speeds-1-16-1-18.99022/