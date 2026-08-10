# Cylinder Grip
A type of grip that lets you hold items like handles, rods, beams and sticks. 

This grip lets you slide your hand across it while not holding the **GRIP** button.

While holding the **GRIP** button, your hand stays fixed at its current position along the cylinder grip.

## Requirements
A `Cylinder Grip` **must** have a `Capsule Collider` on the same `GameObject` with `Is Trigger` typically set to `True`, and `Direction` typically set to `Z-Axis`, although these values are not strictly required. The `GameObject` **must** be set to the `Interactable` layer.

## Example
<img src="../examplescript_cylinder_grip.png" alt="Example Script: Cylinder Grip" width="50%">

## Properties
<table>
  <tr>
    <td><b>Property Name</b></td>
    <td><b>Property Type</b></td>
    <td><b>Property Usage</b></td>
  </tr>
  <tr>
    <td>Is Throwable</td>
    <td><code>bool</code></td>
    <td>Typically always <code>true</code>. <b style="color: #ff0000">DOES THIS DO ANYTHING WHEN FALSE?</b></td>
  </tr>
  <tr>
    <td>Ignore Grip Target On Attach</td>
    <td><code>bool</code></td>
    <td>If <code>true</code>, the Target value won't be used when determining the position of your hand for the grip. <b style="color: #ff0000">THEN WHAT'S USED INSTEAD?</b></td>
  </tr>
  <tr>
    <td>Additional Grip Colliders</td>
    <td><code>Collider[]</code></td>
    <td>While this grip is held, the <code>Collider</code>s in this list won't collide with your body. <b style="color: #ff0000">NEEDS VERIFICATION</b></td>
  </tr>
  <tr>
    <td>Handle Amplify Curve</td>
    <td><code>AnimationCurve</code></td>
    <td><b style="color: #ff0000">UNKNOWN</b></td>
  </tr>
  <tr>
    <td>Hand Pose</td>
    <td><code>HandPose</code></td>
    <td>When this grip is held, your hand will match the pose assigned.</td>
  </tr>
  <tr>
    <td>Primary Movement Axis</td>
    <td><code>Vector3</code></td>
    <td>When this object is gripped, this axis should be pointing in the same direction as your thumb in a "thumbs up" position. Typically set to <code>(0, 0, 1)</code>.</td>
  </tr>
  <tr>
    <td>Secondary Movement Axis</td>
    <td><code>Vector3</code></td>
    <td>When this object is gripped, this axis should be pointing down your forearm. Typically set to <code>(0, 1, 0)</code>.</td>
  </tr>
  <tr>
    <td>Grip Options</td>
    <td><code>InteractionOptions</code></td>
    <td>See <b style="color: #ff0000">InteractionOptions</b>.</td>
  </tr>
</table>