# Pending Strategies

<!-- Auto-managed by AIRA. Format: - 📌 Title | why: reason | fix: action | tag: type | date: YYYY-MM-DD -->

- 📌 Buffer social post scheduling | why: BUFFER_ACCESS_TOKEN not configured in n8n | fix: buffer.com → Settings → Apps & API → copy Access Token → n8n Credentials → Header Auth (Authorization: Bearer TOKEN) | tag: api-key | date: 2026-05-27
- 📌 LinkedIn Jobs API posting | why: LinkedIn OAuth token + Developer Portal approval needed | fix: developer.linkedin.com → create app → request Job Postings API → OAuth → set LINKEDIN_JOB_TOKEN + LINKEDIN_COMPANY_ID in n8n env | tag: oauth | date: 2026-05-27
- 📌 Bayt.com job posting API | why: BAYT_API_KEY and BAYT_COMPANY_ID not configured | fix: bayt.com → Recruiter Portal → API & Integrations → generate key → set BAYT_API_KEY + BAYT_COMPANY_ID in n8n environment variables | tag: api-key | date: 2026-05-27
- 📌 Indeed UAE automated posting | why: Indeed has no direct REST API for job posting without Enterprise agreement | fix: Option A - post manually at employers.indeed.com (free) | Option B - host XML job feed on bran-vps and submit to indeed.com/intl/en/feedsubmission/ | tag: approval | date: 2026-05-27
- 📌 Import n8n workflows to bran-vps | why: CANONICAL_buffer-social-post.json and CANONICAL_uae-job-multi-post.json need to be imported and IDs updated in worker.js | fix: n8n dashboard → Import workflow → note ID → update worker.js buffer_post.id and uae_job_post.id → wrangler deploy | tag: pending | date: 2026-05-27
- 📌 Set n8n environment variables | why: TELEGRAM_BOT_TOKEN GATEWAY_TOKEN WORKER_BASE_URL needed by new workflows | fix: n8n → Settings → Environment Variables → add all three (same values as Cloudflare secrets) | tag: api-key | date: 2026-05-27
