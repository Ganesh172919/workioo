# Error Control Prompts

## What are Error Control Prompts?
Error control prompts are techniques that help AI catch potential mistakes, verify accuracy, and provide safeguards against common errors. They build quality control directly into your prompts.

## Why Error Control Matters

1. **Improved accuracy**: Catch mistakes before they cause problems
2. **Build confidence**: Trust AI responses more when verified
3. **Learning tool**: Understanding errors helps avoid them
4. **Critical applications**: Essential for important decisions
5. **Iterative improvement**: Errors guide better follow-up questions

## Types of Error Control

### 1. **Pre-emptive Error Prevention**
Anticipate and prevent common mistakes upfront.

```
"When answering, please:
- Double-check all calculations
- Verify facts from reliable sources
- Note any assumptions you're making
- Flag anything you're uncertain about
- Avoid speculation beyond the information given"
```

### 2. **Built-in Verification**
Ask AI to verify its own work.

```
"[Your question]

After answering:
1. Verify your math/logic
2. Check for internal consistency
3. Identify potential errors
4. Rate your confidence (High/Medium/Low)
5. Note any caveats or limitations"
```

### 3. **Error Boundary Setting**
Define what errors to avoid.

```
"Common mistakes to avoid in this type of problem:
- [Error type 1]
- [Error type 2]
- [Error type 3]

Please check your answer against these before responding."
```

## Basic Error Control Techniques

### Technique 1: Explicit Accuracy Request

```
"[Question]. Accuracy is critical. Please:
- Take your time with calculations
- Show your work for verification
- Double-check before answering
- If unsure, say so"
```

### Technique 2: Confidence Scoring

```
"[Question]

Provide:
- Your answer
- Confidence level (0-100%)
- Reasoning for confidence level
- What could make you more/less confident"
```

**Example:**
```
Q: "What's the capital of Kazakhstan?"

A: "The capital of Kazakhstan is Astana (renamed Nur-Sultan in 2019, 
though there's been discussion about changing it back).

Confidence: 90%
Reasoning: This is well-documented, though the recent name changes 
create some uncertainty about the current official name.
Note: Would need to verify if the name change back to Astana was 
officially completed."
```

### Technique 3: Assumption Documentation

```
"[Question]

List all assumptions you're making:
1. [Assumption 1]
2. [Assumption 2]
...

Then provide your answer. Flag if any assumptions are questionable."
```

### Technique 4: Alternative Answers

```
"[Question]

Provide:
- Your primary answer with reasoning
- Alternative answer if there's ambiguity
- Conditions under which each would be correct
- Confidence in the primary answer"
```

## Advanced Error Control Patterns

### Pattern 1: Devil's Advocate

Ask AI to challenge its own answer.

```
"[Question]

First, provide your answer.

Then, play devil's advocate:
- What could be wrong with this answer?
- What have I potentially overlooked?
- What alternative interpretations exist?
- What would change if [key assumption] were different?

Finally, provide your refined answer incorporating this analysis."
```

### Pattern 2: Multiple Methods Verification

```
"Solve [problem] using two different methods:

Method 1: [Approach A]
Result: [Answer]

Method 2: [Approach B]
Result: [Answer]

Verification: Do both methods agree? If not, identify the error."
```

**Example:**
```
"Calculate 15% tip on $68.50 using two methods:

Method 1 (Direct):
$68.50 × 0.15 = $10.28

Method 2 (10% + 5%):
10% = $6.85
5% = $3.43 (half of 10%)
Total = $6.85 + $3.43 = $10.28

Verification: ✓ Both methods agree: $10.28"
```

### Pattern 3: Sanity Check Protocol

```
"[Question]

Answer, then perform these sanity checks:
1. Order of magnitude: Is this roughly the right size?
2. Units: Are units consistent throughout?
3. Edge cases: Does it work for extreme values?
4. Common sense: Does this make intuitive sense?
5. Comparison: How does this compare to similar cases?"
```

### Pattern 4: Error Type Specification

