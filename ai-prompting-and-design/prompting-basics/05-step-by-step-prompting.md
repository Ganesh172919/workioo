# Step-by-Step Prompting

## What is Step-by-Step Prompting?
Step-by-step prompting asks the AI to break down tasks or explanations into clear, sequential steps. This technique ensures thorough coverage and makes complex processes easier to understand and follow.

## Why Use Step-by-Step Prompting?

1. **Clarity**: Complex tasks become manageable when broken down
2. **Completeness**: Reduces the chance of missing important details
3. **Actionability**: Each step can be executed independently
4. **Learning**: Easier to understand the logic and sequence
5. **Debugging**: Easy to identify where something went wrong

## Basic Step-by-Step Structure

### Simple Request Format
```
"Explain [topic] step by step."
"Walk me through [process] one step at a time."
"Break down [task] into clear steps."
```

**Examples:**
- "Explain how to set up a React project step by step"
- "Walk me through debugging a memory leak one step at a time"
- "Break down the process of writing a research paper into clear steps"

## Enhanced Step-by-Step Prompting

### Specify Step Characteristics

**Template:**
```
"Provide step-by-step [instructions/explanation] for [task].
Each step should:
- [Characteristic 1]
- [Characteristic 2]
- [Characteristic 3]"
```

**Example:**
```
"Provide step-by-step instructions for deploying a web app to AWS.
Each step should:
- Be a single, concrete action
- Explain why it's necessary
- Include the exact commands to run
- Mention expected outcomes
- Note common errors and how to fix them"
```

## Different Step-by-Step Patterns

### Pattern 1: Numbered Sequential Steps

Best for: Procedures that must be done in order

```
"Create a numbered list of steps for [task].
Format:
Step 1: [Action]
   Why: [Explanation]
   Expected result: [Outcome]

Step 2: [Action]
   Why: [Explanation]
   Expected result: [Outcome]
..."
```

**Example:**
```
Step 1: Install Node.js and npm
   Why: Required to run React and its development tools
   Expected result: Running 'node -v' shows version number
   Command: Download from nodejs.org or use 'brew install node'

Step 2: Create project directory
   Why: Organize project files in a dedicated folder
   Expected result: New empty directory ready for project
   Command: mkdir my-react-app && cd my-react-app
```

### Pattern 2: Phased Approach

Best for: Large tasks with distinct phases

```
"Break down [task] into phases:

Phase 1: [Name] - [Goal]
  - Step 1.1: [Action]
  - Step 1.2: [Action]

Phase 2: [Name] - [Goal]
  - Step 2.1: [Action]
  - Step 2.2: [Action]
..."
```

**Example:**
```
Break down launching a blog into phases:

Phase 1: Setup (Goal: Get technical foundation ready)
  - Step 1.1: Choose and register a domain name
  - Step 1.2: Select hosting provider and plan
  - Step 1.3: Install WordPress or static site generator

Phase 2: Configuration (Goal: Make site functional)
  - Step 2.1: Select and install a theme
  - Step 2.2: Configure essential plugins
  - Step 2.3: Set up analytics and SEO basics
```

### Pattern 3: Conditional Steps

Best for: Processes with decision points

```
"Provide step-by-step guidance for [task] including:
- Decision points (if X then Y, else Z)
- Alternative paths
- When to choose each option"
```

**Example:**
```
Step 1: Assess your skill level
   → If complete beginner: Start with HTML/CSS basics (go to Step 2A)
   → If you know HTML/CSS: Jump to JavaScript fundamentals (go to Step 2B)
   → If you know JS: Begin with React concepts (go to Step 3)

Step 2A: Complete beginner path
   - Learn HTML structure (2 weeks)
   - Practice CSS styling (2 weeks)
   - Build 3 static websites
   Then proceed to Step 2B

Step 2B: JavaScript fundamentals
   - Variables, functions, arrays (1 week)
   - DOM manipulation (1 week)
   - Async programming (1 week)
   Then proceed to Step 3
```

## Real-World Examples

### Example 1: Troubleshooting Guide

```
"Create a step-by-step troubleshooting guide for when a website won't load.
Include:
- What to check at each step
- How to check it
- What it means if the check passes/fails
- When to move to the next step"
```

**Result:**
```
Step 1: Check your internet connection
   Action: Open another website or ping google.com
   Pass: Other sites load → Go to Step 2
   Fail: No internet → Restart router, check cables, contact ISP

Step 2: Verify the URL is correct
   Action: Check for typos, ensure it starts with https://
   Pass: URL is correct → Go to Step 3
   Fail: Fix URL and try again

Step 3: Clear browser cache and cookies
   Action: Press Ctrl+Shift+Delete, select all, clear
   Pass: Site still won't load → Go to Step 4
   Fail: Site loads now → Problem solved!
```

### Example 2: Learning Path

```
"Create a step-by-step learning path for becoming a data analyst.
Include:
- Time estimate for each step
- Prerequisites
- Resources to use
- Practice project for each step
- How to know you're ready for the next step"
```

