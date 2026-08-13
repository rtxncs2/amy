# Athena Matrimony

A lightweight static demo web app that showcases matrimonial profiles (Athena Matrimony. The site is a single-page static HTML app (index.html) that reads profiles from `profiles.json` and provides filtering, sorting and detail views.

## Features

- Responsive single-page UI (index.html) with filters for gender, age, religion, education, and more
- Profile grid with quick summary cards
- Modal detail view with contact mailto link
- Data-driven: profiles are loaded from `profiles.json` (array of profile objects)
- No build step — ready to host on any static file server (GitHub Pages, Netlify, Vercel, or plain web server)

## Data format (profiles.json)

`profiles.json` contains an array of profile objects. Each object includes fields used by the UI. Common fields seen in the dataset:

- id: unique profile ID (e.g. `BS001`)
- name, gender, dob (ISO date `YYYY-MM-DD`)
- maritalStatus, heightCm, physicalStatus
- email, phone
- profileCreatedBy
- religion, motherTongue, caste, gothra, manglik
- education, educationDetail, employment, occupation, annualIncome
- country, state, city, citizenship, residentialStatus
- diet, smoking, drinking, familyValues
- bio, emoji

When adding profiles ensure `dob` is a valid date string and `id` is unique.

## How to run locally

Because this is a static site you only need a web server to serve the files. Examples:

- Using Python 3 (recommended):

  - From the repository root:

    python3 -m http.server 8000

  - Open http://localhost:8000 in your browser.

- Using Node (http-server):

    npx http-server -p 8000

- Open `index.html` directly in your browser (some browsers restrict fetch for local files; using a local server avoids CORS/file protocol issues).

## Customization

- Add or edit profiles in `profiles.json`. The UI will reload profiles on page refresh.
- Edit `index.html` to tweak styles, text, or filtering logic.
- To switch the site name/title change the `<title>` and `.nav-brand` text in `index.html`.

## Recommended improvements

- Add tests and a build pipeline
- Split UI/JS into separate files for maintainability
- Add proper form validation and a secure backend for profile management
- Add pagination and server-side filtering for large datasets
- Add a LICENSE and CODE_OF_CONDUCT if you plan to open-source or accept contributions

## Contributing

This repo currently contains only a static demo. If you'd like to contribute:

1. Fork the repository
2. Make changes on a feature branch
3. Send a pull request describing the change

If you plan to add any backend, please include documentation and migration steps.

## License

No license file is present in this repository. If you want this project to be open source, add a `LICENSE` file (e.g., MIT) before accepting contributions.

## Contact

This is a demo project. The sample profiles include personal-contact fields only for demonstration; do not reuse real personal data without permission.
