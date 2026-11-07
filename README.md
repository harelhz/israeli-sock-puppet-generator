# Israeli Sock Puppet Generator

A single-page tool that builds consistent Israeli research personas ("sock puppets" or "legends") for OSINT investigations.

Every detail is generated to fit together: a Hebrew or Arabic name that matches the community, a real hometown and neighborhood, army or national service that matches age and background, studies at an institution that actually offers that degree, a job that follows from it, interests, handles, Hebrew and English bios, and an activity rhythm (for example, a Religious-Zionist persona never posts on Shabbat).

It is one HTML file with no build step, no dependencies and no network calls apart from Google Fonts. Nothing you generate leaves your browser.

## Use it

Download `index.html` and open it in any modern browser, or clone the repo:

```bash
git clone https://github.com/harelhz/israeli-sock-puppet-generator.git
```

Then open `index.html`. It works offline (fonts fall back to system fonts).

## What it generates

| Section | Contents |
| --- | --- |
| Identity | Name in Hebrew (and Arabic for Arab and Druze personas) plus English transliteration, gender, age, date of birth, family origin, languages, marital status |
| Hometown | City (Hebrew / English / Arabic), district, neighborhood, local football team |
| Background | IDF unit, role and rank, Hesder or mechina track, Sherut Leumi or civic service, reserve duty, degree and institution, occupation, travel |
| Interests | 4–5 interests in English and Hebrew, weighted by community |
| Online presence | Username ideas, Hebrew and English bios, a prompt for an AI-generated profile photo, platforms the persona fits on |
| Activity rhythm | Posting habits, holidays, timezone, browser language and keyboards |

Communities: Secular Jewish, Traditional Jewish (Masorti), Religious-Zionist, Arab Muslim, Arab Christian and Druze. "Any" picks one weighted roughly by population. You can filter by gender and age range.

## Persona codes

Generation is deterministic. Each persona has a code such as `K7Q2MX` (or `K7Q2MX-20100` after rerolling sections). The same code with the same filters always produces the same persona, so you can store the code in your case notes and restore the persona later. Each section (name, hometown, background, interests, online presence) can be rerolled on its own without changing the rest.

Export the full legend as plain text or JSON with the buttons in the sidebar.

## Not generated, on purpose

- **National ID (Teudat Zehut) numbers.** Fake numbers with valid check digits can belong to real people and have no legitimate OSINT use.
- **Phone numbers.** A made-up number belongs to someone. Use a real number you control.
- **Photos.** The tool gives you a prompt for an AI image generator. Never use a real person's pictures.
- **Arabic bios.** Write these with a native speaker so they read naturally.

Workplaces are generic ("a startup", "a bank") so a persona never claims a specific real employer.

## Responsible use

This tool is meant for investigators, journalists, researchers and analysts who need to observe open sources without exposing their own identity. Before a persona goes live:

- Run it in an isolated environment (a VM or a dedicated browser profile).
- Match the network and device to the persona: Israeli exit IP, `Asia/Jerusalem` timezone, the right browser language and keyboards.
- Keep a legend log of everything the persona says and does.
- Collect passively by default. Interacting with targets, joining closed groups, or anything deceptive needs legal sign-off and clear rules of engagement for your organization and jurisdiction.
- Most platforms prohibit fake accounts in their terms of service. You are responsible for how you use it.

Do not use this tool for harassment, fraud, impersonation of real people, or coordinated inauthentic behavior.

## Contributing

Data corrections and additions are welcome: names, surnames, cities, neighborhoods, units, institutions, degree programs, jobs and interests all live in plain arrays near the top of the `<script>` block in `index.html`. Please keep entries realistic and consistent (for example, add a degree program only to institutions that actually offer it).

## License

[MIT](LICENSE)
