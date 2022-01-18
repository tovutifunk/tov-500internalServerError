# AC: 500 Server Error Page

[https://tovuti.atlassian.net/browse/DSN-1083](https://tovuti.atlassian.net/browse/DSN-1083)

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
  | ☑️ Protanopia  | ☑️ Achromatopsia | ☑️ Deuteranopia  | ☑️ Protanomaly | ☑️ Tritanopia |
  | -------------- | ---------------- | ---------------- | -------------- | ------------- |
  | ☑️ Tritanomaly | ☑️ Deuteranomaly | ☑️ Achromatomaly | ☑️ Blurred     |               |
- Color Contrast
  - Same grade both ways ;) obviously no surprise here.
- Focus Order Page Sequence
  - Single mockup. The pages here are all similiar enough and one does fit all in this case.
  - If anyone has questions I’m happy to help! Or if you prefer to explore yourself this would be: tabindex and also confirming the DOM is loading up in the focus order as well.

## Nav Links

- Target \_blank on both
