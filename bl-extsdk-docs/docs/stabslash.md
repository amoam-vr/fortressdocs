# Stab Slash
Gives a `Marrow Entity` (a spawnable) the ability to stab and damage enemies and certain spawnables. Can also be used to inflict blunt damage.

## Requirements
A `Stab Slash` **must** be on the same `GameObject` as a `Marrow Entity`.

## Properties
<table>
  <tr>
    <td><b>Property Name</b><br><b style="color:#000000">______________________</b></td>
    <td><b>Property Type</b><br><b style="color:#000000">______________________</b></td>
    <td><b>Property Description</b></td>
  </tr>
  <tr>
    <td>Stab Points</td>
    <td><code>StabPoint[]</code></td>
    <td>Points on the blade where objects and enemies can be impaled in a straight line.</td>
  </tr>
  <tr>
    <td>Point Tran</td>
    <td><code>Transform</code></td>
    <td>The <code>Transform</code> at which the stabbing begins; the 'tip' of the blade. <b style="color: #05ffc0">NOTE: Make sure the Z axis of this Transform points outward in the direction of the stab, and that the Transform sits near the surface of the Point Collider, but not within the Point Collider.</b></td>
  </tr>
  <tr>
    <td>Point Collider</td>
    <td><code>Collider</code></td>
    <td>The <code>Collider</code> on which this point should detect collisions with. Normally should have <code>Is Trigger</code> set to <code>false</code>.</td>
  </tr>
  <tr>
    <td>Max Depth</td>
    <td><code>float</code></td>
    <td>How far this stab point can impale an object in meters.</td>
  </tr>
  <tr>
    <td>Aspect Ratio</td>
    <td><code>float</code></td>
    <td>The shape of the tip of the blade. <b style="color: #e2ce46">NEEDS CONFIRMATION</b></td>
  </tr>
  <tr>
    <td>Stab Break Force</td>
    <td><code>float</code></td>
    <td>The amount of force required to snap off the current stab connection.</td>
  </tr>
</table>

## Example
<img src="../examplescript_stab_slash.png" alt="Example Script: Stab Slash" width="50%">