# Multi-Link Cards
These cards have multiple sections to allow for heirarchy of the Links.
Iconography uses the Material Symbols library to have access to a braod set of icons

# Top of Card
## Main Image Link
The main image on the top of the card is a link. This should be the primary link users will follow when visiting the card, or a link to broad information.

## Linkbar Links
There are two type of Linkbar Links: Direct and Modal. These links are at the top right, and fill from right to left. They are an icon only (and Title text for mouse navigation hover)
- Direct Links are ones were the Icon alone is sufficient to provide users with where the link is going. This is best used when it is a consistent icon between mutliple cards (such as to a help link, an email, etc)
- Modal Overlay Links create a modal overlay on the card with more content. Great for grouping common items (such as multiple emails, multiple phone numbers).

Modal Overlay Links require the id of the `<a>` tag to be a Material Symbol Icon name. This is tied to the Modal that will open via the included JavaScript. See inline comments for more details.

# Bottom of Card
## Content
Text content can be placed here. Use `<h2>` tags are styled to section content

## Multi-links
Flexbox container that will scale from 1 wide to 2 wide depending on device display.
Links here are button with Labels and optional sub-labels. The come in three sizes: large (default), medium, and small. Small buttons cannot have sub-labels.
Buttons can be themed a light or dark theme. Dark is the primary theme for the bottom of the card. Use the light theme versions for Modals

# Info Corner
Cards have an informational corner icon in the bottom right that opens a modal overlay. Use this for help text, additional information, or links to documentation.

Info Corners use included JavaScript to manage their overlays.

Use in SDK
These are not designed for SDK use and would require overhaul to use there. This is because of how the SDK has access to the entire DOM, whereas HTML cards are Sandboxed. To convert to SDK you will need to modify the Modal Overlay and Info Corner JavaScripts to work with React and pass unique identifiers to them to prevent cards from "talking" to each other.
