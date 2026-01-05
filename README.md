
![Logo](/Picsart_26-01-05_16-06-55-977.png)

![GitHub followers](https://img.shields.io/github/followers/kaiserlone)

| Chat | Logo | Invite |
|---|---|---|
| ![Discord](https://img.shields.io/discord/1312012526829043722) | <img src="https://edent.github.io/SuperTinyIcons/images/svg/discord.svg" width="30"> | [`https://discord.gg/cNpf49Rw4m`](https://discord.gg/cNpf49Rw4m) |


Here is a professional README.md file tailored for your project.
# CSS-only-scroll-animations-No-JS-included-

A lightweight, high-performance demonstration of the modern **CSS Scroll-driven Animations API**. This project achieves complex, scroll-linked interactive effects—such as parallax, scrollytelling, and progress tracking—without writing a single line of JavaScript.

## 🚀 Features

All animations are driven entirely by the browser's compositor thread, ensuring 60fps performance even on lower-end devices.

-   **Scroll Progress Bar**: A reading indicator that automatically fills as the user scrolls down the page.
-   **Parallax Hero Section**: Background images move at a slower speed than the foreground text, creating depth.
-   **Viewport Reveal Effects**:
    -   *Fade & Slide*: Elements animate smoothly into position as they enter the viewport.
    -   *Scale*: Cards expand from 50% to 100% size based on visibility.
    -   *Side Slide*: Content flies in from off-screen left and right without causing horizontal overflow.
-   **Scroll-Linked Rotation**: Elements spin in direct relation to the scroll position.
-   **Horizontal Scrollytelling**: A "sticky" section that locks the viewport vertically while scrolling content horizontally (Pure CSS).

## 🛠️ Tech Stack

-   **HTML5**
-   **CSS3** (specifically the Scroll-driven Animations Level 1 specification)
-   **No JavaScript**

## 📂 Project Structure
| Lang | Workfunction |
|---|---|
| index.html | Semantic markup and structure |
| style.css | All styles and animation logic (animation-timeline) |
| README.md | Documentation |

⚠️ Browser Compatibility
This project uses the cutting-edge animation-timeline property.
| Browser | Support Status |
|---|---|
| Chrome / Edge | ✅ Supported (Version 115+) |
| Opera | ✅ Supported |
| Firefox | ⚠️ Behind Feature Flag (layout.css.scroll-driven-animations.enabled) |
| Safari | ⚠️ Behind Feature Flag (Develop > Experimental Features) |

Note: For production use in unsupported browsers, a polyfill would typically be required.

🏃‍♂️ How to Run
 * Download or clone this repository.
 * Ensure you have index.html and style.css in the same folder.
 * Open index.html in a modern browser (Chrome 115+ recommended for best results).
   
💡 Key Concepts Used
1. animation-timeline: scroll()
   
Used for the Progress Bar and Parallax Background. It links the animation progress to the scroll position of the nearest scrolling container (usually the page root).
```
.progress-bar {
  animation-timeline: scroll();
}
```
2. animation-timeline: view()
   
Used for Reveal Animations (fade-ins, fly-ins). It triggers animations based on when a specific element enters the viewport.
```
.card {
  animation-timeline: view();
  animation-range: entry 0% cover 40%;
}
```
3. Named Timelines (--name)
   
Used for the Horizontal Gallery. We define a timeline on a parent container and reference it inside the sticky child to translate vertical scrolling into horizontal movement.
```
.horizontal-scroll-section {
  view-timeline-name: --gallery-scroll;
}
```
```
.scroll-track {
  animation-timeline: --gallery-scroll;
}
```
📝 License
Free to use for educational purposes and personal projects.

