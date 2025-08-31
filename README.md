# Task_06_Deep_Fake
**Goal.** Turn the Syracuse Women’s Lacrosse 2025 narrative from Task 5 into a short, human-sounding **interview** with two distinct AI voices (Host ↔ Analyst), created entirely with **free tools**. The emphasis is on a transparent, reproducible **process**—from narrative → script → synthesis → assembly—along with ethical disclosure.

> **Disclosure :**  
> This interview is a dramatized, AI-generated piece for academic purposes. Voices are synthetic; no real individuals were recorded. Statistics are based on Syracuse Women’s Lacrosse 2025 data and prior analysis. This work is not affiliated with Syracuse University.

---

## What’s included in this repo

- **Task_6_Interview script.docx** — the finalized, interactive Host↔Analyst dialogue (with the disclosure line up front). This script was adapted directly from the prior season narrative and preserves the key facts, turning them into natural back-and-forth prompts and follow-ups.
- **audio_file_creation_python_script.py** — a self-contained, Colab-friendly script that uses free text-to-speech to synthesize each line, then stitches clips into a single MP3 with natural pauses and normalized levels. No paid API keys required. 
- **AI Audio Interview.mp3** — the finished two-voice interview export.

---

## Task summary (what I set out to do)

1. **Transform the narrative into dialogue.**  
   I converted the season summary and insights into a concise Q&A between a curious Host and a data-savvy Analyst—keeping numbers accurate, writing them in words for clearer TTS pronunciation, and adding “human” touches (quick follow-ups, reactions, and a brief lightning round). 

2. **Generate two distinct AI voices using free tools.**  
   I used a free text-to-speech workflow to synthesize **each line** separately—one voice for **Host**, another for **Analyst**—so pacing feels conversational. The Python script automates synthesis and file naming to keep clips organized. :contentReference

3. **Assemble and polish the final audio.**  
   After synthesis, the script **normalizes** loudness and stitches clips with ~650–700 ms pauses for a natural cadence. It then exports a single **MP3** for listening/grading. Optional enhancements (e.g., a very soft music bed) are documented but not required. 

4. **Document the process and ethics.**  
   The repo explains tooling choices, the reasoning behind per-line synthesis, and the importance of a **spoken disclosure** at the start of the interview.

---

## Process (step-by-step, no code)

**A. Script development (from narrative to interview)**  
- Start with the Task 5 narrative and key stats (games played, record, close losses, top performers, standout games, and coaching levers).  
- Rewrite as a **dialogue**: short Host questions, direct Analyst answers with one key stat + one implication.  
- Place the disclosure as the **first spoken line**.  
- Spell out numbers (“nineteen”, “ten-and-nine”) and add light phonetic hints for tricky names if needed. 

**B. Two-voice synthesis (free TTS)**  
- Choose two voices (e.g., warm/energetic for Host; calm/analytical for Analyst).  
- Run the provided Python script (in Colab or locally) to **batch-synthesize each line** into separate audio clips; this makes timing and edits easier. 

**C. Assembly & export**  
- Automatically **normalize** levels and insert brief pauses between clips to create a realistic conversational rhythm.  
- Export a single **MP3** (the included “AI Audio Interview.mp3”).
  
**D. Quality checks**  
- Listen for pacing and pronunciation; if it’s too fast/slow, adjust the pause length and/or split long sentences.  
- Re-synthesize only the lines that need fixes, then re-stitch.

**E. Optional polish**  
- Add a very low music bed if desired (keep it subtle so it never masks the voices).  
- For a stretch goal, animate an avatar or talking head with free lip-sync tools and overlay the interview audio.

---

## Why these choices?

- **Per-line synthesis** produces cleaner pacing than one long TTS blob, and it lets you re-record only the lines that need adjustments.
- **Numbers in words** improve clarity for TTS engines, especially with sports scores.
- **Short Q&A** segments keep the interview punchy while ensuring every claim maps back to the original narrative/analysis.

---

## Ethics & disclosure

- The piece is fully **AI-generated**; this is explicitly documented here.  
- No impersonation of real individuals; the “Analyst” is a **generic** AI voice.  
- Stats are derived from the Syracuse Women’s Lacrosse 2025 analysis used in Task 5; claims in the dialogue reflect that source material. :contentReference[oaicite:11]{index=11}

---

## How to reproduce (high-level)

1. Open the provided script in a free, hosted environment (e.g., Google Colab).  
2. Paste/update your dialogue (if you change lines).  
3. Choose two voices, run the synthesis, and export the MP3.  
4. Listen, tweak pauses or wording if needed, and re-export.
