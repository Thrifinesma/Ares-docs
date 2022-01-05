.. index::
  Paradrops; Parachute animations per unit
  TechnoTypes; Parachute animations
  Art; Parachute animations

自定义降落伞动画
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Units can now have their own individual parachute animation.

:tagdef:`[TechnoType]Parachute.Anim=animation`
  Specifies the animation from :file:`artmd.ini` to use as the unit's parachute
  when it is falling. If omitted, :tag:`Parachute.Anim` will default to
  :value:`PARACH`. The SHP is expected to be in the unit palette.

.. versionadded:: 0.1
