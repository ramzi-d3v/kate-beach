Hassan Kitesurfing & Excursions — Website Package
================================================

FILES
  index.html          The whole website. Open it in any browser.
  images/             Your 7 kite photos + logo
  fonts/              Chalisa Octavia (unused now, kept in case you
                       want the cursive wordmark back — see note below)
  README.txt          This file

TO PUT IT ONLINE
  Upload index.html, images/ and fonts/ together, keeping the folder
  structure exactly as it is. Nothing else is needed — no database,
  no build step, no plugins.


WHAT'S ON THE PAGE
------------------
  Header               Just your logo (no text label — the logo
                       already has your name in it). WhatsApp CTA
                       in the top bar and "Book a trip" in the header
                       shrink to fit one row on phones.
  Hero                 Aerial reef photo background, a thin bordered
                       line with "Kite Beach, Paje" + "Since 2015",
                       then "Book your trip", a green pinging
                       WhatsApp button, and a tours link
  Mobile menu          A slide-in panel with a backdrop, chevron
                       icons, staggered entrance animation, a close
                       button, and a green WhatsApp button pinned to
                       the bottom. The hamburger icon morphs into an
                       X when open.
  About us             Two short paragraphs on the business, plus
                       stats and photos
  Why travellers       The four things that go wrong on Zanzibar day
    choose us          trips, and how you fix them
  Kite school          Three lesson levels as overlay cards (photo
                       fills the card, price on a gradient scrim) +
                       wind season chart
  Tours & excursions   ALL 20 tours from your Kite Beach sign, each
                       as its own full section — big photo on one
                       side (alternating left/right), tour title
                       displayed on the photo, number, name and
                       description on the other. Press "read more" on
                       any one to expand the rest of the story, what's
                       included and the meeting point with a Google
                       Maps link.
  Mainland safaris     6 packages as overlay cards, in a slider —
                       Serengeti, Ngorongoro, Tarangire/Manyara,
                       Great Migration, Mikumi, Selous + Big Five
  Find us              Live Google Map + 4 directions cards
  Gallery              Your own photos, each with a title and a full
                       descriptive line overlaid on the photo
  Our team             4 people as round profile photos — circular
                       photo, role badge, name and bio centred below
  Testimonials, FAQ    Reviews and 8 common questions
  Contact              A form (name, phone, dates, tour, message)
                       that opens WhatsApp with everything filled
                       in — plus a WhatsApp/call/email/map panel
  Footer                Site map, contact details


