Empties player's inventory on death and spawns a container with its contents, available for anyone to take.

Requires [DataManager](https://github.com/tes3mp-scripts/DataManager) and [ContainerFramework](https://github.com/tes3mp-scripts/ContainerFramework)!

You can find the configuration file in `server/data/custom/__config_FullLoot.json`.
* `container` parameters of the container permanent record to make for use in `ContainerFramework`.
  * `refId`
  * `name`
  * `baseId`
  * `packetType`
  * `type`
* `guise` container's appearance.
  * `name`
  * `models` a list of different models, chosen at random.
  * `type` type of the object used for appearance.
  * `packetType` should be `spawn` for NPCs and creatures and `place` otherwise.
  * `script` set do `noPickUp` to prevent players from grabbing containers. Not recommended to change.
* `offset` vector that is added to player's location to position the container. Useful for making its rotation match the players' or hiding transparent parts of the model underground.
  * `posX`
  * `posY`
  * `posZ`
  * `rotX`
  * `rotY`
  * `rotZ`
* `collision` whether `guise` has collision
* `despawn` whether containers should disappear (`false` by default).
* `despawnTime` how long (in game hours) containers take to despawn.