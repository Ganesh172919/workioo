# Spaced Repetition with AI

## What is Spaced Repetition?

Spaced repetition is reviewing information at increasing intervals. Instead of cramming, you review just before you're about to forget - maximizing retention with minimal time.

**Traditional:** Review everything equally ❌  
**Spaced:** Review based on forgetting curve ✓

## The Forgetting Curve

```
Memory
100% ─┐
      │╲
 75%  │ ╲  ← Review here
      │  ╲
 50%  │   ╲
      │    ╲
  0%  └────────→ Time
     1h 1d 3d 7d 14d 30d
```

## Why AI + Spaced Repetition is Powerful

1. **Dynamic scheduling**: AI adjusts intervals based on YOUR memory
2. **Content generation**: Creates review material automatically
3. **Adaptive difficulty**: Makes reviews appropriately challenging
4. **Pattern recognition**: Identifies what you struggle with
5. **Zero maintenance**: No manual flashcard creation

## Basic Spaced Repetition Prompt

```
"Help me learn [topic] with spaced repetition:

Today (Day 1): Teach me [concept]
Day 2: Test me on it (first review)
Day 4: Test again (second review)
Day 7: Third review
Day 14: Fourth review
Day 30: Fifth review

Adjust intervals based on my performance:
- If I remember well: Longer interval next time
- If I struggle: Shorter interval next time

Track my progress through all reviews."
```

## Spaced Repetition Schedules

### Conservative Schedule (High Retention)
```
Review Intervals:
- 1 hour after learning
- 1 day later
- 3 days later
- 7 days later
- 14 days later
- 30 days later
- 60 days later

Use when: Information is critical, can't afford to forget
```

### Aggressive Schedule (Efficient)
```
Review Intervals:
- 1 day after learning
- 4 days later
- 10 days later
- 25 days later
- 60 days later

Use when: Large volume of material, some forgetting acceptable
```

### Adaptive Schedule (AI-Driven)
```
"Adjust intervals based on my recall:

Easy (remembered perfectly):
→ Multiply interval by 2.5

Good (remembered with effort):
→ Multiply interval by 2.0

Hard (struggled but got it):
→ Multiply interval by 1.3

Failed (couldn't remember):
→ Reset to 1 day

Track difficulty for each item individually."
```

## AI-Powered Spaced Repetition Patterns

### Pattern 1: Smart Scheduling

```
"I'm learning [multiple topics]. Manage spaced repetition:

Track for each topic:
- When I learned it
- Last review date
- Performance on last review (Easy/Good/Hard/Fail)
- Next scheduled review

Today is [date]. Tell me:
1. What topics are due for review today
2. Expected difficulty based on interval
3. After I complete reviews, schedule next sessions

Maintain review calendar across multiple conversations."
```

### Pattern 2: Difficulty-Adjusted Reviews

```
"Review [topic] learned on [date] with adaptive difficulty:

First question: Easier (broad recall)
→ If correct: Medium difficulty next
→ If incorrect: Stay at easy level

Medium question: Standard recall
→ If correct: Hard question next
→ If incorrect: Back to easy

Hard question: Deep understanding
→ If correct: Mark as 'mastered', long interval
→ If incorrect: More practice needed, shorter interval

Based on overall performance, schedule next review."
```

### Pattern 3: Interleaved Spaced Practice

```
"I've learned [Topic A, Topic B, Topic C] on different days.

Create mixed review session:
- Include items due from all topics
- Randomize order
- Don't group by topic (tests real recall)
- After each item, rate difficulty
- Adjust future schedule for each

This simulates real-world recall situations."
```

### Pattern 4: Pre-Review Preparation

```
"Tomorrow I have scheduled reviews for [topics].

Before the review:
1. List topics I'll be tested on
2. My last performance on each
3. Predicted difficulty
4. Brief context reminder (no content reveal)
5. Mental preparation tips

After review:
- Compare predicted vs actual difficulty
- Adjust scheduling
- Note improvements or concerns"
```

## Creating Effective Review Sessions

### Quick Review (5-10 minutes)

```
"Quick spaced repetition review:

Due today: [List of items]

For each:
1. Question (no hints)
2. I answer
3. You confirm/correct
4. Rate: Easy/Good/Hard/Again
5. Schedule next review

Rapid-fire format, move quickly."
```

