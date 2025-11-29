# AI Governance Framework: The Zero-to-One Guide (v3.0)

## 1. The Philosophy: Context is King
In AI-assisted coding, the bottleneck is **specifying** code, not writing it. An AI agent is only as good as its context.
- **Vague Context** = Vague, buggy code.
- **Governance Suite** = Production-ready software.

This framework is a **"Generator of Generators."** It guides you through creating the standard "Context Stack" (8 specific artifacts) that turns a simple idea into a robust application with 95%+ AI success rates.

### The "Project-Specific Intelligence" Rule
Generic templates produce generic apps. To achieve 99% comprehensiveness, this framework forces the AI to generate **Domain-Specific Patterns** (e.g., a "Timer Pattern" for a meditation app) rather than just standard boilerplate.

---

## 2. The Artifact Suite
You will generate these 8 artifacts in order.

### Layer 1: The Foundation (What & How)
1.  **`PRODUCT_SPEC.md`**: Features, User Personas, State Machines.
2.  **`SYSTEM_ARCHITECTURE.md`**: Data Models, API Contracts, Error Handling.
3.  **`DESIGN_SYSTEM.md`**: Colors, Typography, **Implementation Logic**.
4.  **`CONTENT_REPOSITORY.md`**: All app copy (strings, prompts).

### Layer 2: The Rules (Constraints)
5.  **`ENGINEERING_STANDARDS.md`**: File structure, naming conventions.
6.  **`CODE_TEMPLATES.md`**: Proven patterns + **Domain-Specific Patterns**.
7.  **`DEVELOPMENT_PHASES.md`**: Build order + **Context Scoping** (Active/Ignored Context).

### Layer 3: The Process (Orchestration)
8.  **`AI_WORKFLOW.md`**: The runbook with specific prompts for each phase.

---

## 3. The Generation Workflow
Follow these phases to generate the suite.

### Phase 0: Bootstrap (The Master Prompt)
**Goal**: Prime the AI with the Governance Philosophy.
**Action**: Paste this into a fresh AI session.

> **Prompt**:
> "You are an expert Software Architect specializing in AI-driven development. I want to build a new application. We will not write code yet. First, we must generate a 'Governance Suite' of 8 artifacts that will guide the coding AI.
>
> The Suite consists of:
> 1. `PRODUCT_SPEC.md` (Requirements & State Machines)
> 2. `SYSTEM_ARCHITECTURE.md` (Data Models & APIs)
> 3. `DESIGN_SYSTEM.md` (UI Rules & Component Logic)
> 4. `CONTENT_REPOSITORY.md` (Text Assets)
> 5. `ENGINEERING_STANDARDS.md` (File Structure)
> 6. `CODE_TEMPLATES.md` (Implementation & Domain Patterns)
> 7. `DEVELOPMENT_PHASES.md` (Build Order & Context Scoping)
> 8. `AI_WORKFLOW.md` (Prompts for the Builder AI)
> 9. `AI_CHECKLIST.md` (Quality Control & Pitfalls)
>
> Acknowledge if you understand this goal. Wait for my product idea."

---

### Phase 1: Expansion (Idea → Spec)
**Goal**: Turn your rough idea into a detailed specification with implementation logic.
**Input**: Your idea (e.g., "A mindful app that pauses social media").

> **Prompt**:
> "Here is my product idea: [INSERT IDEA].
>
> Act as a Product Manager & UI Engineer. Expand this into a `PRODUCT_SPEC.md`.
> Requirements:
> 1. **User Personas**: Define 2 core personas.
> 2. **Functional Requirements**: List features with IDs (REQ-01).
> 3. **State Machines**: Define the exact states for key flows (e.g., Onboarding: Welcome -> Form -> Success).
> 4. **UI Rules**: Extract all visual requirements (colors, fonts) into a separate `DESIGN_SYSTEM.md`.
>    - **CRITICAL**: For complex components (e.g., Timers, Graphs), provide **Implementation Logic** or **SwiftUI Code Snippets** in `DESIGN_SYSTEM.md`, not just visual descriptions.
> 5. **Content**: Extract all text (titles, buttons, error messages) into `CONTENT_REPOSITORY.md`."

**Output**: `PRODUCT_SPEC.md`, `DESIGN_SYSTEM.md`, `CONTENT_REPOSITORY.md`

---

### Phase 2: Technical Design (Spec → Architecture)
**Goal**: Derive the technical blueprint and build strategy.
**Input**: `PRODUCT_SPEC.md`

