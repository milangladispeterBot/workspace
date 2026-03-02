## Instructions
Website project is located at `/Users/peter/Projects/gladboy-com/`
After small chunk of work, publish new branch and create a pull request.
When tasks are completed, update this file.

---
### Sprint Planning - Q1 2026

#### Sprint 0 (3–4 days): Standardize layout + JSON data layer
**Goal**: One reusable page shell, same structure across all routes; recipes/tracking data in JSON for easy scaling.
- [ ] Create shared Layout component with consistent header/footer/nav and responsive grid
- [ ] Add data loader hook that reads from /data/*.json (recipes, supplements, foods, conditions)
- [ ] Set up TypeScript types for Recipe, Supplement, FoodItem, Condition, SymptomCategory
- [ ] Add "Data Catalog" page listing all JSON sources with counts and last updated date
- [ ] Ensure mobile menu works consistently across pages

#### Sprint 1 (5–6 days): Better daily tracking app + symptom tracking MVP
**Goal**: A clean, fast daily log that's easy to use every day; add symptoms properly.
- [x] Daily Log page with sections: Supplements/Meds, Meals, Activities, Symptoms, Energy/Mood/Sleep/Water/Notes
- [x] Symptom tracking:
  - Categories: pain, fatigue, digestion, mood, energy, other
  - Severity 1–10 with emoji scale; optional location and notes
  - Quick-add common symptoms (e.g., headache, joint pain, bloating)
- [x] Supplements/Meds quick actions:
  - Predefined list from JSON (name, dosage, timing, frequency)
  - One-tap "Take all morning" / "Take all evening"
  - Optional reminders via local notifications (if supported in browser)
- [x] Meals:
  - Quick-add from recipe library or free text
  - Meal type selector (breakfast/lunch/dinner/snack), optional taste rating
- [x] Activities:
  - Type selector (workout/walk/yoga/meditation/other), duration, distance/calories optional
- [x] Energy/Mood/Sleep/Water:
  - Energy slider (1–10), mood dropdown, sleep hours input, water ml counter with +250ml buttons
- [x] Local storage persistence and undo for last entry

#### Sprint 2 (6–7 days): Daily templates + recurring routines
**Goal**: Eliminate manual entry for daily must-takes; make it frictionless.
- [ ] Daily Templates (routines):
  - Create/edit templates like "Morning Routine" and "Evening Routine"
  - Assign items to templates: supplements, meds, symptoms check-in, water goal, sleep target
  - One-click "Start Day" populates today's log with template items
- [ ] Recurring rules engine (simple):
  - Frequency options: daily, weekdays, custom days
  - Time windows (morning/evening) and optional repeat intervals
- [ ] Smart suggestions:
  - If an item is marked "daily" and not taken today, show a gentle prompt on the dashboard

#### Sprint 3 (5–6 days): Insights + correlations (local-first)
**Goal**: Turn your logs into actionable insights without cloud.
- [ ] Correlation engine:
  - Simple stats: average energy by low-GI meals, by supplement adherence, by activity duration
  - Pattern detection: "On days with X, energy is Y% higher."
- [ ] Weekly digest view:
  - Summary card for the week (logs completed, avg energy, top insights)
- [ ] Export:
  - CSV export of logs and insights; PDF summary for doctor visits

#### Sprint 4 (5–6 days): Condition pages + health filters
**Goal**: Make GladBoy useful for multiple conditions with consistent layout.
- [ ] Condition landing pages (diabetes, blood pressure, inflammation, weight management) using the same layout shell
- [ ] Health filters on recipe list and detail pages (low-GI, heart-healthy, anti-inflammatory, diabetes-friendly)
- [ ] Recipe badges + "Why this helps" callouts per condition
- [ ] Medical disclaimer system across all health-related content

#### Sprint 5 (4–5 days): Signup page + email capture MVP
**Goal**: Start building an audience without full auth yet.
- [ ] Simple email capture with value prop and lead magnet (e.g., "7-Day Low-GI Starter Guide")
- [ ] Thank-you page with download link; basic automation via existing ESP
- [ ] Optional: save user preferences locally for future personalization

#### Sprint 6 (5–6 days): Polish + accessibility + performance
**Goal**: Make it feel premium and reliable.
- [ ] Micro-interactions, hover states, consistent shadows/borders, gradients on CTAs
- [ ] Accessibility audit (contrast, focus states, keyboard navigation)
- [ ] Performance tuning (lazy load images, optimize charts)
