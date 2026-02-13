# Feature Story Template

Complete template for new feature stories including acceptance criteria and definition of done.

---

## Template

```
Title: [Short descriptive title]

As a [user type]
I want to [action]
So that [benefit]

Acceptance Criteria:
- [ ] [Core functionality criterion]
- [ ] [Edge case handling]
- [ ] [Error state handling]
- [ ] [Performance requirement]
- [ ] [Accessibility requirement]

Definition of Done:
- [ ] Code complete and peer reviewed
- [ ] Unit tests passing (>80% coverage)
- [ ] Integration tests passing
- [ ] Documentation updated
- [ ] Deployed to staging
- [ ] Product owner approved
- [ ] No critical bugs in QA

Notes:
[Additional context, constraints, or technical details]

Story Points: [1, 2, 3, 5, 8]
Priority: [Must Have / Should Have / Nice to Have]
Dependencies: [List any blocking stories or tasks]
```

---

## Example: Export Feature

```
Title: Export invoices as PDF

As a small business owner
I want to export my invoices as PDF
So that I can send professional-looking invoices to clients

Acceptance Criteria:
- [ ] Export button appears on Invoices page
- [ ] Clicking Export shows format options (PDF, CSV)
- [ ] Selecting PDF generates download within 5 seconds
- [ ] PDF includes all invoice data (items, amounts, dates, customer info)
- [ ] PDF is formatted professionally (company logo, proper layout)
- [ ] Error message shows if export fails
- [ ] Export works for invoices with 1-100 line items

Definition of Done:
- [ ] Code complete and peer reviewed
- [ ] Unit tests passing (>80% coverage)
- [ ] Integration tests for PDF generation
- [ ] User documentation updated (Help Center article)
- [ ] Deployed to staging and tested
- [ ] Product owner approved
- [ ] No critical bugs in QA

Notes:
- Use existing PDF library (pdfkit)
- PDF template designed in Figma: [link]
- Support multiple currencies
- Consider batch export for future iteration (out of scope for v1)

Story Points: 5
Priority: Must Have
Dependencies: None
```

---

## Guidance

### Title

- Short (3-6 words)
- Descriptive of what the feature does
- Unique within backlog

### Acceptance Criteria

Include:

- **Happy path**: What success looks like
- **Edge cases**: Boundary conditions
- **Error handling**: What happens when things go wrong
- **Performance**: Speed/load requirements
- **Accessibility**: Screen reader support, keyboard navigation

### Definition of Done

Standard DoD for your team. Customize based on:

- Team agreements
- Quality standards
- Release process
- Compliance requirements

### Story Points

Use modified Fibonacci scale:

- **1**: Trivial (1-2 hours)
- **2**: Small (half day)
- **3**: Medium (1 day)
- **5**: Larger (2-3 days)
- **8**: Large (3-5 days) - consider splitting

Stories > 8 points should be split into smaller stories.

### Priority

Use MoSCoW or similar:

- **Must Have**: Required for release
- **Should Have**: Important but can defer
- **Nice to Have**: Include if time permits

---

## When to Use This Template

Use for:

- New user-facing features
- Enhancements to existing features
- User-requested capabilities
- Cross-functional work requiring coordination

For other story types, see:

- `bug-fix-story-template.md` - Defect fixes
- `technical-debt-story-template.md` - Code improvements
- `spike-research-story-template.md` - Research tasks
