# CCC Project Conversation History

## Project Overview
A website for "CCC" - a creative project/brand showcase featuring:
- 3D interactive "CCC" text logo using Three.js
- Vanta.js animated topology background
- Video showcase sections (CLOUDS, YEARBOOK)
- Dark aesthetic similar to igloo.inc
- Scroll animations with fade/blur effects

## Key Technical Stack
- **Three.js** - 3D graphics (TextGeometry, ExtrudeGeometry, EdgesGeometry, LineSegments)
- **Vanta.js** - Animated topology background (color: 0x89964e olive green, backgroundColor: 0x222222)
- **CSS** - Scroll animations with IntersectionObserver, 3D transforms, perspective effects
- **Fonts** - Inter (body), Owners XXWide Medium (video titles)

## File Structure
- `/Users/josephdeypalan/Desktop/trae/the-CC-project/`
  - `index.html` - Main HTML with video sections
  - `styles.css` - Dark theme, animations, hover effects
  - `script.js` - Three.js setup, Vanta background, scroll handling
  - `video1.mp4` - CLOUDS video
  - `video2.mp4` - YEARBOOK video

## GitHub
- Repo: https://github.com/drshizels/CCC-Project
- GitHub Pages: https://drshizels.github.io/CCC-Project/

## Key Implementation Details

### Three.js 3D Text
```javascript
const fontLoader = new THREE.FontLoader();
fontLoader.load('https://threejs.org/examples/fonts/helvetiker_bold.typeface.json', function(font) {
    const textGeometry = new THREE.TextGeometry('CCC', {
        font: font,
        size: 1.5,
        height: 0.4,
        curveSegments: 12,
        bevelEnabled: true,
        bevelThickness: 0.03,
        bevelSize: 0.02,
        bevelSegments: 5
    });
    textGeometry.center(); // Important: centers the pivot point
    // ... material and mesh creation
});
```

### Wireframe CCCs Floating Throughout Page
- 6 small wireframe CCCs positioned at fixed Y coordinates
- Spread across the page scroll with camera.position.y moving with scroll
- Uses EdgesGeometry + LineSegments for wireframe effect
- Three.js container is `position: fixed` to cover entire viewport

```javascript
const positions = [
    { x: 3, y: 1, z: -1 },
    { x: -3, y: -6, z: -2 },
    { x: 3.5, y: -14, z: -1.5 },
    { x: -3.5, y: -22, z: -1 },
    { x: 3, y: -30, z: -2 },
    { x: -3, y: -38, z: -1.5 }
];
```

### Camera Scroll Movement
```javascript
window.addEventListener('scroll', function() {
    const scrolled = window.pageYOffset;
    camera.position.y = -scrolled * 0.005;
});
```

### Video Hover Effect
Videos start "pushed back" and pull forward on hover:
```css
.video-player {
    transform: perspective(1000px) translateZ(-100px) scale(0.85);
}
.video-player:hover {
    transform: perspective(1000px) translateZ(0px) scale(1);
}
```

### Scroll-Triggered Animations
```css
.video-section {
    opacity: 0;
    transform: translateY(60px) scale(0.95);
    filter: blur(10px);
    transition: opacity 0.8s ease, transform 0.8s ease, filter 0.8s ease;
}
.video-section.visible {
    opacity: 1;
    transform: translateY(0) scale(1);
    filter: blur(0);
}
```

## Important User Preferences
- **Don't make changes without asking** - User got frustrated when I made unsolicited changes
- **Keep it simple** - "i hate doing too much" - User prefers minimal, not overdone
- **No more than 6-7 wireframe CCCs** - User explicitly said to keep count under 7

## Previous Attempts (Don't Repeat)
1. **Crescent moon logo** - User asked to try it, didn't like the result, reverted to normal CCC text
2. **Too many wireframe CCCs** - Started with 12, reduced to 6
3. **Z-position issues** - Positive z values put CCCs in front of camera causing clipping, use negative z

## Commits Made
1. `3D mesh CCC text + Vanta topology background`
2. `Add video sections, scroll animations, and wireframe CCCs`

## Date
December 8, 2025
