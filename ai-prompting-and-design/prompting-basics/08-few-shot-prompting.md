# Few-Shot Prompting

## What is Few-Shot Prompting?
Few-shot prompting teaches AI through examples. Instead of just describing what you want, you show 2-5 examples of inputs and desired outputs. The AI learns the pattern and applies it to new cases.

## Why Few-Shot Works

1. **Shows, not just tells**: Examples clarify expectations better than descriptions
2. **Pattern recognition**: AI excels at identifying and replicating patterns
3. **Reduces ambiguity**: Examples demonstrate exactly what you want
4. **Handles edge cases**: Examples can show how to handle tricky situations
5. **Faster than fine-tuning**: Quick way to adapt AI behavior

## Basic Structure

```
[Example 1 Input] → [Example 1 Output]
[Example 2 Input] → [Example 2 Output]
[Example 3 Input] → [Example 3 Output]

Now you try:
[Your actual input] → ?
```

## Simple Few-Shot Example

### Task: Classify sentiment

```
Review: "This product exceeded my expectations!" → Sentiment: Positive
Review: "Terrible quality, broke after one day." → Sentiment: Negative
Review: "It's okay, nothing special." → Sentiment: Neutral

Now classify:
Review: "Best purchase I've made this year!" → Sentiment: ?
```

**Expected Output:** Positive

## Few-Shot vs Other Approaches

### Zero-Shot (No Examples)
```
"Classify the sentiment of this review as Positive, Negative, or Neutral:
'Best purchase I've made this year!'"
```

### One-Shot (Single Example)
```
Example: "This product exceeded my expectations!" → Positive

Now classify: "Best purchase I've made this year!" → ?
```

### Few-Shot (Multiple Examples)
```
"This product exceeded my expectations!" → Positive
"Terrible quality, broke after one day." → Negative
"It's okay, nothing special." → Neutral

Now classify: "Best purchase I've made this year!" → ?
```

**Few-shot usually performs best for complex patterns!**

## How Many Examples?

- **2-3 examples**: Simple tasks with clear patterns
- **3-5 examples**: Most common tasks
- **5-8 examples**: Complex tasks with nuances
- **More than 8**: Rarely helps; consider fine-tuning instead

## Creating Effective Examples

### Principle 1: Representative Examples
Choose examples that cover typical cases.

**❌ Poor Examples:**
```
Input: "cat" → Output: "feline"
Input: "dog" → Output: "canine"

Now: "elephant" → ?
```
(Output unclear - could be "pachyderm," "mammal," or something else)

**✅ Good Examples:**
```
Input: "cat" → Output: "a small domesticated carnivorous mammal"
Input: "dog" → Output: "a domesticated carnivorous mammal bred in many varieties"
Input: "bird" → Output: "a warm-blooded egg-laying vertebrate with feathers and wings"

Now: "elephant" → ?
```
(Pattern is clear: brief scientific-style description)

### Principle 2: Show Edge Cases
Include examples that handle tricky situations.

```
# Handling negation
"The movie was not good" → Negative
"The movie was not bad" → Positive
"The movie was okay" → Neutral

# Handling sarcasm
"Oh great, another delay" → Negative
"This is just perfect!" [context: something broke] → Negative
```

### Principle 3: Consistent Format
Keep input and output formats identical across examples.

**❌ Inconsistent:**
```
Email: "Hey, what's up?" → Casual
"Dear Sir/Madam, I am writing to inquire..." → Formal
msg: "thx for ur help!!!" → Casual
```

**✅ Consistent:**
```
Text: "Hey, what's up?" → Casual
Text: "Dear Sir/Madam, I am writing to inquire..." → Formal
Text: "thx for ur help!!!" → Casual
```

## Few-Shot for Different Tasks

### Text Classification

```
Email: "CONGRATULATIONS! You've WON $1000000!!!" → Spam
Email: "Hi John, can we reschedule our meeting to 3pm?" → Not Spam
Email: "Click here for AMAZING deals you won't believe!" → Spam

Classify:
Email: "Your Amazon order has been shipped" → ?
```

### Data Extraction

