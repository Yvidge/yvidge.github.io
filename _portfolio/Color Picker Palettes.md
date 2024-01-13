---
layout: single
title: Color Picker Palettes
image:
  thumbnail: assets/images/ColorPickerPalettesPreview2.png
project_type: Plugin
portfolio: true
year: 2023
priority: "-1"
---

Simple UE plugin that makes the work under the color guide easier.

![ColorPicker](/assets/images/ColorPickerPalettes01.png){: .align-center}

I wrote this plugin because I was really annoyed with copy-pasting colors from Figma while working. The plugin extends the color picker, so you can easily access predefined colors straight from the editor.

![ColorPicker](/assets/images/ColorPickerPalettes02.png){: .align-center}

Also, it was created with team work and source control in mind, so configs separated to have important data shared between all team members while staying highly configurable for everyone in regards to the features they want to use.

<div class = "badge-box">
  {% include badge-button.html url = "https://github.com/Yvidge/UEColorPickerPalette" badge = "GitHub" %}
  {% include badge-button.html url = "https://www.unrealengine.com/marketplace/en-US/product/color-picker-palettes" badge = "Unreal"%}
</div>

## Features
- Color palettes. You can define named sets of colors in the project settings.
- Extended color picker. You can access all palettes while editing any color in any editor.
- Unregistered color warnings. You will see warning icons if a color is not listed in any palette. This makes it easy to spot minor disagreements with the color guide.
- BP access to palettes if you want to change color from code.
- `FStrictLinearColor` type that will only show registered colors while editing.

## Implementation details
The core of the plugin consists of a few `FPropertyTypeCustomization` inherited from `FColorStructCustomization`. Our property customizations are registered in the editor module on the `PostEngineInit` loading phase, overriding default ones.
```cpp
FName PropertyEditor("PropertyEditor");  
FPropertyEditorModule& PropertyModule = FModuleManager::GetModuleChecked<FPropertyEditorModule>(PropertyEditor);  
PropertyModule.RegisterCustomPropertyTypeLayout(NAME_LinearColor, FOnGetPropertyTypeCustomizationInstance::CreateStatic(&FColorStructPaletteCustomization::MakeInstance));
PropertyModule.NotifyCustomizationModuleChanged();
```
`FColorStructPaletteCustomization` extends common color customization, adding a warning icon and overriding color picker creation. Instead of a common color picker, we create a window widget consisting of a color picker and the color palettes' extension (if it's enabled in user settings).
## The experience I got:  
- Setting up a marketplace account and preparing content for marketplace
- Working with Slate
- Working with Property Customizations. They are handy!
- Writing documentation and promotion materials
- Trying to provide good UX to users