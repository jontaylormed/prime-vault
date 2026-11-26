# Operation Prime Vault

Find factors with dot grids, test divisibility rules, sort primes from composites, then build a vault key by multiplying two 3-digit primes.

**Live site:** <https://jontaylormed.github.io/prime-vault/>

**Source:** <https://github.com/jontaylormed/prime-vault>

**Site created by Claude and Jon Taylor.**

[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)

---

## What it does

| Section | What the student does |
|---|---|
| Factors | Sees 3, 5, 8, 12, 24 and 27 as dot grids, with every factor pair and the factor count |
| Divisibility | Learns the rules for 2, 3, 4, 5, 6, 8, 9 and 10 with worked examples, then answers a quiz on random 3-digit numbers |
| Prime Numbers | Sends a number into the Factor Splitter, compares two numbers' factors side by side, and sees factor counts from 2 to 19 |
| Prime Database | Browses every number from 1 to 1,000 with the primes marked, and highlights the multiples for any rule |
| Vault Mission | Picks two different 3-digit primes, multiplies them by hand to make the key, decides whether the key is prime, and checks which divisibility rules apply |

## Who it's for

Grades 4–6.

Common Core State Standards for Mathematics:

| Standard | What it asks |
|---|---|
| 4.OA.B.4 | Find all factor pairs for a whole number from 1 to 100, recognize multiples, and determine whether a number is prime or composite |
| 5.NBT.B.5 | Fluently multiply multi-digit whole numbers using the standard algorithm |

## How it teaches

- **See it first.** Each number starts as a set of dots beside its factor pairs, so students see that 12 can be grouped as 3 × 4 or 2 × 6, while a prime such as 5 only pairs as 1 × 5.
- **Structure before numbers.** Students learn factor pairs first, then the divisibility rules that find factors quickly, then what makes a number prime.
- **Check every claim.** The mission checks each prime students choose and lists the factors of any number that isn't prime. It explains why the key can't be prime, and shows which rules really apply.
- **A story with a goal.** The bank-vault mission gives the practice a purpose. The tool says plainly that a key this small could be cracked by a computer, and that real keys use primes hundreds of digits long.

## How the math was checked

- **Checks page:** [`checks.html`](https://jontaylormed.github.io/prime-vault/checks.html) runs 99 checks in the browser against its own arithmetic: a sieve of Eratosthenes and direct division. All 99 pass. It checks:
  - every prime from 1 to 1,000, and factor lists up to 300;
  - all 1,000 cells of the prime database, and that there are 168 primes;
  - every factor card: its pairs, its count, its label and its number of dots;
  - every number pool, each comparison panel from 1 to 60, every divisibility rule for all numbers up to 20,000, and all 15 worked examples;
  - 300 random quiz questions;
  - the full mission, and every key that could be made from two 3-digit primes;
  - each real-world example;
  - keyboard use, contrast and labels;
  - a scan for outside requests and storage.
- **Fixed after checking:**
  - The comparison summary called 1 "composite".
  - "Every number has at least two factors" was false for 1.
  - "For 7, the only reliable method is to do the division" was false; 7 does have divisibility tests.
  - The encryption story called composite keys weak, but a product of two primes is itself composite.
  - It also said a key made from two 3-digit primes is "practically impossible to crack". At most 168 trial divisions factor it.
  - Unsupported claims about jazz, cicadas and architecture were rewritten to what the math shows. For example, a 4-year cycle meets a 13-year cycle only every 52 years.
  - The mission said a product of two different primes has "at least 4" factors; it has exactly 4.
- **Known limits:**
  - The factor cards cover six chosen numbers. The comparison tool covers any number a student types.
  - The encryption story is simplified. Real keys use primes hundreds of digits long.

## Accessibility

- **Keyboard:** everything works with the keyboard, and focus outlines are visible. The section tabs, training cards, rule buttons, quiz answers and mission steps all work with Tab and Enter.
- **Contrast:** text meets the WCAG 2.1 AA target of 4.5:1. Main text is 16:1, purple "prime" text 5.9:1 or better, and buttons with purple backgrounds use dark text (7.7:1).
- **Screen readers:**
  - Feedback, status lines, quiz questions and results are read aloud.
  - Every box is labeled.
  - The Factor Splitter and divisibility pictures are described, and their results are always written out as text.
- **Motion:** when the device asks for reduced motion, the blinking, scanning and fade effects stop. The splitter and vault animations run only when a student starts them.
- **Text size:** there is no separate setting; the page follows browser zoom.

## Privacy

No accounts, no tracking, no cookies and no stored data. The page makes no network requests: its typefaces are built into the file, and `checks.html` confirms nothing loads from outside.

## Running it

Open `index.html` in any modern browser.

`checks.html` reads the tool, so open it from the live site or any local web server, not as a file.

**Publishing:** GitHub Pages, deployed from the `main` branch at the repository root. There is no build step.

## License

[CC BY-NC-SA 4.0](LICENSE). Free to share and adapt for non-commercial use, with credit, under the same license.

The bundled typefaces keep their own licenses, and their license files are in [`fonts/`](fonts/):

| Typeface | Designer | License |
|---|---|---|
| Orbitron | Matt McInerney | [SIL Open Font License 1.1](fonts/OFL-orbitron.txt) |
| Share Tech Mono | Carrois Type Design (Ralph du Carrois) | [SIL Open Font License 1.1](fonts/OFL-sharetechmono.txt) |
| Nunito | The Nunito Project Authors | [SIL Open Font License 1.1](fonts/OFL-nunito.txt) |
