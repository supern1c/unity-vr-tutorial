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

## 5. Hover, Grab and Use Interactable

1. Download Unity Pistol Package
2. Import asset
3. On Left Hand & Right Hand, add Sphere Collider and set Radius & check Is Trigger
4. Add cube as table
5. Add cube as Interactable
6. Add Rigid Body to cube
7. Add XR Simple Interactable to cube
8. Add action on hover, hover exited, and on select to XR Simple Interactable
9. For grabbing mechanism, add Grab Interactable to object. Set movement type to Velocity Tracking.
10. Add Pistol object, add Box Collider, Rigid Body, and XR Grab Interactable.
11. Create empty object named Attach Point inside pistol object
12. Add the Attach Point object to Attach Transform in pistol
13. Create empty object and put in front of pistol a little bit (to spawn the bullet)
14. Create bullet material (you can build from sphere), disable Use Gravity and set Collision Detection to 
Continuous Dynamic
15. Create Script that trigger bullet in pistol object
16. Add bullet and the object in front of pistol to the script
17. Add script to disable teleportation when grabbing object in XR Origin > Activate Teleportation Ray
18. Add Layer named Player & Interactable
19. Add XR Origin  to Player
20. Add all interactable to Interactable
21. Disable physics in project settings for Player > Interactable
