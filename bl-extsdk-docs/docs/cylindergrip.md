# Cylinder Grip
A type of grip that lets you hold items like handles, rods, beams and sticks. 

This grip lets you slide your hand across it while not holding the **GRIP** button.

While holding the **GRIP** button, your hand stays fixed at its current position along the cylinder grip.

## Requirements
A `Cylinder Grip` **must** have a `Capsule Collider` on the same `GameObject` with `Is Trigger` usually set to `True`, and `Direction` usually set to `Z-Axis`, although these values are not strictly required. The `GameObject` **must** be set to the `Interactable` layer (internally 15). 

Additionally, an `Interactable Host` is required beside a `Marrow Entity` on a parent for grips to work.

## Properties
<table>
  <tr>
    <td><b>Property Name</b><br><b style="color:#000000">______________________</b></td>
    <td><b>Property Type</b><br><b style="color:#000000">______________________</b></td>
    <td><b>Property Description</b></td>
  </tr>
  <tr>
    <td>Is Throwable</td>
    <td><code>bool</code></td>
    <td>Usually always <code>true</code>. <b style="color: #e2ce46">DOES THIS DO ANYTHING WHEN FALSE?</b></td>
  </tr>
  <tr>
    <td>Ignore Grip Target On Attach</td>
    <td><code>bool</code></td>
    <td>If <code>true</code>, the <code>Transform</code> this grip is on will be used when determining the position of your hand for the grip instead of the assigned Target value. <b style="color: #e2ce46">NEEDS CONFIRMATION</b></td>
  </tr>
  <tr>
    <td>Additional Grip Colliders</td>
    <td><code>Collider[]</code></td>
    <td>While this grip is held, the <code>Collider</code>s in this list won't collide with your body. <b style="color: #e2ce46">NEEDS CONFIRMATION</b></td>
  </tr>
  <tr>
    <td>Handle Amplify Curve</td>
    <td><code>AnimationCurve</code></td>
    <td><b style="color: #e2ce46">UNKNOWN</b></td>
  </tr>
  <tr>
    <td>Hand Pose</td>
    <td><code>HandPose</code></td>
    <td>When this grip is held, your hand will match the pose assigned. <b style="color: #e2ce46">NOTE: Some HandPoses that come with the SDK can break the grip completely (Found by Rusky).</b></td>
  </tr>
  <tr>
    <td>Primary Movement Axis</td>
    <td><code>Vector3</code></td>
    <td>When this object is gripped, this axis should be pointing in the same direction as your thumb in a "thumbs up" position. Usually set to <code>(0, 0, 1)</code>.</td>
  </tr>
  <tr>
    <td>Secondary Movement Axis</td>
    <td><code>Vector3</code></td>
    <td>When this object is gripped, this axis should be pointing down your forearm. Usually set to <code>(0, 1, 0)</code>.</td>
  </tr>
  <tr>
    <td>Grip Options</td>
    <td><code>InteractionOptions</code></td>
    <td>See <b style="color: #e2ce46">InteractionOptions</b>.</td>
  </tr>
  <tr>
    <td>Priority</td>
    <td><code>float</code></td>
    <td>The lower this number is, the higher priority this grip has. For example, if at 0, and other grips with priority greater than 0 are near your hand, then this grip will always be grabbed instead of the others.</td>
  </tr>
  <tr>
    <td>Min Break Force</td>
    <td><code>float</code></td>
    <td>Usually set to <code>Infinity</code>, this number is the minimum amount of force required for your hand to automatically let go of the grip.</td>
  </tr>
  <tr>
    <td>Max Break Force</td>
    <td><code>float</code></td>
    <td>Usually set to <code>Infinity</code>. Honestly not sure why this is here since a <code>Joint</code> doesn't have a BreakForce range value.</td>
  </tr>
  <tr>
    <td>Default Grip Distance</td>
    <td><code>float</code></td>
    <td>Usually set to <code>Infinity</code>. Unsure on what this value does, because despite this regularly being <code>Infinity</code>, you can't grab this from an infinite distance away.</td>
  </tr>
  <tr>
    <td>Radius</td>
    <td><code>float</code></td>
    <td>This value should roughly match the <code>Radius</code> value of the <code>Capsule Collider</code> this grip belongs to.</td>
  </tr>
  <tr>
    <td>Target Transform</td>
    <td><code>Transform</code></td>
    <td>Determines the actual location at which your hand will grab around.</td>
  </tr>
  <tr>
    <td>Rotation Limit</td>
    <td><code>float</code></td>
    <td>Usually set to <code>180</code>. Determines how far (in degrees) your hand can spin around the grip from the default position.</td>
  </tr>
  <tr>
    <td>Rotation Priority Buffer</td>
    <td><code>float</code></td>
    <td><b style="color: #e2ce46">UNKNOWN</b></td>
  </tr>
  <tr>
    <td>Hand Pose On Flipped Primary Axis</td>
    <td><code>HandPose</code></td>
    <td>If you hold the grip upside down, this pose will be used rather than the normal assigned pose. <b style="color: #e2ce46">NEEDS CONFIRMATION</b></td>
  </tr>
  <tr>
    <td>Target Flip On Primary Axis</td>
    <td><code>bool</code></td>
    <td><b style="color: #e2ce46">UNKNOWN</b></td>
  </tr>
  <tr>
    <td>Target Flip On Tertiary Axis</td>
    <td><code>bool</code></td>
    <td><b style="color: #e2ce46">UNKNOWN</b></td>
  </tr>
  <tr>
    <td>Dynamic Friction</td>
    <td><code>float</code></td>
    <td>When you hold this grip with only <b>TRIGGER</b>, this is how much friction your hand receives when moving it along the grip. <b style="color: #e2ce46">NEEDS CONFIRMATION</b></td>
  </tr>
  <tr>
    <td>Static Friction</td>
    <td><code>float</code></td>
    <td>When you hold this grip with <b>GRIP</b>, this is how much friction your hand receives when moving it along the grip. <b style="color: #e2ce46">NEEDS CONFIRMATION</b></td>
  </tr>
  <tr>
    <td>Limit</td>
    <td><code>float</code></td>
    <td>This value should match the <code>Height</code> value of the <code>Capsule Collider</code> this grip belongs to divided by 2. This value determines how far you can slide your hands up and down the grip.</td>
  </tr>
  <tr>
    <td>Has Cap A</td>
    <td><code>bool</code></td>
    <td><b style="color: #e2ce46">UNKNOWN</b></td>
  </tr>
  <tr>
    <td>Has Cap B</td>
    <td><code>bool</code></td>
    <td><b style="color: #e2ce46">UNKNOWN</b></td>
  </tr>
  <tr>
    <td>Ignore Flip On Z</td>
    <td><code>bool</code></td>
    <td>If <code>true</code>, this object cannot be gripped upside down. <b style="color: #e2ce46">NEEDS CONFIRMATION</b></td>
  </tr>
  <tr>
    <td>Rotational Friction Mult</td>
    <td><code>float</code></td>
    <td><b style="color: #e2ce46">UNKNOWN</b></td>
  </tr>
  <tr>
    <td>Aspect Ratio</td>
    <td><code>float</code></td>
    <td><b style="color: #e2ce46">UNKNOWN</b></td>
  </tr>
  <tr>
    <td>Variable Radius</td>
    <td><code>bool</code></td>
    <td>If <code>true</code>, this grip will use the <code>Radius Curve</code> value to determine the grip radius along the object.</td>
  </tr>
  <tr>
    <td>Radius Curve</td>
    <td><code>AnimationCurve</code></td>
    <td>As you slide your hand across the grip, this curve determines the radius of the grip at that position by overriding the <code>Radius</code> property. The left side of the curve (where Time = 0) is the bottom of the grip, and the right side of the curve (where Time = 1) is the top of the grip.</td>
  </tr>
</table>

## Example
<img src="../media/examplescript_cylinder_grip.png" alt="Example Script: Cylinder Grip" width="50%">