# Stab Slash
Gives a `Marrow Entity` (a spawnable) the ability to stab and damage enemies and certain spawnables. Can also be used to inflict blunt damage.

## Requirements
A `Stab Slash` **must** be on the same `GameObject` as a `Marrow Entity`. 

All Blade Audio fields that require an `AudioClip` **must** be filled out with at least one valid sound, otherwise the blade will not work properly.

For every `Stab Point` and `Slash Blade`, there **must** be at least one `StabJoint`/`BladeJoint` (does not need to be filled out and can be completely empty), otherwise the blade will not work properly likely because of the blade script always expecting there to be a first element.

## Properties
<table>
  <tr>
    <td><b>Property Name</b><br><b style="color: #00000000">______________________</b></td>
    <td><b>Property Type</b><br><b style="color: #00000000">______________________</b></td>
    <td><b>Property Description</b></td>
  </tr>
  <tr>
    <td>Stab Points</td>
    <td><code>StabPoint[]</code></td>
    <td>Points on the blade where objects and enemies can be impaled in a straight line.</td>
  </tr>
  <tr>
    <td><code>StabPoint</code><br>Point Tran</td>
    <td><code>Transform</code></td>
    <td>The <code>Transform</code> at which the stabbing begins; the 'tip' of the blade. <b style="color: #05ffc0">NOTE: Make sure the Z axis of this Transform points outward in the direction of the stab, and that the Transform sits near the surface of the Point Collider, but not within the Point Collider. Position this Transform where you want the stab to start.</b></td>
  </tr>
  <tr>
    <td><code>StabPoint</code><br>Point Collider</td>
    <td><code>Collider</code></td>
    <td>The <code>Collider</code> on which this point should detect collisions with. Normally should have <code>Is Trigger</code> set to <code>false</code>.</td>
  </tr>
  <tr>
    <td><code>StabPoint</code><br>Max Depth</td>
    <td><code>float</code></td>
    <td>How far this stab point can impale an object in meters.</td>
  </tr>
  <tr>
    <td><code>StabPoint</code><br>Aspect Ratio</td>
    <td><code>float</code></td>
    <td>The shape of the tip of the blade. <b style="color: #e2ce46">NEEDS CONFIRMATION</b></td>
  </tr>
  <tr>
    <td><code>StabPoint</code><br>Stab Break Force</td>
    <td><code>float</code></td>
    <td>The amount of force required to snap off the current stab connection.</td>
  </tr>
  <tr>
    <td><code>StabPoint</code><br>Sharpness</td>
    <td><code>float</code></td>
    <td><b style="color: #e2ce46">UNKNOWN</b></td>
  </tr>
  <tr>
    <td><code>StabPoint</code><br>Depth Resistance Multiplier</td>
    <td><code>float</code></td>
    <td>Determines how hard it is to push an object along the blade while stabbing it.</td>
  </tr>
  <tr>
    <td><code>StabPoint</code><br>Linear Spring</td>
    <td><code>float</code></td>
    <td>The strength of the spring on this stab. <b style="color: #e2ce46">UNCLEAR</b></td>
  </tr>
  <tr>
    <td><code>StabPoint</code><br>Linear Damp</td>
    <td><code>float</code></td>
    <td>The damping of the spring joint on this stab. <b style="color: #e2ce46">UNCLEAR</b></td>
  </tr>
  <tr>
    <td><code>StabPoint</code><br>Damage</td>
    <td><code>float</code></td>
    <td>The amount of damage this stab causes when an object is impaled on it.</td>
  </tr>
  <tr>
    <td><code>StabPoint</code><br>Stab Joints</td>
    <td><code>StabJoint[]</code></td>
    <td><b style="color: #e2ce46">UNKNOWN</b></td>
  </tr>
  <tr>
    <td><code>StabPoint</code><br>Impale Count</td>
    <td><code>int</code></td>
    <td><b style="color: #e2ce46">UNKNOWN</b></td>
  </tr>
  <tr>
    <td>Slash Blades</td>
    <td><code>SlashBlade[]</code></td>
    <td>Points on the blade where objects and enemies can be slashed along a line.</td>
  </tr>
  <tr>
    <td><code>SlashBlade</code><br>Blade Tran</td>
    <td><code>Transform</code></td>
    <td>The center point of the slash; the 'edge' of the blade. <b style="color: #05ffc0">NOTE: Make sure the Z axis of this Transform points outward in the direction of the slash, and the Y axis of this Transform faces in the direction the edge of the blade goes in. Also, position this Transform right above the surface of the associated collider where you want the slash to be and not within it.</b></td>
  </tr>
  <tr>
    <td><code>SlashBlade</code><br>Blade Collider</td>
    <td><code>Collider</code></td>
    <td>The <code>Collider</code> on which this point should detect collisions with. Normally should have <code>Is Trigger</code> set to <code>false</code>.</td>
  </tr>
  <tr>
    <td><code>SlashBlade</code><br>Blade Length</td>
    <td><code>float</code></td>
    <td>The length of the blade in meters centered around the <code>Blade Tran</code>.</td>
  </tr>
</table>

## Example
<img src="../media/examplescript_stab_slash.png" alt="Example Script: Stab Slash" width="50%">