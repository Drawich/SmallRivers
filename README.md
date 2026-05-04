# Small Rivers
Final project for the Building AI section in AI Fundamentals 2 at Linköping University (LiU).

## Summary
Small Rivers is a conversational AI coach that helps users understand the hidden opportunity cost of modern media consumption habits. It is based on the idea that “small streams make an ocean”. The small recurring costs (subscriptions or movie tickets turning into streams) accumulate over time, creating an ocean of missed opportunities and dreams. 

Instead of restricting behavior, Small Rivers uses reflective dialogue and personalized comparisons to help users align short-term habits with meaningful long-term goals. Over time, users develop a more intentional approach to spending that aligns with their personal values and long-term goals.

## Background
In the United States, many people underestimate how small recurring expenses affect their long-term financial goals. These costs are often perceived as insignificant in isolation but can accumulate into substantial amounts over time. 
- **The Consumption Paradox:** According to Pew Research Center (2025), 77% of low-income adults in the US maintain streaming subscriptions (e.g. Netflix, $8.99-$26.99/month). Despite financial constraints, digital convenience remains a priority, highlighting how small recurring costs are normalized.
- **The Debt vs. Pleasure Gap:** Gen Z carries an average of $34,328 in debt (Experian, 2025), while cinema attendance in this group grew by 25% over the past year (Cinema United, 2025). This suggests a disconnect between spending on short-term impulses and financial stability.
- **Behavioral framing challenge:** Many users do not perceive small recurring costs as meaningful financial decisions. Small Rivers disrupts this "just a few dollars" mindset by visualizing the long-term impact of these choices. The goal isn't to stop spending, but to ensure that every dollar spent is a conscious choice that aligns with the user's future.

## How is it used?
Small Rivers is a multi-turn conversational AI agent. Users report their media-related expenses or intended purchases, and the system responds with reflections, projections, and comparisons. For example, a user might mention a subscription, and the system can show its long-term cost or compare it to potential investment growth.

The interaction is continuous, allowing users to revisit decisions, adjust habits, and reflect on how their spending evolves.

The system is restricted to non-essential media spending (e.g. streaming services, cinema visits, digital purchases) to avoid interfering with essential financial decisions such as food, housing, or healthcare.

**Example Interaction:**
1. A user reports having both a Netflix ($19.99/month) and Disney+ ($18.99/month) subscription.
2. The system first acknowledges the value of the user’s choice to avoid judgment. It may ask follow-up questions to understand the user's reasoning.
    - Example: *“Having access to a wide range of shows and movies can be a great way to relax and unwind. Are there any shows you’re currently following that are only available on one platform?”*
3. The system then presents a “what if” comparison to make the long-term impact visible:
    - **Path 1** – *Current Habit*: Keeping both subscriptions would cost approximately $2,339 over 5 years.
    - **Path 2** – *Opportunity*: If the same $38.98/month were invested with a historical average return of ~10% (based on the S&P 500), it could grow to approximately $2,918.50 over 5 years, and in 20 years, it would be $27,053.19 despite only putting in ~$9,400 of your own money (Source: compound interest calculator – investor.gov).
    - **Path 3** – *Middle Ground*: If the user prefers not to give up both services, the system explores alternatives. For example:
        - Example: *“What if you alternated between Netflix and Disney+ each year, while investing the difference? Over 20 years, this approach could accumulate to roughly $13,000, depending on contribution consistency and market performance assumptions.”*

### Core features
  - **Predictive Modeling (Linear Regression):** The agent uses reported habits and projects where the user will be in 5 years if the habit continues, while giving an alternative scenario where the same amount is invested. This is used to visualize long-term opportunity cost using historical market return assumptions (e.g. S&P 500 averages)
  - **The waiting tax:** Demonstrates how delaying investment reduces long-term gains. Example, showing the difference between investing $20 today vs. 5 years from now to motivate an early start and build stronger habits earlier.
  - **Multi-turn conversational nudging:** Instead of providing static feedback, the agent engages in a dialogue to challenge the user's assumptions and reinforce forward-looking thinking. It starts with stronger guidance and gradually shifts control back to the user as understanding improves.
  - **Interactive goal planning:** Goals are continuously linked to emotionally meaningful future outcomes to prevent motivation decay over time.
    
    Example of conversation: *"I know you've been thinking about seeing the new Star Wars movie at the cinema, but imagine walking by Luke Skywalker and Yoda as we make it into the Black Spire Marketplace at Disney World. Hearing the noise of the ships' engines in the background and alien chatter in the stalls. I'm getting a Jedi robe when we get there, and I am not taking it off until we get home! What are you planning to buy?"*

### Audience
- Users interested in improving financial awareness and decision-making
- Individuals with subscription-heavy or impulse-driven spending habits
- Learners exploring behavioral change in their spending habits

### Approach
  * Rather than restricting behavior, Small Rivers focuses on increasing awareness and supporting internal motivation. The system reframes financial decisions as long-term trade-offs and helps users align daily actions with their own stated goals.

The goal is not control, but self-directed behavioral change through reflection and projection.

## Challenges
### System Limitations
- **Scope restriction to non-essential spending:** The system is designed only for media-related expenses. It is not intended for essential financial domains (e.g. housing, healthcare). Using it outside its intended scope may lead to inappropriate interpretations of outputs.
- **Simplified financial model:** The system uses simplified projections based on historical averages (e.g. S&P 500). It does not account for real-world uncertainty such as income changes, inflation, or financial emergencies.
- **Dependency on user input:** The system relies on user-reported data. Incomplete or inaccurate input reduces output reliability and may introduce bias.
- **Narrow domain:** The system only addresses media consumption, limiting its applicability to broader financial decision-making.
  
### Ethical Implications
- **Behavioral influence and autonomy risk (High):** The system uses nudging and future-oriented framing that may influence user decisions. This raises concerns about autonomy and persuasive system design, as reflected in AI ethics discussions such as the EU AI Act.
- **Psychological impact (High):** The system may unintentionally create guilt or anxiety around normal discretionary spending by emphasizing opportunity costs. It is intended as a reflective tool, not a restrictive system, and users are expected to retain full decision-making autonomy.
- **Privacy and behavioral data (High):** User-reported spending behavior constitutes sensitive personal data. Even without external storage, it must be handled according to data minimization and privacy principles (e.g. GDPR).
- **Goal misalignment (Medium):** Users may have vague or conflicting goals, which can lead to recommendations that do not fully reflect their actual values or intentions.
- **Over-reliance risk (Medium):** Users may become dependent on the system for financial decision-making, reducing independent judgment through cognitive offloading.
- **Bias in financial framing (Medium):** The system assumes access to investment opportunities and frames reduced spending as beneficial, which may not reflect all socioeconomic contexts or user priorities.
- **Persuasive design escalation (Medium):** Continuous nudging may gradually increase persuasive intensity, shifting the system from reflective support toward behavioral optimization if not carefully constrained.
  
## What next?
The next step is to implement a prototype of SmallRivers and evaluate its behavior in practice. This includes building the conversational agent, integrating a simple financial projection model, and testing how it responds to reflective dialogue, behavioral nudging, and edge cases. The system will then be iteratively improved based on testing results, gradually refining performance through repeated evaluation and adjustment.

## Acknowledgments
This project was developed as part of the Building AI course at Linköping University (LiU). The assignment framework and course materials provided guidance for the design and evaluation of the system.
