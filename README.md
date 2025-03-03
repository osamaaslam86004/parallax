# Ukiyo.js Parallax Effects

## Overview

This project demonstrates various parallax scrolling effects using [Ukiyo.js](https://github.com/yitengjun/ukiyojs), a lightweight JavaScript library for image-based parallax effects. The repository includes multiple implementations, each showcasing different scrolling animations and effects.

## Features

- **Single Image Parallax**: Smooth parallax effect on full-screen background images.
- **Multiple Image Parallax**: Dynamically loads images from Unsplash and applies Ukiyo.js parallax.
- **Overlapping Fixed Text Parallax**: A unique parallax effect where the text remains fixed while the background moves.
- **Smooth Scrolling**: Utilizes [Lenis.js](https://github.com/studio-freight/lenis) for buttery-smooth scrolling.
- **Animated Sections**: Implements [AOS (Animate On Scroll)](https://michalsnik.github.io/aos/) for scroll-based animations.
- **Responsive Design**: Fully responsive and works across different devices.
- **Start-Stop Scrolling**: A real-world implementation where scrolling pauses during specific interactions like modal popups and video playback.
- **Sticky Header**: Implements a header that changes appearance when scrolling.



## Start-Stop Scrolling (start-stop.html)

This implementation showcases how Lenis.js can be used to dynamically stop and resume scrolling based on user interactions. It includes:

- A **Breaking News Modal** that stops scrolling when opened and resumes when closed.
- A **Video Section** that halts scrolling while a video is playing and resumes when paused or ended.
- A **Newsletter Sign-Up Form** that stops scrolling when a user interacts with an input field.

### How It Works

1. **Lenis.js Initialization**

   - Smooth scrolling is enabled using Lenis.js with custom easing and duration settings.

2. **Pausing Scroll on Modal Open**

   - A modal popup appears for breaking news.
   - When the modal is shown, `lenis.stop()` is called to prevent scrolling.
   - When the modal is closed, `lenis.start()` resumes scrolling.

3. **Pausing Scroll on Video Play**

   - When the user plays the video, `lenis.stop()` prevents scrolling.
   - When paused or ended, `lenis.start()` allows scrolling again.

4. **Pausing Scroll on Input Focus**

   - When an input field is focused, scrolling is paused.
   - When the input loses focus, scrolling resumes.

This technique ensures a better user experience by managing scrolling behavior dynamically based on user interaction.


## Sticky Header (sticky-header.html)

This feature demonstrates a sticky header that changes appearance as the user scrolls.

### How It Works

1. **Lenis.js Initialization**
   - Smooth scrolling is initialized using Lenis.js with a custom duration and easing.

2. **Dynamic Header Styling**
   - The script listens for scroll events and changes the header's background and text color when the user scrolls beyond a threshold.

3. **Section Background Effects**
   - Sections change their background color when hovered over, enhancing the visual experience.

This implementation provides a sleek and interactive navigation experience, improving usability.


## Installation & Usage
1. Clone the repository:
   ```bash
   git clone https://github.com/osamaaslam86004/parallax.git
   ```
2. Navigate to the project directory:
   ```bash
   cd parallax
   ```
3. Open any `.html` file in a browser to see the effects in action.

## File Structure
```
📂 project-root
├── 📂 assets          # Contains images used in the parallax effects
├── 📜 index.html    # Main file implements only Image Parallax
├── 📜 image-parallax.html    # Basic Ukiyo.js parallax effect
├── 📜 parallax-multiple-images.html  # Multiple images with dynamic parallax
├── 📜 overlapping-parallax.html  # Parallax effect with fixed text
├── 📜 ukiyo-with-lenis.html      # Implements Parallax with Smooth Scrolling
├── 📜 ukiyo+aos+lenis.html      # HTML file with full implementation
├── 📜 start-stop.html  # Implements pause/resume scrolling with Lenis.js
├── 📜 sticky-header.html  # Implements a sticky header with Lenis.js
├── 📜 zoom-and-horizontal-parllax.html # Implement zoom effect with Parallax and Horizontal Parallax
├── 📂 css             # Additional stylesheets
└── 📜 README.md       # Project documentation
```

## Technologies Used
- **HTML5 & CSS3**
- **JavaScript (ES6+)**
- **Ukiyo.js** - Parallax scrolling library
- **Lenis.js** - Smooth scrolling
- **AOS.js** - Animate on scroll

## Dependencies (CDN-based)
The project uses CDN links for simplicity. These can be replaced with local files if needed:
```html
<script src="https://cdn.jsdelivr.net/npm/ukiyojs@4.1.2/dist/ukiyo.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/@studio-freight/lenis@1.0.8/bundled/lenis.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4/aos.js"></script>
```

## Customization
- Modify `scale` and `speed` values in Ukiyo.js initialization for different effects.
- Update Unsplash API key for dynamically loaded images in `parallax-multiple-images.html`.

## License
This project is open-source and available under the MIT License.

## Author
[Osama Aslam](https://github.com/osamaaslam86004)

---
Enjoy building immersive web experiences! 🚀
