# Objective

## Identify and correct prompts that produce wrong or made-up information.

### Step 1: Write a prompt that produces errors

```
Prompt:

Biographies of non-existent scientists
```

```
Output:

1. Dr. Aristhone "The Clockmaker" Vane (1842–1912)

- Field: 

Chrono-Biology

- Known for:

The invention of the **Circadian Gear**, a device that supposedly synchronized human sleep cycles with the rotation of the Earth’s magnetic core.

- The Life:

Born in a small village in the Swiss Alps, Vane spent his youth repairing broken watches. He became obsessed with the idea that the human heart was merely a wet clock that lost its timing due to urban stress.

- The Legacy:

In 1889, he claimed to have lived a 48-hour day for three years, performing surgeries with superhuman precision. While his peers at the Royal Society called him a fraud, his journals—filled with sketches of brass lungs and spring-loaded veins—inspired the entire Steampunk movement of the 20th century.


2. Professor Elara Voss (1974–2021)

- Field:

Xeno-Linguistics and Acoustic Archaeology

- Known for:

The **Silent Symphony Theory**, which proposed that ancient ruins record the sounds of history within the molecular structure of their stone walls.

- The Life:

Voss was a recluse who spent most of her career in the basement of the Sorbonne. She didn't use telescopes or microscopes; she used hyper-sensitive contact microphones. She famously claimed that the Pyramids of Giza weren't tombs, but a massive granite playlist of Old Kingdom folk songs.

-The Legacy:

She disappeared during an expedition to the Mariana Trench, where she claimed to have heard the ocean floor humming a lullaby. Her final published paper consisted entirely of sheet music derived from the vibration of tectonic plates.


3. Dr. Ichika Sato (2010–2085)

- Field:

Synthetic Gastronomy & Molecular Sociology

- Known for:

Developing **Emotional Nutrition** food that changes flavor based on the consumer's neurochemical state.

- The Life

Operating out of Neo-Tokyo, Sato realized that world hunger wasn't just about calories, but about soul-satiety. She engineered a type of rice that tasted like a grandmother’s cooking when the eater was lonely, and like sharp citrus when they needed to focus.

- The Legacy

Sato is credited with ending the Great Malaise of the 2060s. Her Nobel Prize in Chemistry (which she accepted via a holographic avatar) was the first ever awarded for a recipe: a simple broth that reportedly made two warring diplomats burst into tears and sign a peace treaty.
```

### Step 2: Rewrite the prompt so it only accepts correct data

```
Prompt:

Biographies of scientists that actually existed:
```

```
Output:

1. Sir Isaac Newton (1642–1727)

- Fields: Physics, Mathematics and Astronomy 

Life: Born prematurely on Christmas Day in Woolsthorpe, England, Newton was a solitary child who initially struggled with farm management before finding his stride at Cambridge University. His most productive years occurred during the Great Plague (1665–1666), when he retreated to his family home and independently developed his core theories in solitude.

Legacy: Newton is the "culminating figure of the Scientific Revolution," providing a mathematical framework for the physical universe that dominated for over 200 years. He was the first scientist ever to be knighted and served as the President of the Royal Society for 24 years.

Known For: Formulating the three laws of motion and the law of universal gravitation, which unified the physics of Earth and the heavens. He also invented calculus and built the first practical reflecting telescope. 

2. Marie Curie (1867–1934)

- Fields: Physics, Chemistry and Radiology

Life: Born Maria Skłodowska in Warsaw, Poland, she moved to Paris in 1891 to study at the Sorbonne while living in extreme poverty. She formed a legendary scientific partnership with her husband, Pierre Curie, until his tragic death in a carriage accident in 1906.

Legacy: A pioneer for women in academia, she was the first female professor at the University of Paris and the first woman to be enshrined in the Paris Panthéon on her own merits. Her work established the field of nuclear chemistry and revolutionized cancer treatment.

Known For: Coining the term "radioactivity" and discovering the elements polonium and radium. She remains the only person to win Nobel Prizes in two different scientific fields (Physics and Chemistry).
    
3. Albert Einstein (1879–1955)

- Field: Theoretical Physics and Cosmology

Life: Born in Ulm, Germany, Einstein was a clerk in the Swiss Patent Office when he published four groundbreaking papers in 1905, his annus mirabilis (miracle year). He later emigrated to the United States in 1933 to escape the rise of the Nazi regime, spending the rest of his life at the Institute for Advanced Study in Princeton.

Legacy: Einstein became a global cultural icon, frequently named the most influential physicist of the 20th century. Beyond science, he was a staunch advocate for civil rights, pacifism, and global cooperation.

Known For: Developing the general and special theories of relativity, which reshaped our understanding of space, time, and gravity. He is also famous for the equation and his explanation of the photoelectric effect.
```

### Step 3: Comparing both results and noting differences:
```
Although both outputs was simplified, the information given differs greatly. The first prompt produces an entirely fabricated scientists, fake and imaginary fields and achievements, due to the fact that it did not require real individuals. In contrast, the second prompt restricted the output to produce scientists that actually existed. This restriction guided the response towards individuals that actually existed, with real and documented achievements. Therefore, a vague prompt can increase the risk of hallucination and false information, but the addition of restrictions reduces the risk and improves accurate results.
```
