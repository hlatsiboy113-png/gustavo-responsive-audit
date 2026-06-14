Responsiveness Audit Report

Overview

This audit evaluated the responsiveness of the web page across multiple screen sizes using Chrome DevTools. The page was tested at 375px (mobile), 768px (tablet), and 1280px (desktop) resolutions. Several responsiveness and layout issues were identified and corrected to improve usability and visual consistency across devices.




Screen Size: 375px (Mobile)

Issue 1: Horizontal Content Overflow

Errors Identified
Content overflowed horizontally, creating white-space on the right side of the screen. The navigation bar and page content extended beyond the visible viewport when loaded on a mobile device.

Cause
Fixed-width elements and non-responsive layout sizing caused the content to exceed the mobile viewport width.

![375px before fix](../../assets/screenshots-before/375px-before..png)

Fix Applied
Responsive styling was implemented using flexible widths and overflow prevention techniques.

CSS Fix

CSS


body {
  overflow-x: hidden;
}

.card-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
}



Result
The navigation bar and content now fit correctly within the mobile viewport without horizontal scrolling.

![375px after fix](../../assets/screenshots-after/375px-after.png)













Issue 2: Images Not Displaying

Errors Identified
Images did not appear inside their allocated containers on mobile devices.

Cause
Image files were not located inside the required assets/images or images directory referenced in the HTML file paths.

![375px before fix](../../assets/screenshots-before/375px-before..png)

Fix Applied
The missing images were added to the correct folder structure, and responsive image styling was implemented.

CSS Fix

CSS


img {
  max-width: 100%;
  height: auto;
  display: block;
}



Result
Images now load and display correctly within their containers on mobile devices.

![375px after fix](../../assets/screenshots-after/375px-after.png)













Screen Size: 768px (Tablet)

Issue 3: Navigation Bar Layout Issues

Errors Identified
The navigation bar did not extend correctly across the screen width and elements became misaligned on tablet-sized screens.

Cause
The navigation layout lacked responsive flexbox adjustments for medium screen sizes.

![768px before fix](../../assets/screenshots-before/768px-before..png)

Fix Applied
Responsive flexbox properties were added to improve layout alignment and wrapping behavior.

CSS Fix

CSS


@media (max-width: 768px) {
  .nav {
    flex-wrap: wrap;
    justify-content: center;
  }

  header {
    flex-direction: column;
    align-items: center;
  }
}



Result
The navigation bar now aligns correctly and adapts properly to tablet screen sizes.

![768px after fix](screenshots-after/768px-after.png)


Screen Size: 1280px (Desktop)

Issue 4: White-Space on Right Side of Screen

Errors Identified
White-space appeared on the right side of the screen when viewed on laptop or desktop devices. Certain layout elements extended beyond the visible desktop viewport.

Cause
Large fixed-width containers and images caused layout overflow on wider screens.

![1280px before fix](screenshots-before/1280px-before.png)

Fix Applied
Responsive width constraints and scalable image sizing were implemented.

CSS Fix

CSS


.hero img {
  width: 100%;
  height: auto;
  object-fit: cover;
}

.contact-inner {
  max-width: 800px;
  width: 100%;
  margin: 0 auto;
}



Result
The navigation bar and page content now fit correctly within the desktop viewport without creating horizontal white-space.

![1280px after fix](screenshots-after/1280px-after.png)

![375px Responsive Fix](screenshots-after\375px-after.png)



Issue 5: Images Not Displaying on Desktop

Errors Identified
Images did not appear in their allocated containers on laptop and desktop devices.

Cause
Incorrect image file paths prevented the browser from locating image assets.

![1280px before fix](screenshots-before/1280px-before.png)

Fix Applied
Image assets were placed in the correct directory and responsive image handling was implemented.

Result
Images now appear correctly on laptop and desktop devices and scale appropriately across screen sizes.

![1280px after fix](screenshots-after/1280px-after.png)




Conclusion

The responsiveness audit identified multiple layout and asset-loading issues across mobile, tablet, and desktop resolutions. After implementing responsive CSS techniques, correcting image paths, and replacing fixed-width layouts with flexible structures, the web page now adapts effectively across all tested screen sizes.

