# Requirements

## Functional

- **The system must allow users to search and retrieve research papers within ≤ 3 seconds using keyword filters (title, author, year, journal, domain, source, date range, topic, paper type, affiliation, citation number, publication type) and advanced semantic/contextual search powered by NLP embeddings, supporting at least 100,000 indexed documents.**

- **Paper Ingestion & External API Fetching** — The system must fetch papers and metadata from APIs such as Semantic Scholar, arXiv, CrossRef, PapersWithCode, CORE, and Unpaywall. Fetched data must include title, authors, abstract, year, DOI, keywords, citations, references, code availability, and Open Access status. The system must support batch fetching (daily sync), rate limit handling, retries, normalization into a unified schema, and deduplication. This ingestion powers search, summarization, recommendations, analytics, and library enrichment.

- **The system must provide AI-based summaries at abstract, section, and full-text levels, generated in ≤ 10 seconds, with options to select use-case modes (“Quick Skim,” “Teaching,” “Deep Dive”, “Plain English”, “Technical”) and capture explicit user feedback for iterative refinement with options to export/copy to the integrated notes making app.**

- Papers must be grouped automatically into categories (e.g., AI, DSA, Biology) using unsupervised clustering with ≥ 90% classification precision, and users must be able to override or manually edit categories.

- **The platform must provide recommendations of at least 5 related papers per item based on semantic similarity and a section for why it was recommended.**

- **A library-based storage system must maintain user collections, organized into personal and team libraries, with versioning and duplication checks across uploads along with preset lists like “Recently Added”, “Read Next”, “History”, “Notes”, “Uploads”, “Playlist/Bookmark”.**

- **Users must be able to form and manage teams and associated reading lists/notes/annotations (CRUD: create, join, leave, update), with role-based access (Owner, Contributor, Viewer) enforced consistently across modules with invitation link sent via mail/code/manually.**

- The system must display relevant paper content views: Abstract-only, Section-based, with additional functions like search/GPT.

- **Analytics dashboards must track reading streaks, time spent per paper/overall, and progress bars (percent completion of paper), topic distribution, completion rate, and visualizations refreshing within ≤ 1 second of action logging. The system shall provide usage insights such as number of papers read per week, most active categories.**

- The platform must allow notifications (new papers, author updates, team activity) to be delivered within ≤ 30 seconds of event trigger.

- **Export & Import Integrations** — Users should be able to export citations (BibTeX, RIS, APA/MLA). Import support from third-party apps (Zotero, Mendeley, Notion) must be available. Exports should allow opening papers directly in external tools (e.g., Notion).

- The system must allow subscriptions to authors and display recent/most cited papers, updated every 24 hours using external bibliometric datasets (Google Scholar, CrossRef). Notifications (web or email) must inform them of new uploads, new citations, or updates in followed lists. The system shall provide reminder notifications for unread or due papers in a list.

- Users/AI upon Admin approval must be able to attach/extract external resources (datasets, supplementary links, citations, blogs, articles, YouTube videos) to papers, with validation to prevent broken links and ensuring HTTPS compliance.

- The system must support secure sign-up, login, and logout with JWT tokens. Users should be able to manage their profile (name, email, password, education level, research domains, interests). OAuth support (Google, ORCiD) must be available. Accounts must store personalization preferences and track activity history.

- **WorkMode & Split View (paper + notes), Paper-only mode.**

- **Users must be able to upload papers in PDF (≥ v1.5), DOCX, and TXT formats up to 50 MB, with automatic metadata extraction (title, authors, institution, keywords, citations) achieving ≥ 95% accuracy.**

- The system shall allow guest/unpaid access with limited functionality like limited number of summarizations, and team access not available (for guest, partial access to teams for unpaid).

- The system shall provide an admin dashboard for managing users, logs. The system shall provide logging and monitoring of API usage and recommendation models. The system shall enforce security measures.
