# Chain-of-Thought Shaping

## What is Chain-of-Thought?
Chain-of-Thought (CoT) prompting encourages AI to show its reasoning process step-by-step before arriving at an answer. Instead of jumping to conclusions, the AI "thinks out loud," making the logic transparent and often more accurate.

## Why Chain-of-Thought Matters

1. **Better accuracy**: Especially for complex reasoning tasks
2. **Transparent logic**: You can see and verify the thinking process
3. **Error detection**: Easier to spot where reasoning went wrong
4. **Learning tool**: Understanding the thought process helps you learn
5. **Debugging**: Identify flawed assumptions or missing steps

## Basic Chain-of-Thought Prompting

### Simple Trigger Phrases
```
"Let's think step by step..."
"Let's break this down..."
"Think through this carefully..."
"Let's reason through this..."
"Show your work..."
```

**Example:**
```
❌ Without CoT:
Q: "If a train travels 120 miles in 2 hours, then speeds up and 
travels 180 miles in the next 2 hours, what's the average speed?"
A: "75 mph"

✅ With CoT:
Q: "If a train travels 120 miles in 2 hours, then speeds up and 
travels 180 miles in the next 2 hours, what's the average speed? 
Let's think step by step."

A: "Let me work through this step by step:
1. First segment: 120 miles in 2 hours
2. Second segment: 180 miles in 2 hours
3. Total distance: 120 + 180 = 300 miles
4. Total time: 2 + 2 = 4 hours
5. Average speed: 300 miles ÷ 4 hours = 75 mph

The average speed is 75 mph."
```

## Types of Chain-of-Thought

### 1. **Zero-Shot CoT** (No Examples)
Simply ask the AI to think step by step.

```
"[Your question]. Let's approach this systematically."
```

### 2. **Few-Shot CoT** (With Examples)
Provide examples that show the reasoning process.

```
"Here's an example of how to solve this type of problem:

Q: A baker made 12 cookies and gave away 5. How many remain?
A: Let's think through this:
   - Started with: 12 cookies
   - Gave away: 5 cookies
   - Remaining: 12 - 5 = 7 cookies
   Answer: 7 cookies

Now solve this:
Q: A baker made 24 cookies and gave away 8. How many remain?"
```

### 3. **Structured CoT**
Specify the structure of reasoning.

```
"Analyze this problem using this structure:
1. Identify: What information do we have?
2. Determine: What are we trying to find?
3. Plan: What approach should we use?
4. Execute: Work through the solution
5. Verify: Check if the answer makes sense"
```

## Chain-of-Thought for Different Tasks

### For Math Problems

```
"Solve this problem, showing your reasoning at each step:

Problem: Sarah has $100. She spends 30% on groceries and 
then 20% of the remaining on entertainment. How much does 
she have left?

Show:
1. What we know
2. What we're finding
3. Each calculation
4. Verification that the answer makes sense"
```

### For Logical Reasoning

```
"Let's reason through this carefully:

Premise 1: All cats are mammals
Premise 2: Some mammals are pets
Premise 3: This animal is a cat

Question: Is this animal a pet?

Think through:
- What can we conclude from Premise 1 + 3?
- What can we conclude from Premise 2?
- What can we NOT conclude?
- Final answer with reasoning"
```

### For Code Debugging

```
"I'm getting an error. Let's debug this systematically:

Code: [paste code]
Error: [paste error]

Let's analyze:
1. What is the error message telling us?
2. Which line is causing the issue?
3. What are the possible causes?
4. Let's trace the execution step by step
5. What values do variables have at each point?
6. Where does the logic break?
7. What's the fix?"
```

### For Decision Making

```
"Help me decide whether to [decision]. Let's think through this:

1. What are the pros and cons?
2. What are my priorities and constraints?
3. What are the short-term impacts?
4. What are the long-term implications?
5. What are the risks and how can they be mitigated?
6. What would happen if I choose X vs Y?
7. Based on this analysis, what's the recommendation?"
```

## Advanced CoT Techniques

### Self-Ask CoT
The AI asks and answers its own questions.

```
"Solve this by asking yourself relevant questions:

Problem: Which weighs more - a pound of feathers or a pound of gold?

Ask yourself:
- Q1: [First question to consider]
- A1: [Answer]
- Q2: [Next question]
- A2: [Answer]
...
Final answer: [Conclusion]"
```

### Contrastive CoT
Show both correct and incorrect reasoning.

```
"Analyze this problem in two ways:

Approach A (Incorrect):
- [Common wrong approach]
- Why this fails: [Explanation]

Approach B (Correct):
- [Right approach]
- Why this works: [Explanation]
- Final answer: [Result]"
```

### Verification CoT
Build in self-checking.

```
"Solve this problem and verify your answer:

Step 1-N: [Work through solution]
Verification:
- Does this answer the original question?
- Are the units correct?
- Is the magnitude reasonable?
- Can we check it differently?
Alternative check: [Try another method]
Confidence: [High/Medium/Low] because [reason]"
```

## Shaping the Chain-of-Thought

### Control the Depth

**Shallow:**
```
"Give a brief reasoning outline for [task]"
```

**Medium:**
```
"Think through [task] step by step, showing main reasoning"
```

**Deep:**
```
"Provide detailed reasoning for [task], including:
- Every assumption made
- Each calculation or logical step
- Why each step follows from previous ones
- Alternative approaches considered and rejected"
```

### Control the Format

**Bullet Points:**
```
"Reason through this in bullet points:
• First observation: ...
• This means: ...
• Therefore: ...
• Conclusion: ..."
```

**Numbered Steps:**
```
"Think through this with numbered reasoning steps:
1. [First step]
2. [Second step]
..."
```

