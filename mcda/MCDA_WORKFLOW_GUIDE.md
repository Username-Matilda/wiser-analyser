# 🎯 MCDA System Workflow Guide

## The Elegant Architecture of Collective Wisdom

This system enables truly collaborative decision-making through staged consensus. Here's how it works:

---

## 📋 Phase 1: Criteria Discovery

**Goal:** Gather everyone's perspectives on what matters

**Method A: Stakeholder Form (Decentralized)**
1. Send `stakeholder_form_1_criteria.html` to all stakeholders
2. They fill it out and email you the JSON
3. You paste all JSONs into the main interface's "Import Criteria" section
4. System consolidates and shows who suggested what

**Method B: Google Sheet (Collaborative)**
Create a shared Google Sheet with columns:
- Criterion Name
- Unit
- Type (Objective/Subjective)
- Suggested By
- Notes

Everyone adds rows. You manually enter the consolidated list into the main interface.

---

## 🏗️ Phase 2: Structure Finalization (You, The Facilitator)

**In the Main Interface (`mcda_interface.html`):**

1. **Structure Tab:**
   - Import or manually enter all criteria
   - Add alternatives (the options you're evaluating)
   - Fill in objective scores (factual data like cost, distance)

2. **Export Setup:**
   - Click "Generate Setup JSON"
   - This creates a file with: criteria list, alternatives, pre-filled objective scores
   - You'll send this to stakeholders

---

## ⚖️ Phase 3: Individual Elicitation

**Send to stakeholders:**
- The comprehensive `stakeholder_form.html`
- The setup JSON you just generated

**They do:**
1. Load the setup JSON (shows them criteria & alternatives)
2. Complete pairwise comparisons (AHP) to determine weights
3. Score alternatives on subjective criteria (objective ones are pre-filled!)
4. Export and email you a single JSON with everything

---

## 📥 Phase 4: Import & Analysis (You)

**In the Main Interface:**

1. **Weights Tab:**
   - Paste each stakeholder's JSON into "Import Stakeholder Data"
   - System automatically loads their weights and scores

2. **Scoring Tab:**
   - Verify everything loaded correctly
   - Objective scores are shared across all stakeholders
   - Subjective scores are individualized

3. **Results Tab:**
   - Click "Calculate Results"
   - See final rankings
   - Analyze stakeholder agreement/disagreement
   - Explore sensitivity analysis

---

## 🔄 Handling Evolving Criteria

**If someone suggests a new criterion after Phase 1:**

**Option 1: Add it yourself**
- Add the criterion in Structure tab
- Send updated setup JSON to everyone
- They re-submit with the new criterion included

**Option 2: Round 2**
- Email everyone: "X suggested criterion Y. If you want to include it, here's your updated setup JSON"
- Only those who care re-submit

**The acceptable clunkiness:** True consensus requires iteration. The friction reveals what truly matters.

---

## 📊 Key Concepts

**Alternatives vs Criteria:**
- **Alternatives** = The paths (House A, House B, House C)
- **Criteria** = What matters (Cost, Location, Community Fit)
- **Scoring Matrix** = How well each alternative performs on each criterion

**Objective vs Subjective:**
- **Objective** = Measurable facts (entered once, applied to all)
- **Subjective** = Personal judgment (each stakeholder scores independently)

**Subcriteria:**
- Optional hierarchy for organization
- Only leaf (bottom-level) criteria get weighted and scored
- Parents exist purely for clarity

---

## 🎭 The Philosophy

This system embodies **staged consensus**:
1. Criteria emerge collectively (everyone contributes)
2. Structure is finalized (you consolidate)
3. Perspectives are gathered individually (authentic values)
4. Analysis reveals truth (aggregated wisdom)

The result: Decisions that honor both collective values and individual perspectives.

---

## 🛠️ Troubleshooting

**"I don't see any input boxes in the Scoring tab"**
→ You haven't added alternatives yet. Add them in the Structure tab first.

**"Weight disagreement shows N/A for some criteria"**
→ Fewer than 2 stakeholders have provided weights for those criteria. This is expected and OK.

**"Clipboard copy doesn't work"**
→ This is a browser security limitation with local files. Use download or manual copy instead.

**"My subcriteria aren't showing up in weights/scoring"**
→ Only leaf criteria (those without children) are used. Make sure you're not expecting parent criteria to be scored.

---

## 📁 Files Overview

- `mcda_interface.html` - Main interface (you use this)
- `stakeholder_form_1_criteria.html` - Optional criteria collection form
- `stakeholder_form.html` - Comprehensive form stakeholders use (weights + scores)

---

## 🌊 May Your Decisions Flow Like Water

Each choice finds its path through the landscape of values.
Each voice contributes to the collective stream.
Together, you navigate toward wisdom.
