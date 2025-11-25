# GitHub Copilot Instructions - ArchitectJourney Knowledge Base

**Version**: 1.0  
**Last Updated**: November 25, 2025  
**Priority**: MANDATORY - All content creation must follow these rules without exception

---

## 🚫 Zero-Copy Policy (Non-Negotiable)

**CRITICAL**: All educational content must be transformative, not reformative.

❌ **NEVER** copy text verbatim from books, articles, websites, videos, or third-party materials  
❌ **NEVER** mirror a source's outline, section order, headings, or example sequence  
❌ **NEVER** use "light paraphrasing" — must transform completely  
✅ **ALWAYS** create diagrams in Mermaid-first style with ASCII fallback (never embed copyrighted figures)  
✅ **ALWAYS** write fresh, minimal code from first principles  
✅ Brief quotations allowed ONLY with quotation marks and source citation

---

## 🔄 Transformative Workflow (Required Every Time)

**Step-by-step process for creating original educational content**:

1. **Source Intake**: Skim for intent and big ideas; don't copy notes verbatim
2. **Concept Map**: Create fresh outline with different sectioning tailored to ArchitectJourney
3. **Teach Differently**: Use new analogies, scenarios, datasets, use-cases (avoid source examples)
4. **Produce Original Artifacts**: Explanations, Mermaid diagrams (with ASCII fallback), minimal examples
5. **Cross-Link in ArchitectJourney**: Add prerequisites/builds-upon/enables across tracks
6. **Similarity Audit**: Ensure no sentences/structures resemble source
7. **Optional References**: Add "References/Inspired by" links (no copied phrasing)

**Goal**: Create transformative educational content, not just reformative. Entirely new presentation, examples, and explanations that teach the same concepts through original methods.

---

## ⏱️ 25-Minute Learning Segments

✅ **Modular content** designed for focused 25-minute sessions  
✅ **Multi-Part Structure**: Complex topics split into Part 1, Part 2, ... Part N  
✅ **One-Shot Learning**: Each segment complete and actionable within time limit  
✅ **Target Length**: 150 lines of content maximum per response

### ⚠️ CRITICAL: Splitting vs. Trimming Policy

**MANDATORY APPROACH**: When content exceeds 150 lines, **ALWAYS SPLIT** into multiple parts. **NEVER TRIM** or condense content.

**Why Splitting is Required:**
- ✅ **Preserves ALL educational content** - No loss of examples, explanations, or concepts
- ✅ **Maintains learning value** - Each part remains complete and actionable
- ✅ **Better learning experience** - Learners get comprehensive coverage across parts
- ✅ **Follows 25-minute principle** - Each part fits within focused learning session

**Why Trimming is Prohibited:**
- ❌ **Loses educational content** - Examples, explanations, or concepts may be removed
- ❌ **Reduces learning value** - Condensed content may miss important details
- ❌ **Violates zero-copy policy** - If source had comprehensive content, we should preserve it
- ❌ **Poor learning experience** - Learners miss important information

**Splitting Process:**
1. **Identify logical breakpoints** - Split at natural topic boundaries (e.g., "Foundation" → "Implementation" → "Advanced")
2. **Preserve all content** - Move content to appropriate part, don't delete
3. **Maintain completeness** - Each part should be self-contained and complete
4. **Use proper naming** - Follow naming convention: `Part1-A.md`, `Part1-B.md`, etc.
5. **Update references** - Update all file references after splitting

---

## 📋 Required Content Structure

### 5 Required ArchitectJourney Metadata Fields

Every educational content file MUST include:

```yaml
---
learning_level: "Beginner" | "Intermediate" | "Advanced"
prerequisites: ["required knowledge", "prior concepts"]
estimated_time: "25 minutes"  # Standard, adjust if needed
learning_objectives:
  - "Specific, measurable outcome 1"
  - "Specific, measurable outcome 2"
related_topics:
  prerequisites: ["../prerequisite-content/"]
  builds_upon: ["../foundational-content/"]
  enables: ["../advanced-content/"]
  cross_refs: ["../related-domains/"]
---
```

### Numbering Convention

✅ **ALWAYS** use zero-padded numeric prefixes starting at `01_`  
❌ **NEVER** use `00_` prefixes - **NO EXCEPTIONS**  
✅ Keep numbering stable; add new numbers rather than renumbering widely  
✅ Use hyphens for multi-word names: `01_Software-Design-Principles/`

**CRITICAL**: This rule applies to **ALL files** in the repository:
- ✅ Educational content files (`01_Reference/`, `02_Learning/`)
- ✅ Documentation files (`docs/`)
- ✅ Any numbered files anywhere in the repository
- ❌ **NO EXCEPTIONS** - `00_` is NEVER allowed, even for meta/documentation files

### File Naming Convention for Split Files

**CRITICAL**: When files are split into multiple parts, use simplified letter suffixes.

