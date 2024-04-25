# Practical Task: Specialist Software Engineer

This document outlines the issues encountered in a Specialist Software Engineer role and provides solutions for addressing them.

## Test URL
The following problems are based on this URL: [Wrext Design - Practical SSE Test](https://wrextdesign.william-reed.com/tests/practical_sse/)

## Adjustments URL based on brief
Here's the HTML page I put together to fix/add the adjustments wanted, 
not anywhere near the finished article, but does everything wanted
and helps you see my problem solving logic, ways of working/documenting. 
Thanks! 

https://kendallgmason.github.io/SSE_Test/

## Overview of Problems
After restoring the server, several issues were reported:

1. **Device Tracking Failure**: The mobile/desktop device tracking system is not capturing data on the external tracking platform.
2. **Dynamic Content Update Failure**: The 'related news' and 'popular news' sections are not updating dynamically.
3. **Sticky Panel Behavior**: The 'related news' and 'popular news' sections should stick to the page during scrolling (desktop only), but this behavior is absent.

## Task Descriptions
To resolve these issues, complete the following tasks:

1. **Fix Device Tracking**: Investigate why `DataLayer.journey_data.is_mobile` isn't functioning and correct the issue.

2. **Update Dynamic News Sections**: Review the source code and implement JavaScript to dynamically update 'related news' and 'popular news' sections.

3. **Implement Sticky Styling**: Apply CSS to make the 'related news' and 'popular news' sections sticky as users scroll on desktop, but not on mobile devices.

## Development Guidelines
Consider these guidelines while addressing the tasks:

- The 'related news' and 'popular news' sections should load dynamically, similar to the body content.
- Sticky behavior should only apply to desktop devices, not mobile.
- Document your process in this README to showcase your documentation skills.

## Solution Delivery
Submit your solution by providing a public Git repository link.

---

## Solution Approach

### Problem 1: Device Tracking Failure
**Issue:** The external tracking platform was not picking up data from mobile/desktop devices.

**Solution:**
- **Root Cause:** The tracking data was not initialized correctly.
- **Steps Taken:**
  1. Created a new `data.json` file in the root directory with the required values to model the expected behavior.
  2. Debugged with Chrome Developer Tools, identified an error due to a missing function definition.
  3. Ensured that `dataLayer.journey_data.is_mobile` is set with an appropriate value instead of an empty string.
- **Outcome:** Device tracking now works correctly after initialization.

### Problem 2: Dynamic Content Update Failure
**Issue:** 'Related news' and 'popular news' sections were not updating dynamically.

**Solution:**
- **Root Cause:** Hardcoded HTML for the 'related news' and 'popular news' sections.
- **Steps Taken:**
  1. Analyzed the source code and observed the static structure of these sections.
  2. Created a JavaScript function to dynamically fetch data from `data.json` and update the sections.
- **Outcome:** Sections now update dynamically with correct content.

### Problem 3: Sticky Panel Behavior
**Issue:** The 'related news' and 'popular news' sections were not sticky during scrolling on desktop.

**Solution:**
- **Root Cause:** Missing CSS to achieve sticky behavior.
- **Steps Taken:**
  1. Verified the use of Bootstrap in the project.
  2. Tested how panels behaved at different screen sizes and breakpoints.
  3. Implemented `position: fixed` and additional styles to make these sections sticky during scrolling.
  4. Applied a media query (`@media breakpoint(980px)`) to ensure sticky behavior is restricted to desktop.
- **Outcome:** Sticky behavior works as expected on desktop, but not on mobile.
