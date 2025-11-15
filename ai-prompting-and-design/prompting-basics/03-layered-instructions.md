# Layered Instructions

## What Are Layered Instructions?
Layered instructions break down complex requests into organized levels, making it easier for AI to process your requirements systematically. Think of it as building a pyramid of instructions from broad to specific.

## The Layering Concept

```
Layer 1: High-Level Goal (What you want)
    ↓
Layer 2: Key Requirements (Must-haves)
    ↓
Layer 3: Preferences (Nice-to-haves)
    ↓
Layer 4: Format & Style (How to present it)
    ↓
Layer 5: Examples or References (Show what you mean)
```

## Why Use Layered Instructions?

1. **Prevents information overload**: AI processes organized information better
2. **Ensures priority**: Important requirements come first
3. **Allows flexibility**: AI can adapt within your layers
4. **Easy to debug**: If output is wrong, you know which layer to adjust

## Basic Layered Structure

### Simple 3-Layer Approach

**Layer 1 - Main Task:**
State your primary objective clearly

**Layer 2 - Key Details:**
List critical requirements or constraints

**Layer 3 - Format:**
Specify how you want the output

**Example:**
```
Layer 1: Create a weekly meal plan for healthy eating
Layer 2: Must be vegetarian, under 2000 calories/day, budget-friendly
Layer 3: Present as a table with meals and calories for each day
```

## Advanced Layered Structure

### Comprehensive 5-Layer Approach

**Example: Blog Post Request**

```
Layer 1 - GOAL:
Write a blog post about remote work productivity

Layer 2 - REQUIREMENTS:
- Target audience: Remote workers new to work-from-home
- Length: 1200-1500 words
- Include 5 actionable tips
- Backed by research or real examples

Layer 3 - STRUCTURE:
- Engaging introduction with a relatable scenario
- One section per tip with explanation and example
- Conclusion with encouragement and next steps

Layer 4 - TONE & STYLE:
- Conversational but professional
- Use "you" to address readers
- Short paragraphs (3-4 sentences max)
- Include subheadings for each tip

Layer 5 - REFERENCE:
Similar to the style of James Clear's blog posts - 
practical, evidence-based, immediately actionable
```

## Layering Patterns for Different Tasks

### Pattern 1: Creative Writing

```
Layer 1: Genre and basic premise
Layer 2: Characters and setting
Layer 3: Tone and style preferences
Layer 4: Length and structure
Layer 5: Specific elements to include/avoid
```

### Pattern 2: Technical Explanation

```
Layer 1: Topic and target audience
Layer 2: Depth level and prerequisites
Layer 3: Required components to cover
Layer 4: Examples and analogies to use
Layer 5: Format (tutorial, reference, guide)
```

### Pattern 3: Analysis Task

```
Layer 1: What to analyze
Layer 2: Analysis criteria/framework
Layer 3: Data or sources to consider
Layer 4: Output format (report, summary, comparison)
Layer 5: Specific questions to answer
```

## Real-World Examples

### Example 1: Code Review Request

```
Layer 1 - TASK:
Review this Python function for processing user data

Layer 2 - FOCUS AREAS:
- Security vulnerabilities
- Performance bottlenecks
- Code readability
- Error handling

Layer 3 - CONTEXT:
- Function processes 10K+ records daily
- Runs in a production environment
- Team follows PEP 8 standards

Layer 4 - OUTPUT FORMAT:
- List issues by severity (Critical, Important, Minor)
- Provide specific code suggestions for fixes
- Explain the reasoning for each suggestion

[Include code here]
```

### Example 2: Learning Material Creation

```
Layer 1 - GOAL:
Create a lesson plan teaching recursion to beginners

Layer 2 - REQUIREMENTS:
- Suitable for students with basic Python knowledge
- 45-minute lesson duration
- Include 3 progressive examples
- Provide practice exercises

Layer 3 - TEACHING APPROACH:
- Start with real-world analogy (Russian dolls)
- Show iterative solution first, then recursive
- Build from simple to complex
- Emphasize base case importance

Layer 4 - DELIVERABLES:
- Lesson outline with timestamps
- Code examples with comments
- 3 practice problems (easy, medium, hard)
- Common mistakes section

Layer 5 - STYLE:
- Encouraging and patient tone
- Use print statements to show execution flow
- Relate to concepts they already know
```

## Practicing Layered Instructions

### Exercise 1: Build Layers
Take this single-line prompt and expand it into layers:
"Help me prepare for a job interview"

Create 4-5 layers including:
- The role you're applying for
- Your experience level
- Specific areas you need help with
- How you want the help presented

### Exercise 2: Reorganize
This prompt is messy. Reorganize it into clear layers:

"I want to lose weight maybe 10 pounds and I like pizza and pasta but also want to exercise maybe 3 times a week but I'm busy and I need it to be cheap and also I'm vegetarian and don't like running and prefer working out at home with maybe 30-minute sessions oh and I want to see results in 2 months."

### Exercise 3: Create Your Own
Think of a complex task you need help with. Structure a layered prompt including:
- Main goal
- Key constraints
- Preferences
- Format
- Examples or references

## Common Mistakes

1. **Too many layers**: 3-5 is usually enough
   - ❌ 10 layers with micro-details
   - ✅ 4 well-organized layers

2. **Mixed priorities**: Don't mix must-haves with nice-to-haves
   - ❌ Layer 2: "Must be free, preferably blue, definitely secure, maybe fast"
   - ✅ Layer 2 (Must): "Free and secure" / Layer 3 (Prefer): "Fast loading, blue theme"

3. **Contradictory layers**: Ensure layers don't conflict
   - ❌ Layer 2: "Keep it brief" / Layer 4: "Include detailed examples for everything"
   - ✅ Align your expectations across layers

## Pro Tips

1. **Start broad, get specific**: Each layer should drill down
2. **Use clear labels**: Mark your layers explicitly (Goal:, Requirements:, etc.)
3. **Prioritize**: Put most important information in earlier layers
4. **Review**: Read through your layers to ensure coherence
5. **Iterate**: Refine layers based on AI's output

## Template for Quick Use

```
TASK: [What you want done]

REQUIREMENTS:
- [Must have #1]
- [Must have #2]
- [Must have #3]

PREFERENCES:
- [Nice to have #1]
- [Nice to have #2]

FORMAT:
[How to present the output]

CONTEXT:
[Background info that helps]
```

## Key Takeaways

✓ Layer instructions from general to specific  
✓ Separate must-haves from nice-to-haves  
✓ Use clear labels for each layer  
✓ Keep layers coherent and non-contradictory  
✓ 3-5 layers work for most tasks  

## Next Steps
Learn about role prompting to get AI to respond from specific perspectives or expertise areas.
