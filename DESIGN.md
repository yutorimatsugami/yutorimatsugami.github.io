# Design direction

## References

Desktop screenshots of these four public sites were inspected on 2026-10-18.

| Reference | Observation | Adopted idea |
| --- | --- | --- |
| [Brittany Chiang's GitHub Pages](https://bchiang7.github.io/) | Large introductory typography, generous spacing, and a direct email link. This is the older GitHub Pages portfolio. | Clear name and contact information before detailed work. |
| [Jon Barron](https://jonbarron.info/) ([GitHub Pages source](https://github.com/jonbarron/jonbarron.github.io)) | Compact introduction and social links, then research entries with project links. The github.io URL redirects to this custom domain. | Concrete work entries, linked to original sources. |
| [You Liang Tan](https://youliangtan.github.io/) | Robotics imagery and a profile/contact area establish the research field. | Show Robotics & AI immediately and keep profile links easy to find. |
| [Yuki Shirai](https://yukishirai.github.io/) | Clear research identity, restrained accent color, and news/publication sections. | Separate the introduction, selected work, and supporting background. |

Only structure and hierarchy were used as references. Reference-site code, portraits, project imagery, and biographical text were not reused.

## Proposed design

- Fixed dark theme: charcoal #0c1015, off-white #edf2f7, ice-blue #95d5ee.
- A short digital business card with a share dialog.
- Embedded Inter for Latin text and Noto Sans JP for Japanese; system monospace for years and small labels. The name uses medium weight with -0.03em tracking.
- Desktop: introductory text and an original geometric coordinate motif.
- Mobile: one column; the name and student affiliation introduce the person, followed by research interests and prominent GitHub/X buttons. The email address and a compact copy control sit underneath; Hugging Face and ORCID follow in a separate research-profile row.
- The introduction describes language- and vision-guided robot systems; research interests remain visible as topic labels. Descriptions use 15px text, with 14px Japanese supporting text.
- Two selected work entries: SAM3 software and RSJ2026 co-authored work.
- Compact team result rows; education, teaching, scholarship, and career offer below.
- Static geometry, subtle transitions, and support for reduced-motion preferences.
- Font subsets are embedded as WOFF2 data URLs, including their SIL Open Font License notices. There are no runtime font downloads, tracking scripts, image services, or QR APIs.
- The editable OGP SVG embeds the same Inter and Noto Sans JP fonts; its exported PNG uses the same palette, name, and field labels.

## Content hierarchy

1. Name, student affiliation, research interests
2. GitHub and X buttons, email, then Hugging Face and ORCID
3. Research & projects
4. Robotics competitions
5. Background
6. Share / QR at a public URL
