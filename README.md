# 📱 Tag Browser + Filters (FlowRow / FlowColumn)

## Overview

This project implements a **Tag Browser screen** using Jetpack Compose with dynamic layout behavior.  

The screen allows users to:

- Browse tags that automatically wrap across the screen using `FlowRow`
- Select and deselect tags with clear visual feedback
- View selected tags in a separate section built using `FlowColumn`
- Remove selected tags interactively
- Apply or clear filters using Material 3 action buttons

The implementation focuses on responsive layout behavior, consistent spacing, and proper state management.

---

## 🧱 Layout Structure

The screen is structured as follows:

### Section 1 — FlowRow

- Displays all available tags
- Chips automatically wrap to the next line when horizontal space runs out
- Uses:
  - `horizontalArrangement = Arrangement.spacedBy(...)`
  - `verticalArrangement = Arrangement.spacedBy(...)`
- Fully responsive with `fillMaxWidth` and padding

### Section 2 — FlowColumn

- Displays selected tags
- Stacks into multiple columns when needed
- Allows tags to be removed by tapping them
- Uses `maxItemsInEachColumn` to control vertical stacking behavior

## Material 3 Components Used

The screen includes the following Material 3 components:

- TopAppBar
- FilterChip (required component)
- AssistChip (required chip type)
- Card
- Button
- FilledTonalButton
- HorizontalDivider
- Snackbar


## Interaction + Selected State Behavior

Tag selection is handled using Compose state:

- `selectedTags` is stored as a `Set<String>`
- Clicking a tag toggles its presence in the set
- UI recomposes automatically when state changes

Selected tags visually differ through:

- Leading check icon
- Border color change
- Background tint
- Elevation shadow

This ensures a clear visual indication of selected state.

## Modifier Techniques Demonstrated

The implementation intentionally demonstrates:

- `Arrangement.spacedBy(...)` for consistent spacing
- `fillMaxWidth` for responsive layout
- `padding` for visual structure
- `shadow` for selected elevation state
- `border` and `background` for visual state change
- `verticalScroll` to ensure full-page scroll behavior

These techniques ensure layout clarity and responsiveness across screen sizes.

## Screenshots

## How to Run

1. Open the project in Android Studio  
2. Use an emulator with API 33–34 recommended  
3. Run `MainActivity`  

---

## AI Disclosure

ChatGPT was used as a supplementary tool during development for clarification of FlowRow / FlowColumn behavior, layout structuring guidance, and documentation drafting.

The overall layout structure, state management logic, chip interaction behavior, and visual styling decisions were independently implemented and tested in Android Studio. The selected-state behavior, scroll handling, and responsive layout adjustments were manually designed and refined.

AI assistance was used as a learning and refinement resource rather than as a substitute for independent development.
