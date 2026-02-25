# Objective

## Create a reusable prompt for text summarizing.

### Step 1: Write a weak prompt:

#### Prompt 1 (Weak prompt):
```
Prompt:

Summarize this text:

Text:

The rising worldwide development of schooling has highlighted the vital significance of advanced innovations in working with online stages for leading classes, sharing assets, directing evaluations, and overseeing scholastic foundations extensively. At first, there was a proactive reception of these stages, yet the Coronavirus pandemic sped up the progress to web-based showing techniques, fundamentally helping exceptionally created countries. However, this  shift also presented significant challenges for developing countries, which faced obstacles in effectively implementing and accessing digital education resources. This global crisis emphasizes the urgency of international integration within education systems, with digital technologies instrumental in nurturing critical skills essential for professional competence, including problem-solving, structured thinking, and adeptness  with processes, preparing students for an increasingly unpredictable future reliant on technology. Educational resources and digital tools significantly enhance classroom dynamics, making the teaching-learning process more engaging and adaptable. Moreover, they grant educational institutions greater flexibility to tailor curricula based on individual student needs.

Output:

The text discusses the growing importance of digital technologies in education, especially with the shift to online learning during the COVID-19 pandemic. While developed countries benefited significantly, developing nations faced challenges in accessing digital resources. It emphasizes the need for global integration in education systems and highlights how digital tools enhance learning, flexibility, and skill development for the future.
```

### Step 2: Refine it into a reusable pattern:

#### Prompt 2 (Refined):
```
Prompt:

Summarize this text in 3 bullet points, focusing on the main arguments and ignoring examples:

Text:

The rising worldwide development of schooling has highlighted the vital significance of advanced innovations in working with online stages for leading classes, sharing assets, directing evaluations, and overseeing scholastic foundations extensively. At first, there was a proactive reception of these stages, yet the Coronavirus pandemic sped up the progress to web-based showing techniques, fundamentally helping exceptionally created countries. However, this  shift also presented significant challenges for developing countries, which faced obstacles in effectively implementing and accessing digital education resources. This global crisis emphasizes the urgency of international integration within education systems, with digital technologies instrumental in nurturing critical skills essential for professional competence, including problem-solving, structured thinking, and adeptness  with processes, preparing students for an increasingly unpredictable future reliant on technology. Educational resources and digital tools significantly enhance classroom dynamics, making the teaching-learning process more engaging and adaptable. Moreover, they grant educational institutions greater flexibility to tailor curricula based on individual student needs.

Output:

- Digital technologies have become essential in modern education for online learning, resource sharing, assessments, and institutional management.

- The COVID-19 pandemic accelerated the global shift to online education, benefiting developed countries while exposing challenges in developing nations.

- Digital tools enhance skill development, classroom engagement, and curriculum flexibility, preparing students for a technology-driven future.
```

### Step 3: Test with two inputs (news article and blog post)
```
News Article:

Prompt 1:

Summarize this text:

Sometimes, the simplest technologies are the most powerful. Inside the table tennis arena, I felt the electricity in the atmosphere as fans rallied behind Japan, a global powerhouse in the sport. But instead of focusing on the ball's rhythmic rally, deaf spectators are invited to look up. Above the court, giant animated graphics flash across a screen: bold Japanese onomatopoeic words that mirror the rhythm of play. Each strike is matched with expressive characters that visually represent sound effects; the impact of the ball, the speed of the rally, the power of a smash. Sound, translated into language you can see. Onomatopoeia; words that imitate sounds; plays a unique role in Japanese culture, where visual sound expressions are widely used in manga and media. At the Deaflympics, that cultural familiarity becomes an accessibility tool. For some fans, especially newcomers to the sport, the system provides instant context: how fast the rally is, when a point is decisive, when momentum shifts.

Output:

The article describes how animated Japanese onomatopoeic graphics are used at a table tennis event to help deaf spectators follow the game. These visual sound effects represent the rhythm, speed, and impact of play. The system uses Japan’s cultural familiarity with visual sound expressions to improve accessibility and provide better context during matches.

Prompt 2:

Summarize this text in 3 bullet points, focusing on the main arguments and ignoring examples:

Output:

- Animated Japanese onomatopoeic graphics are used during table tennis matches to visually represent sounds for deaf spectators.

- The system translates the rhythm, speed, and impact of gameplay into expressive visual language.

- This approach improves accessibility and leverages Japan’s cultural familiarity with visual sound expressions to enhance understanding of the sport.
```
```
Blog Post:

Prompt 1:

Summarize this text:

It’s often said that we are the average of the five people we spend the most time with. In 2026, I’d argue that’s no longer true: we are now the average of the five AI agents we delegate our lives to. We are moving past the parlor trick phase of generative AI; where making a chat bot write a poem about a toaster was peak entertainment into the utility phase, where these engines are effectively becoming junior partners in our personal and professional lives. But here is the rub: the best AI isn’t a single brand. Just as you wouldn’t use a high-performance sports car to haul a load of gravel, you shouldn’t rely on a general-purpose chat bot to manage your tax liability or review a prenuptial agreement. The trick to staying ahead and staying sane is selecting a curated cabinet of AI engines tailored to specific high-value tasks.

Output:

The blog post argues that people are increasingly shaped by the AI tools they use rather than just the people around them. It suggests that generative AI has moved beyond novelty and is becoming a practical assistant in daily life. The author emphasizes that different AI tools should be used for different specialized tasks instead of relying on one general-purpose system.

Prompt 2:

Summarize this text in 3 bullet points, focusing on the main arguments and ignoring examples:

Output:

- People are increasingly influenced by the AI tools they rely on, as generative AI becomes integrated into daily life and work.

- AI has transitioned from entertainment novelty to a practical partner for personal and professional tasks.

- Different AI systems should be selected strategically for specialized tasks rather than relying on one general-purpose tool.
```

### Validating the output:

The weak prompt has no length control, compared to the strong prompt whose length was specified (3 bullet points). The weak prompt also had no focus, as it just gave a general summary, unlike the strong prompt whose main focus was on the main argument, and the strong prompt output format was well specified.
