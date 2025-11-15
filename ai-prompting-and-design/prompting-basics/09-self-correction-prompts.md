# Self-Correction Prompts

## What are Self-Correction Prompts?
Self-correction prompts instruct AI to review, critique, and improve its own outputs. Instead of accepting the first answer, the AI iterates on its work, catching errors and refining the response.

## Why Self-Correction Works

1. **Better quality**: Reviewed and refined outputs are more accurate
2. **Catches errors**: AI can spot its own mistakes upon review
3. **Improves reasoning**: Second-pass thinking often yields insights
4. **Reduces iterations**: Get better results without multiple user prompts
5. **Teaches patterns**: Shows the improvement process

## Basic Self-Correction Structure

```
Step 1: Provide your initial answer
Step 2: Review your answer critically
Step 3: Identify any errors or improvements needed
Step 4: Provide the corrected/improved version
```

## Simple Self-Correction Example

### Basic Format

```
"[Your question]

First, provide your initial answer.
Then, review it for errors or ways to improve.
Finally, provide your corrected final answer."
```

**Example:**
```
Question: "Write a professional email declining a job offer"

Process:
1. Initial answer: [first draft]
2. Review: [critique of first draft]
3. Final answer: [improved version]
```

## Types of Self-Correction

### 1. **Error Detection**
Focus on finding and fixing mistakes.

```
"[Task]

Step 1: Complete the task
Step 2: Check for these specific errors:
   - Factual mistakes
   - Logical inconsistencies
   - Calculation errors
   - Grammar/spelling issues
Step 3: Correct any errors found
Step 4: Provide final corrected version"
```

### 2. **Quality Improvement**
Focus on enhancing overall quality.

```
"[Task]

Step 1: Provide initial response
Step 2: Evaluate against quality criteria:
   - Clarity: Is it easy to understand?
   - Completeness: Does it cover everything?
   - Accuracy: Is the information correct?
   - Conciseness: Is it efficiently worded?
Step 3: Improve based on evaluation
Step 4: Present final improved version"
```

### 3. **Perspective Shift**
Review from different angles.

```
"[Task]

Step 1: Provide your answer
Step 2: Review from these perspectives:
   - As a beginner: Is it accessible?
   - As an expert: Is it accurate?
   - As a skeptic: What could be challenged?
Step 3: Refine based on these perspectives
Step 4: Final answer incorporating insights"
```

### 4. **Iterative Refinement**
Multiple passes of improvement.

```
"[Task]

Draft 1: Initial attempt
Review 1: What's missing or unclear?
Draft 2: Improved version
Review 2: Any remaining issues?
Final: Polished version"
```

## Self-Correction Patterns

### Pattern 1: Answer-Critique-Revise

```
"[Question]

STEP 1 - Initial Answer:
[Provide your first answer]

STEP 2 - Self-Critique:
What could be improved?
- Accuracy: Any facts to verify?
- Clarity: Any confusing parts?
- Completeness: Anything missing?

STEP 3 - Revised Answer:
[Improved version based on critique]"
```

**Example:**
```
Question: Explain why the sky is blue.

STEP 1 - Initial Answer:
The sky is blue because of how sunlight interacts with the atmosphere.

STEP 2 - Self-Critique:
- Too vague - doesn't explain the mechanism
- Missing key physics concept (Rayleigh scattering)
- Doesn't explain why specifically blue, not other colors

STEP 3 - Revised Answer:
The sky appears blue due to Rayleigh scattering. Sunlight contains all colors, but when it enters Earth's atmosphere, shorter wavelengths (blue and violet) scatter more than longer wavelengths (red, orange). While violet scatters even more than blue, our eyes are more sensitive to blue, and some violet is absorbed by the upper atmosphere, making the sky appear blue to us.
```

### Pattern 2: Multiple Validation Checks

```
"[Task]

Initial response: [Your answer]

Validation checks:
1. Accuracy check: Are all facts correct? ✓/✗
2. Logic check: Does the reasoning hold? ✓/✗
3. Completeness check: Is anything missing? ✓/✗
4. Clarity check: Is it easy to understand? ✓/✗

Issues found: [List any problems]
Corrections needed: [Specific fixes]

Final corrected response: [Improved answer]"
```

### Pattern 3: Comparative Improvement

```
"[Task]

Version A (Initial):
[First attempt]

Analysis:
- Strengths: [What works well]
- Weaknesses: [What needs improvement]
- Missing: [What's absent]

Version B (Improved):
[Enhanced version addressing weaknesses]

Why Version B is better:
[Explanation of improvements]"
```

### Pattern 4: Constraint Checking

