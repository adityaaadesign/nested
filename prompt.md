Build "Nested", a single-file infinite-zoom dictionary made only of DOM and typography. One word fills the screen, and its definition is printed inside it, forty times smaller. Zoom into any underlined word of the definition and find its definition inside it, forever, until you loop.

Look: cool paper #F6F7F9, ink #15171C, ghost #E2E6ED, slate #5B6270, cobalt #3355D1. The current word is huge ghost-grey EB Garamond, its letterforms giant shapes behind the text. The definition sits centred: small-caps headword, italic part of speech, text. Dictionary words get a thin cobalt underline. Chivo UI: italic "Nested" title, "words deep / loops found" counter, and a bottom dock: Out, pill breadcrumbs, Random.

Data: about 70 hand-written circular definitions that reuse each other.

Mechanics: the DOM holds two levels. The root has a .def at scale(0.025), and each linkable word inside it has its own .def at 0.025. A camera transform (translate + scale) zooms about the cursor on wheel or pinch, and drag pans. Seamless infinity: when a first-level word passes 30% of the viewport height while zooming in, rebuild with it as the new root and solve the camera so its box lands exactly where the span was. Zooming out rebuilds the parent the same way. Cap the zoom over empty space, dive only while zooming in, and never re-dive into the word you just left.

Interaction: click a word to glide into it; the flight carries through the re-root until the new definition is readable. Esc climbs out, Tab + Enter dives, breadcrumbs jump back, and a "?" dialog lists the controls. Announce entries to screen readers.

Signature moment: reaching a word already on your path shows "↺ all again: a loop, 3 words long. Every dictionary is a circle." and turns the crumb red. It stands alone: top right is one capsule matching the dock, holding sound (three breathing bars), an italic Garamond "?" and a sliding sun/moon night switch.

Night mode: slate-black paper #0E1014, ink #E4E8EF, ghost #1B1F27, periwinkle #7D9BFF; follows the system until chosen, then remembered.

Sound, all Web Audio and very quiet: slow distant sine swells from the same pentatonic scale (no noise), a breathing low fifth (A2 + E3), a paper rustle and soft note on each dive, one pentatonic step lower per level and wrapping round, and a rising three-note chord when a loop closes. Starts on the first gesture; M mutes.
