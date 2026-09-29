# DOCX Assembly Plan

## Verified order

1. Title page
2. Approval page
3. Certification
4. Dedication
5. Acknowledgements
6. Table of Contents
7. Abstract
8. Chapter One
9. Chapter Two
10. Chapter Three
11. Chapter Four
12. Chapter Five
13. Bibliography

This order is listed in the inherited project manuscript. Whether items 2–5 are mandatory remains subject to the front-matter decisions below. The substantive heading structure must match `research-bible/03-table-of-contents.md` exactly.

## Inspection method

Both DOCX files were inspected through their actual Word paragraph/run properties and OOXML parts, including `document.xml`, `styles.xml`, `settings.xml`, `footnotes.xml`, section properties, and header/footer relationships. Rules below are not inferred solely from extracted text.

## Formatting evidence and working rules

| Item | Departmental precedent | Inherited project manuscript | Agreement | Clear enough for working rule? | Human confirmation still required? |
|---|---|---|---|---|---|
| Page size | 8.5 × 11 inches | 8.5 × 11 inches | Yes | Yes: US Letter | No |
| Margins | One inch on all sides; header/footer distance 0.5 inch | Same | Yes | Yes | No |
| Body font | Times New Roman 12 point dominates substantive runs | Times New Roman 12 point in supplied prose/abstract | Yes | Yes: Times New Roman 12 point | No |
| Body alignment | Justified | Supplied prose and abstract justified | Yes | Yes: justified | No |
| Body line spacing | Double spacing explicitly applied to substantive paragraphs | Abstract uses double spacing; completed chapter body is absent | Substantial agreement | Yes: double-spaced body | No for working rule |
| First-line indentation | Substantive precedent paragraphs generally have no first-line indent | Abstract paragraphs use a 0.5-inch first-line indent; completed chapter body is absent | No/insufficient comparison | No | Yes |
| Paragraph spacing | Mixed zero and 5-point before/after values because of inconsistent imported styles | Similarly mixed style defaults | No stable rule | No | Yes |
| Footnote form | 146 genuine Word footnotes | No populated footnotes; only an empty footnote placeholder part | No contradiction | Yes: genuine Word footnotes | No |
| Footnote font and size | Direct OOXML formatting shows Times New Roman 9 point | No populated note for comparison | Precedent only | Yes: Times New Roman 9 point as working rule | No for working rule |
| Footnote spacing/indentation | No sufficiently consistent departmental rule recoverable | No evidence | Insufficient | No | Yes |
| Page-number field and position | No `PAGE` field in body, header, or footer; one section only | Same | Yes as absence only | No convention established | Yes |
| Preliminary Roman numbering | No `w:pgNumType`; no separate front-matter section | Same | Yes as absence only | No convention established | Yes |
| Arabic restart for main text | No numbering restart or separate section | Same | Yes as absence only | No convention established | Yes |
| Chapter starts | No reliable manual page-break or page-break-before pattern | Full chapter text is absent | Insufficient | No | Yes |
| Heading hierarchy | Major headings are generally bold/uppercase, but style and alignment vary | TOC and abstract headings provide only partial evidence | Partial | Black bold headings are supportable; exact hierarchy is not | Yes for sizes, alignment, and chapter-title layout |
| Bibliography organization | One undivided alphabetical bibliography | Separate “Primary Sources” and “Secondary Sources” headings | No | No | Yes |
| Bibliography indentation/spacing | Justified entries; no consistently encoded hanging indent | Mostly justified; embedded tabs and one anomalous negative indent | No reliable agreement | Alphabetization only | Yes |
| Citation-style extensions | Journal/article notes exist but are inconsistent and incomplete | No populated notes demonstrating extensions | Insufficient | Project convention remains provisional | Yes |

## Front-matter evidence

| Item | Departmental precedent | Inherited project manuscript | Agreement | Clear enough for working rule? | Human confirmation still required? |
|---|---|---|---|---|---|
| Title page | Group title page with title, authorship, institution, course, lecturer, and November 2025 | Individual title page with approved title, Maxwell Chimaobi Ngwu, institution, and June 2026 | Structural agreement only | Yes: retain inherited individual-project structure and verified identity | Yes for final month/year |
| Approval page | Absent | Listed in TOC; no page text | No usable wording | No | Yes: supply wording/signatories or confirm omission |
| Certification | Absent | Listed in TOC; no page text | No usable wording | No | Yes: supply wording/signatories or confirm omission |
| Dedication | Absent | Listed in TOC; no text | No usable wording | No | Yes: supply text or confirm omission |
| Acknowledgements | Absent | Listed in TOC; no text | No usable wording | No | Yes: supply text or confirm omission |
| Table of contents | Manually typed list without page fields | Manually typed approved outline without page fields | Yes as content type | Yes: use actual heading styles and a generated TOC | No for mechanism; numbering convention remains unresolved |
| Abstract | Present | Present | Yes | Yes: include the verified final abstract | No |
| Final submission date | November 2025 | June 2026 | No | No | Yes |

## Section and field design after decisions

- Create front-matter pages only from researcher-supplied or expressly approved text.
- Separate front matter from main text with a Word section break only after the pagination convention is confirmed.
- Do not assign Roman or Arabic numbering until the starting number, visibility, position, and restart rule are confirmed.
- Apply Word heading styles to the approved hierarchy without changing heading text.
- Convert all 89 Markdown notes into native `word/footnotes.xml` footnotes using Times New Roman 9 point, subject to confirmation of note spacing and indentation.
- Insert a Word TOC field after headings are styled and update it in Word before review.

## Remaining stop-condition decisions

Human confirmation or supplied text is still required for:

- whether approval, certification, dedication, and acknowledgements are mandatory;
- exact approval/certification wording and signatory titles;
- dedication and acknowledgement text;
- final submission month/year;
- body first-line indentation and paragraph spacing;
- footnote spacing and indentation;
- page-number presence, location, visible starting page, numeral style, and main-text restart;
- chapter-start convention and exact heading sizes/alignment;
- bibliography division and exact indentation/spacing;
- departmental approval of the working journal, chapter, institutional, and web citation extensions.

DOCX assembly remains paused. No missing institutional wording or formatting rule will be invented.
