# Client session: personality test to professions

**Trigger**
"new client", "client is here", "score this test", "here are the answers", "what's their personality type", "match strengths to careers"

**Goal**
Turn a client's questionnaire answers into a personality type, strengths and weaknesses, and a reviewed list of suited professions.

**Inputs**
- The client's completed written questionnaire (usually a high school student). Test used: Big Five/OCEAN by default, or Myers-Briggs, DISC, Enneagram if I say so.
- Weighted scoring key for that test. If none exists, stop and say so.

**Steps**
1. Check every question has a clear answer. If any are blank, unclear or the client seemed confused, list them and stop. Do not score a gappy test.
2. Add up the weighted scores per trait (for OCEAN: openness, conscientiousness, extraversion, agreeableness, emotional sensitivity). No need to ask me before doing this.
3. Assign the personality type or trait profile from the scores.
4. Write the strengths and weaknesses that follow from the profile.
5. Map strengths to professions: which strengths suit which professions, and why. This mapping is the critical step.
6. Draft the client report in my voice (warm, brief, plain words for a teenager and their parents).
7. Give me everything to review. Mark anything researched or guessed.

**Output**
A draft saved in `clients/`, named `<client code>_<yyyymmdd>.md`, e.g. `c001_20261006.md`. The date is the day the client came in. Contains: scores, personality type, strengths and weaknesses, suggested professions. Nothing is sent to the client.

**Standing rules**
- I review and edit before anything reaches the client.
- Identify clients by code only. New client: give the next code and add a row to private/client-key.md. Never put real names, initials, schools or contact details in clients/ files.
- Filenames: code, underscore, date as yyyymmdd. This gives me a timeline. No full names or contact details in anything public.
- Colleges, courses and lenders are NOT part of this session; they come next sitting.
- Good session: every answer clear and complete. Bad session: missing, unclear or confused answers.
