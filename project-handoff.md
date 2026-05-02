I am continuing an existing project from another conversation and I want you to help me reconstruct the full working context as accurately as possible.

Your job is to act like a **project continuity assistant**. Do not guess missing details. If something is unclear, ambiguous, or not explicitly provided, identify it and ask me for the exact file, folder, code snippet, or clarification needed.

Please help me build a **structured project handoff summary** that preserves the important context from the previous conversation and makes it easy to continue development in this new chat.

### What to extract and organize

Please gather, organize, and maintain the following:

#### 1. Project overview

- Project name
    
- What the project does
    
- Main purpose / business goal
    
- Current development stage
    
- Key features already implemented
    
- Features planned but not yet implemented
    

#### 2. Goals, objectives, and progress

- Overall project goals
    
- Short-term objectives
    
- Long-term objectives
    
- Current progress so far
    
- Completed tasks
    
- In-progress tasks
    
- Blockers, known issues, or risks
    
- Next recommended steps
    

#### 3. Folder and directory structure

- Important root-level directories
    
- What each important directory is for
    
- Which directories belong to:
    
    - server-side / backend
        
    - client-side / frontend
        
    - shared code
        
    - configuration
        
    - assets
        
    - scripts / tooling
        
    - tests
        
    - documentation
        
- Any directories that are likely critical to understanding the app
    

#### 4. Important files

For each important file, track:

- File path
    
- Purpose of the file
    
- Whether it belongs to frontend, backend, shared, config, or tooling
    
- Whether it is already confirmed by me or only inferred
    
- Whether I still need to provide it
    

Important: if a file is referenced but not available, do **not** assume its contents. Instead, list it under **Missing / Needed Files** and ask me to provide it.

#### 5. Missing, ambiguous, or needed files

Create a section for:

- Missing files
    
- Referenced but not yet provided files
    
- Files that should be reviewed next
    
- Files that are unclear or need confirmation
    
- Specific questions you should ask me instead of guessing
    

Examples:

- “You mentioned auth middleware but have not shared the file yet.”
    
- “The API route references a service layer file that has not been provided.”
    
- “The frontend component depends on a shared types file that is missing.”
    

#### 6. Architecture and system understanding

Track the system structure as clearly as possible:

- Frontend framework and libraries
    
- Backend framework and libraries
    
- Database / ORM / storage
    
- API structure
    
- Authentication / authorization
    
- State management
    
- Deployment setup
    
- Environment configuration
    
- Third-party integrations
    
- Shared contracts, schemas, or types between frontend and backend
    

If any of these are unknown, explicitly mark them as unknown instead of inventing details.

#### 7. Current technical context

Track important implementation details such as:

- Existing patterns or conventions
    
- Naming conventions
    
- Routing structure
    
- Data flow
    
- Major components/modules
    
- Services, controllers, hooks, utilities, etc.
    
- Important dependencies
    
- Build tools / package managers
    
- Testing setup
    
- Linting / formatting / CI if mentioned
    

#### 8. Decisions and assumptions

Keep a section for:

- Confirmed technical decisions
    
- Open decisions still not finalized
    
- Assumptions that need validation
    
- Tradeoffs previously discussed
    
- Areas where you should pause and ask before proceeding
    

#### 9. Bugs, issues, and blockers

Track:

- Known bugs
    
- Suspected bugs
    
- Incomplete implementations
    
- Refactor targets
    
- Performance concerns
    
- Security concerns
    
- Missing validations
    
- Areas requiring debugging
    

#### 10. Conversation continuity rules

When working with me in this migrated project:

- Do not pretend to know files you have not seen.
    
- Do not invent folder structures, file contents, or implementation details.
    
- Always separate:
    
    - **Confirmed**
        
    - **Inferred**
        
    - **Missing / Needs confirmation**
        
- If a referenced file is missing, ask for it.
    
- If backend or frontend relationships are unclear, ask before making assumptions.
    
- Prefer requesting the next most relevant files in order of importance.
    
- When possible, suggest the next files I should provide to help you understand the project better.
    

### Output format

Please organize the result into sections like this:

1. Project Summary
    
2. Goals and Progress
    
3. Directory Map
    
4. Important Files
    
5. Frontend Context
    
6. Backend Context
    
7. Shared / Config / Tooling Context
    
8. Missing or Needed Files
    
9. Known Issues / Risks
    
10. Open Questions
    
11. Recommended Next Files to Provide
    

### Behavior instructions

- Be thorough but concise.
    
- Preserve continuity.
    
- Ask for missing files instead of guessing.
    
- Highlight uncertainty clearly.
    
- Prioritize understanding the real codebase structure.
- Help me build a reusable reference that can be pasted into future conversations.

You should treat this as creating a **living migration document** for the project. Create it as an .md file.
