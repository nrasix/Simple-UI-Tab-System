# **SUITS** - Simple UI Tab System

If you need to quickly integrate tabs into your UI windows, then this asset is perfect for you. A lightweight and easy-to-use tab system for Unity UI.

## Features

- Simple integration with Unity's UI system
- Customizable `Tab` and content panels
- Minimal code, easy to extend
- Has some effect to Tab

## Installation

- Install via UPM - [Unity Package Manager](https://docs.unity3d.com/Manual/upm-ui-giturl.html):

  ```
  https://github.com/nrasix/SUITS.git
  ```
- Download from GitHub
    1. Copy the `Simple-UI-Tab-System` folder into your Unity project's `Assets` directory.
    2. Open your Unity project.

## Usage

### Setup Tabs in the Editor

- Create a Canvas and add a Panel for your tab buttons.
- Add Button objects as children of the panel for each tab.
- Create separate Panels for each tab's content.
- Add the `TabSystem` component to the parent panel of the tab buttons.
- Assign each tab button and its corresponding content panel in the `TabSystem` inspector.

### Scripting

You can control Tabs via script from event:

```csharp
using Nrasix.SimpleTabSystem;

public class TestTabSystem : MonoBehaviour
{
    [SerializeField] private TabSystem _tabSystem;

    private Tab _currentTab;

    private void OnEnable() => _tabSystem.OnTabSelected += OnTabSelected;
    private void OnDisable() => _tabSystem.OnTabSelected -= OnTabSelected;
    private void OnTabSelected(Tab tab) => _currentTab = tab;
}
```

## Customization

- This system include simple effect for Tab like switch color on selected and deselected Tab - `TabColorEffect`.
- You can make self effect to `Tab` from class `BaseTabEffect`.
- Style your tab buttons and content panels using Unity's UI tools.
- Extend the `TabSystem` script to add animations or custom behaviors.


## Support

For issues or feature requests, open an issue on the repository.