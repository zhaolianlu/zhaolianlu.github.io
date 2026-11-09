# Zhaolian Lu Lab Website

This repository hosts the bilingual website of the Zhaolian Lu Lab at Shandong Cancer Hospital. English is the default language and Simplified Chinese is available under `/zh/`.

## Content structure

- `content/en/`: English lab pages
- `content/zh/`: Simplified Chinese lab pages
- `content/en/publications/*/index.md`: HugoBlox-compatible publication bundles
- `layouts/`: additive lab layouts and shared header/footer partials
- `static/css/lab.css`: responsive lab design system
- `static/media/zhaolian-lu.png`: portrait derived from the supplied CV
- `config/_default/zz_lab.yaml`: additive site identity and bilingual configuration

## Updating content

Edit Markdown files in the appropriate language directory. Keep equivalent information in both languages. Do not add unverified team members, claims, publication identifiers, news, contact details, or compensation.

## Local development

```bash
pnpm install --frozen-lockfile
pnpm run dev
```

The existing GitHub Actions workflows build and deploy the site on pushes to `main`. See `DEPLOYMENT.md` for safety checks and `DOMAIN_SETUP.md` for the deferred custom-domain procedure.

## Source and privacy policy

The website content was prepared from the supplied CV and recruitment announcement. Original source documents are not included in the public repository. A phone number, date of birth, and older institutional email found in the CV are intentionally excluded.