**Narrative:**
```
"Explain your thinking in a flowing narrative, as if explaining 
to a colleague how you arrived at the answer."
```

### Control the Focus

**Data-Focused:**
```
"Analyze this focusing on the data:
- What data do we have?
- What does each piece tell us?
- How do the pieces relate?
- What conclusion does the data support?"
```

**Logic-Focused:**
```
"Use formal logical reasoning:
- Premise 1: [State]
- Premise 2: [State]
- If P1 and P2, then: [Conclusion]
- Therefore: [Final answer]"
```

**Intuition-Focused:**
```
"Share your intuitive reasoning:
- Initial impression: [First thought]
- Why this makes sense: [Explanation]
- Checking against facts: [Verification]
- Refined conclusion: [Final answer]"
```

## Real-World Examples

### Example 1: Complex Problem-Solving

```
Prompt: "A website takes 5 seconds to load with 100 users. With 
200 users it takes 12 seconds. With 300 users, what would you 
expect and why? Let's reason through this step by step."

Expected CoT Response:
"Let's analyze this systematically:

Step 1: Examine the pattern
- 100 users: 5 seconds
- 200 users: 12 seconds
- Difference: 2x users, 2.4x time

Step 2: Identify the relationship type
- If linear: 200 users should take 10 seconds (2x5)
- Actual: 12 seconds
- This suggests super-linear growth

Step 3: Calculate growth rate
- From 100 to 200: (12-5)/(200-100) = 0.07 seconds per user
- This isn't constant, indicating non-linear scaling

Step 4: Consider possible causes
- Could be O(n²) complexity in code
- Could be database bottleneck
- Could be memory pressure

Step 5: Project to 300 users
- If continuing pattern: likely 20-25 seconds
- Conservative estimate: ~22 seconds
- But this could accelerate further

Conclusion: Expect ~22 seconds, but this system needs optimization 
as it's showing concerning scaling behavior."
```

### Example 2: Code Analysis

```
Prompt: "This function sometimes returns unexpected results. 
Let's trace through it step by step:

function average(numbers) {
    let sum = 0;
    for (let i = 0; i <= numbers.length; i++) {
        sum += numbers[i];
    }
    return sum / numbers.length;
}

Input: [2, 4, 6]
Expected: 4
Actual: NaN

Let's debug by tracing execution:"

Expected CoT Response:
"Let's trace this execution step by step:

Initial state:
- numbers = [2, 4, 6]
- numbers.length = 3

Loop iteration analysis:
i=0: sum = 0 + numbers[0] = 0 + 2 = 2 ✓
i=1: sum = 2 + numbers[1] = 2 + 4 = 6 ✓
i=2: sum = 6 + numbers[2] = 6 + 6 = 12 ✓
i=3: sum = 12 + numbers[3] = 12 + undefined = NaN ✗

Problem identified: 
- Loop condition is i <= numbers.length
- Should be i < numbers.length
- Arrays are 0-indexed, length is 3, but last valid index is 2
- Accessing numbers[3] returns undefined
- Adding undefined causes NaN

Final calculation:
- sum = NaN
- return NaN / 3 = NaN

Fix: Change loop condition from i <= numbers.length to i < numbers.length

Verification with fix:
- Loop runs for i=0,1,2 (not 3)
- sum = 2 + 4 + 6 = 12
- return 12 / 3 = 4 ✓"
```

## Practice Exercises

**Exercise 1: Add CoT**
Take this question and create a prompt that elicits chain-of-thought:

"If you invest $1000 at 5% annual interest compounded annually, 
how much will you have after 3 years?"

Your prompt should:
- Trigger step-by-step thinking
- Specify what to show at each step
- Ask for verification

**Exercise 2: Structured CoT**
Create a CoT template for analyzing whether a business idea is viable.
Include:
- Market analysis steps
- Financial reasoning
- Risk assessment
- Final recommendation with confidence level

**Exercise 3: Debug with CoT**
Write a prompt that uses CoT to debug this scenario:
"My code works fine locally but fails in production."

Include steps for:
- Identifying differences between environments
- Tracing potential causes
- Testing hypotheses
- Finding the root cause

## Common Mistakes

1. **Too vague**: "Think about it" vs "Think step by step showing calculations"
2. **Skipping verification**: Always ask for checking the answer
3. **Too rigid**: Allow some flexibility in how AI structures reasoning
4. **Forgetting examples**: Few-shot CoT often works better than zero-shot
5. **Wrong granularity**: Match detail level to complexity

## Pro Tips

1. **Combine with other techniques**: Role + CoT = "As a teacher, explain your step-by-step thinking"
2. **Make it explicit**: "Show your work" is clearer than "think about it"
3. **Request verification**: "Check your answer using a different method"
4. **Use for learning**: CoT responses teach you the process, not just the answer
5. **Format matters**: Specify bullet points, numbered steps, or narrative
6. **Test assumptions**: Ask AI to question its own assumptions during reasoning

## When to Use Chain-of-Thought

**Best for:**
- Math and logic problems
- Multi-step reasoning
- Complex analysis
- Debugging
- Learning new concepts
- Verifying answers
- Decision-making

**Not necessary for:**
- Simple factual questions
- Definitions
- Direct instructions
- Creative writing
- Open-ended brainstorming

## Key Takeaways

✓ CoT makes AI reasoning transparent and more accurate  
✓ Simple phrases like "let's think step by step" trigger CoT  
✓ Structure the reasoning process for specific needs  
✓ Include verification steps for critical tasks  
✓ Combine with examples for better results  
✓ Match depth to problem complexity  

## Next Steps
Learn about error control prompts to help AI catch and correct its own mistakes.