### Deep Review (20-30 minutes)

```
"Comprehensive review session:

Items due: [List]

For each:
1. Initial recall question
2. If correct: Follow-up application question
3. If incorrect: Explain, then simplified question
4. Connection question (relate to other knowledge)
5. Rate confidence and schedule

Include mini-lessons on frequently missed items."
```

### Weekly Consolidation

```
"Weekly review of [topic]:

Show me:
1. All items learned this week
2. Items I struggled with
3. Items mastered
4. Connections between concepts

Combined review:
- Mix old and new material
- Focus on integration
- Test understanding at system level

Adjust overall strategy based on weekly patterns."
```

## Real-World Examples

### Example 1: Learning Vocabulary

```
"Spanish vocabulary with spaced repetition:

New words learned today: [list 20 words]

Schedule reviews:
Day 1 (today): Learn words with context
Day 2: Quick recall test (all 20 words)
Day 4: Test words I got wrong on Day 2
Day 7: Test all 20 again
Day 14: Test only difficult words
Day 30: Final review

For each review:
- Spanish → English (recognition)
- English → Spanish (recall, harder)
- Use in sentence (application)

Adjust intervals based on my performance on each word individually."
```

### Example 2: Programming Concepts

```
"Learning data structures with spaced repetition:

Week 1: Arrays, Linked Lists
Week 2: Stacks, Queues
Week 3: Trees, Graphs

Spaced reviews:
- Week 1 content: Review Day 2, 5, 10, 20
- Week 2 content: Review Day 2, 5, 10, 20
- Week 3 content: Review Day 2, 5, 10, 20

Review format:
1. Concept explanation test
2. Implementation from memory
3. Problem-solving with that structure
4. Comparison with other structures

Track: Which structures I confuse, adjust practice."
```

### Example 3: Exam Preparation

```
"Biology exam in 8 weeks. Spaced repetition schedule:

Week 1-2: Learn all topics
Week 3-8: Spaced reviews

Optimal schedule:
- High-priority topics: Review every 3 days
- Medium priority: Review every 5 days
- Low priority: Review every 7 days

6 weeks before exam: Review everything
4 weeks before: Review weak areas twice
2 weeks before: Final comprehensive review
1 week before: Focus on most forgotten items

Adapt based on practice test results."
```

## Advanced Spaced Repetition Techniques

### Technique 1: Leitner System with AI

```
"Implement Leitner system for [topic]:

5 boxes with different intervals:
- Box 1: Daily review (new/difficult items)
- Box 2: Every 2 days
- Box 3: Every 4 days
- Box 4: Every 7 days
- Box 5: Every 14 days (mastered)

Rules:
- Correct answer: Move to next box
- Incorrect: Move back to Box 1

Track:
- What's in each box currently
- Due for review today
- Progress over time

Tell me what to review each day."
```

### Technique 2: Graduated Intervals

```
"Use graduated intervals for [concepts]:

New items start at: 1 day
Each successful review: Interval × multiplier

Multiplier based on difficulty:
- Easy: ×2.5 (grows fast)
- Good: ×2.0 (moderate growth)
- Hard: ×1.5 (slow growth)
- Fail: Reset to 1 day

Maximum interval: 180 days (then maintain)

This balances efficiency with retention."
```

### Technique 3: Anticipatory Scheduling

```
"Predict my forgetting curve for [topic]:

Based on:
- Initial learning quality
- Complexity of material
- My performance on similar topics
- Time since last review

Predict:
- Current retention level
- Optimal next review time
- Expected difficulty
- Items most likely to be forgotten

Schedule proactively before forgetting occurs."
```

### Technique 4: Meta-Review Sessions

```
"Periodic meta-review for [subject]:

Every 2 weeks, analyze:
1. Which topics have shortest intervals (struggling)
2. Which have longest intervals (mastered)
3. Overall retention trend
4. Items that keep resetting
5. Patterns in my forgetting

Adjust strategy:
- More frequent reviews for weak areas
- Different explanation for confusing topics
- Connect difficult concepts to known material

Show me the analysis and recommendations."
```

## Integration with Other Learning Techniques

### With Active Recall

```
"Combine spaced repetition + active recall:

Spaced schedule: When to review
Active recall: How to review

Each review session:
1. Scheduled based on interval
2. Conducted via active recall (no hints)
3. Performance affects next interval
4. Weak items get extra active recall practice

Both techniques reinforce each other."
```

