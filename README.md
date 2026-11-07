# Israeli Sock Puppet Generator

Realistic, internally consistent Israeli research personas ("sock puppets" or "legends") for OSINT investigations.

**Use it online:** https://harelhz.github.io/israeli-sock-puppet-generator/

Everything runs in your browser. The page sends no persona data anywhere; the only network request is for Google Fonts. You can also download `index.html` and open it offline.

## What a persona includes

The persona is one card with four tabs.

| Tab | Contents |
| --- | --- |
| Overview | A full backstory in English and Hebrew, a visual life timeline from age 18, identity (family origin, aliyah, church, siblings, languages, status) and places (hometown, where they live now, team) |
| Life | Army or national service with unit, role, dates and rank; reserve duty; degree and institution; job; travel; phone, car, pet, music and TV; interests |
| Online | Username ideas, Hebrew and English bios, a prompt for an AI-generated profile photo, the platforms they would use, and their voice: language mix, slang, emoji and sample captions |
| Calendar | This week's Shabbat offline window computed from sunset in their city (or Friday prayer, Ramadan iftar, Sunday church), posting habits, timezone and keyboard settings, and the upcoming holidays they would mark |

Communities: Secular Jewish, Traditional Jewish (Masorti), Religious-Zionist, Arab Muslim, Arab Christian and Druze. Filter by community, hometown, gender and age (18–65).

## Why it holds up

Each detail is generated to fit the others:

- **Names match the era.** Every first name carries the birth years it was common in, so a 45-year-old is not called Liam and a 20-year-old is not called Orit.
- **The timeline is built month by month.** 12th grade ends in June of the year they turn 18; enlistment, a mechina gap year or the Hesder track follow; men serve 32 months, women 24, officers longer. Then a few months of work, often the big post-army trip, and a degree starting in October. Nobody studies while serving or starts a degree mid-trip.
- **Service follows the community.** Druze men serve, Druze women are exempt, Religious-Zionist women mostly do Sherut Leumi, Arab citizens are not drafted (some do civic service). Reserve duty only appears a year after discharge.
- **Degrees exist where they are taught.** Pharmacy only at the three universities that offer it, architecture only at the four schools with a program, master's degrees only at universities. Fields and jobs are weighted by gender, and army skills carry over (Mamram veterans tend to end up in tech).
- **Hebrew is gendered correctly** in bios and the backstory: שירתה כמשקית ת"ש, השתחררה בדרגת סמלת, סטודנטית שנה ב' לסיעוד באוניברסיטת בן-גוריון.
- **Families fit places.** Big Arab family names belong to their towns (Mahameed in Umm al-Fahm, Halabi in Daliyat al-Karmel), Jewish surnames match family origin, and immigrants arrive with the real waves (the 1990s from the former USSR, 2001–2003 from Argentina).
- **Students live near campus.** A Technion student from Ashdod lives in Haifa; young secular professionals often move to Tel Aviv.
- **The calendar is real.** Holiday dates run through mid-2028; Christian personas get Christmas on December 25 or January 7 depending on their church, and Easter on the Orthodox date, as most local churches do. Muslim dates are approximate because they depend on the moon.

## Persona codes

Generation is deterministic. Each persona has a code such as `K7Q2MX` (or `K7Q2MX-201034` after rerolling parts of it). The same code with the same filters always produces the same persona, so you can keep the code in your case notes. Each part (name, places, background, daily life, interests, online presence) can be rerolled on its own.

Save legends in the browser, or export them as text or JSON (copy or download).

## Not generated, on purpose

- **National ID (Teudat Zehut) numbers.** Fake numbers with valid check digits can belong to real people and have no legitimate OSINT use.
- **Phone numbers.** A made-up number belongs to someone. Use a real number you control.
- **Photos.** The tool writes a prompt for an AI image generator. Never use a real person's pictures.
- **Arabic bios.** Write these with a native speaker so they read naturally.
- **Real employers.** Workplaces stay generic ("a startup", "a bank").

## Responsible use

This tool is for investigators, journalists, researchers and analysts who need to observe open sources without exposing their own identity. Before a persona goes live:

- Run it in an isolated environment (a VM or a dedicated browser profile).
- Match network and device to the persona: Israeli exit IP, `Asia/Jerusalem` timezone, the right browser language and keyboards.
- Keep a legend log of everything the persona says and does.
- Collect passively by default. Interacting with targets, joining closed groups, or anything deceptive needs legal sign-off and clear rules of engagement for your organization and jurisdiction.
- Most platforms prohibit fake accounts in their terms of service. You are responsible for how you use it.

Do not use this tool for harassment, fraud, impersonation of real people, or coordinated inauthentic behavior.

## Contributing

All data lives in plain arrays near the top of the `<script>` block in `index.html`: names (with eras), surnames, cities (with coordinates), units, institutions, degree programs, jobs, interests, music, TV and the holiday calendar. Corrections and additions are welcome. Please keep entries realistic and consistent, for example add a degree program only to institutions that actually offer it. The `EVENTS` calendar needs new dates every year.

## License

[MIT](LICENSE)
