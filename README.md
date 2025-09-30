
# Boxing-Style Slot Template (Unity-friendly)

**What this ZIP contains**
- `Assets/Scripts/SlotManager.cs` — Core slot logic (5x3 grid).
- `Assets/Scripts/ReelCell.cs` — Optional helper for UI images.
- `Assets/Scripts/UIController.cs` — Basic UI button hooks.
- `Assets/Art/` — placeholder PNG sprites for symbols.
- `README.md` — this file.

**Important note**
This ZIP is *not* a full Unity project (Unity projects need ProjectSettings and Library metadata).  
Instead, it's a ready **Assets** folder you can import into a **new Unity project**.

---

## How to use (step-by-step)

1. Install **Unity Hub** and **Unity 2020 LTS / 2021 LTS / 2022 LTS** (any recent version).
2. Create a **New 2D** Unity Project.
3. Close Unity. Extract this ZIP and copy the `Assets` folder into your Unity project folder (overwrite or merge).
4. Open Unity Hub and open the project.
5. Open `Assets -> Scenes` (if you don't have a scene, create a new Scene: `File -> New Scene` and save it as `Main.unity` inside `Assets/Scenes`).
6. In the Scene:
   - Create an empty GameObject named `SlotManager` and attach the `SlotManager` script.
   - Create a Canvas with UI Images arranged in a grid (3 rows x 5 columns). Make sure each cell has an `Image` component. Create them as children of an empty `ReelParent` GameObject for easy assignment.
   - Assign the `reelParent` field on the SlotManager to the `ReelParent` Transform.
   - Assign the placeholder sprites from `Assets/Art` into `SlotManager.symbolSprites` (set Size to number of sprites).
   - Create UI Text objects for `BalanceText` and `WinText` and assign them.
   - Create Buttons and connect their OnClick to `UIController.OnSpinButton` and `UIController.OnAutoSpinButton`.
7. Press Play and test spinning.

---

## Customization tips
- Replace placeholder art in `Assets/Art` with your own placeholder PNGs (same filenames OK).
- Modify `CheckWin()` in `SlotManager.cs` to implement paylines, scatter, wild, free spins, and bonus rounds.
- Add audio by creating an `AudioSource` and playing SFX on spin/win.

---

## License / Use
This template is provided as-is to help you start building a slot game. For publishing on stores, follow Google Play / Apple App Store rules and gambling regulations in your country.

Enjoy — if you want, I can also:
- create a GitHub repo,
- add more advanced features (paylines, free spins),
- make a ready-to-import Unity Package (.unitypackage).
