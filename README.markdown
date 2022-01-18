# AC: 500 Server Error Page

[https://tovuti.atlassian.net/browse/DSN-1083](https://tovuti.atlassian.net/browse/DSN-1083)

```jsx
<iframe style="border: 1px solid rgba(0, 0, 0, 0.1);" width="800" height="450" src="https://www.figma.com/embed?embed_host=share&url=https%3A%2F%2Fwww.figma.com%2Fproto%2FhXhgz1YnpQBpWYmWBbarLq%2F500-Server-Error%3Fpage-id%3D2%253A38763%26node-id%3D2%253A39163%26viewport%3D438%252C48%252C0.29%26scaling%3Dscale-down%26starting-point-node-id%3D2%253A39163%26show-proto-sidebar%3D1" allowfullscreen></iframe>
```

```jsx
<iframe style="border: 1px solid rgba(0, 0, 0, 0.1);" width="800" height="450" src="https://www.figma.com/embed?embed_host=share&url=https%3A%2F%2Fwww.figma.com%2Fproto%2FhXhgz1YnpQBpWYmWBbarLq%2F500-Server-Error%3Fpage-id%3D2%253A34335%26node-id%3D2%253A37248%26viewport%3D438%252C48%252C0.73%26scaling%3Dscale-down%26starting-point-node-id%3D2%253A37248%26show-proto-sidebar%3D1" allowfullscreen></iframe>
```

![LightMode-16_9-Desktopaccess.jpg](AC%20500%20Server%20Error%20Page%20efe0cedf3a6f4e0399a393ad3c0ab0f1/LightMode-16_9-Desktopaccess.jpg)

![DarkMode-16_9-Desktopaccess.jpg](AC%20500%20Server%20Error%20Page%20efe0cedf3a6f4e0399a393ad3c0ab0f1/DarkMode-16_9-Desktopaccess.jpg)

![LightMode-16_9-Desktop-grid.png](AC%20500%20Server%20Error%20Page%20efe0cedf3a6f4e0399a393ad3c0ab0f1/LightMode-16_9-Desktop-grid.png)

# Acceptance Criteria

- No Bootstrap dependency needed on this project. 2 color single page design no need to weight it down.

## Grid

- Bootstrap Grid or MOYO Design System Grid
- {if} Bootstrap evaluate spacing is base-8 (it should be with the new theme if not I’d call this a bug)
- Requirement: Follow spacing guidelines closely.
- Vertical spacing adheres to base 8. Helpers on that could be reviewing redline document, or reviewing the final Figma file.

## Theming

- Requirement: Light and Dark theme. on/off interaction trigger via switcher provided [here](https://github.com/tovutifunk/tov-500internalServerError)
- Note: Bryan will have a light shade of gray that will replace white when the Dark theme is applied. White text on flooded black is strenuous on the eyes. This shouldn’t hold up this project.

## Tooltips

- Custom Tooltips — Popper & Tippy like we did in 2.0.

## FontAwesome Icons

- No FontAwesome dependency needed on this project. 2-3 Icons, I’ll compile SVG’s, they should play perfect with theming and we’ll save more time on load.

## Graphics

- All Designs are vector based and should be exported and used as SVG’s. In this case I will supply all the assets. If any happen to sneak though there’s been an oversight and new assets will be supplied.

## Graphics cont. SVG’s & ALT tags

- Every SVG needs an ALT attribute ALTHOUGH if an SVG is purely decorative it does validate through accessibility standards when left empty. Without an ALT tag it would fail.
- Nav Menu: Help Center: Icon:`<svg alt=”Learn more about your LMS with Tovuti's new Help Center” role=”img”>args...</svg>`
    - Nav Menu: Support: Icon: `<svg alt=”Escalate an issue to your Tovuti Support team here.” role=”img”>args...</svg>`

## Day/Night Switch

- The code repo for the switch element can be [found here](https://github.com/tovutifunk/tov-500internalServerError).
- switch element is `not 100% complete`. No JS for toggling theme mode when UI element action occurs.

## Responsiveness

- Designs are provided in 3 breakpoints. 1 more may be needed for md
- MOYO-DS Grid for reference:
    
    ![moyo-ds-disabled.svg](AC%20500%20Server%20Error%20Page%20efe0cedf3a6f4e0399a393ad3c0ab0f1/moyo-ds-disabled.svg)
    
    ```jsx
    - xlg — default break up to 1584px, supports 16 columns by default
    - lg — default break up to 1312px, supports 16 columns by default
    - md — default up to 1056px, supports 8 columns by default
    - sm — default breakpoint up to 672px, supports 4 columns by default
    - max — working through this but essentially this will be an open ended user defined at time of need for a custom value
    ```
    
    ```jsx
    Compared to Bootstrap...
    $grid-breakpoints: (
      xs: 0,
      sm: 576px,
      md: 768px,
      lg: 992px,
      xl: 1200px,
      xxl: 1400px
    );
    ```
    

## Accessibility

- Vision Simulation completed 1/18/2022
    
    
    | ☑️ Protanopia | ☑️ Achromatopsia | ☑️ Deuteranopia | ☑️ Protanomaly | ☑️ Tritanopia |
    | --- | --- | --- | --- | --- |
    | ☑️ Tritanomaly | ☑️ Deuteranomaly | ☑️ Achromatomaly | ☑️ Blurred |  |
- Color Contrast
    - Same grade both ways ;) obviously no surprise here.
    
    ![Untitled](AC%20500%20Server%20Error%20Page%20efe0cedf3a6f4e0399a393ad3c0ab0f1/Untitled.png)
    
- Focus Order Page Sequence
    - Single mockup. The pages here are all similiar enough and one does fit all in this case.
    - If anyone has questions I’m happy to help! Or if you prefer to explore yourself this would be: tabindex and also confirming the DOM is loading up in the focus order as well.

## Nav Links

- Target _blank on both
