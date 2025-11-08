# Tampermonkey

Adds pull down list for Gemini personalities. See orig Reddit post at:
https://www.reddit.com/r/GeminiAI/comments/1o3qnie/heres_how_to_create_a_free_personality_switcher/
------------------

Used Gemini to create a Tampermonkey script. It shows a little pulldown which you can select items from which are then pasted into the Gemini prompt window. At the moment it does not send the request, you have to click enter. But, this is what I want for now to allow me to edit or add anything.
The script shows all your personality options plus I added yes and no prompts. And, for those on Ipad or Iphones, you can install the Tampermonkey app and paste the script into it and it works in Safari.  For Windows and Mac, you just add the Tampermonkey extension to Chrome or Brave or Edge and add the script via the Tampermonkey dashboard.
I have never created a Tampermonkey script before. I used the prompt shown below. The prompt initially only adds a few starter pulldown items, but the full script below has all your personalities - which I added later. It's easily modified.
I know the script can be improved but thought I'd share to show you what you can do in support of your script and to open the door to folks doing similar. 
***** prompt to create the script: <<< this is for reference as to how to create a script. The actual full working script is below this prompt. Also, I didn't add all that fancy stuff like "use strict" in my original request. I started out saying to build a script for the Gemini site that shows a pulldown list. Then I added things and had Gemini keep fixing things until it worked. I was up to 12 versions and about an hour of effort. Then, I asked it to show me the final prompt I could have used in the first place and that is what you see below.

"Create a Tampermonkey script for Google Chrome that runs on gemini.google.com.
The script must do the following:
1. Add a pulldown menu (<select>).
2. Position the pulldown in the top-right corner of the window using position: fixed, top: 10px, right: 10px, and a high z-index.
3. Style the pulldown to be theme-aware so it works in both light and dark mode, using system colors like Canvas and CanvasText.
4. Wait for the UI to load by using a setInterval to check for a stable element (like div[role="textbox"]) before injecting the menu.
5. When an item is selected, the script must inject the item's text into the main Gemini chat input (div[role="textbox"]).
6. The script should not use 'use strict'; to prevent silent failures.
7. Use this list of items for the pulldown:
    * "Select a prompt..." (value: "")
    * "Yes" (value: "Yes")
    * "No" (value: "No")
    * "Personality Factory" (value: "Personality Factory")
    * "Personality charming" (value:F "Personality charming")"
