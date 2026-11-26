# Update prompt

Paste this into the Vermont Ski Trip project with the new Wanderlog export attached.
Run on Sonnet 5.5, medium effort (first build or a redesign: Opus 5.5 or Fable 5.2, high).

```
Build or update the family trip site for our Vermont ski week (Dec 26, 2026 to Jan 1, 2027) from the attached Wanderlog export.

<context>
Wanderlog is where I plan. The site is a read-only portal for the six people traveling with me, mostly on phones, so it must be quick to scan and never show anything stale or private. It is a single index.html on GitHub Pages (repo: adamevelynlcsw-hash/vermont-2026). All trip content lives in the TRIP data block at the top of that file.
</context>

<instructions>
1. Read the export's date. The newest dated export is the source of truth: where it conflicts with the site, overwrite the site. Where the export says "not specified", keep details the knowledge base or shared calendar supplies (flight numbers and times, both rental vehicles, pickup address).
2. Cross-check against Vermont_Ski_Trip_Knowledge_Base.md and the shared calendar. List every conflict rather than silently picking one.
3. For each place on a dated day, confirm on the web that it is open that date. Add a short heads-up to the item when it is closed or sources disagree.
4. Tag every itinerary item Confirmed, Optional, or Backup/weather. Tag every place "In our plan" (from the export) or "Extra idea" (curated). Extras follow the project's research filters.
5. Edit only the TRIP block and its "updated" date unless I ask for design changes. Push to the repo and confirm the live page loads.
</instructions>

Always include: flights with times, both rental cars, lodging, ski plan, day-by-day itinerary, saved activities and food with listed hours, search across everything, and the Where to eat picker on each day (the `eat` lists: keep them, drop any pick that is closed that date, and add new food places from the export where they fit).
Always exclude: last names, confirmation and loyalty numbers, traveler emails and phone numbers, health notes. Photos come only from Wikipedia/Wikimedia, with a credit link.

If the export has no date, or drops a traveler or a confirmed booking, ask before changing anything.

<output_format>
1. What changed on the site (short list).
2. Conflicts table: Item | Export says | Other source says | What the site shows.
3. The live link.
Under 200 words plus the table.
</output_format>
```