```
"[Question]

While answering, specifically check for these error types:
- Calculation errors (arithmetic mistakes)
- Logic errors (faulty reasoning)
- Assumption errors (incorrect premises)
- Interpretation errors (misunderstanding the question)
- Scope errors (too broad/narrow answer)

Mark each check: ✓ Verified or ✗ Needs review"
```

## Domain-Specific Error Control

### For Code

```
"Review this code and check for:
1. Syntax errors
2. Logic errors
3. Edge cases not handled
4. Performance issues
5. Security vulnerabilities

For each category, report:
- ✓ Looks good
- ⚠ Potential issue: [description]
- ✗ Definite problem: [description with fix]"
```

### For Math

```
"Solve [problem]

Error control checklist:
- [ ] Checked arithmetic
- [ ] Verified order of operations
- [ ] Confirmed units match
- [ ] Tested with simple example
- [ ] Answer is reasonable magnitude
- [ ] Used alternative method to verify

Show which checks passed/failed."
```

### For Factual Information

```
"[Question about facts]

Provide:
1. Answer with sources if possible
2. Certainty level: Certain/Probable/Uncertain
3. Last verified: Recent/Older/Unknown
4. Caveats: Any reasons this might be outdated or incomplete
5. How to verify: Where to double-check this information"
```

### For Advice

```
"[Request for advice]

Provide advice with:
1. Main recommendation
2. Assumptions this is based on
3. Situations where this might NOT apply
4. Risks or downsides to consider
5. Alternative approaches
6. Confidence level and why"
```

## Real-World Examples

### Example 1: Financial Calculation

```
Prompt: "I want to buy a house for $400K with 20% down at 6% interest 
for 30 years. What's my monthly payment?

Error control required:
- Show calculation steps
- Verify with standard mortgage formula
- Check if answer is reasonable range
- Note what's included/excluded (taxes, insurance, etc.)
- Provide confidence level"

Good Response:
"Let me calculate this carefully:

Given:
- Home price: $400,000
- Down payment: 20% = $80,000
- Loan amount: $320,000
- Interest rate: 6% annual (0.5% monthly)
- Term: 30 years (360 months)

Calculation using mortgage formula:
M = P[r(1+r)^n]/[(1+r)^n-1]
M = 320,000[0.005(1.005)^360]/[(1.005)^360-1]
M = 320,000[0.005(6.023)/5.023]
M = 320,000[0.00599]
M = $1,918.56

Sanity check:
✓ Total paid: $1,918.56 × 360 = $690,682
✓ Interest paid: $370,682 (reasonable for 30 years at 6%)
✓ Monthly payment is ~0.6% of loan (typical range)

Confidence: High (95%)

Important caveats:
- This is principal + interest only
- Does NOT include: property taxes, insurance, HOA, PMI
- Actual payment will be higher
- This assumes fixed rate for full term

To verify: Use online mortgage calculator at [bank website]"
```

### Example 2: Technical Troubleshooting

```
Prompt: "My website is slow. Help me diagnose why. Use error control 
to ensure accurate diagnosis.

Required:
- List what you need to know
- State assumptions clearly
- Provide most likely causes with confidence levels
- Suggest verification tests
- Note what you can't determine without more info"

Good Response:
"Let me diagnose this systematically with proper error control:

INFORMATION NEEDED (Currently Missing):
⚠ "Slow" is vague - need specific metrics:
  - Page load time? (1s? 5s? 30s?)
  - For all pages or specific ones?
  - For all users or certain locations?
  - Recent slowdown or always slow?

ASSUMPTIONS I'm Making (Please confirm):
1. Assuming you mean front-end load time (not API response time)
2. Assuming this is compared to previous performance
3. Assuming multiple users experience this, not just one device

DIAGNOSIS (With Confidence Levels):

High Confidence (70-90%):
1. Unoptimized images (very common)
   - Test: Check image file sizes
   - Fix: Compress and use modern formats

2. Too many HTTP requests
   - Test: Check network tab (50+ requests is concerning)
   - Fix: Bundle files, use CDN

Medium Confidence (40-60%):
3. Database queries slow
   - Test: Check server response times
   - Need: Access to backend logs

4. Server resource limits
   - Test: Monitor CPU/RAM during load
   - Need: Server metrics

Low Confidence (10-30%):
5. DNS issues
   - Less likely if only some pages slow
6. DDoS attack
   - Would affect all users severely

VERIFICATION STEPS:
1. Use PageSpeed Insights for objective metrics
2. Test from multiple locations/devices
3. Check browser console for errors
4. Monitor network tab while loading

WHAT I CAN'T DETERMINE:
- Exact root cause without metrics
- Whether it's caching, CDN, or hosting issue
- If it's code or infrastructure problem

CONFIDENCE IN OVERALL DIAGNOSIS: Medium (50%)
REASON: Need specific measurements to be certain

Next step: Please provide actual load times and run PageSpeed Insights test."
```

