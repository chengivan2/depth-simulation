# Savings Goal Tracker UI

A modern, visually polished savings goal display component featuring a 3D depth effect. This component showcases a piggy bank icon with a savings amount displayed within an elegant circular white ring on a deep purple gradient background.

## Overview

This UI component is designed to display financial savings goals or achievements. It features:
- A vibrant purple gradient background
- A prominent white circular ring with sophisticated 3D depth effects
- A centered piggy bank icon with the savings amount

## Visual Design

The component uses **layered shadow techniques** to create a realistic 3D plastic ring appearance:

1. **Outer Drop Shadow** - Creates a "lift" effect, making the ring appear to float above the background
2. **Inner Bevel** - Adds subtle light and shadow to give the white ring a rounded, plastic-like quality
3. **Inner Sunken Effect** - Makes the purple center appear recessed, enhancing the 3D depth illusion

## Project Structure

```
.
├── index.html     # HTML structure
├── main.css       # Styling with shadow effects and layout
└── README.md      # This file
```

## Features

### Styling Highlights
- **Gradient Background**: Linear gradient from `#300099` to `#1a0055` (purple tones)
- **Circular Ring**: 240px diameter with 24px white border
- **Icon System**: Font Awesome icons (currently using the piggy bank icon)
- **Responsive Shadow Layers**: Multiple box-shadow properties for depth

### Key CSS Techniques
- **`box-shadow`** with multiple values for layered depth
- **`::before` pseudo-element** for additional inner shadow effects
- **Flexbox** for perfect centering of content
- **CSS Variables** for maintainable color management

## How It Works

The design creates the illusion of a 3D object through strategic use of shadows:

```css
box-shadow: 
  /* Drop shadow - creates the "lift" */
  0px 20px 40px rgba(0, 0, 0, 0.4),
  /* Outer edge bevel - light reflection on plastic */
  inset 0px 4px 6px rgba(255, 255, 255, 0.5),
  /* Inner edge shadow - sunken effect on center */
  inset 0px -4px 10px rgba(0, 0, 0, 0.2);
```

## Display

Opens in the browser as a full-screen component (100vh) with the ring centered. The design is clean, modern, and optimized for displaying financial information.

## Icons

Uses [Font Awesome 6](https://fontawesome.com/) for the piggy bank icon. The icon is scalable and animatable for future enhancements.

## Customization

To modify the design:
- **Colors**: Update `--bg-gradient` CSS variable in the `:root` selector
- **Ring Size**: Adjust the `width` and `height` of `.depth-ring`
- **Amount**: Change the `$300` value in the HTML
- **Icon**: Replace `fa-piggy-bank` with any other Font Awesome icon
- **Font Size**: Modify the `font-size` in `.amount` or `.icon-circle` classes

## Future Enhancements

Potential additions:
- Animation on load (ring expand, icon fade-in)
- Progress bar functionality (fill the ring as you save)
- Dark/Light mode toggle
- Responsive sizing for mobile devices
- Animated counter for the amount value