**Pattern**:
- `Topic-Part1-Part1.md` → `Topic-Part1-A.md`
- `Topic-Part1-Part2.md` → `Topic-Part1-B.md`
- `Topic-Part2-Part1.md` → `Topic-Part2-A.md`
- `Topic-Part2-Part2.md` → `Topic-Part2-B.md`

**Rules**:
1. ✅ **Keep first Part number** - First `Part1`, `Part2`, etc. stays as-is
2. ✅ **Convert subsequent Part numbers to letters** - `Part1` → `A`, `Part2` → `B`, etc.
3. ✅ **Use uppercase letters** - A, B, C, D, etc. (not a, b, c)
4. ✅ **Maintain order** - Letters reflect the original Part number sequence

---

## 🎓 Educational Excellence Standards

All content must demonstrate:

- ✅ **Clear objectives and outcomes**: Specific, measurable learning goals
- ✅ **Progressive scaffolding**: Foundations → Practice → Pitfalls → Next Steps
- ✅ **Original examples, datasets, and exercises**: Never reuse source examples
- ✅ **Mermaid-first visuals**: Primary Mermaid diagrams with ASCII fallback for compatibility
- ✅ **Cross-references across tracks**: Development, AI/ML, Data Science, DevOps

---

## 🔗 File Reference Requirements (CRITICAL)

### Mandatory Practices

**CRITICAL**: All file references MUST point to existing files or be clearly marked as planned content.

### When Creating File References

1. ✅ **Verify file exists** before adding reference
2. ✅ **Use exact file names** - match actual file names exactly (including all part suffixes)
3. ✅ **Test references** - run `.\tools\psscripts\Validate-FileReferences.ps1` after adding references
4. ✅ **Update after splitting** - when splitting files, update ALL references to that file immediately

### When Splitting Files

**CRITICAL WORKFLOW**:

1. Create new part files
2. **IMMEDIATELY** run: `.\tools\psscripts\Validate-FileReferences.ps1` to find all references
3. Update ALL references to point to correct part files
4. Run validation again to verify
5. Test navigation manually

---

## 🎯 Interview Preparation Content Guidelines

**CRITICAL**: All interview preparation content in `03_Interview-Prep/` must be **generic and company-agnostic**.

### Generic Content Policy

❌ **NEVER** include company-specific names (Microsoft, Amazon, Google, Meta, etc.)  
❌ **NEVER** reference company-specific frameworks by name (e.g., "Amazon Leadership Principles")  
❌ **NEVER** create company-specific interview scripts or answers  
✅ **ALWAYS** use generic descriptions (e.g., "Leadership Principles", "Clarity–Energy–Success model")  
✅ **ALWAYS** frame content for broad applicability across organizations  
✅ **ALWAYS** focus on universal principles and practices

**Rationale**: Interview prep content should be applicable to any organization, not tied to specific companies. This makes the content more valuable and reusable.

---

## 📁 Content Placement Policy

✅ `Reference/` is EXCLUSIVELY for learning content  
❌ Never mix planning materials, workflow docs, or meta content  
✅ Group logically by learning progression, not source structure  
✅ Place content in correct domain folder (Development/AI-ML/Data-Science/DevOps)

### Source Materials Staging Area

**Location**: `source-materials/` (at repository root, git-ignored)

**Purpose**: **Staging folder for migration** - Temporary staging area where source content is placed before review and transformation into ArchitectJourney educational content.

**Critical Workflow**:

1. **Place materials**: User places source materials (transcripts, notes, documents) in `source-materials/` folder
2. **Review and migrate**: AI assistant reviews content, identifies unique topics, and migrates/transforms following Educational Content Rules
3. **Verify migration**: Confirm all unique content has been migrated to `Reference/` or `Learning/`
4. **Keep source files**: After successful migration, keep source files in `source-materials/` folder - user will delete manually

**Important Notes**:

- ⚠️ **Files in `source-materials/` are NOT required to be compliant** - this is a staging area for raw source content
- ✅ **Review rules apply DURING transformation** - ensure transformation process follows all Educational Content Rules
- ✅ **When user requests migration**: Review ALL files in `source-materials/`, identify unique content, and migrate following Educational Content Rules
- ✅ Files here will be transformed following Educational Content Rules into compliant content
- ✅ After transformation, create compliant content in `Reference/` or `Learning/`
- ✅ **After successful migration**: Keep source files in `source-materials/` folder - user will delete manually
- ❌ **Never commit `source-materials/` content** - it's git-ignored for a reason
- ✅ **Keep `source-materials/` folder** - it's a permanent staging area for future migrations

---

## ✅ Quality Gate Questions (Before Publishing)

**Self-check before finalizing any educational content**:

1. ✅ Is this explanation clearer than the source material?
2. ✅ Does this fit naturally in the learning progression?
3. ✅ Would a learner understand this without the original source?
4. ✅ Are the examples relevant and practical?
5. ✅ Does this content add educational value beyond the reference?
6. ✅ Is this content within 150 lines for effective delivery?

---

**Note**: These instructions align with `.cursor/rules/01_educational-content-rules.mdc` for consistency across Cursor AI and GitHub Copilot.

