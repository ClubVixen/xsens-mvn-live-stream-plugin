# Updates

## 2026-10-31: MVN 2023.2 support + reprocess fix

- **Fixed:** "Reprocess failed: Missing property: ScenarioLabel" on recordings made with **MVN 2022 / 2023.0**. These are now processed as single-level, which is MVN's default.
- **New:** **MVN 2023.2** downloads (base and Euler). They use the 2024 build, since 2023.2 ships the same Ogre engine.
  - Add `Plugin=BipedStreamerPlugin` to `ogre_plugins.cfg`. The 2023.2 file doesn't include it by default.
  - Don't copy `RenderSystem_Direct3D11.dll`. That's only for 2025+. Leave the original one in there
- All downloads include the updated reprocess solver.

## 2026-10-24: Reprocess MVN File

- **New:** **REPROCESS MVN FILE…** button. It re-solves a recorded `.mvn` offline and saves a new, cleaned-up `.mvn`.
  - Progress bar, status text, and a Cancel button.
  - Saves to a new file (default `<name>_reprocessed.mvn`). The original is never overwritten.
  - Native solver in the `MvnReprocess` folder next to the plugin. No Python or Xsens SDK needed.
- Builds for **MVN 2024** and **MVN 2025+**, each in **base** and **Euler** variants.

## Beta v4.0

- BVH export directly from the app.
- Streaming to Unity, Blender, Maya, and iClone (Euler as an add-on).
