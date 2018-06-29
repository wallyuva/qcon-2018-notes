# Succession: A Refactoring Story

## Speakers

Katrina Owen

### Notes

- Should i refactor? Is there a reason to change 
- Code that's harder to understand is harder to change - you can name it if you understand it
- Three common strategies for naming
  1. Use a fragment of the implementation - concrete
  2. Structurally
  3. Concepts in the domain
- Names anchor our understanding

- Dupication - some people focus on sameness vs differences
  - Sameness is a trap
- Rules for refactoring *follow them meticulously
  - Find the things that are the most alike
  - Select the smallest difference beteween them
  - Make the smallest change that will remove that difference

- Each of your steps need to be safe, don't keep refactoring beyond breaking tests
- Large steps carry a massive cognitive load
- In legacey codebases take itny steps backwards