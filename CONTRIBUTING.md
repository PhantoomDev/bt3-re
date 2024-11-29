# Contributing to BT3 Rollback Project

## Pull Request Format

```markdown
## Description
[Brief description of your changes/findings]

## Type of Changes
- Labeled Functions
- Memory Addresses Found
- Documentation Updates
- Other Changes

## Details
For reverse engineering findings:
- List newly labeled functions in Ghidra project
- New memory addresses/patterns discovered
- Any specific test cases or verification steps
- Tools/methods used to verify findings

For documentation/other changes:
- What was updated
- How to verify the changes

## Notes
- Any uncertainties or areas needing review
- Related findings that might be useful
- Known limitations or edge cases

Closes #[issue number]
```

### Examples

Good PR description: (This is not how the game works but just purely an example)
```markdown
## Description
Labeled character state transition functions and documented related memory addresses

## Type of Changes
- Labeled Functions:
  - 0x80XXXXX - BT3_CharacterStateInit
  - 0x80XXXXX - BT3_StateTransitionHandler
- Memory Addresses:
  - 0x80XXXXX - Current character state ID
  - 0x80XXXXX-0x80XXXXX - State transition table

## Details
- Found main state transition function using function call tracing
- Verified addresses using DME and test cases with different characters
- Added comments in Ghidra project explaining the state flow

## Notes
- State transition table might vary for some special characters (Gogeta, etc.)
- Related to character animation system at 0x80XXXXX
```
