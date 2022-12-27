# Unity XR Project

## 1. Getting Started
1. Project settings
- On XR Plug-in Management, enable Open XR in Windows & Android
- On OpenXR Settings, add Interaction Profiles
2. Add Scene, then add plane and also apply the material
3. Click on camera, add Tracked Pose Driver profile
4. Package Manager, install com.unity.xr.interaction.toolkit
5. Add XR Origin to scene
6. Set Tracking Origin Mode to Floor
7. Add empty object, then add component XR Controller (Left & Right).
8. Import XR Interaction Toolkit from XR Package Toolkit
9. On Hand Controller, select preset based on each hand.
10. Add Input Action Manager component on XR Origin scene
11. Add XRI Default Input Actions from assets samples folder
12. Add cube into Left Hand & Right Hand to test out

## 2. Input & Hand Presence
1. Download Oculus hands
2. Import into assets
3. Add hand prefabs
4. Check in window > animation > animator, select blend tree to see the hands animation
5. On Right Hand Model, add component AnimateHandOnInput
6. Check "Use Reference"
7. Start coding, then drag animator to Hand Animator (Both)

## 3. Continuous Movement
1. Select XR Origin, add Locomotion System, Continuous Move Provider, Character Controller
2. Drag Main Camera to Continuous Move Provider forward source.
3. Add XRI Locomotion/Move to Continuous Move Provider
4. Add 1 to Y value in Character Controller to prevent falling
5. Add Continuous Turn Provider & Snap Turn Provider to turn
6. Add Character Controller Driver
7. Add Character Controller Driver and add Continuous Move Provider to Locomotion Provider

## 4. Teleportation

1. On XR Origin object, click Camera Offset and add XR > Ray Interactor (Action Based)
2. On Ray Interactor > XR Controller, click setting and choose which joystick you want to use for teleportation.
3. On XR Origin, add Teleportation Provider
4. On Plane, add Teleportation Area and add Mesh Collider to Collider settings
5. On Ray Interactor > XR Controller, change action reference to XRI ***Hand Interaction/Activate
6. Add Plane
7. Add Empty Object name Teleportation Anchor, and then add Object
8. Add material with Universal Render Pipeline/Unlit Shader
9. Choose color and transparency
10. Apply to Teleportation Anchor child object
11. Add Teleportation Anchor to Teleportation Anchor object
12. Add colliders (Teleportation Anchor child component or anything)
13. Set Match Orientation to "Target Up & Forward"
14. On Teleportation  Ray > XR Ray Interactor change Line Type to Bezier Curve and add Reference Frame
15. Add Cylinder object to Teleportation Ray, make as child and resize also rename it to Reticle and remove the 
Collider
16. Add the Reticle to Teleportation Ray > XR Interactor Line Visual > Reticle
17. Create Script named ActivateTeleportationRay and see the source
