# Task_06_Deep_Fake

**Goal.** Turn the Syracuse Women’s Lacrosse 2025 narrative from Task 5 into a short, human-sounding **interview** with two distinct AI voices (Host ↔ Analyst) created entirely with **free tools**. Emphasis is on a transparent, reproducible **process**—from narrative → script → synthesis → assembly along with clear ethical disclosure.

> **Disclosure**  
> This interview is a dramatized, AI-generated piece for academic purposes. Voices are synthetic; no real individuals were recorded. Statistics are based on Syracuse Women’s Lacrosse 2025 data and prior analysis. This work is not affiliated with Syracuse University.

---

## Final Deliverables

- **Task_6_Interview script.docx** — final interactive Host ↔ Analyst script with the disclosure as the first spoken line; adapted directly from the Task 5 narrative to keep every claim grounded in validated stats.  
- **Workflow document.docx** — step-by-step process write-up (approach, tools, failures, decisions, and QA) to prioritize “process over product.”  
- **audio_file_creation_python_script.py** — Colab-friendly script that synthesizes each line with two free voices, inserts natural pauses, normalizes loudness, and exports a single MP3 (no paid API keys).  
- **download.mp3** — final two-voice interview audio export.

---

## Task Summary (what I set out to do)

1. **Transform the narrative into dialogue**  
   Converted the season summary and insights into a concise Q&A between a curious **Host** and a data-savvy **Analyst**. Wrote numbers as words for better TTS (e.g., “nineteen,” “ten-and-nine”) and added small “human” touches—quick follow-ups, reactions, and a short lightning-round.

2. **Generate two distinct AI voices using free tools**  
   Used a fully free text-to-speech workflow to synthesize **each line** separately—one voice for **Host**, another for **Analyst**—so pacing feels conversational and line-level fixes are easy. The provided script automates file naming and organization.

3. **Assemble and polish a single audio file**  
   After synthesis, normalized loudness and stitched clips with ~650–700 ms pauses to emulate natural turn-taking, then exported a single **MP3** for review and grading.

4. **Document the process and ethics**  
   Captured tooling choices, why per-line synthesis was used, common pitfalls (runtime/async and pronunciation), and kept a **spoken disclosure** up front.

---

## Tools Used (all free)

- **Google Colab** — hosted environment to run the workflow without local setup.  
- **edge-tts** — neural text-to-speech with multiple voices (no API key).  
- **pydub** + **FFmpeg** — simple audio assembly (concatenate, insert pauses, normalize, export).  

---

## Process (step-by-step, no code)

**A. Script development (from narrative to interview)**  
- Start with Task 5’s validated stats (record, closest game, largest win, top scorers/playmaker, narrow losses, shots→goals correlation).  
- Rewrite as a **dialogue**: short Host questions; direct Analyst answers with one key stat **plus one implication**.  
- Put the **disclosure** as the **first spoken line**.  
- Spell out numbers and simplify long sentences; add light phonetic hints for tricky names if needed.

**B. Two-voice synthesis (free TTS)**  
- Choose two contrasting voices (e.g., warm/energetic Host; calm/analytical Analyst).  
- Use the provided script to **batch-synthesize each line** into separate clips; this keeps timing natural and makes re-takes fast.

**C. Assembly & export**  
- Normalize levels and insert ~650–700 ms pauses between lines to create a realistic cadence.  
- Export a single **MP3**.

**D. Quality checks**  
- **Cadence:** adjust pause length if it feels rushed or draggy.  
- **Clarity:** fix any mispronunciations by rewriting the line (numbers as words, light phonetics).  
- **Facts:** confirm every spoken claim still matches the validated numbers.  
- Re-synthesize only the lines that need fixes, then re-stitch and re-export.


---

## Why These Choices

- **Per-line synthesis** gives cleaner pacing than one long TTS pass and lets you re-record only the lines that need changes.  
- **Numbers written as words** significantly improve TTS clarity—especially for scores and dates.  
- **Short Q&A segments** keep the interview punchy while ensuring every claim traces back to the original analysis.

---

## Ethics & Disclosure

- The piece is fully **AI-generated** and begins with a **spoken disclosure**.  
- No impersonation of real individuals. The **Analyst** is a generic voice/persona.  
- All spoken stats reflect the Syracuse Women’s Lacrosse 2025 analysis

---

## Reproducibility (high-level)

1. Open the script in a free, hosted environment (e.g., Colab).  
2. Update dialogue if needed; keep disclosure first.  
3. Select two voices; run synthesis to create per-line clips.  
4. Normalize, insert pauses, and export a single MP3.  
5. Listen, tweak wording/pauses if needed, and re-export.

---

## Lessons Learned & Future Improvements

**Lessons:** 
- Per-line synthesis speeds iteration
- Short sentences and spelled-out numbers improve naturalness
- Small pause adjustments (±100–150 ms) dramatically improve human feel
- Light normalization is usually enough

**Next steps:** 
- Try light SSML for emphasis and micro-pauses
- Gentle compression/limiting for a broadcast finish
- Audition more voice pairs for tone
- Create a simple video variant with subtitles for accessibility