> **Prompt**:
> "Act as a System Architect. Analyze the `PRODUCT_SPEC.md`.
>
> 1. **Data Modeling**: Identify every noun that needs persistence. Create `SYSTEM_ARCHITECTURE.md` with exact SwiftData/CoreData schemas, including fields and relationships.
> 2. **API Contracts**: Define the Service protocols needed to handle business logic (e.g., `protocol AuthService`).
> 3. **Error Handling**: Define specific error enums and handling strategies.
> 4. **Phasing**: Break the build into logical phases (Foundation -> Core Features -> Polish) and write `DEVELOPMENT_PHASES.md`.
>    - **CRITICAL**: For EACH phase, define the **Active Context** (files the AI *must* read) and **Ignored Context** (files the AI *must* ignore) to prevent context window pollution."

**Output**: `SYSTEM_ARCHITECTURE.md`, `DEVELOPMENT_PHASES.md`

---

### Phase 3: Standardization (Stack → Rules)
**Goal**: Define *how* the code should be written, including domain-specific patterns.
**Input**: Your Tech Stack (e.g., "SwiftUI, MVVM, SwiftData").

> **Prompt**:
> "Act as a Lead Engineer. We are using [INSERT TECH STACK].
>
> 1. **Standards**: Create `ENGINEERING_STANDARDS.md`. Define the exact file structure (e.g., `Core/Feature/View.swift`) and naming conventions.
> 2. **Templates**: Create `CODE_TEMPLATES.md`.
>    - **Standard Patterns**: Write production-ready boilerplate for ViewModel, View, Service, Data Model.
>    - **CRITICAL - Domain Patterns**: Analyze `PRODUCT_SPEC.md` and create **Domain-Specific Patterns** for unique features. (Example: If there is a Timer, create a 'Timer Pattern'; if there is a Wizard Flow, create a 'State Machine Pattern')."

**Output**: `ENGINEERING_STANDARDS.md`, `CODE_TEMPLATES.md`

---

### Phase 4: Orchestration (Context → Workflow)
**Goal**: Create the instructions for the Builder AI, anticipating failure modes.
**Input**: All previous artifacts.

> **Prompt**:
> "Act as an Engineering Manager. Create `AI_WORKFLOW.md`.
>
> Structure this document as a series of 'Copy-Paste Prompts' for the Builder AI.
> For EACH phase in `DEVELOPMENT_PHASES.md`:
> 1. Define a 'Universal Context Block' that lists the specific Governance files to read.
> 2. Write a specific Task Prompt that instructs the AI to implement that phase using the `CODE_TEMPLATES.md`.
>

**Output**: `AI_WORKFLOW.md`

---

## 4. Artifact Structure Definitions (Enhanced)
Ensure your generated artifacts contain these specific sections **with the depth and detail standards** specified below.

### 1. PRODUCT_SPEC.md

**Minimum Content Requirements**:
- **200+ lines** for MVP projects
- **15-30 functional requirements** with IDs (REQ-XXX-NN format)
- **At least 1 complete state machine** for primary user flow
- **2-3 user personas** with motivations and pain points

**Required Sections**:
1. **Introduction**: Project name, version, status, brief summary
2. **User Personas**: Name, description, pain points, goals, behaviors
3. **Functional Requirements**: Organized by module (3.1, 3.2, 3.3...)
   - Each requirement: Clear ID, description, acceptance criteria
4. **State Machine Specifications** (CRITICAL):
   - Swift enum definition with all cases and properties
   - Navigation rules table (forward/back/skip/dismiss policies)
   - Data persistence mapping table (what data, where stored, when)
   - Interruption handling scenarios (app backgrounds, force quit)
   - Completion triggers and state transitions
5. **Non-Functional Requirements**: Privacy, performance, reliability metrics
6. **Success Metrics**: KPIs with target values

**Detail Level Standards**:
- ❌ INSUFFICIENT: "Display a countdown timer"
- ✅ GOOD: "Display a circular countdown timer with seconds remaining"
- ✅ EXCELLENT: "Display a circular countdown timer per `DESIGN_SYSTEM.md` Section 5.1 with exact button states per Section 3.3.1, recording UsageStat per `SYSTEM_ARCHITECTURE.md` Section 4.3.2"

