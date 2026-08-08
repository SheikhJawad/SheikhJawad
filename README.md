## Jawad Yousaf

**Backend engineer — Django, distributed task pipelines, and LLM systems in production.**

I work on the unglamorous half of AI products: the queueing, the retries, the idempotency,
the cost accounting, and the parsers that have to survive whatever a customer actually uploads.

📍 Pakistan · [LinkedIn](https://linkedin.com/in/jawad-yousaf-devloper360) · [Portfolio](https://personal-portfolio-seven-amber-80.vercel.app/) · hafizjawad858@gmail.com

---

### Currently

Backend for a **language-quality-assurance platform** — an AI pipeline that scores translated
content against the MQM error taxonomy, then routes every segment through a multi-stage human
review workflow before producing an auditable quality report.

**Things I built or own there**

- **Dual-agent LLM pipeline** — one model detects errors, a second adjudicates them. Semaphore-bounded
  concurrency with Redis checkpointing, so a run can stop, resume, or restart mid-file without losing work.
- **Provider-agnostic LLM layer** over OpenAI, Anthropic, Google and AWS Bedrock — one interface,
  per-model pricing sync, and pre-flight cost estimation before a job is allowed to start.
- **Celery on a threads pool** so `asyncio.gather` can fan out inside tasks, with explicit connection
  lifecycle handling that a prefork pool would otherwise hide.
- **Quality scoring engine** with client-configurable severity weights, per-category penalties and
  pass thresholds — one formula mirrored across four surfaces, and the guardrails that keep it from drifting.
- **Format-preserving parsers** for XLSX, CSV and four XLIFF dialects, with lossless inline-tag
  round-trip so a translated file comes back out intact.
- **Integration surface** — S3 ingestion, event-driven partner notifications, and HMAC-signed public APIs.

**Stack** · Django 5 · DRF · PostgreSQL · Redis · Celery · Docker · AWS

---

### How I work

- **Root cause over symptom.** One guard in the shared function beats a guard in every caller.
- **Boring beats clever.** Clever is what someone has to decode at 3am.
- **Deletion is a feature.** The best code is the code that never needed to exist.

---

### Also interested in

Applied NLP and sentiment analysis · real-time systems over WebSockets · data pipelines and crawlers.
A few of these live in the pinned repositories below.
