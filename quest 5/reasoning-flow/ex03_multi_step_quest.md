# Objective

## Break complex questions into smaller steps.

### Step 1: Select a multi-step question
```
- Question:

A store gives a 20% discount on a ₦15,000 item. After the discount, a 7.5% tax is added. What is the final price?
```

### Step 2: Create a prompt that asks the model to:

- Restate the problem

- Break it into smaller steps

- Solve each step before giving the final answer

```
- Restate the problem:

The goal is to determine the final amount a customer pays for an item originally priced at ₦15,000. 

This involves first reducing the price by a 20% discount and then applying a 7.5% tax to the remaining balance.
```

```
- Break it into smaller steps:

Step 1: Calculate the discount amount

Step 2: Calculate the price after the discount

Step 3: Calculate the tax amount

Step 4: Calculate the final price
```

```
- Solve each step before giving the final answer:

Step 1: Calculate the discount amount:

The discount is 20% of the original price (₦15,000).

Discount = 0.20 × 15,000 = ₦3,000

Step 2: Calculate the price after the discount:

Subtract the discount amount from the original price.

Price after discount = 15,000 − 3,000 = ₦12,000

Step 3: Calculate the tax amount:

The 7.5% tax is applied to the discounted price (₦12,000).

Tax = 0.075 × 12,000 = ₦900

Step 4: Calculate the final price

Add the tax amount to the price after the discount.

Final Price = 12,000 + 900 = ₦12,900
```
```
- Final Answer

The final price of the item is ₦12,900.
```

### Step 3: Review and accuracy check

The model successfully restated the problem. It then broke it down into smaller, simpler steps by first calculating the 20% discount, subtracting it from the original price, and then calculating the tax on the discounted amount. Each step was solved properly before moving to the next, and the final answer was accurate.
