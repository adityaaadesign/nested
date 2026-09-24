Build "Nested", a single-file infinite-zoom dictionary made only of DOM and typography. One word fills the screen, and its definition is printed inside it, forty times smaller. Zoom into any underlined word of the definition and find its definition inside it, forever, until you loop.

Look: paper #FBFAF7, ink #141414, ghost #E7E3D8, grey #6A655A, vermilion #D6452B. The current word is huge ghost-grey EB Garamond, its letterforms giant shapes behind the text. The definition sits centred: small-caps headword, italic part of speech, text. Dictionary words get a thin vermilion underline. Chivo UI: italic "Nested" title, "words deep / loops found" counter, and a bottom dock: Out, pill breadcrumbs, Random.

Data: about 70 hand-written circular definitions that reuse each other.

Mechanics: the DOM holds two levels. The root has a .def at scale(0.025), and each linkable word inside it has its own .def at 0.025. A camera transform (translate + scale) zooms about the cursor on wheel or pinch, and drag pans. Seamless infinity: when a first-level word passes 30% of the viewport height while zooming in, rebuild with it as the new root and solve the camera so its box lands exactly where the span was. Zooming out rebuilds the parent the same way. Cap the zoom over empty space, dive only while zooming in, and never re-dive into the word you just left.

Interaction: click a word to glide into it; the flight carries through the re-root until the new definition is readable. Esc climbs out, Tab + Enter dives, breadcrumbs jump back, and a "?" dialog lists the controls. Announce entries to screen readers.

Signature moment: reaching a word already on your path shows "↺ all again: a loop, 3 words long. Every dictionary is a circle." and turns the crumb red. It stands alone: top right holds only a sound toggle, "?" and, in the corner, a night-mode toggle.

Night mode: warm near-black paper #131211, ink #ECE6DA, ghost #24221E, coral #E0674D; follows the system until chosen, then remembered.

Sound, all Web Audio and very quiet: brown-noise room tone, a breathing low fifth (A2 + E3), a paper rustle and soft note on each dive, one pentatonic step lower per level and wrapping round, and a rising three-note chord when a loop closes. Starts on the first gesture; M mutes.