### With Interleaving

```
"Spaced + interleaved practice for [subjects]:

Don't just space single topics.
Space different topics and mix them:

Session 1: Review A₁, B₁, C₁ (oldest from each)
Session 2: Review A₂, C₂, B₂ (mixed order)
Session 3: Review B₃, A₃, C₃ (different mix)

This is harder but more effective for real understanding."
```

## Tracking and Optimization

### Performance Metrics

```
"Track my spaced repetition effectiveness:

For [topic/period]:
- Total items learned: [X]
- Average retention rate: [%]
- Items in each interval: [breakdown]
- Most difficult items: [list]
- Items mastered: [list]
- Time spent reviewing: [hours]

Calculate:
- Efficiency (retention per hour)
- Weak areas needing focus
- Optimal review frequency for me
- Predicted mastery date"
```

### Schedule Optimization

```
"Optimize my review schedule:

Current schedule: [describe]
Results so far: [retention rates]

Analyze:
- Are intervals too long? (high forgetting)
- Too short? (wasting time)
- Which topics need adjustment?

Recommend:
- Ideal intervals for my memory
- Topics to review more/less frequently
- Better time distribution

Test new schedule for 2 weeks, then reassess."
```

## Practice Exercises

**Exercise 1: Plan Your Schedule**
For something you're learning:
- List main concepts
- Design spaced review schedule
- Plan what each review will test
- Set up tracking method

**Exercise 2: Simulate Reviews**
Take any 5 pieces of information:
- Day 1: Learn them
- Day 2: Test recall
- Rate each (Easy/Good/Hard)
- Calculate next review dates
- Compare to what you'd naturally do

**Exercise 3: Analyze Your Forgetting**
Think about something you learned and forgot:
- When did you learn it?
- When did you forget it?
- When should you have reviewed?
- Design optimal schedule to prevent forgetting

## Common Mistakes

1. **Reviewing too early**: Waiting helps strengthen memory
2. **Giving up too soon**: Spaced repetition shows benefits over weeks
3. **Irregular reviews**: Consistency is crucial
4. **Not tracking**: Can't optimize without data
5. **Reviewing too much**: More isn't always better
6. **Ignoring difficulty ratings**: All items need same treatment
7. **No adjustments**: Schedule should evolve based on performance

## Pro Tips

1. **Start conservative**: Better too frequent than losing information
2. **Be honest about difficulty**: Accurate ratings = better scheduling
3. **Review at consistent times**: Build habit (e.g., every morning)
4. **Don't skip due reviews**: Compounds the forgetting
5. **Celebrate progress**: Note items reaching longer intervals
6. **Adjust for importance**: Critical info gets shorter intervals
7. **Combine with sleep**: Review before bed for better consolidation
8. **Use idle time**: Perfect for commute, waiting, etc.

## Templates

**Quick Start:**
```
"Set up spaced repetition for [topic]:
- Today: Learn [concepts]
- Schedule reviews: 1d, 3d, 7d, 14d, 30d
- Remind me when reviews are due
- Track performance"
```

**Comprehensive:**
```
"Full spaced repetition system for [subject]:

Phase 1: Initial learning (Week 1-2)
Phase 2: Intensive reviews (Week 3-4)
Phase 3: Maintenance (Week 5+)

For each phase:
- Review frequency
- Types of questions
- Performance tracking
- Schedule adjustments

Monitor retention rate and optimize schedule."
```

**Maintenance:**
```
"Maintain knowledge of [topic]:
- Learned: [date]
- Last review: [date]
- Next review: [calculate]
- Current interval: [X days]

If I fail today's review:
→ Reset to 2-day interval

If I succeed:
→ Double current interval

Continue indefinitely for long-term retention."
```

## Key Takeaways

✓ Review just before forgetting for optimal retention  
✓ Increase intervals after successful recalls  
✓ Reset to short intervals after failures  
✓ Track performance to optimize your personal schedule  
✓ AI can manage complex scheduling automatically  
✓ Combine with active recall for maximum effect  
✓ Consistency over time beats cramming  

## Next Steps

- Start spaced repetition for one topic
- Track your first week of reviews
- Adjust intervals based on results
- Move on to Concept-Strengthening Prompts to deepen understanding
