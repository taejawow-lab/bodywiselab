# BodyWiseLab AdSense resubmission package — 2026-06-10

## Status

Recommended status: ready to resubmit after the recent quality fixes.

Scope covered in this package:
- Thin tag/search index cleanup.
- Health/YMYL trust and medical-boundary improvements.
- Editorial, expert, policy, privacy, contact, and disclaimer page checks.
- Representative production smoke tests.
- Remaining risk notes for future improvement.

No external AdSense submission was performed in this ops pass.

## Recent quality work completed

Recent commits verified:

- `5b3fea09` — Improve AdSense readiness and thin archive indexing.
- `89b3f86e` — Strengthen priority health guides for AdSense review.
- `1e914e58` — Reduce affiliate pressure in equipment guides.
- `c2ec9c93` — Strengthen outdoor safety guides for AdSense.
- `9485dbf3` — Improve remaining thin practical guides.

Latest deployed head SHA verified through GitHub Actions / Cloudflare Pages:

- `9485dbf392053df977a5935a4ff9074cd38cb1c0`
- Workflow: Deploy to Cloudflare Pages
- Conclusion: success

## Current site inventory

Local content audit after latest fixes:

- Total MDX posts: 40
- Indexable posts: 39
- Draft/noindex post: `welcome.mdx`
- Indexable posts with fewer than 8 sources: 0
- Generic FAQ / weak `Source 1` labels found in indexable posts: 0
- Affiliate-marked indexable posts: 19
- Posts with explicit `Source interpretation note`: 12

Important caveat: 16 older posts remain below 1,500 body-word count. They all have 8+ sources and no generic FAQ/source-label flags, but they should remain the next gradual improvement queue after resubmission. The site is not blocked on these because the highest-risk thin practical guides and safety/YMYL guides were improved first.

## Sitemap and indexation checks

Production sitemap check:

- `https://bodywiselab.org/sitemap-0.xml` → 200 `application/xml`
- URL count: 62
- `/tags/` entries in sitemap: 0
- `/search` entries in sitemap: 0

Archive/search behavior:

- `/search/` → 200, `noindex, follow`
- `/tags/exercise/` → 200, `noindex, follow`

This addresses the original risk where tag/search archives could make the site look thin relative to the number of actual posts.

## Representative production smoke results

All representative URLs below returned HTTP 200 on production with realistic crawler/browser user agent.

Trust and policy pages:

- `https://bodywiselab.org/`
- `https://bodywiselab.org/about/`
- `https://bodywiselab.org/editorial-standards/`
- `https://bodywiselab.org/editorial-process/`
- `https://bodywiselab.org/experts/`
- `https://bodywiselab.org/privacy/`
- `https://bodywiselab.org/disclaimer/`
- `https://bodywiselab.org/contact/`

Representative improved articles:

- `https://bodywiselab.org/posts/home-blood-pressure-monitoring-routine/`
- `https://bodywiselab.org/posts/hot-weather-workout-hydration-electrolyte-plan/`
- `https://bodywiselab.org/posts/indoor-workout-air-quality-heat-plan/`
- `https://bodywiselab.org/posts/kettlebell-weight-selection/`
- `https://bodywiselab.org/posts/zone-2-cardio-talk-test-plan/`
- `https://bodywiselab.org/posts/wildfire-smoke-outdoor-exercise-aqi-plan/`
- `https://bodywiselab.org/posts/pre-workout-supplements-tested/`

Article marker checks observed on representative posts:

- `MEDICAL SAFETY NOTE`
- `SOURCE-CHECKED`
- `Source interpretation note`
- Topic-specific decision tables
- Updated date shown
- Source count shown

Browser QA:

- Representative page: `https://bodywiselab.org/posts/home-blood-pressure-monitoring-routine/?v=9485dbf3`
- Browser console messages: 0
- JavaScript errors: 0

## Resubmission explanation draft

Suggested concise wording for AdSense review notes if a text field is available:

> We improved BodyWiseLab after the low-value-content rejection. We reduced thin archive exposure by keeping tag and search pages out of the sitemap and marking them noindex, strengthened About, Editorial Standards, Editorial Process, Experts, Disclaimer, Privacy, and Contact pages, and expanded priority health/fitness articles with source-backed decision tables, safety checklists, medical-boundary notes, and clearer source interpretation. We also reduced affiliate pressure in equipment/supplement guides, added non-commercial alternatives and skip rules, validated representative source URLs, and verified production pages and sitemap after deployment.

Shorter version:

> BodyWiseLab has been updated after the prior review. Thin tag/search pages are noindex and excluded from the sitemap, trust/policy/editorial pages were strengthened, and key health/fitness articles now include source-backed decision tables, medical safety notes, practical checklists, updated dates, and clearer editorial boundaries. Product-related articles were revised to reduce purchase pressure and include non-commercial alternatives.

## Recommended resubmission URL set

Use these URLs for manual confidence checks before pressing resubmit:

1. `https://bodywiselab.org/`
2. `https://bodywiselab.org/about/`
3. `https://bodywiselab.org/editorial-standards/`
4. `https://bodywiselab.org/editorial-process/`
5. `https://bodywiselab.org/experts/`
6. `https://bodywiselab.org/privacy/`
7. `https://bodywiselab.org/disclaimer/`
8. `https://bodywiselab.org/contact/`
9. `https://bodywiselab.org/posts/home-blood-pressure-monitoring-routine/`
10. `https://bodywiselab.org/posts/wildfire-smoke-outdoor-exercise-aqi-plan/`
11. `https://bodywiselab.org/posts/kettlebell-weight-selection/`
12. `https://bodywiselab.org/sitemap-0.xml`

## Remaining improvement queue after resubmission

Not blockers for resubmission, but useful follow-up:

- Continue expanding older under-1,500-word posts, especially affiliate-marked supplement/equipment posts.
- Add explicit `Source interpretation note` to more legacy posts.
- Add real article images to older text-only legacy posts where possible.
- Keep tag/search archives noindex and out of the sitemap.
- Avoid publishing thin daily posts; maintain 8+ sources, safety notes, practical tables/checklists, and source URL validation.

## Rollback plan

If a regression appears, rollback target is the previous deployed commit before this final packaging round:

- `9485dbf392053df977a5935a4ff9074cd38cb1c0`

This ops note itself does not change the public site content.
