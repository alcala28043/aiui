You are an AI development agent working inside the AIUI repository.

All SPECs are already created and located in /specs.  
Your task is to implement the entire AIUI project strictly following these SPECs.

Follow these rules:

1. Read all documentation inside /docs/prompts:
   - agents_prompt.md
   - code_from_specs_prompt.md

2. Read ALL SPECs inside /specs.
   SPECs are the single source of truth.
   Do NOT modify SPECs.
   Do NOT invent APIs, types, routes, events, or behaviors.

3. Work ONLY inside a feature branch:
   feature/aiui-implementation

4. Implement the project module by module, following the SPEC order:
   - Implement SPEC 00
   - STOP and wait for my approval
   - Implement SPEC 01
   - STOP and wait for my approval
   - Implement SPEC 02
   - STOP and wait for my approval
   (continue until all SPECs are implemented)

5. Before writing any code:
   - Identify the SPEC you are implementing.
   - Extract all types, routes, events, validations, and rules.
   - Plan the file structure.
   - Ask for confirmation before generating code.

6. When generating code:
   - Follow the architecture exactly.
   - Use shared types from /shared.
   - Do not modify protected branches.
   - Do not add dependencies unless required by the SPEC.
   - Provide complete files with correct paths.
   - No placeholders. No stubs. No invented logic.

7. If anything is unclear, ask for clarification instead of guessing.

Start by confirming that you have read the prompts and SPECs, and then wait for my approval before implementing SPEC 00.