```
"[Task with specific requirements]

Initial attempt: [Your response]

Requirement checklist:
- [ ] Requirement 1: Met/Not Met
- [ ] Requirement 2: Met/Not Met
- [ ] Requirement 3: Met/Not Met

Gaps identified: [What's missing]

Corrected version: [Meets all requirements]"
```

## Domain-Specific Self-Correction

### For Writing

```
"Write [content]

Draft 1: [Initial writing]

Editorial review:
- Tone: Is it appropriate for the audience?
- Structure: Does it flow logically?
- Grammar: Any errors?
- Impact: Does it achieve its purpose?
- Wordiness: Can anything be tightened?

Draft 2: [Revised based on review]"
```

### For Code

```
"Write code to [task]

Version 1:
[Initial code]

Code review:
- Correctness: Does it work? Edge cases?
- Performance: Any inefficiencies?
- Readability: Is it clear?
- Best practices: Any violations?
- Security: Any vulnerabilities?

Version 2:
[Improved code with fixes]

Changes made: [List of improvements]"
```

### For Math/Logic

```
"Solve: [Problem]

Solution attempt:
[Initial solution]

Verification:
- Check arithmetic: [Verify each calculation]
- Check logic: [Verify each step follows]
- Alternative method: [Solve differently]
- Sanity check: [Does answer make sense?]

Error found: [If any]
Corrected solution: [Fixed version]"
```

### For Analysis

```
"Analyze [topic]

Initial analysis:
[First take]

Critical review:
- Are all perspectives considered?
- Is evidence sufficient?
- Are conclusions justified?
- What contradicts this analysis?
- What's been overlooked?

Refined analysis:
[More balanced, thorough version]"
```

## Real-World Examples

### Example 1: Professional Email

```
Task: Write an email asking for a deadline extension

INITIAL DRAFT:
"Hi, I need more time for the project. Can we extend the deadline?"

SELF-CRITIQUE:
Issues identified:
- Too casual for professional context
- No explanation of reason
- No proposed new deadline
- Doesn't acknowledge impact
- No reassurance about quality

IMPROVED VERSION:
"Hi [Name],

I'm writing regarding the [Project Name] currently due on [Date]. Due to [specific, valid reason], I would need additional time to deliver work that meets our quality standards.

Would it be possible to extend the deadline to [specific date]? This would allow me to [specific benefit].

I apologize for any inconvenience this may cause and appreciate your understanding. Please let me know if this works for you or if you'd like to discuss alternatives.

Best regards,
[Your name]"

IMPROVEMENTS MADE:
✓ Professional tone
✓ Clear explanation
✓ Specific new timeline
✓ Acknowledges impact
✓ Shows commitment to quality
```

### Example 2: Technical Explanation

```
Question: Explain how binary search works

INITIAL ANSWER:
"Binary search looks at the middle element and decides which half to search next. It keeps doing this until it finds what it's looking for."

SELF-REVIEW:
Weaknesses:
- Assumes array is sorted (prerequisite not mentioned)
- Doesn't explain "which half" decision logic
- No complexity information
- Missing edge cases
- Would benefit from example

IMPROVED ANSWER:
"Binary search is an efficient algorithm for finding an item in a sorted array:

Prerequisites: The array must be sorted

How it works:
1. Check the middle element
2. If it's the target, done!
3. If target is less, search the left half
4. If target is greater, search the right half
5. Repeat until found or range is empty

Example: Finding 7 in [1, 3, 5, 7, 9, 11, 13]
- Check middle (7): Found! ✓

Time complexity: O(log n) - much faster than O(n) linear search

Edge cases:
- Empty array: Return 'not found'
- Single element: Check if it matches
- Target not present: Return 'not found' after range exhausted"
```

### Example 3: Problem-Solving

```
Problem: Website gets 10 million visits per month. Estimate database size needed.

INITIAL ESTIMATE:
"Probably need about 1TB of storage."

SELF-CHECK:
Issues with this estimate:
- No calculation shown
- No assumptions stated
- Doesn't consider what data is stored
- Doesn't account for growth
- No confidence level
- Doesn't consider redundancy

CORRECTED ESTIMATE:
"Let me calculate this properly:

Assumptions:
- 10M visits/month
- Average 5 pages per visit = 50M page views
- Store: user sessions, page views, user data

Storage per record:
- Session: ~1KB × 10M = 10GB
- Page view: ~500B × 50M = 25GB
- User data: ~10KB × 2M active users = 20GB
Total raw data: ~55GB/month

Additional considerations:
- Indexes: +50% = ~82GB/month
- Backups: 3× = ~246GB/month
- 1 year retention: ×12 = ~3TB
- Growth buffer: 50% = ~4.5TB

Recommended: 5TB with ability to scale

Confidence: Medium - depends heavily on actual data structure and features

Note: This is primary storage. With replication (3 copies for high availability), total storage would be ~15TB."
```