**Cross-Reference Patterns**:
- Reference other governance docs: `` `governance/DESIGN_SYSTEM.md` ``
- Reference specific sections: `` `CONTENT_REPOSITORY.md` Section 2.1 ``
- Reference implementation: `` See `SYSTEM_ARCHITECTURE.md` Section 3.2.1 for exact schema ``

---

### 2. SYSTEM_ARCHITECTURE.md

**Minimum Content Requirements**:
- **300+ lines** for MVP projects
- **Complete Swift code schemas** for all data models (not just descriptions)
- **Service protocol definitions** with exact method signatures
- **Error scenario tables** with cause/detection/mitigation

**Required Sections**:
1. **System Overview**: Architecture pattern (MVVM, MVC, etc.), dependencies
2. **Architectural Pattern**: Detailed explanation of chosen pattern
3. **Data Architecture**:
   - Persistence layer strategy (SwiftData, CoreData, UserDefaults)
   - Data model schemas with **complete Swift code**
   - Data flow diagrams or descriptions
   - **Data seeding strategy** with exact implementation
4. **Component Design**: Module breakdown (Hub, Gateway, Onboarding, etc.)
5. **Services**: 
   - Service API contracts with **complete protocol definitions**
   - Exact method signatures, parameters, return types
   - Implementation requirements and constraints
6. **Error Handling & Failure Modes**:
   - Critical error scenarios (5-10 scenarios minimum)
   - Each with: Trigger, Detection, User Message, Action, Mitigation
   - Error enum definitions
7. **Security & Privacy**: Data storage, permissions, third-party services
8. **Deployment**: Target OS versions, device support

**Detail Level Standards**:
- ❌ INSUFFICIENT: "Create a UserSettings model"
- ✅ EXCELLENT: Complete Swift code with `@Model`, properties, types, init methods

**Cross-Reference Patterns**:
- Reference requirements: `` Implements `PRODUCT_SPEC.md` Section 3.2 ``
- Reference by section: `` See Section 3.4.1 for seeding logic ``

---

### 3. DESIGN_SYSTEM.md

**Minimum Content Requirements**:
- **100+ lines** for MVP projects
- **At least 1 implementation snippet** for complex components
- **Complete color palette** with exact values
- **Typography scale** with font sizes and weights

**Required Sections**:
1. **Color Palette**: Primary, secondary, semantic colors with exact values
2. **Typography**: Font families, sizes, weights, line heights
3. **Components**: Button styles, cards, inputs with exact specs
4. **Iconography**: Icon library and usage guidelines
5. **Custom Components** (CRITICAL):
   - **Visual specifications**: Size, colors, stroke widths, animations
   - **Implementation approach**: SwiftUI code snippets or detailed pseudocode
   - **Timer logic**: If applicable, exact implementation pattern
   - **Animation requirements**: Duration, easing, triggers

**Detail Level Standards**:
- ❌ INSUFFICIENT: "Use a circular timer"
- ✅ EXCELLENT: Complete SwiftUI snippet with `Circle().trim()`, rotation, animation

**When to Include Code**:
- Complex custom components: YES (circular timers, charts, custom animations)
- Standard components: NO (just specs like "corner radius: 12")
- Layout logic: SOMETIMES (if complex state-driven layout)

---

### 4. CONTENT_REPOSITORY.md

**Minimum Content Requirements**:
- **40+ lines** minimum
- **All UI copy** categorized by module/screen
- **Error messages** for all error scenarios
- **Table format** for structured content (e.g., onboarding steps)

**Required Sections**:
1. **Onboarding Content**: All step titles, descriptions, button labels
2. **UI Copy**: Organized by screen/module
3. **Quotes/Dynamic Content**: If applicable, complete list with authors
4. **Error Messages**: All user-facing error messages
5. **Success Messages**: Confirmations, toasts, celebrations

**Format Standards**:
- Use tables for multi-field content (onboarding steps with title/description/button)
- Use numbered lists for quotes/content libraries
- Group by module/feature, not by type

---

### 5. ENGINEERING_STANDARDS.md

**Minimum Content Requirements**:
- **50+ lines** minimum
- **File structure tree** showing exact folder organization
- **Naming conventions** for files, classes, variables
- **Git workflow** and commit message format

**Required Sections**:
1. **Code Style & Conventions**: Language-specific idioms
2. **Naming**: Types (PascalCase), properties (camelCase), files
3. **File Organization**: Feature-first or layer-first with examples
4. **Git Workflow**: Branching strategy, commit message format
5. **Testing Strategy**: Unit tests scope, UI tests scope
6. **Definition of Done**: Checklist for task completion

