# Objective

## Force responses to be tied to given material.

### Step 1: Write a factual question prompt (Without Constraints)
```
Prompt:

What was the cause of the great depression
```
```
Output:

The Great Depression was not caused by a single event, but rather a perfect storm of overlapping economic and policy failures. While the Stock Market Crash of 1929 is often cited as the trigger, economists and historians generally agree it was one of several contributing factors.

Source: Great Depression — Wikipedia.
```
### Step 2: Add Instructions (With Constraints)
```
What was the cause of the great depression, using the text below, cite your source in the answer

The Great Depression was a devastating and prolonged economic recession that followed the crash of the United States stock market in 1929. It lasted through 1941, the same year that the U.S. entered World War II. The period was marked by several economic contractions, including the stock market crash of 1929, banking panics in 1930 and 1931. and the Smoot-Hawley Tariff that crashed world trade. Other events and policies helped to prolong the Depression during the 1930s. Economists and historians often cite the Great Depression as the most significant, if not the most catastrophic, economic event of the 20th century.
```
```
Output:
Based on the text you provided, the causes of the Great Depression include:

- The crash of the United States stock market in 1929 (often called the Wall Street Crash of 1929)

- Banking panics in 1930 and 1931

- The Smoot-Hawley Tariff Act, which severely reduced world trade.

The text explicitly states that the Depression “followed the crash of the United States stock market in 1929” and was further prolonged by banking failures and the Smoot-Hawley Tariff that “crashed world trade.”

Source: The passage provided in the question.
```

### Step 3: Observation:

The output from the constrainted prompt strictly used the passage and avoided using outside knowledge. Each answer is traceable to the text, thereby reducing the risk of hallucination.