## Practice Exercises

**Exercise 1: Apply Self-Correction**
Write an answer to this question, then apply self-correction:

"What are the benefits of learning to code?"

Steps:
1. Write initial answer
2. Critique it (what's weak?)
3. Write improved version
4. Explain what you improved

**Exercise 2: Create Self-Correction Template**
Design a self-correction template for:
"Explaining technical concepts to non-technical people"

Include:
- Initial explanation step
- Specific things to check
- Revision step
- Validation step

**Exercise 3: Error Detection**
This answer contains errors. Write a self-correction prompt that would catch them:

"Question: How long does it take light to travel from the Sun to Earth?
Answer: About 8 seconds because the Sun is 93 million kilometers away and light travels at 300,000 km/s."

What should the self-correction process reveal?

## Common Mistakes

1. **Vague review criteria**
   - ❌ "Review for quality"
   - ✅ "Check: accuracy, clarity, completeness, tone"

2. **Skipping initial attempt**
   - ❌ Just asking for "the perfect answer"
   - ✅ Explicit initial → review → improve cycle

3. **No specific corrections**
   - ❌ "This could be better"
   - ✅ "Change X to Y because Z"

4. **Too many iterations**
   - ❌ Draft 1, 2, 3, 4, 5...
   - ✅ Usually 1-2 revision cycles is enough

5. **Ignoring the improvement**
   - ❌ Review without applying changes
   - ✅ Explicitly produce improved version

## Pro Tips

1. **Be specific about criteria**: List exactly what to check
2. **Show the process**: Make review step visible, not just final answer
3. **Combine techniques**: Self-correction + CoT works great
4. **Use for learning**: The review process teaches good practices
5. **Scale to importance**: More iterations for critical tasks
6. **Document changes**: Note what was improved and why
7. **Include confidence**: Rate certainty even after correction
8. **Test edge cases**: Part of review should consider unusual scenarios

## Advanced Self-Correction

### Recursive Self-Correction

```
"[Task]

Attempt 1: [Answer]
Review 1: [Identify issues]
Attempt 2: [Corrected answer]
Review 2: [Any remaining issues?]
If issues remain: Attempt 3
If no issues: Mark as final"
```

### Peer-Review Simulation

```
"[Task]

Your answer: [Initial response]

Simulate peer review from 3 perspectives:

Reviewer 1 (Technical accuracy):
[Feedback on correctness]

Reviewer 2 (Clarity):
[Feedback on understandability]

Reviewer 3 (Completeness):
[Feedback on coverage]

Revised answer addressing all feedback:
[Final version]"
```

### Pre-Mortems

```
"[Task]

Initial solution: [Your approach]

Pre-mortem: Imagine this solution failed. Why might that be?
- Potential failure 1: [Description]
- Potential failure 2: [Description]
- Potential failure 3: [Description]

Improved solution addressing potential failures:
[More robust approach]"
```

## Template Library

**Basic Template:**
```
[Task]

Initial: [First attempt]
Review: [What to improve?]
Final: [Improved version]
```

**Detailed Template:**
```
[Task]

DRAFT 1:
[Initial response]

SELF-REVIEW:
Accuracy: [Check]
Clarity: [Check]
Completeness: [Check]
Quality: [Check]

ISSUES IDENTIFIED:
1. [Issue 1]
2. [Issue 2]

DRAFT 2:
[Corrected version]

IMPROVEMENTS MADE:
- [Change 1]
- [Change 2]
```

**Critical Task Template:**
```
[Task]

ATTEMPT:
[Your answer]

CRITICAL REVIEW:
- Factual accuracy: [Verify]
- Logic soundness: [Verify]
- Edge cases: [Consider]
- Assumptions: [State & validate]
- Alternative views: [Consider]

CORRECTIONS:
[List specific fixes needed]

FINAL (HIGH-CONFIDENCE):
[Thoroughly reviewed answer]

VERIFICATION METHOD:
[How to independently verify this is correct]
```

## Key Takeaways

✓ Self-correction catches errors and improves quality  
✓ Explicit review criteria make correction effective  
✓ Show the process: initial → review → improved  
✓ Multiple perspectives strengthen the review  
✓ Specific corrections beat vague suggestions  
✓ Combine with other techniques for best results  
✓ Scale correction effort to task importance  

## Next Steps
Learn about evaluating prompt quality to assess and improve your prompting techniques systematically.