```
Text: "John Smith lives in New York and works at Google"
Extract: {"name": "John Smith", "location": "New York", "company": "Google"}

Text: "Sarah Johnson is based in London, employed by Microsoft"
Extract: {"name": "Sarah Johnson", "location": "London", "company": "Microsoft"}

Now extract from:
Text: "Mike Chen works for Apple in San Francisco"
Extract: ?
```

### Format Transformation

```
Input: "2023-12-25"
Output: "December 25, 2023"

Input: "2024-01-01"
Output: "January 1, 2024"

Input: "2024-07-04"
Output: ?
```

### Creative Writing

```
Topic: "rainy day"
Haiku: "Soft drops descending / Windows blur with liquid art / Earth drinks deeply now"

Topic: "morning coffee"
Haiku: "Steam rises upward / Bitter warmth brings consciousness / Day begins anew"

Topic: "autumn leaves"
Haiku: ?
```

### Code Generation

```
Task: "Create a function that adds two numbers"
Code:
```python
def add(a, b):
    return a + b
```

Task: "Create a function that multiplies two numbers"
Code:
```python
def multiply(a, b):
    return a * b
```

Task: "Create a function that finds the maximum of two numbers"
Code: ?
```

## Advanced Few-Shot Techniques

### Chain-of-Thought Few-Shot
Combine few-shot with reasoning steps.

```
Q: "A shirt costs $20. It's on sale for 25% off. What's the final price?"
A: Let's solve step by step:
   - Original price: $20
   - Discount: 25% of $20 = $5
   - Final price: $20 - $5 = $15

Q: "A laptop costs $800. It's on sale for 15% off. What's the final price?"
A: Let's solve step by step:
   - Original price: $800
   - Discount: 15% of $800 = $120
   - Final price: $800 - $120 = $680

Q: "Headphones cost $60. They're on sale for 30% off. What's the final price?"
A: ?
```

### Structured Few-Shot
Use clear structure for complex outputs.

```
Product: "Wireless Headphones - $79.99"

Analysis:
- Category: Electronics
- Price Point: Mid-range
- Keywords: wireless, headphones, audio
- Target Audience: Consumers seeking portable audio
- Competitive Position: Affordable quality option

Product: "Gaming Laptop - $1,299.99"

Analysis:
- Category: Computers
- Price Point: Premium
- Keywords: gaming, laptop, high-performance
- Target Audience: Gamers and power users
- Competitive Position: High-end gaming market

Product: "Fitness Tracker - $49.99"

Analysis: ?
```

### Negative Examples
Show what NOT to do.

```
Input: "summarize this article about AI"

❌ Bad: "AI is a thing."
Reason: Too brief, no useful information

✅ Good: "The article discusses artificial intelligence applications in healthcare, including diagnostic tools, treatment planning, and patient monitoring systems."
Reason: Captures key points with appropriate detail

Input: "summarize this article about climate change"

❌ Bad: "Climate change is happening and is caused by human activities through greenhouse gas emissions leading to global temperature rise affecting weather patterns ecosystems sea levels and..."
Reason: Run-on sentence, too much detail, no structure

✅ Good: "The article examines climate change impacts, causes, and potential solutions, focusing on the role of carbon emissions and renewable energy transitions."
Reason: Concise, well-structured, covers main points

Now summarize:
Input: "summarize this article about renewable energy"
```

## Real-World Examples

### Example 1: Email Auto-Response Classification

```
Email: "Can you send me the Q4 report by Friday?"
Action: "Forward to team lead"
Priority: "High"
Reasoning: "Time-sensitive request requiring specific deliverable"

Email: "Thanks for your help yesterday!"
Action: "No action needed"
Priority: "Low"
Reasoning: "Acknowledgment only, no request"

Email: "URGENT: Server down, clients can't access the system"
Action: "Escalate to IT immediately"
Priority: "Critical"
Reasoning: "System outage affecting customers"

Email: "I'd like to schedule a meeting sometime next month"
Action: "Add to calendar review list"
Priority: "Medium"
Reasoning: "Meeting request with flexible timing"

Now classify:
Email: "The client presentation is tomorrow and the slides aren't ready"
Action: ?
Priority: ?
Reasoning: ?
```

### Example 2: Code Comment Generation