### Example 3: Recipe-Style Instructions

```
"Provide step-by-step instructions for implementing user authentication.
Format like a recipe:
- List all prerequisites (ingredients)
- Prep work needed
- Main steps in order
- Optional variations
- Common mistakes to avoid"
```

## Step-by-Step for Different Purposes

### For Learning:
```
"Teach me [topic] step by step:
1. Start with the simplest concept
2. Build complexity gradually
3. Provide an example after each concept
4. Include a practice exercise before moving on
5. Review previous steps periodically"
```

### For Building:
```
"Guide me through building [project] step by step:
1. Set up the development environment
2. Create the basic structure
3. Implement core features one by one
4. Add enhancements
5. Test and debug
6. Deploy"
```

### For Debugging:
```
"Help me debug [problem] using a step-by-step approach:
1. Reproduce the issue reliably
2. Identify symptoms and error messages
3. Form hypotheses about causes
4. Test each hypothesis systematically
5. Implement the solution
6. Verify the fix works"
```

## Practice Exercises

**Exercise 1: Create Steps**
Choose a task you know well (making coffee, solving an equation, writing code).
Write a step-by-step guide that a complete beginner could follow.

Requirements:
- 5-8 steps
- Each step is one clear action
- Include expected outcomes
- Note what could go wrong

**Exercise 2: Request Steps**
Write a prompt asking for step-by-step guidance on ONE of these:
- Setting up a home network
- Learning a musical instrument
- Preparing for a marathon
- Starting a podcast

Include:
- Your current situation
- Desired end goal
- Time constraints
- Preferred level of detail

**Exercise 3: Improve Vague Steps**
This guide is too vague. Request a better step-by-step version:

"To make a website:
1. Learn coding
2. Build it
3. Put it online"

Your improved prompt should specify:
- Technical detail level needed
- Specific technologies
- Time frame
- What "done" looks like

## Common Mistakes

1. **Steps too large**
   - ❌ "Step 1: Build the entire backend"
   - ✅ "Step 1: Set up Express server; Step 2: Create database schema; Step 3: Build API endpoints..."

2. **Missing prerequisites**
   - ❌ Starting with "Step 1: Run npm install"
   - ✅ "Prerequisites: Node.js installed; Step 1: Create project folder; Step 2: Initialize npm..."

3. **Unclear outcomes**
   - ❌ "Step 3: Configure settings"
   - ✅ "Step 3: Configure settings → Result: You should see 'Configuration successful' message"

4. **Skipping decision points**
   - ❌ "Step 4: Choose framework" (but no guidance on how to choose)
   - ✅ "Step 4: Choose framework (React if building SPA, Next.js if need SSR, Vue if want simplicity)"

5. **No verification**
   - ❌ Steps without checking if they worked
   - ✅ Include "Verify:" or "Test:" after important steps

## Pro Tips

1. **Number appropriately**: 5-10 steps for quick tasks, more for complex ones
2. **Add checkpoints**: "At this point, you should have..."
3. **Include time estimates**: Helps plan and set expectations
4. **Highlight critical steps**: Mark steps that absolutely can't be skipped
5. **Provide recovery**: "If Step X fails, do this..."
6. **Link steps**: Show how each step leads to the next
7. **Use consistent format**: Makes steps easier to follow

## Advanced Techniques

### Recursive Steps
For complex topics, each step can have sub-steps:
```
Step 1: Set up development environment
  1.1: Install Node.js
    1.1.1: Download installer
    1.1.2: Run installation
    1.1.3: Verify installation
  1.2: Install VS Code
  1.3: Install Git
```

### Parallel Steps
When multiple things can happen simultaneously:
```
Step 3: While the server is building (3-5 minutes):
  → Do Step 3A: Review documentation
  → Or do Step 3B: Set up deployment configuration
  → Or do Step 3C: Write tests

Then proceed to Step 4 once build completes
```

### Milestone-Based Steps
```
Milestone 1: Basic functionality (Week 1-2)
  - Steps to achieve this milestone...
  
Milestone 2: Enhanced features (Week 3-4)
  - Steps to achieve this milestone...
```

## Template Library

**Basic Template:**
```
"Provide step-by-step instructions for [task]:
1. [Step]
2. [Step]
3. [Step]
...
Include what success looks like at each step."
```

**Detailed Template:**
```
"Create a comprehensive step-by-step guide for [task]:

Prerequisites:
- [What's needed before starting]

Step 1: [Action]
  - How: [Detailed instructions]
  - Why: [Reason]
  - Success: [Expected outcome]
  - If it fails: [Troubleshooting]

[Repeat for each step]

Final verification:
- [How to confirm everything worked]"
```

## Key Takeaways

✓ Break complex tasks into manageable steps  
✓ Make each step a single, clear action  
✓ Include prerequisites and expected outcomes  
✓ Add decision points for different scenarios  
✓ Verify progress at key points  
✓ Provide troubleshooting guidance  

## Next Steps
Learn about chain-of-thought shaping to get AI to show its reasoning process explicitly.
