# Next.js i18n Locale Missing in getStaticProps

This repository demonstrates a bug and its solution related to the `locale` parameter being undefined in `getStaticProps` or `getStaticPaths` within a Next.js application using internationalization (i18n).  Even with seemingly correct i18n configuration, the locale parameter was unexpectedly missing from the context, resulting in failed localization.

## Bug Description
The `locale` parameter was missing from the `context` object passed to `getStaticProps`. This prevented the proper loading of localized content.

## Solution
The solution involves ensuring the Next.js i18n configuration is correct and potentially using the `router.locale` within `getServerSideProps` if static generation isn't essential for a specific route.