---

### 6. CODE_TEMPLATES.md

**Minimum Content Requirements**:
- **600+ lines** for comprehensive coverage
- **Standard templates**: ViewModel, View, Service, Data Model (4 minimum)
- **3-5 domain-specific patterns** unique to your project
- **8+ common mistakes** with ❌ wrong and ✅ correct examples
- **Complete code blocks** (not pseudocode) that can be copied

**Required Sections**:
1. **How to Use This Document**: Instructions for AI/developers
2. **ViewModel Pattern**: Complete template with @Observable
3. **SwiftUI View Pattern**: Complete template with proper state management
4. **Service Pattern**: Singleton template
5. **SwiftData Operations**: Query, insert, update, delete patterns
6. **Navigation & Presentation**: Sheet, fullScreenCover patterns
7. **Error Handling Pattern**: Try-catch, error propagation
8. **State Management Examples**: @State, @Binding, @Environment guidance
9. **Common Mistakes & Fixes** (CRITICAL):
   - 8+ specific mistakes with before/after code
10. **Domain-Specific Patterns** (CRITICAL):
    - Analyze PRODUCT_SPEC for unique features
    - Create 3-5 custom patterns (e.g., "Timer Pattern", "Recording Pattern")
    - Each 20-40 lines with error handling

**Detail Level Standards**:
- All templates must be **production-ready** (not TODO-filled)
- Include **debug logging** patterns
- Include **error handling** in every pattern

---

### 7. DEVELOPMENT_PHASES.md

**Minimum Content Requirements**:
- **150+ lines** minimum
- **Context Scoping** (Active vs Ignored) for EACH phase
- **Testing checklists** with checkbox format
- **Device vs Simulator** test differentiation

**Required Sections**:
1. **Strategy**: Context scoping philosophy
2. **Phase Definitions** (3-5 phases):
   - **Goal**: What this phase achieves
   - **Why**: Dependency rationale
   - **Active Context**: Exact files/sections to read
   - **Ignored Context**: Files to exclude with rationale
3. **Testing Strategy & Verification**:
   - Phase-specific testing checklists
   - Simulator vs device requirements
   - URL scheme testing (if applicable)
   - Debugging tips for common issues
4. **Definition of "Phase Complete"**: Exit criteria

**Context Scoping Format**:
```markdown
### Active Context
- **Governance**: `governance/SYSTEM_ARCHITECTURE.md` (Sections 3.2, 4.3)
- **Code**: `Core/Hub/*`, `Services/AppLauncherService.swift`

### Ignored Context
- `Core/Onboarding/*` (not needed for this phase)
```

---

### 8. AI_WORKFLOW.md

**Minimum Content Requirements**:
- **400+ lines** for comprehensive workflow
- **Universal Context Block** (50+ lines) used for ALL phases
- **Copy-paste prompts** in fenced markdown blocks
- **Exact file references** using `@file/path` syntax

**Required Sections**:
1. **How to Use This Document**: Two-block approach explanation
2. **Universal Context Block** (CRITICAL):
   - Protocol rules (5-7 rules)
   - Governance document list with purposes
   - Standard workflow (7-step checklist)
   - Must be copied for EVERY phase
3. **Phase-Specific Prompts** (one per DEVELOPMENT_PHASES phase):
   - ACT AS role
   - CONTEXT FILES TO READ (with `@` syntax and section numbers)
   - YOUR TASKS (numbered, specific)
   - CONSTRAINTS (with checklist format)
   - TESTING (from DEVELOPMENT_PHASES.md)
4. **After Completing All Phases**: Final verification
5. **If Something Goes Wrong**: Troubleshooting guide

**Prompt Format Standard**:
```markdown
## PHASE X: Phase Name

**ACT AS**: Role

**CONTEXT FILES TO READ**:
- `@governance/FILE.md` (Sections X.Y, X.Z)

**YOUR TASKS**:
1. Task with exact specifications
2. Reference CODE_TEMPLATES.md Section N

**CONSTRAINTS**:
- Use exact pattern from CODE_TEMPLATES.md
- **Before starting**: Review AI_CHECKLIST.md
- **When stuck**: See AI_CHECKLIST.md Pitfall #N

**TESTING**:
- [ ] Checkbox format from DEVELOPMENT_PHASES.md
```

---
