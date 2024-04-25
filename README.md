# Practical Task: Specialist Software Engineer

The following practical task outlines the common issues encountered in the Specialist Software Engineer role and proposes solutions for addressing them.

## Test URL
The errors mentioned below are based on the following URL:
[Wrext Design - Practical SSE Test](https://wrextdesign.william-reed.com/tests/practical_sse/)

### Overview
After a restoration effort on the server, several issues have been reported:

- The mobile/desktop device tracking has stopped picking up data on the external tracking platform.
- The 'related news' and 'popular news' panel isn't updating dynamically.
- The 'related news' and 'popular news' panel should be "sticky" and follow the user as they scroll down the page (desktop only).

### Tasks
To resolve these issues, you need to complete the following tasks:

1. **Fix Mobile/Device Tracking**: Understand why `DataLayer.journey_data.is_mobile` isn't functioning and fix it as needed.
2. **Update the 'Related News' and 'Popular News' Blocks**: Review the source code and write JavaScript that updates these blocks with the correct content dynamically.
3. **Apply "Sticky" Styling**: Add CSS to make the 'related news' and 'popular news' blocks stick to the right side of the page as users scroll, only on desktop.

### Pointers
Here are a few pointers to help you with the tasks:

- The 'related news' and 'popular news' blocks should load similarly to how the body content loads.
- The blocks should only be "sticky" on desktop, not on mobile devices.
- Document your work in the repository's README file to demonstrate your documentation skills.

### Delivery
Provide your solution as a public Git repository link.

--------------------------------------------

### How I Approached These Tasks

- Problem 1: The **mobile/desktop device tracking** has stopped working on the external tracking platform. ✅

Pre-problem bug fix: 
 -There was no data.json to fetch from, so I created one and added the values that it was looking for into an external json in the root of this repo. Then fetched from there what was needed to model what it wanted. 

- Steps I took to debug Problem 1: 

 a. I brought the test link up that was provided. 
 b. Used Developer Tools in Chrome to see if anything was erroring in the console. 
 c. Straight away I noticed it was not referenced right aka the function wasn't 
 defined before it was called, so it was causing it to error. 
 d. I also set the dataLayer.journey_data.is_mobile with a value as opposed to a 
 blank string. 
 e. This no longer errors and would now work depending on what it was used for specifically. 

- Problem 2: The **related news** and **popular news** panels are not updating dynamically. ✅

 a. I could see that both related news and popular news were already set in 
 the html and hardcoded by looking at the source code. 
 b. I used as reference the way the body content loaded and did a similar method in javascript to implement being able to dynamically call in popular news and related news from the data.json file. 

- Problem 3: These panels should be **"sticky"** and follow the user down the page on desktop devices. ✅

a. Looked at the related panels 