## Practice Exercises

**Exercise 1: Add Error Control**
Take this prompt and add error control mechanisms:
"Calculate the ROI if I invest $10,000 and get $15,000 back in 2 years."

Add:
- Verification steps
- Sanity checks
- Assumption documentation
- Confidence rating

**Exercise 2: Create Error Checklist**
Create an error control checklist for prompts about:
"Converting recipe measurements"

Include:
- Common mistakes to avoid
- Verification methods
- Edge cases to consider
- Confidence indicators

**Exercise 3: Analyze Error Control**
Review this AI response and identify what error controls are missing:

"Q: Should I take this job offer?
A: Yes, definitely take it. The salary is higher."

What should have been included?

## Common Error Control Mistakes

1. **Too paranoid**: Excessive checks slow down simple tasks
   - ❌ "Double-check the spelling of 'apple'"
   - ✅ Save thorough checks for complex/critical tasks

2. **Vague verification**: "Check if correct" doesn't help
   - ❌ "Make sure this is right"
   - ✅ "Verify using [specific method]"

3. **Ignoring uncertainty**: Acting certain when uncertain
   - ❌ Stating facts without confidence levels
   - ✅ "Based on available info, I'm 70% confident that..."

4. **No recovery path**: Catching errors but not fixing them
   - ❌ "This might be wrong"
   - ✅ "If wrong, here's how to verify and correct..."

## Pro Tips

1. **Scale to importance**: More critical = more error control
2. **Automate checks**: Build verification into your prompt templates
3. **Learn from errors**: When AI makes mistakes, add those to your error control list
4. **Balance thoroughness and efficiency**: Don't over-engineer simple tasks
5. **Make uncertainty visible**: It's better to know what's uncertain
6. **Provide context for errors**: Explain WHY an error is possible
7. **Test edge cases**: Ask about extreme or unusual scenarios

## Error Control Template Library

**Basic Template:**
```
"[Question]

Requirements:
- Show work for verification
- Note any assumptions
- Check your answer
- Rate confidence (High/Medium/Low)
- Flag anything uncertain"
```

**Advanced Template:**
```
"[Question]

Process:
1. State what you understand the question to be
2. List assumptions
3. Provide answer with reasoning
4. Verify using [alternative method]
5. Sanity check results
6. Note limitations or caveats
7. Confidence: X% because [reasons]
8. How to independently verify: [method]"
```

**Critical Decision Template:**
```
"[Decision question]

Analyze with maximum error control:
1. Restate the decision to confirm understanding
2. List all assumptions and their validity
3. Present main recommendation with full reasoning
4. Devil's advocate: What could go wrong?
5. Alternative recommendations and trade-offs
6. Conditions that would change the recommendation
7. Information gaps that affect confidence
8. Confidence level with detailed justification
9. Suggested verification before acting"
```

## Key Takeaways

✓ Build error control into prompts for critical tasks  
✓ Request confidence levels and reasoning  
✓ Ask AI to verify using multiple methods  
✓ Document assumptions explicitly  
✓ Include sanity checks for calculations  
✓ Make uncertainty visible  
✓ Scale error control to task importance  

## Next Steps
Learn about few-shot prompting to teach AI through examples of correct behavior.
