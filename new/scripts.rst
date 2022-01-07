脚本动作
~~~~~~~~~~~~~~

See :doc:`Editor Support </new/editorsupport>` on how to use the new Script
Actions from map editors.

敌方基地外集合（53）
``````````````````````````````````

The previously unused parameter of the :value:`Gather at Enemy` script action is
now added to :tag:`[General]AISafeDistance` to determine the distance from the
center of the enemy base the team should gather at. Can be negative to shorten
the distance.

.. versionadded:: 2.0



.. index:: Scripts; Distance setting for Gather at Base

己方基地外集合（54）
`````````````````````````````````

:game:`Ares` splits the tag :tag:`[General]AISafeDistance` into two, which is
used for two similar team script actions serving different purposes.

:tagdef:`[General]AIFriendlyDistance=integer - cells`
  Cell distance the AI will use for gathering outside the owning player's base
  using script action 54. Defaults to :tag:`[General]AISafeDistance`.

Like for the :value:`Gather at Enemy` script action, the previously unused
parameter of the :value:`Gather at Base` script action is now added to the
distance from the center of the own base the team should gather at. Can be
negative to shorten the distance.

.. versionadded:: 2.0



.. index:: Scripts; Iron Curtain team script extended

.. _script-ironcurtain:

铁幕 / 请求超武（55）
```````````````````````````````

Previously, the game would only look at the first (and usually only) super
weapon with :tag:`Type=IronCurtain`, then check whether it was either ready or
almost charged. If that was not the case, the script action failed.

:game:`Ares` will instead check all super weapon with
:tag:`SW.AITargetingMode=IronCurtain` and will fire the first one that is fully
charged, or wait, if any is at least almost charged. The script will fail
otherwise.

The previously unused parameter of the :value:`IronCurtain` script action is now
used to denote the group the Iron Curtain super weapon has to belong to before
being considered. This allows to create super weapon groups (for instance for
traditional Iron Curtain and new AttachEffect boosts) and different teams to
rely on different super weapon groups.

.. versionadded:: 2.0



.. index:: Scripts; Auxiliary Power

给予额外电力（65）
``````````````````````````````````

This new script action permanently changes the power output of the house owning
the team. Power value can be negative to create a power drain. Applying this
effect multiple times is cumulative.

The format is :value:`65,<power>`.

.. versionadded:: 3.0



.. index:: Scripts; Kill Drivers

杀死驾驶员（66）
```````````````````````````````

Kills all drivers of the units in this team. This script respects Protected
Drivers, Iron Curtain and all the other mechanisms that prevent drivers being
killed.

All affected units will change to the country called :value:`Special`.

The format is :value:`66,0`.

.. versionadded:: 3.0



.. index:: Scripts; Take Vehicles

夺取最近可占领载具（67）
````````````````````````````````

All infantry in this team that are either :tag:`CanDrive=yes` or
:tag:`VehicleThief=yes` will be assigned the closest vehicle they can drive or
hijack. If the infantry finds a vehicle to take, it will leave the team.

This works like the similar script actions :value:`Garrison Structure`,
:value:`Enter Occupiable`, and :value:`Enter Tank Bunker`: The infantry will try
to find a new object once the current one becomes unavailable for capturing. If
there is none such alternative object to take, the infantry will stop.

The format is :value:`67,0`.

.. versionadded:: 3.0



.. index:: Scripts; Convert Type

.. _script-converttype:

变形（68）
```````````````````````````````

Immediately changes all members of this team into their respective script
conversion types, if set. Units that don't have this tag set stay unaffected.
This is a generalization of the script actions :value:`Unload Truck` and
:value:`Load Truck`.

See :ref:`Conversion Triggered by Team Script <convert-script>` for a
description of this feature.

The format is :value:`68,0`.

.. versionadded:: 3.0



.. index:: Scripts; Sonar Reveal

声呐探测 / 解除隐形（69）
```````````````````````````````

Disables the ability of all team members to cloak themselves for a number of
frames defined by the second parameter.

Use :value:`0` to end the sonar effect.

The format is :value:`69,<frames>`.

.. versionadded:: 3.0



.. index:: Scripts; Disable Weapons

禁用武器（70）
``````````````````````````````````

Disables the ability of all team members to fire for a number of frames defined
by the second parameter.

Use :value:`0` to end the weapon disabling effect.

The format is :value:`70,<frames>`.

.. versionadded:: 3.0
