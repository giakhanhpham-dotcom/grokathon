[README.md](https://github.com/user-attachments/files/35001715/README.md)[Uploadin# Routed
video recording: https://drive.google.com/drive/u/0/folders/1xOShuVBCruVrW4b9_y5-OtIoerzczdSf 
**Routed helps Yale College undergrads, especially first-years and international students, figure out what they need and who to go to.**

Yale Hub is where you *do* things: register for classes, check your transcript, update your info. Routed is where you figure out *what to do first*. You describe your problem in plain language. Routed works out which office owns it, puts the offices in the right order, tells you what to bring, and drafts the message for you. Around that core, it also helps you plan your courses, find clubs and jobs, and get quick, private answers to the questions you might not want to ask a FroCo.

> **Status:** prototype / demo (November 2026). Some data is example data, and every contact needs human verification before real students use it. See [What's real and what isn't](#whats-real-and-what-isnt).

---

## What it does

Routed has four tabs.

### 1. Route me: find the right office
Type what's going on, for example *"My tuition is due and my family's transfer from abroad is delayed."*

- **Emergencies first.** If what you type sounds like danger, a medical emergency, sexual misconduct, or thoughts of self-harm, Routed skips everything else and shows the right 24/7 number. It doesn't draft an email.
- **Matches the office that owns the decision.** It searches a curated directory of Yale offices, comparing your words with what each office handles (and what it doesn't).
- **Puts offices in order.** If you need more than one office, they appear as *Step 1, the office that owns the decision*, then the supporting offices. International students asking about jobs always see OISS first.
- **Guided cards.** Each card explains why that office handles it, what to bring, how to reach them, and who to try next, and includes a drafted message with a subject line and a Copy button.
- **Personalized to your college.** It uses your residential college dean and Head of College where it matters.
- **Makes nothing up.** It only recommends offices, people, emails, and phone numbers that appear in its verified directory. If nothing fits, it says so and points you to your FroCo and dean.

### 2. Courses: a one-screen planner
Built on real **Spring 2027 Yale College** course data.

- Enter your interests, the classes you already plan to take (with times and workload), and a workload range (default 16–20).
- Routed lists course combinations with **no time conflicts** that fit your workload cap, and explains each pick: the interests it matches, the distributional requirements it covers, its total workload, and whether it leaves Friday free.
- Each course card shows short summary bullets, meeting times, prerequisites, whether permission is required, final exam info, and links to Yale Course Search and CourseTable.
- A weekly calendar shows your schedule, with any conflicts outlined in red, plus running totals for credits and workload.

### 3. Clubs & Jobs: beyond pre-professional
- Recommends groups based on your interests, across **fun and wellbeing** groups (Y Pop-UP, Asian Recipes at Yale, improv like Just Add Water, a cappella, dance), **pre-professional** ones, and **community** ones.
- Each recommended group shows how selective it is (no-cut or audition), how to join, its recruiting timeline with a source, coffee-chat norms, and its wellbeing value. You can also search the full Yale Connect directory.
- **Jobs:** how student employment works at Yale, including the rules for international students. Talk to **OISS first**. Yale caps all students at **19 hours a week** across all on-campus jobs, and the F-1 visa limit is 20. An hours planner warns you if you go over.

### 4. Life: private, practical answers
Short, judgment-free answers to things first-years often don't want to ask out loud:
- Sexual and reproductive health: STI symptoms and testing, pregnancy concerns, and what stays confidential at Yale Health.
- Vaccines: flu, COVID, HPV, and meningococcal.
- Health logistics: appointments, insurance, and where to go after hours.
- First-year life: homesickness, roommates, feeling behind.

Each answer gives next steps and verified Yale links. Crisis numbers are always on screen, and the tab uses the same emergency detection as the router. Nothing you type here is stored or sent anywhere.

The tabs link to each other. For example, telling the router your workload is overwhelming points you to your dean *and* offers to open the planner with a lower workload cap.

---

## Try it

**Quickest:** open `routed-demo.html` in any browser. It's a single self-contained file, so there's nothing to install. This demo build has 1,000 courses and 200 clubs.

**Full app:**
```bash
./run.sh        # rebuilds the data files and serves the app at http://localhost:8080
```
Or open `app/index.html` directly from disk.

**Things to try in "Route me":**
- "I'm an international student. How do I waive the Yale health insurance?"
- "I'm international and got fired from my dining job. Can I work more hours somewhere else?"
- "I'm panicking about a midterm and my workload is too much."
- "I want to request a single room."

---

## What's real and what isn't

| Real (from public Yale sources) | Example data (placeholder, marked **EXAMPLE** in the app) |
|---|---|
| 2,104 Spring 2027 Yale College courses: titles, descriptions, instructors, meeting times, distributional requirements, credits, prerequisites | Workload ratings, professor ratings, grading/curve, typical class size, % first-years. The real versions sit behind a Yale login and weren't used. |
| 493 Yale College groups from Yale Connect, plus 26 hand-checked groups with sourced timelines | Some club dates are from the 2026 cycle and will shift |
| Office directory, phone numbers, and Yale Health links (checked November 2026) | Only Timothy Dwight College is fully filled in; some office contacts are still placeholders |

**Important:** Routed is not medical, legal, immigration, or financial advice, and it isn't a replacement for counseling. It points you to the people who make those calls. The Life content has not yet been reviewed by Yale Health, Mental Health & Counseling, or OISS.

**If you're in crisis:** call 911, Yale Mental Health & Counseling (24/7) at 203-432-0290, or 988.

---

## Data sources
All public, no login: [CourseTable public catalog](https://coursetable.com), [Yale Course Search](https://courses.yale.edu), [Yale Connect](https://yaleconnect.yale.edu), [Yale Health](https://yalehealth.yale.edu), [OISS](https://oiss.yale.edu), the Student Employment Office, and individual group pages.

## For developers
Project structure, the data pipeline, router internals, tests, and known gaps are in [`docs/DEVELOPMENT.md`](docs/DEVELOPMENT.md).
g README.md…]()
