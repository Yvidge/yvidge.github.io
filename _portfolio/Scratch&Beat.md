---
title: Scratch n Beat
header:
image:
    thumbnail: assets/images/SnBPreview.png
project_type: Game
portfolio: true
---
Mobile music arcade similar to OSU. I was responsible for implementing and maintaining the entire UI of the game.

I joined this project as part of my internship at DreamVR. After a short time, we planned a complete redesign of the UI, which also meant huge refactoring. So **I was assigned to rewrite the UI subsystem** while implementing new UIs.

<div class = "badge-box">
    {% include badge-button.html url = "https://play.google.com/store/apps/details?id=com.dreamvrstudiollc.DJArcade" badge = "GooglePlay" %}
</div>

## UI System I designed
System design was inspired by Lyra and the Common UI Plugin.

A UI system with these key characteristics was created:  
- Supports async actions  
- Is quickly and easily extensible   
- Uses fewer hard dependencies   
- Has a convenient and explicit way of controlling which widgets are shown at each moment and how they overlay with each other. There are no more 999 different hardcoded Z-orders.

### Balance between C++ and BP  
For our needs, we decided to have all functionality in CPP and use BP only for layout and insignificant visual-related code. `BindWidget` and `BindAnimation` meta modifiers are used to control BP components in C++.

However, I think this is not the best approach in terms of iteration speed and flexibility, especially when you are working under a deadline. If I were doing it now, I would look at MVVM architecture and Epic's UMG MVVM plugin.

## The experience I got:  
- Lot's of work with UMG and Common UI   
- Teamwork, planning, and AGILE  
- Close work with a design team, rapid prototyping and iterating  
- Writing materials for UI's needs 
- Precise mockup implementation, working with Figma  
- Writing documentation  
- Code reviews, both reviewing and being reviewed  
- Working with Plastic SCM, Playfab, DevToDev, Jenkins 
- Support of existing content during development. Dump cleaning