WHATSAPP BUTTONS
-----------------
Every WhatsApp button on the site is now WhatsApp green (#25D366)
with a small pulsing "ping" ring behind the icon — the top bar CTA,
the hero button, the CTA band, the contact form's WhatsApp card, and
the mobile menu's bottom button. If you ever want to reuse this
style elsewhere, give any button class="btn btn--whatsapp" and wrap
its icon in <span class="wa-ping">...</span>.


THE 20 TOURS (in order, exactly as on your sign)
------------------------------------------------
  01 Whales Watching            11 Spice Tour
  02 Dolphins Tour              12 Mtende Beach
  03 Paradise Island            13 Salaam Cave
  04 Mnemba Island              14 Kite Surfing Lesson / Surf
  05 Stone Tour                 15 Transfer Air Port / Sea Port
  06 Prison Island              16 Local Fishing
  07 Nakupenda Isles            17 Diving / Snorkeling / Mnemba
  08 Deep Sea Game Fishing      18 The Rock / Sun Set Cruise
  09 Blue Lagoon / Star Fish    19 Jet Ski
  10 Jozani Forest              20 Horse Riding


HOW TO EDIT A TOUR
------------------
All 20 tours live in one list near the bottom of index.html.
Search for:   var TOURS = [

Each tour looks like this:

  {
    n:"Mnemba Island",          <- name shown on the section
    cat:"island",               <- filter: ocean / island / culture /
                                   action / beach / service
    price:70, unit:"per person",
    dur:"Half day",
    badge:"Atoll · 2 snorkel stops",   <- unused decorative tag, safe to ignore
    img:"full-url-to-image.jpg", <- photo (see below)
    teaser:"...",               <- short line under the title
    facts:["Departs 7:30am","Turtles most days"],
    p1:"first paragraph...",    <- always visible
    p2:"second paragraph...",   <- revealed by "read more"
    inc:["...", "...", "...", "..."],  <- what's included
    best:"...", meet:"...", group:"...",
    map:"Mnemba Island Zanzibar"       <- Google Maps search term
  }

Change the text between the quotes. Don't remove the commas or quotes.
This same list also fills the "Tour or safari" dropdown in the
contact form automatically — you never need to edit that separately.


HOW TO SWAP A PHOTO
-------------------
Your own photos:   put the file in images/ and write
                   img:"images/my-photo.jpg"

External images:   write the full URL
                   img:"https://example.com/photo.jpg"

Your 7 real photos are already used in: About us, the kite school,
the gallery, and all 4 team members.


TOUR IMAGES (CURRENT)
---------------------
  Mnemba Island (tour 04): Turtle photo from Google Images
  Blue Lagoon / Star Fish (tour 09): Starfish photo from Zanzibar Star Tours

To replace these, edit the img field for each tour and use a new URL.


PHONE NUMBER / WHATSAPP
-----------------------
Search index.html for  255777481937  and replace every instance.
It appears in the top bar, header, hero, mobile menu, tour sections,
the contact form and button, footer, and every WhatsApp button.

Email: search for  info@hassankitezanzibar.com
Social: search for  instagram.com  and  facebook.com


TEAM SECTION
------------
Shows 4 people, each as a round photo with role, name and a short
bio centred below it. To add a 5th person, copy one whole block:

  <article class="mate">
    <div class="mate-photo"><img src="images/x.jpg" alt="..."></div>
    <span class="mate-role">Role here</span>
    <div class="mate-body"><b>Name</b><span class="yrs">Detail line</span>
      <p>One or two sentences.</p>
      <div class="mate-langs"><span>Swahili</span><span>English</span></div>
    </div>
  </article>

To use initials instead of a photo (no picture yet), replace the
<img> with:  <span class="mate-init">AB</span>


GALLERY CAPTIONS
----------------
Each photo has a bold title and a full descriptive sentence, both
overlaid on the image. Search for class="gal-cap" to find and edit
them — the pattern is <b>Title</b><span>Description</span>.


CONTACT FORM
------------
The form doesn't need a server. On submit it builds a message from
whatever the visitor typed and opens WhatsApp with it pre-filled —
your team just taps send on their end. Nothing is stored anywhere.

To change which number it messages, search for wa.me/255777481937
inside the contactForm submit handler near the bottom of the file.


LATEST CHANGES
--------------
  Topbar on tablet/phone (900px and below) now shows only the
  gold star row on the left and the WhatsApp/Instagram/Facebook
  icons on the right. The "4.9 / 5", the divider, the location
  and the green "Book on WhatsApp" pill are hidden at those widths.

  The header "Book a trip" button now scrolls to the Contact
  form instead of jumping straight to WhatsApp. The form builds
  the WhatsApp message with name, phone, dates, tour and message.

  All 20 tour sections now display the tour name as a large title
  overlaid on the bottom of each photo, with a dark gradient for
  readability.

  Price tags ($50 per person, etc.) have been removed from the
  tour photo sections — prices are still in the form dropdown and
  individual tour descriptions if needed.

  Mnemba Island tour now shows a turtle photo (turtles seen on
  most mornings). Blue Lagoon / Star Fish tour now shows an actual
  starfish photo matching the tour description.


TESTED
------
  20 tour sections render, alternating left/right, read-more works
  6 safari and 3 kite-level overlay cards render correctly
  4 team members as round profile cards, name/role/bio centred
  Gallery captions show a title + full sentence on every photo
  Contact form dropdown auto-fills with all 20 tours + Mainland safari
  Contact form submit builds a correct WhatsApp deep link
  Header fits one row down to narrow phone widths
  Mobile menu slides in, staggers its links, hamburger morphs to X
  WhatsApp buttons render green with a pinging icon everywhere
  Tour title overlays on all photos + no price chips displayed
  0 JavaScript errors, no horizontal scrolling
  Keyboard accessible, respects reduced-motion settings