```
Code: `total = sum(prices)`
Comment: "Calculate the total by summing all prices in the list"

Code: `user = db.query(User).filter_by(id=user_id).first()`
Comment: "Retrieve the first user from database matching the given user_id"

Code: `sorted_items = sorted(items, key=lambda x: x.price, reverse=True)`
Comment: ?
```

### Example 3: Customer Support Response Templates

```
Issue: "My order hasn't arrived and it's been 2 weeks"
Response Type: Empathetic + Investigation
Template: "I understand your concern about the delayed order. Let me check the shipping status immediately. Could you please provide your order number so I can investigate and provide you with an update?"

Issue: "How do I reset my password?"
Response Type: Helpful + Direct
Template: "I'd be happy to help you reset your password. Please click the 'Forgot Password' link on the login page, enter your email, and follow the instructions sent to your inbox. If you don't receive the email within 5 minutes, please check your spam folder."

Issue: "Your product is terrible and I want a refund!"
Response Type: ?
Template: ?
```

## Practice Exercises

**Exercise 1: Create Few-Shot Examples**
Create 3-4 few-shot examples for teaching AI to:
"Convert informal text to professional tone"

Example format:
Input: [informal text]
Output: [professional version]

**Exercise 2: Improve Weak Examples**
These few-shot examples are weak. Improve them:

```
Text: "good" → "positive"
Text: "bad" → "negative"

Classify: "The service was outstanding!" → ?
```

What's wrong? How would you improve it?

**Exercise 3: Design Few-Shot for Your Need**
Think of a task you frequently do. Design a few-shot prompt with 3-5 examples that would teach AI to help you with it.

## Common Mistakes

1. **Too few examples for complex tasks**
   - ❌ One example for a nuanced classification task
   - ✅ 4-5 examples showing different nuances

2. **Examples don't match actual use case**
   - ❌ Examples about animals when you need business text
   - ✅ Examples from the actual domain

3. **Inconsistent formatting**
   - ❌ Different formats for each example
   - ✅ Identical structure across all examples

4. **Missing edge cases**
   - ❌ Only showing typical cases
   - ✅ Include at least one tricky example

5. **Too similar examples**
   - ❌ All examples are almost identical
   - ✅ Examples show variety within the pattern

6. **Unclear pattern**
   - ❌ Examples don't clearly demonstrate what you want
   - ✅ Pattern is obvious from the examples

## Pro Tips

1. **Start with 3**: Three examples often hit the sweet spot
2. **Test your examples**: Try them with the actual task first
3. **Cover the spectrum**: Include examples from different parts of the range
4. **Make format obvious**: Use clear delimiters (→, |, :, etc.)
5. **Include instructions**: Add a line like "Follow the same pattern:"
6. **Iterate**: If output is wrong, add an example showing the correct way
7. **Use labels**: "Example 1:", "Example 2:" helps clarity
8. **Progressive complexity**: Start simple, gradually add complexity
9. **Quality over quantity**: 3 great examples > 10 mediocre ones
10. **Document patterns**: Note what pattern your examples demonstrate

## Few-Shot Template

```
Task: [Brief description of what you want]

Examples:

Example 1:
Input: [First example input]
Output: [First example output]

Example 2:
Input: [Second example input]
Output: [Second example output]

Example 3:
Input: [Third example input]
Output: [Third example output]

Now apply this pattern:
Input: [Your actual input]
Output: ?
```

## When to Use Few-Shot

**Best for:**
- Pattern-based tasks
- Classification problems
- Format transformations
- Style matching
- Consistent output structure
- Teaching specific behavior

**Not ideal for:**
- Simple definitions
- Open-ended creative tasks
- When examples are hard to create
- Highly variable outputs
- Tasks requiring deep reasoning (use CoT instead)

## Key Takeaways

✓ Few-shot teaches through examples, not just instructions  
✓ 3-5 examples work for most tasks  
✓ Examples should be representative and consistent  
✓ Include edge cases in your examples  
✓ Clear formatting makes patterns obvious  
✓ Combine with other techniques (CoT, role, etc.)  
✓ Quality examples are crucial  

## Next Steps
Learn about self-correction prompts to get AI to review and improve its own outputs.
