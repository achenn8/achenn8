### Hi, I'm Angela 👋

I'm building **[The Stacks](https://thestacks.page)**, a book-ranking app that replaces 5-star ratings with head-to-head comparisons.

**Why:** Star ratings bunch at the top. When most of the books you liked get a 4 or a 5, the scale stops telling you anything. The Stacks makes you commit to an order instead: each book you finish is placed by a few "which did you enjoy more?" comparisons within a tier, and its score is a readable view of where it sits on *your* shelf.

**A few product decisions behind it:**
- **Local-first.** Your books live on your device and the app works offline. An account is optional: it keeps a copy in sync across devices, and the device stays the source of truth.
- **An honest Goodreads import.** Import reads the CSV export Goodreads provides, entirely in your browser, so the file never leaves your device. Books placed by their old star rating are flagged *not yet ranked by you*, and books you never rated go to a *Read, not yet filed* shelf with no score, because no judgement has been given.
- **Sync that asks.** If two devices change your books, the app shows you both versions and asks which to keep, rather than letting the last save silently win.
- **Passwordless and private.** Sign-in is by email link, so there's no password to leak. Database rules mean each person can only ever read their own data, and deleting your account removes everything stored on the server.

**Built with:** vanilla HTML, CSS and JavaScript in a single file · Supabase (auth, Postgres with row-level security, an Edge Function) · Resend · Vercel. I wrote the product spec, made the product and design decisions, tested each release, and directed the implementation with Claude Code.

The source repository is private; happy to walk through it.
