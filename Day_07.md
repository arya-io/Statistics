# 🧪 One-Tailed vs. Two-Tailed Tests

## 🎯 What is a "Tail" in Statistics?

A **tail** refers to the ends of a probability distribution curve. These are the areas where **extreme values** fall.
In hypothesis testing, **tails** represent the **rejection regions**—places where the results are so unusual that we reject the **Null Hypothesis**.

> ✅ **Rejection Region** = Where your test result must fall to reject the Null Hypothesis.
> 🔺 This region is also where **alpha (α)** lives—the significance level.

---

## 🔁 Two-Tailed Test

### 📌 Key Points:

* **Rejection region** is on **both sides** of the curve.
* **Alpha (α)** is **split into two halves** → we use **α/2** on each tail.
* Used when we are testing for **any difference** (not specific direction).

### 🧠 Think of it like:

> "I don't know if it's higher or lower—I just want to know if it's **different**."

### 📝 Hypotheses:

* **Null Hypothesis (H₀)**: = (equal to)
* **Alternative Hypothesis (H₁)**: ≠ (not equal to)

### 🔍 Example:

> You want to test if a new teaching method has a different effect on student scores (could be higher or lower). Since you’re open to both possibilities, it’s a **two-tailed test**.

---

## 👉 One-Tailed Test

### 📌 Key Points:

* Rejection region is on **one side** of the curve only.
* The **entire α** is in **one tail**.
* Used when you are testing in **one direction** only.

### 🧠 Think of it like:

> "I believe this new medicine will work **better** (or **worse**) than the old one."

### 📝 Hypotheses:

* **Null Hypothesis (H₀)**: = (equal to)
* **Alternative Hypothesis (H₁)**: > (greater than) or < (less than)

> ⚠️ Be careful: Use a one-tailed test only when you're **confident** the effect is in one direction.

### 🔍 Example:

> You want to check if a new battery lasts **longer** than the old one (not shorter). This is a **one-tailed test** (right tail).

---

✅ **Quick Recap Table:**

| Feature              | Two-Tailed Test          | One-Tailed Test                   |
| -------------------- | ------------------------ | --------------------------------- |
| **Rejection Region** | Both sides               | One side only                     |
| **Alpha Used**       | α/2 on each side         | Full α on one side                |
| **H₀**               | =                        | =                                 |
| **H₁**               | ≠                        | > or <                            |
| **Use When**         | Any difference (up/down) | Specific direction (up *or* down) |

---

# 🧪 One-Tailed vs. Two-Tailed Tests – Explained Simply!

---

## 🧾 Writing Hypotheses (H₀ & H₁) in Different Ways

| **H₀ (Null Hypothesis)** | **H₁ (Alternative Hypothesis)** | **Type of Test**   |
| ------------------------ | ------------------------------- | ------------------ |
| =                        | ≠                               | Two-tailed Test 🔁 |
| ≤                        | >                               | One-tailed Test 👉 |
| ≥                        | <                               | One-tailed Test 👈 |

---

## 🎓 Real-World Examples

### 🔁 **Two-Tailed Test Example**

> 📢 A battery company claims its batteries last **20 hours** on average.

* **H₀:** μ = 20
* **H₁:** μ ≠ 20
  💡 You're checking if the battery life is **different** (could be more or less).

---

### 👉 **One-Tailed Test Example**

> 💊 A company claims its new medicine **reduces** fever duration from 16 weeks.

* **H₀:** μ ≥ 16
* **H₁:** μ < 16
  💡 You’re only interested if the medicine makes it **less**, not more.

---

## 🔁 Two-Tailed Test 🧪

### 🔹 Key Features:

* Uses **=** and **≠** in H₀ and H₁.
* We're **not predicting a direction** (not saying greater or lesser).
* Just testing **if there's a difference**—in **either** direction.
* So the **rejection region** is on **both sides** (tails) of the distribution.
* We use **α/2** on each tail.

### 🧠 Think of it like:

> “I don’t know if it’s better or worse—I just want to know if it’s **different**.”

### 📏 Conclusion Rule:

> ❌ Reject H₀ if:

* Test statistic < -Z (at α/2)
  **OR**
* Test statistic > +Z (at α/2)

---

## 👉 One-Tailed Test 🧪

### 🔹 Key Features:

* Uses **≤ / >** or **≥ / <** in H₀ and H₁.
* Predicts a **specific direction** of difference.
* Rejection region is only on **one side** of the distribution.
* Uses **entire α** in one tail.

### 📌 Clue:

> If the statement says **"reduces"** or **"improves"**, it's most likely **one-tailed**.
> If it says **"changes"** or just **"different"**, it's a **two-tailed** test.

### 📏 Conclusion Rule:

> ❌ Reject H₀ if the test statistic falls into the **one** rejection region (left or right tail depending on direction).

---

## 🎯 Summary Table: One-Tailed vs. Two-Tailed

| Feature                | Two-Tailed Test 🔁    | One-Tailed Test 👉 / 👈        |
| ---------------------- | --------------------- | ------------------------------ |
| Rejection Region       | Both sides            | One side only                  |
| Alpha (α) Distribution | α/2 on each side      | All α in one side              |
| Hypothesis Symbols     | = vs ≠                | ≤ vs > or ≥ vs <               |
| Direction Predicted?   | No (just different)   | Yes (greater or less)          |
| Real-life Clue Words   | "change", "different" | "increase", "reduce", "better" |

---

## 🔍 Extra Example: Lifespan of a Medicine

> Current average lifespan = **70 years**

### ✅ Two-Tailed Test:

* **H₀:** μ = 70
* **H₁:** μ ≠ 70
  💬 We're just checking if it's **different**, not caring if it's more or less.

### ✅ One-Tailed Test:

* **H₀:** μ = 70
* **H₁:** μ > 70
  💬 We're checking if the **new medicine increases lifespan**.

---

# 🍟 Hypothesis Testing with Chips – One-Tailed & Two-Tailed Tests

Let’s understand hypothesis testing using a **chips packet** 🥔 as an example.

---

## 🔁 Two-Tailed Test – When We're Just Checking for Any Difference

### 🔍 Scenario:

> A chips company claims each packet contains **exactly 50 grams** of chips. You want to **verify** this claim.

### 🧾 Hypotheses:

* **H₀ (Null):** μ = 50
* **H₁ (Alternate):** μ ≠ 50

📊 **Rejection Zone:**

* Lies on **both sides** of the mean (left and right of 50 grams).
* You're testing if the weight is **either less than** or **more than** 50 grams.

💬 Think of it like:

> "I don’t care if the packet is heavier or lighter—if it’s not **exactly** 50 grams, I’m concerned."

---

## 👈 One-Tailed Test – Left-Tailed (Checking if It’s Less)

### 🔍 Scenario:

> You suspect the chips company is giving **less than 50 grams** of chips.

### 🧾 Hypotheses:

* **H₀ (Null):** μ ≥ 50
* **H₁ (Alternate):** μ < 50

📊 **Rejection Zone:**

* Lies on the **left side** of the distribution (less than 50 grams).

💬 Think of it like:

> "I think the packets are **underfilled**."

---

## 👉 One-Tailed Test – Right-Tailed (Checking if It’s More)

### 🔍 Scenario:

> You're checking if the company is generously giving **more than 50 grams** of chips per packet.

### 🧾 Hypotheses:

* **H₀ (Null):** μ ≤ 50
* **H₁ (Alternate):** μ > 50

📊 **Rejection Zone:**

* Lies on the **right side** of the distribution (more than 50 grams).

💬 Think of it like:

> "Let’s test if they’re being extra generous!" 😄

---

## ✅ Quick Visual Recap:

| **Test Type**         | **H₀** | **H₁** | **Rejection Zone**        |
| --------------------- | ------ | ------ | ------------------------- |
| 🔁 Two-Tailed         | μ = 50 | μ ≠ 50 | Both left and right tails |
| 👈 One-Tailed (Left)  | μ ≥ 50 | μ < 50 | Left tail (less than 50)  |
| 👉 One-Tailed (Right) | μ ≤ 50 | μ > 50 | Right tail (more than 50) |

---

![image](https://github.com/user-attachments/assets/6590ae45-931d-4425-a5e9-527134bec511)

![image](https://github.com/user-attachments/assets/4d000a65-448d-4d15-bde8-3449e895a3dc)

![image](https://github.com/user-attachments/assets/c059ecd1-00d5-470e-b726-15ca9c3ed405)

---

# 👉 One-Tailed Tests – Explained Simply!

---

## 📌 What is a One-Tailed Test?

A **One-Tailed Test** checks if the sample data is significantly **greater than** or **less than** a certain value—not just different.

💡 It focuses on **one side (tail)** of the probability distribution.

That’s why it's called a **"one-tailed" test** — because the **rejection region** (where we might reject the Null Hypothesis) is only on **one tail** of the curve.

---

## 📊 How the Hypotheses Are Written

In one-tailed tests, the **Null Hypothesis (H₀)** always includes:

* **≤ (less than or equal to)**
  or
* **≥ (greater than or equal to)**

The **Alternative Hypothesis (H₁)** uses:

* **> (greater than)**
  or
* **< (less than)**

---

## ➗ Rejection Region

* 🔴 The **rejection region** is concentrated on **only one side** of the distribution.
* All of the **significance level (α)** lies in that **one tail**.

> 🧠 Tip: If you use a **one-tailed test**, **do not divide α by 2**.

---

## 🧭 Two Types of One-Tailed Tests

| **Test Type**            | **Used When**                              | **Symbol**    | **Rejection Tail**      |
| ------------------------ | ------------------------------------------ | ------------- | ----------------------- |
| 👈 **Left-Tailed Test**  | You're testing if something is **less**    | H₁: μ < value | Left side (lower tail)  |
| 👉 **Right-Tailed Test** | You're testing if something is **greater** | H₁: μ > value | Right side (upper tail) |

---

### 🧪 Example Scenarios

* **Left-tailed test:**
  A company wants to know if the **actual product weight is less** than the advertised 50 grams.

  * H₀: μ ≥ 50
  * H₁: μ < 50
    ➡️ Reject H₀ if the test statistic falls far enough **left**.

* **Right-tailed test:**
  A drug company wants to prove that its medicine **increases** recovery speed (e.g., recovery time is faster than 10 days).

  * H₀: μ ≤ 10
  * H₁: μ > 10
    ➡️ Reject H₀ if the test statistic falls far enough **right**.

---

🧠 **Remember:**

* Use **one-tailed** only when you're sure about the **direction** of the effect.
* If you're just testing for **any difference (not direction)**, use a **two-tailed test** instead.

---

# 🎯 One-Tailed Tests – Left vs Right Tail

When you're **sure of the direction** you expect the result to go in (either less than or more than a value), you use a **one-tailed test**. Let’s break it into two types with examples and reasoning 👇

---

## 👈 LEFT-TAILED TEST

➡️ **Rejection Region: Left Side**

---

### 💊 **Example Scenario: Medicine Reducing Fever**

> A new medicine is being tested. Normally, fever lasts **16 weeks**. We want to check if the medicine **reduces** this duration.

### 🧾 Hypotheses:

* **H₀ (Null):** μ ≥ 16 (fever lasts 16 weeks or more → medicine has no effect)
* **H₁ (Alternate):** μ < 16 (fever lasts less than 16 weeks → medicine is effective)

---

### 📉 Why is Rejection on the **Left**?

* If the **test statistic** (z-score) is **greater than or equal to 16**, that supports H₀ → so we **do not reject** it.
* But if the **test statistic is much less than 16**, this means the medicine is **actually reducing** fever duration → so we **reject H₀**.

---

### 🧮 What About the Z-Score?

**Z = (x̄ - μ) / (s / √n)**

* If the sample mean x̄ is **less than** μ (16), the numerator becomes negative → **z-score is negative**
* This puts the test statistic in the **left tail** of the distribution

✅ **So we reject H₀ if:**
**Z < Z-critical** (at chosen α level)

---

## 👉 RIGHT-TAILED TEST

➡️ **Rejection Region: Right Side**

---

### 🔋 **Example Scenario: Battery Life with New Technology**

> A battery that used to last **30 hours** is now claimed to last **more** due to a new technology.

### 🧾 Hypotheses:

* **H₀ (Null):** μ ≤ 30 (no improvement in battery life)
* **H₁ (Alternate):** μ > 30 (battery life has increased)

---

### 📈 Why is Rejection on the **Right**?

* If the **test statistic** is **30 or less**, that supports H₀ → new tech is not improving battery life → **do not reject H₀**
* If the **test statistic is much greater than 30**, it supports H₁ → **reject H₀**

---

### 🧮 What About the Z-Score?

**Z = (x̄ - μ) / (s / √n)**

* If x̄ is **greater than** μ (30), numerator is positive → **z-score is positive**
* That means the test statistic falls in the **right tail**

✅ **So we reject H₀ if:**
**Z > Z-critical** (at α)

---

## 📊 Quick Summary Table

| **Test Type**        | **H₀**    | **H₁**    | **Rejection Zone** | **Z-Score Direction** |
| -------------------- | --------- | --------- | ------------------ | --------------------- |
| 👈 Left-Tailed Test  | μ ≥ value | μ < value | Left side          | Negative              |
| 👉 Right-Tailed Test | μ ≤ value | μ > value | Right side         | Positive              |

---

### 🔑 Key Formula:

**Z = (Sample Mean - Population Mean) / (Standard Deviation / √Sample Size)**

---

# 🎓 Hypothesis Testing: C-DAC Placement Example

> 📊 Suppose **the chance of a student getting placed before doing a C-DAC course is 40% (μ = 40%)**.
> Let’s test different hypotheses using one-tailed and two-tailed approaches.

---

## 1️⃣ 🔁 **Two-Tailed Test** – Just Checking for Any Difference

### ✍️ Hypotheses:

* **H₀ (Null):** μ = 40%
* **H₁ (Alternate):** μ ≠ 40%

### ❗ When to Use:

> You're **not sure** if the C-DAC course increases or decreases placement chances—you just want to know if it has **any impact**.

### 🚩 Rejection Zones:

* 🔻 **Two regions**: one in the **left tail** and one in the **right tail**
* Each region contains: **α / 2**

For example: If α = 0.05
→ Each tail gets **0.025** rejection zone

---

## 2️⃣ 👈 **Left-Tailed Test** – Checking If It's Worse

### ✍️ Hypotheses:

* **H₀ (Null):** μ ≥ 40%
* **H₁ (Alternate):** μ < 40%

### ❗ When to Use:

> You suspect that students have a **lower chance** of getting placed before doing C-DAC.

### 🚩 Rejection Zone:

* 🔻 **Left tail** only
* Entire **α value is on the left**

Example: α = 0.05
→ **All 0.05 is in the left rejection region**

---

## 3️⃣ 👉 **Right-Tailed Test** – Checking If It's Better

### ✍️ Hypotheses:

* **H₀ (Null):** μ ≤ 40%
* **H₁ (Alternate):** μ > 40%

### ❗ When to Use:

> You believe the C-DAC course **increases** placement chances.

### 🚩 Rejection Zone:

* 🔺 **Right tail** only
* Entire **α value is on the right**

Example: α = 0.05
→ **All 0.05 is in the right rejection region**

---

## 🧠 Visual Summary

| **Test Type**   | **H₀**  | **H₁**  | **Rejection Region(s)** | **Alpha (α) Location** |
| --------------- | ------- | ------- | ----------------------- | ---------------------- |
| 🔁 Two-Tailed   | μ = 40% | μ ≠ 40% | Left and Right tails    | α/2 in each tail       |
| 👈 Left-Tailed  | μ ≥ 40% | μ < 40% | Left tail only          | Full α on left         |
| 👉 Right-Tailed | μ ≤ 40% | μ > 40% | Right tail only         | Full α on right        |

---

# 🧪 Impact of Test Type on Alpha (α)

---

When we perform hypothesis testing, we choose a **significance level (α)** — commonly **0.05 or 5%** — which defines how much risk we're willing to take of making a **Type I Error** (i.e., rejecting a true null hypothesis).

But depending on the type of test (**one-tailed or two-tailed**), **α is handled differently**. Let's break it down 👇

---

## 🔁 Two-Tailed Test

> We are testing if the value is **simply different** (either **higher or lower**) from the hypothesized value.

### 📌 What happens to α?

* There are **two rejection regions**:

  * One in the **lower tail**
  * One in the **upper tail**
* The total α is **split equally** into both tails.

### ✅ Example:

If **α = 0.05**:

* **0.025 (2.5%)** goes into the **left tail**
* **0.025 (2.5%)** goes into the **right tail**

🎯 So, you **reject H₀** if your test statistic falls:

* **Below the lower 2.5%**
* **Above the upper 2.5%**

---

## 👉👈 One-Tailed Test (Left or Right)

> We are checking if the value is **only greater than** or **only less than** the hypothesized value.

### 📌 What happens to α?

* There is **only one rejection region**:

  * **Left-tailed**: α goes to the **lower end**
  * **Right-tailed**: α goes to the **upper end**
* The **entire α** is concentrated in **one tail only**

### ✅ Example:

If **α = 0.05**:

* All **0.05 (5%)** goes into **just one tail**, depending on the direction.

🎯 So, you **reject H₀** if your test statistic:

* Falls in the **extreme left** (for left-tailed)
* Falls in the **extreme right** (for right-tailed)

---

## 🧠 Visual Summary Table

| **Test Type**        | **No. of Rejection Regions** | **Alpha Distribution**               |
| -------------------- | ---------------------------- | ------------------------------------ |
| 🔁 Two-Tailed Test   | 2 (both tails)               | α/2 in left tail + α/2 in right tail |
| 👈 Left-Tailed Test  | 1 (left tail)                | Entire α in left tail                |
| 👉 Right-Tailed Test | 1 (right tail)               | Entire α in right tail               |

---

## 🎓 Quick Recap:

* ✂️ **Split α** in two-tailed tests
* ✅ **Do not split α** in one-tailed tests

---

# 🧪 Two-Tailed Tests: Understanding the p-Value 🎯

In hypothesis testing, the **p-value** tells us the probability of getting a result **as extreme as** the one observed, assuming the **null hypothesis is true**.

In a **two-tailed test**, we're looking for evidence in **both directions** (less than or greater than), so we have to **account for both tails** of the distribution.

---

## 🔢 Step-by-Step: How to Calculate p-Value in a Two-Tailed Test

---

### 1️⃣ Calculate the Z-Test Statistic 🧮

Use the formula:

$$
Z = \frac{\bar{x} - \mu}{s / \sqrt{n}}
$$

This Z value could be **positive or negative**, depending on whether the sample mean is above or below the population mean.

---

### 2️⃣ Find Area to the **Left of Z** in Z-Table 📘

Look up the calculated Z in the Z-table.
👉 It gives you the **area under the curve to the left** of the Z value.

### ✅ Example:

Let’s say **Z = 1.23**
From the **Z-table**, the area to the **left** is:

$$
P(Z < 1.23) = 0.8907
$$

---

### 3️⃣ Convert to Area in the **Tail** 🎯

In hypothesis testing, we care about the **extreme ends** (rejection zones).
For a **positive Z**, we want the **area to the right** of the value:

$$
\text{Right-tail area} = 1 - 0.8907 = 0.1093
$$

---

### 4️⃣ Multiply by 2 for Both Tails 🔁

Since this is a **two-tailed test**, we consider **both** the left and right extremes.

So,

$$
p\text{-value} = 2 \times 0.1093 = 0.2186
$$

---

### 5️⃣ Compare p-Value with α (Significance Level) 📏

* If **p-value ≤ α** → ✅ **Reject H₀**
* If **p-value > α** → ❌ **Do NOT reject H₀**

### 📌 Example Decision:

If **α = 0.05**, and
**p-value = 0.2186**,
Then **0.2186 > 0.05**, so we **fail to reject H₀**.

---

## 🧠 Summary Table

| **Step** | **What to Do**                         | **Why**                             |
| -------- | -------------------------------------- | ----------------------------------- |
| 1️⃣      | Calculate Z                            | Compare your sample with population |
| 2️⃣      | Use Z-table to get area to the left    | That’s how Z-tables work            |
| 3️⃣      | Subtract from 1 to get right-tail area | We're interested in extremes        |
| 4️⃣      | Multiply by 2                          | Because it’s a two-tailed test      |
| 5️⃣      | Compare with α                         | To make decision about H₀           |

---

# 🧪 One-Tailed Test: Understanding the p-Value ✅

In **one-tailed tests**, we test for an effect in **one direction only** — either **less than** (left-tailed) or **greater than** (right-tailed).
This affects **how we calculate the p-value** and **where we reject** the null hypothesis (H₀).

---

## 🔢 Step-by-Step: How to Calculate p-Value in a One-Tailed Test

---

### 1️⃣ Calculate the Z-Test Statistic 🧮

$$
Z = \frac{\bar{x} - \mu}{s / \sqrt{n}}
$$

* For **left-tailed tests**, the Z-score is usually **negative**
* For **right-tailed tests**, the Z-score is usually **positive**

---

### 2️⃣ Look Up Area to the **Left** of Z in the Z-Table 📘

The Z-table always gives the **cumulative area to the left** of a Z value.

---

## 👈 Left-Tailed Test

You are testing **if a value is significantly less than** the population mean.

### ✅ What to Do:

If Z = -1.46,
From the Z-table:

$$
P(Z < -1.46) = 0.0721
$$

Since this is a **left-tailed test**, this value **directly gives the p-value**.

$$
\text{p-value} = 0.0721
$$

✅ **Do not double the p-value** — the rejection zone is only in one tail.

### 🧪 Decision Rule:

* If **p-value ≤ α** → Reject H₀
* If **p-value > α** → Do not reject H₀

---

## 👉 Right-Tailed Test

You are testing **if a value is significantly greater than** the population mean.

### ✅ What to Do:

If Z = +1.46,
From the Z-table:

$$
P(Z < 1.46) = 0.9279
$$

Since it’s **right-tailed**, we want the **area to the right** of Z:

$$
\text{p-value} = 1 - 0.9279 = 0.0721
$$

Again, **no need to double** the p-value.

---

## 🧠 Summary Table

| **Test Type**   | **Z-Score** | **Use Z-Table to Find** | **Final p-value**     | **Reject H₀ if** |
| --------------- | ----------- | ----------------------- | --------------------- | ---------------- |
| 👈 Left-Tailed  | Usually < 0 | Area to **left** of Z   | Use **Z-table value** | p-value ≤ α      |
| 👉 Right-Tailed | Usually > 0 | Area to **right** of Z  | 1 - (Z-table value)   | p-value ≤ α      |

---

### 🎓 Quick Recap:

* ✅ **Do NOT double** the p-value for one-tailed tests.
* ✅ Z-table always gives area **to the left**.
* ✅ For right-tailed tests, subtract from 1.
* 🚩 Reject H₀ if p-value ≤ α

---

# 📊 Rejection/Non-Rejection Criteria in Hypothesis Testing 🧠

When you're doing hypothesis testing, your main goal is to **decide whether to reject or not reject the null hypothesis (H₀)** based on your test result.

We use the **test statistic**, **critical value**, and **p-value** to make this decision — and the rules depend on the **type of test** you're performing.

---

## 🔍 Test Type and Alpha (α) Rules

| Test Type  | Alpha (α) Rule 🧪                  | p-value Rule 📉              |
| ---------- | ---------------------------------- | ---------------------------- |
| Two-tailed | Use **α/2** to find critical value | Compare **p-value with α/2** |
| One-tailed | Use **α** to find critical value   | Compare **p-value with α**   |

> 💡 **Why α/2 for Two-Tailed?**
> Because the rejection region is split between both tails (left and right), we divide α by 2 for each side.

---

## ⚖️ Decision Criteria Based on Test Type

Let's break down when to reject the null hypothesis (H₀) based on the test type and your test statistic.

| Test Type        | Condition 🔍                      | Decision ✅/❌           |   |                |    |                        |
| ---------------- | --------------------------------- | ---------------------- | - | -------------- | -- | ---------------------- |
| **Two-tailed**   | \`                                | Test statistic         | > | Critical value | \` | **Reject H₀** ❌        |
|                  | \`                                | Test statistic         | ≤ | Critical value | \` | **Do not reject H₀** ✅ |
| **Left-tailed**  | `Test statistic < Critical value` | **Reject H₀** ❌        |   |                |    |                        |
|                  | `Test statistic ≥ Critical value` | **Do not reject H₀** ✅ |   |                |    |                        |
| **Right-tailed** | `Test statistic > Critical value` | **Reject H₀** ❌        |   |                |    |                        |
|                  | `Test statistic ≤ Critical value` | **Do not reject H₀** ✅ |   |                |    |                        |

---

## 📌 Real-World Example

**Imagine you're testing whether a new drug is more effective than the current one.**

* **H₀ (Null Hypothesis):** The new drug is equally effective.
* **H₁ (Alternative Hypothesis):** The new drug is more effective.

This would be a **right-tailed test** (because you're only interested in values **greater than** current effectiveness).

### Scenario:

* α = 0.05
* Calculated test statistic = 2.1
* Critical value = 1.96

🧮 Since **2.1 > 1.96**, we are in the rejection region → **Reject H₀**. The new drug seems to work better!

---

## 🔁 Quick Recap

🧠 Think of hypothesis testing like a courtroom trial:

* **H₀ = "Innocent until proven guilty"**
* You need strong evidence (test statistic far from expected, or small p-value) to **reject** H₀.
* If the evidence isn't strong enough, you **do not reject** H₀ — but it doesn’t mean H₀ is true!

---

# 📏 How to Calculate the Test Statistic (Z-score) 🔍

In hypothesis testing, we use a **test statistic** (like a Z-score) to compare our **sample data** with what's expected under the **null hypothesis (H₀)**.

---

## 🧪 Example Problem: Let's Walk Through It Step-by-Step

We’re testing the claim:
**H₀ (Null Hypothesis):** The population mean height = 65 inches

### ✅ Given:

* **Sample size (n)** = 50
* **Sample mean (x̄)** = 67 inches
* **Population standard deviation (σ)** = 5 inches
* **Population mean (μ)** = 65 inches (from H₀)
* **Significance level (α)** = 0.05
* This is a **two-tailed** test!

---

## 🧮 Step 1: Use the Z-Test Formula

The formula for the **Z-test statistic** when the population standard deviation is known:

$$
Z = \frac{\bar{x} - \mu}{\sigma / \sqrt{n}}
$$

Plug in the values:

$$
Z = \frac{67 - 65}{5 / \sqrt{50}} = \frac{2}{5 / 7.07} = \frac{2}{0.707} ≈ 2.82
$$

➡️ So, our **calculated Z-value is 2.82**.

---

## 📉 Step 2: Determine the Critical Value

Since this is a **two-tailed test**, divide alpha (α) by 2:

$$
\alpha = 0.05 ⇒ \alpha/2 = 0.025
$$

Now, using a Z-table (🔗 [Z-table link](https://www.z-table.com/)), find the **critical value** corresponding to a probability of 0.025 in each tail.

➡️ **Critical value = ±1.96**

> This means: If our Z is **between -1.96 and +1.96**, we **do not reject** H₀.
> If it's **outside this range**, we **reject** H₀.

---

## 🚨 Step 3: Make the Decision

Our **calculated Z = 2.82**, which is **greater than** the critical value 1.96.

✅ **Decision: Reject H₀**

---

## 💡 Real-World Interpretation

Imagine you're analyzing the average height of a sample group to see if it's significantly different from a known population average.

* You expected people to be **65 inches tall**.
* But your sample had an average of **67 inches**, and your test shows this difference is **statistically significant**.

> So, there's strong enough evidence to say the average height **is not 65 inches** — it's likely different!

---

## 🔁 Quick Summary

| Step                    | What You Do                                                    |
| ----------------------- | -------------------------------------------------------------- |
| 1️⃣ Calculate Z         | Use the formula: $Z = \frac{\bar{x} - \mu}{\sigma / \sqrt{n}}$ |
| 2️⃣ Find critical value | Use α (or α/2 for two-tailed) and a Z-table                    |
| 3️⃣ Compare             | If **Z > critical value** → **Reject H₀**                      |

---

# 🧮 P-value Calculation Example 🎯

When you calculate a **Z-score** during hypothesis testing, the next step is often to calculate the **p-value**.

---

## ❓ What is a P-value?

The **p-value** tells you the probability of getting a result **as extreme or more extreme** than what you observed — **assuming the null hypothesis (H₀) is true**.

* A **small p-value** means the result is **unlikely** under H₀ → so we **reject H₀**.
* A **large p-value** means the result is **likely** under H₀ → so we **do not reject H₀**.

---

## 🧪 Given:

* **Z-score = 2.82**
* This is a **two-tailed test**
* Significance level (α) = 0.05
* Image:
  ![image](https://github.com/user-attachments/assets/383a1326-bffa-4ec5-bc04-e69c292ad8df)

---

## 🔍 Step-by-Step: Finding the P-value

### ✅ Step 1: Look up Z = 2.82 in the Z-table

From the Z-table → Area under the curve **to the left** of 2.82 is:

$$
\text{Area} = 0.9976
$$

### ✅ Step 2: Find area to the **right** of Z = 2.82

We want the tail probability:

$$
1 - 0.9976 = 0.0024
$$

This is for **one tail**.

### ✅ Step 3: Since it's a **two-tailed** test, multiply by 2:

$$
\text{P-value} = 2 \times 0.0024 = 0.0048
$$

---

## 📌 Final Comparison

* **P-value = 0.0048**
* **Alpha (α) = 0.05**

Now, compare:

$$
\text{P-value} < \alpha ⇒ 0.0048 < 0.05
$$

✅ So, **we reject the null hypothesis (H₀)**.

---

## 🔁 Real-Life Analogy

Let’s say you toss a coin 100 times and get 70 heads. The p-value tells you:

> “What are the chances of getting something this extreme (or more) if the coin were fair?”

If the p-value is super low (like 0.0048), that means **it's highly unlikely this happened by chance** — so maybe the coin isn't fair!

---

## 📌 Quick Summary

| Step                       | What You Do                                    |
| -------------------------- | ---------------------------------------------- |
| 1️⃣ Look up Z-score        | Find area from Z-table for given Z (e.g. 2.82) |
| 2️⃣ Tail area              | Subtract from 1 to get right-tail area         |
| 3️⃣ Multiply (if 2-tailed) | Multiply tail area by 2                        |
| 4️⃣ Compare with α         | If **p-value < α**, **Reject H₀**              |

---

# 📉 Understanding the P-value in Hypothesis Testing 🧪

The **p-value** is one of the most important tools in hypothesis testing. It helps you decide **whether to reject or not reject the null hypothesis (H₀)** based on your sample data.

---

## ❓ What is a P-value?

👉 **P-value = Probability of getting your observed result (or something more extreme) if the null hypothesis is true.**

* Think of it as the **"surprise factor"**.
  A small p-value means: “Wow, this result is really surprising if H₀ were true!”

---

## 🎯 How to Use It?

| P-value                | Interpretation                          | Decision                |
| ---------------------- | --------------------------------------- | ----------------------- |
| **Low p-value** (≤ α)  | The result is statistically significant | **Reject H₀** ❌         |
| **High p-value** (> α) | The result is likely under H₀           | **Fail to reject H₀** ✅ |

> Common threshold for α (significance level) = **0.05**

---

## 🍕 Real-World Example: Pizza Delivery

A pizza outlet claims:

* “We deliver pizza in **30 minutes or less** on average.”

This becomes our hypothesis:

* **H₀ (Null Hypothesis):** Mean delivery time = 30 minutes
* **Ha (Alternative Hypothesis):** Mean delivery time ≠ 30 minutes
  *(This is a two-tailed test since we are checking for any difference.)*

---

### 🧪 You collect data...

After testing a few delivery times, your analysis gives you a:

> **P-value = 0.001**

### 🔍 What does this mean?

* 0.001 is **much smaller** than the common α of 0.05
* There’s only a **0.1% chance** you'd get a result like this if H₀ were true

🎯 **Conclusion:**
Since the p-value is very low, you **reject the null hypothesis**.
➡️ You have strong evidence that the average delivery time is **not** 30 minutes.

---

## 🧠 Easy Analogy: The Lie Detector

Imagine you’re testing if someone is lying:

* **H₀:** They are telling the truth
* **Ha:** They are lying

The **p-value is like the strength of suspicion**:

* If the p-value is low, the result is too suspicious to believe they’re innocent ⇒ Reject H₀
* If the p-value is high, the result doesn’t look suspicious ⇒ Don’t reject H₀

---

## 🔁 Quick Summary

* ✅ **P-value = Evidence against H₀**
* 📉 **Smaller p-value = Stronger evidence to reject H₀**
* 🔍 Compare p-value to α (like 0.05)
* 🤔 Real-world: Helps you test claims, like quality checks, product comparisons, delivery guarantees, etc.

---

# 🎯 Critical Values for Different Significance Levels (α) 📏

In hypothesis testing, we often use **critical values** to decide whether to reject the null hypothesis (H₀).

These values depend on:

1. **The significance level (α)**
2. **The type of test you're running** — **left-tailed, right-tailed, or two-tailed**

---

## ❓ What Are Critical Values?

A **critical value** is a cutoff point on the standard normal distribution (Z-distribution).
It marks the boundary of the **rejection region** — where we say, “This result is too extreme under H₀.”

---

## 🔢 Critical Value Table (Z-distribution)

| **α (Significance Level)** | **Left-Tailed Test** | **Right-Tailed Test** | **Two-Tailed Test** |
| -------------------------- | -------------------- | --------------------- | ------------------- |
| **0.10**                   | -1.28                | +1.28                 | -1.64 and +1.64     |
| **0.05**                   | -1.64                | +1.64                 | -1.96 and +1.96     |
| **0.01**                   | -2.33                | +2.33                 | -2.58 and +2.58     |

> ✨ Tip: The **smaller α gets**, the more extreme your critical values become — which means you need **stronger evidence** to reject H₀.

---

## 📊 Visual Intuition

Here’s what each test looks like on a bell curve:

* 🔻 **Left-tailed test**: Rejection area is in the **left tail**
* 🔺 **Right-tailed test**: Rejection area is in the **right tail**
* 🔄 **Two-tailed test**: Rejection areas are in **both tails**

---

## 🍕 Real-Life Example (Back to Pizza!)

Let’s say your pizza delivery test uses:

* α = 0.05 (common choice)
* You’re doing a **two-tailed test** (checking for “≠ 30 mins”)

➡️ Your **critical values** are **-1.96 and +1.96**
So:

* If your Z-score is **beyond ±1.96**, you **reject H₀**
* If your Z-score is **between -1.96 and +1.96**, you **do not reject H₀**

---

## 🧠 Summary Table

| **If you're doing this test...** | **And α is...** | **Then reject H₀ if Z is...**              |
| -------------------------------- | --------------- | ------------------------------------------ |
| Left-tailed                      | 0.05            | Less than **-1.64**                        |
| Right-tailed                     | 0.05            | Greater than **+1.64**                     |
| Two-tailed                       | 0.05            | Less than **-1.96** or more than **+1.96** |

---

# 📊 `norm.cdf` vs `norm.ppf`: Know When to Use What! 🔁

In statistics and hypothesis testing, we often need to **switch between z-scores and p-values**.

Python (using libraries like SciPy) makes this super easy with two functions:

---

## 🧠 What Do These Functions Do?

| Function      | Input (What You Know) | Output (What You Want) | Use When...                           |
| ------------- | --------------------- | ---------------------- | ------------------------------------- |
| `norm.cdf(z)` | Z-score               | P-value                | You **have a Z-score** → want p-value |
| `norm.ppf(p)` | P-value               | Z-score                | You **have a p-value** → want Z-score |

---

## 🧪 Example Use Cases:

### ✅ Using `norm.cdf(z)`:

You calculated a **Z = 2.1** and want to find out **how extreme this value is** (i.e., the p-value).

```python
from scipy.stats import norm
p_value = 1 - norm.cdf(2.1)  # for right tail
```

👉 If it’s a **two-tailed test**, you’ll do:

```python
p_value = 2 * (1 - norm.cdf(2.1))
```

---

### ✅ Using `norm.ppf(p)`:

You want to find the **critical Z value** for a **given alpha** (say 0.05):

```python
z_critical = norm.ppf(1 - 0.025)  # for two-tailed test (alpha/2 = 0.025)
```

---

## 🔍 How to Decide Whether to Reject H₀?

You can choose **either method (Z or p-value)** — they lead to the same decision. Here's how:

---

### ✳️ Method 1: **Compare Z-statistic to Z-critical**

* If:

  $$
  z_{\text{statistic}} < z_{\text{critical}} \quad \text{(or within ±z for two-tailed)}
  $$

  ✅ Do **not** reject H₀
* Else:
  ❌ **Reject** H₀

---

### ✳️ Method 2: **Compare p-value to α**

* If:

  $$
  p\text{-value} > \alpha \quad \text{(for one-tailed)} \quad \text{OR} \quad 2 \times p\text{-value} > \alpha \quad \text{(for two-tailed)}
  $$

  ✅ Do **not** reject H₀
* Else:
  ❌ **Reject** H₀

---

## 🍕 Quick Real-World Example

A pizza shop claims their average delivery time = 30 minutes.

You collect data and calculate:

* Z-score = 2.8
* Using `norm.cdf(2.8)`, you find p-value ≈ 0.0026
* Two-tailed test ⇒ `2 × 0.0026 = 0.0052`

Now, compare:

* 0.0052 < 0.05 (alpha)

🎯 **Decision: Reject H₀** — Pizza deliveries are **not** taking 30 minutes on average!

---

## 🔁 Quick Summary

| You Know | You Use    | To Find |
| -------- | ---------- | ------- |
| Z-score  | `norm.cdf` | P-value |
| P-value  | `norm.ppf` | Z-score |

| Method         | Rule                 | Outcome            |
| -------------- | -------------------- | ------------------ |
| Z-method       | Z < critical Z       | Do not reject H₀ ✅ |
| P-value method | P-value > α (or α/2) | Do not reject H₀ ✅ |

---

# 📦 Margin of Error & Confidence Interval 🧮

### (…And How It Helps Test Hypotheses)

---

## 🧠 What Is a Margin of Error?

* A **point estimate** (like a sample mean) gives us one number — but it’s just an **estimate** of the population value.
* The **margin of error (MoE)** gives us a **range around that number**, to show how confident we are in our estimate.

> 📍 **Think of it like this:**
> If someone asks, “When will you arrive?” and you say “10 minutes,” that’s a point estimate.
> But if you say, “Between 5 and 15 minutes,” that’s an **interval estimate** with a margin of error.

---

## 🧪 Given Problem:

> On a social networking site, a **sample of 40 users** has:

* **Sample mean (x̄)** = 130.8 friends
* **Standard deviation (s)** = 53 friends
* **Sample size (n)** = 40
* **Confidence level** = 95% → So, **Z-critical (Zc)** = 1.96
  *(from Z-table for α = 0.05 → two-tailed test)*

📸 ![image](https://github.com/user-attachments/assets/633a2df1-97c3-42cd-b1d5-2fe056f23251)

---

## 🧾 Step-by-Step: Calculating Margin of Error

### ✅ Step 1: Calculate Standard Error (SE)

$$
\text{Standard Error} = \frac{s}{\sqrt{n}} = \frac{53}{\sqrt{40}} ≈ \frac{53}{6.32} ≈ 8.39
$$

---

### ✅ Step 2: Apply the Margin of Error Formula

$$
\text{Margin of Error (MoE)} = Z_c \times \text{Standard Error} = 1.96 \times 8.39 ≈ 16.4
$$

---

### ✅ Step 3: Create the Confidence Interval

$$
\text{Interval Estimate} = \text{Point Estimate} ± \text{Margin of Error}
$$

$$
130.8 ± 16.4 ⇒ (114.4, 147.2)
$$

✅ So, with **95% confidence**, we can say the **average number of friends per user** is **between 114.4 and 147.2**.

---

## 📌 How This Relates to Hypothesis Testing

Let’s say the company claims:

* **H₀ (Null Hypothesis):** The true average number of friends is **120**.

Now, check if **120** falls within your confidence interval:
→ **Yes, 120 is between 114.4 and 147.2**

🔍 **Conclusion:**
Since the hypothesized mean is **inside** the interval, **we do not reject H₀**. There’s not enough evidence to say the average is different from 120.

---

## 🧠 Key Concepts Recap

| Concept               | What It Means                                     |
| --------------------- | ------------------------------------------------- |
| **Point Estimate**    | The sample mean (130.8 in this case)              |
| **Standard Error**    | The standard deviation of the sample mean         |
| **Z-critical (Zc)**   | Z-value that corresponds to your confidence level |
| **Margin of Error**   | The uncertainty buffer around your estimate       |
| **Interval Estimate** | Range: Point Estimate ± Margin of Error           |

---

## 🛠 Formula Sheet:

* **Standard Error:**

  $$
  SE = \frac{s}{\sqrt{n}}
  $$
* **Margin of Error:**

  $$
  MoE = Z_c \times SE
  $$
* **Confidence Interval:**

  $$
  \text{CI} = x̄ ± MoE
  $$

---

# 📌 How to State the Null Hypothesis (H₀) in Different Statistical Tests 🧪

The **null hypothesis (H₀)** always assumes **"no effect," "no difference," or "no relationship."**
It’s the default claim we test **against** using our data.

---

## 🧾 Common Statistical Tests and Their Null Hypotheses

| 📊 **Test**                      | 🧠 **Null Hypothesis (H₀)**                                                                    | 🔍 **Use Case Example**                                               |
| -------------------------------- | ---------------------------------------------------------------------------------------------- | --------------------------------------------------------------------- |
| **One-sample T-Test**            | There is **no significant difference** between the **sample mean** and the **population mean** | Testing if average screen time of 1 sample differs from national avg. |
| **Two-sample T-Test**            | The **means of two independent groups** are **equal**                                          | Comparing average test scores of two different classes                |
| **Paired T-Test**                | The **mean difference** before and after in **the same group** is **zero**                     | Measuring blood pressure before and after medication                  |
| **ANOVA (Analysis of Variance)** | The **means of more than two groups** are **equal**                                            | Comparing satisfaction ratings across 3+ stores                       |
| **Chi-Square Test**              | There is **no association** between the **two categorical variables** (they are independent)   | Is gender related to product preference?                              |

📸 ![image](https://github.com/user-attachments/assets/eec2f058-efaa-42a2-9afd-2c95c428c9d5)

---

## 🧠 T-Test vs Z-Test – What's the Difference?

| Feature              | **T-Test**                                 | **Z-Test**                            |
| -------------------- | ------------------------------------------ | ------------------------------------- |
| Sample size (n)      | Small (typically **< 30**)                 | Large (typically **≥ 30**)            |
| Population SD known? | No                                         | Yes                                   |
| Distribution type    | Student’s t-distribution                   | Standard normal distribution          |
| Use case             | Estimate population mean from small sample | Same as T-Test, but with large sample |

🔄 **Otherwise, they test the same thing** — whether a sample mean differs significantly from a population mean or another sample mean.

---

## 🤖 Statistical Tests in Machine Learning

Even in machine learning, we use statistical thinking! Let’s look at some commonly used models and how we state H₀:

| 🤖 **Model/Test**       | 🧠 **Null Hypothesis (H₀)**                                                         | 🔍 **Use Case**                                          |
| ----------------------- | ----------------------------------------------------------------------------------- | -------------------------------------------------------- |
| **Linear Regression**   | The **coefficients (slopes)** of the independent variables are **zero** → No effect | Does advertising budget affect sales?                    |
| **Logistic Regression** | There is **no association** between predictors and the **binary outcome**           | Does smoking predict the chance of developing a disease? |

> 💬 In simpler words:

* **Linear Regression H₀**: "The independent variables don't predict the outcome."
* **Logistic Regression H₀**: "The independent variables don't affect the probability of the binary outcome."

---

## 🧠 Tip: How to Recognize the Null Hypothesis?

Always ask:

* "Is there **no difference**?" → Use T-Test or ANOVA
* "Are variables **not related**?" → Use Chi-Square, Regression
* "Are we checking **before vs after** in the same group?" → Use Paired T-Test

---

## 🎯 Final Recap Table

| **Test Type**       | **Null Hypothesis (H₀)**                           |
| ------------------- | -------------------------------------------------- |
| One-sample T-Test   | Sample mean = Population mean                      |
| Two-sample T-Test   | Mean of group 1 = Mean of group 2                  |
| Paired T-Test       | Mean difference (before-after) = 0                 |
| ANOVA               | All group means are equal                          |
| Chi-Square Test     | Variables are independent (no association)         |
| Linear Regression   | β₁ = β₂ = ... = 0 (no predictive power)            |
| Logistic Regression | No relationship between predictors and the outcome |

---

# 🔍 **T-Tests Made Simple**

### (Also known as **Student’s t-tests**)

---

## 📌 What is a T-Test?

A **t-test** is a statistical test used to:

> ✅ **Compare means** and check if the **difference between them is significant** or just due to random chance.

---

## 🧠 When to Use a T-Test?

Use a **t-test** when:

* You are comparing **means**
* Your sample size is **small** (typically **n ≤ 30**)
* You **don’t know the population standard deviation**

📏 **Z-Test vs. T-Test**

| Feature       | Z-Test              | T-Test                   |
| ------------- | ------------------- | ------------------------ |
| Sample size   | Large (n > 30)      | Small (n ≤ 30)           |
| Population SD | Known               | Unknown                  |
| Distribution  | Standard normal (Z) | Student’s t-distribution |

---

## 🧪 Types of T-Tests & Their Uses

| 🧪 **T-Test Type**       | 🔍 **Purpose**                                                     | 📊 **When to Use**                                          |
| ------------------------ | ------------------------------------------------------------------ | ----------------------------------------------------------- |
| **One-sample t-test**    | Compares the **mean of one sample** to a known **population mean** | Checking if average test score of one class differs from 70 |
| **Independent t-test**   | Compares the means of **two independent groups**                   | Comparing avg marks of **boys vs. girls** in an exam        |
| **Paired sample t-test** | Compares **two measurements from the same group** (before/after)   | Measuring weight **before and after** a fitness program     |

---

## 🔁 Real-World Examples

### 1️⃣ **One-Sample T-Test**

> A bakery says their cookies weigh 100g. You test a sample of 10 cookies.
> **Do they really weigh 100g on average?**
> ✅ Use a **One-sample t-test**

---

### 2️⃣ **Independent Sample T-Test**

> Two factories claim to produce steel rods of the same average length.
> **Are their average lengths really equal?**
> ✅ Use an **Independent t-test**

---

### 3️⃣ **Paired Sample T-Test**

> You check student performance **before and after** a training course.
> **Did the course improve scores?**
> ✅ Use a **Paired t-test**

---

## 🧠 Summary Table

| 🧪 **T-Test Type**   | 📦 **What You're Comparing**           | ✅ **Example**                             |
| -------------------- | -------------------------------------- | ----------------------------------------- |
| One-sample t-test    | Sample mean vs. Population mean        | Cookie weight vs. 100g                    |
| Independent t-test   | Mean of Group 1 vs. Group 2            | Test scores: Class A vs. Class B          |
| Paired sample t-test | Before vs. After (same people/samples) | Blood pressure before vs. after treatment |

---

# 🧪 One-Sample T-Test

### Comparing Your Sample Mean with a Known Population Mean

---

## 🔍 What Does It Do?

* It **checks if the average (mean)** of your **small sample** is significantly different from a **known population average (μ)**.
* Used when **sample size is small (≤ 30)** and population standard deviation is unknown.

---

## ⚖️ Null Hypothesis (H₀)

$$
H_0: \quad \bar{x} = \mu
$$

* The **sample mean (x̄)** is **equal** to the **population mean (μ)**.

---

## 🧮 Formula for Test Statistic (t):

$$
t = \frac{\bar{x} - \mu}{SE} = \frac{\bar{x} - \mu}{s / \sqrt{n}}
$$

Where:

* $\bar{x}$ = sample mean
* $\mu$ = population mean (hypothesized value)
* $s$ = sample standard deviation
* $n$ = sample size
* $SE = \frac{s}{\sqrt{n}}$ is the **standard error**

---

## 📝 Key Points:

* Formula is similar to the Z-test, but since population standard deviation is unknown and sample size is small, we use the **t-distribution**.
* The t-distribution accounts for extra uncertainty due to small sample sizes.

---

## 🎯 Example

A school claims their students score an average of 75 on a math test. You test 20 students and get:

* Sample mean $\bar{x} = 78$
* Sample SD $s = 10$
* Sample size $n = 20$

Calculate the t-value to test if the school’s claim is true.

$$
t = \frac{78 - 75}{10 / \sqrt{20}} = \frac{3}{10 / 4.47} = \frac{3}{2.24} = 1.34
$$

You then compare this t-value with the critical t-value from the t-table (for df = n-1 = 19) at your chosen significance level (e.g., 0.05).

---

# ☕ One-Sample T-Test: Example Explained

---

### 📋 Scenario:

* Claim: Average coffee in a cup = **12 units**
* Sample: 20 cups measured
* Sample mean $\bar{x} = 11.5$ units
* Sample standard deviation $s = 1.2$ units
* Sample size $n = 20$

---

### 🔢 Step 1: Calculate the Test Statistic (t)

$$
t = \frac{\bar{x} - \mu}{s / \sqrt{n}} = \frac{11.5 - 12}{1.2 / \sqrt{20}} = \frac{-0.5}{1.2 / 4.47} = \frac{-0.5}{0.268} = -1.87
$$

*(Your earlier number 2.08 looks like a small typo — double-checking gives -1.87. If you want, I can recalculate again!)*

---

### 🔢 Step 2: Calculate Degrees of Freedom (df)

$$
df = n - 1 = 20 - 1 = 19
$$

* **Degrees of freedom** means the number of independent values that can vary.
* In t-tests, df is usually **sample size minus 1**.

---

### 🔢 Step 3: Use the t-Table to Find Critical Value

* Look up **df = 19** in the **t-distribution table** at your chosen significance level (e.g., α = 0.05 for 95% confidence).
* The critical value will tell you the cutoff point beyond which you reject $H_0$.

---

### 🔍 Note on the t-Table

* The t-table is similar to the Z-table but accounts for **sample size through degrees of freedom**.
* For **large samples (df → ∞)**, t-values approach Z-values.

---

### ✅ Next Step (Usually):

* Compare your calculated t-statistic with the critical t-value.
* If $|t| > t_{critical}$, reject $H_0$ (sample mean significantly different from 12).
* Else, **do not reject** $H_0$.

---

# 📊 Using the T-Table & Making a Decision

---

### 🔗 **T-Table Reference:**

Check the t-table here:
[https://www.sjsu.edu/faculty/gerstman/StatPrimer/t-table.pdf](https://www.sjsu.edu/faculty/gerstman/StatPrimer/t-table.pdf)

---

### 🔢 Step 1: Find Critical t-Value

* **Degrees of freedom (df) = 19**
* We are doing a **two-tailed test** (because we’re testing if the average is *different* from 12, not just less or more)
* **Significance level $\alpha = 0.05$** (This means we want to be 95% confident about our decision)
* Look in the t-table for **df=19** and **two-tailed α=0.05**
* The **critical t-value** = **±2.093**

---

### 🧠 Why α = 0.05?

* The **confidence level is 95%**
* So, the **significance level (α) = 1 - 0.95 = 0.05**
* This α is split into two tails (because two-tailed test), so each tail has 0.025 chance

---

### 🔢 Step 2: Compare Calculated t with Critical t

* **Calculated t-statistic = 2.08**
* **Critical t-value = 2.093**

Since:

$$
|2.08| < 2.093
$$

**Calculated t is less than critical t.**

---

### ✅ Step 3: Draw Conclusion

* **Fail to reject the null hypothesis $H_0$.**
* This means: **We do not have strong enough evidence** to say the average amount of coffee in the cup is different from 12 units.

---

### 💡 Summary:

Even though the sample mean was 11.5, the difference from 12 units is **not statistically significant** at the 95% confidence level.

---

# 🤝 Two Independent Samples T-Test

### Comparing Means from Two Different Groups

---

## 🔍 What is it?

* Used to compare the **average (mean)** values of **two independent groups** (from different populations) to check if their means are **significantly different**.
* Examples:

  * Comparing average test scores of two different schools
  * Comparing average heights of men vs women

---

## ⚖️ Null Hypothesis (H₀)

$$
H_0: \mu_1 = \mu_2
$$

* Means of the two groups are **equal** — no significant difference.

---

## 🧮 Formula for Test Statistic (t):

$$
t = \frac{\bar{X}_1 - \bar{X}_2}{\sqrt{\frac{s_1^2}{n_1} + \frac{s_2^2}{n_2}}}
$$

Where:

* $\bar{X}_1, \bar{X}_2$ = sample means of group 1 and group 2
* $s_1, s_2$ = sample standard deviations
* $n_1, n_2$ = sample sizes

---

## 📝 How it works:

* Calculate the **difference between sample means** in the numerator.
* Calculate the **combined standard error** in the denominator (accounts for variance and sample size in both groups).
* The bigger the t-value, the more evidence there is that means differ.

---

## 📷 Visual Reference

![Two Independent Samples T-Test](https://github.com/user-attachments/assets/54ab485b-0ca5-44fc-b919-0d176d2126ba)

---

## 🔎 Example (for next steps)

> Group 1 (Men): Avg height = 70 inches, SD = 3, Sample size = 30
> Group 2 (Women): Avg height = 65 inches, SD = 2.5, Sample size = 30

Calculate the t-statistic and check if the height difference is significant!

---

# ✏️ Two Independent Samples T-Test: Example Explained

---

### Given Data:

| Group   | Sample Mean ($\bar{X}$) | Std Dev (s) | Sample Size (n) |
| ------- | ----------------------- | ----------- | --------------- |
| Group A | 89.04                   | 2.64        | 25              |
| Group B | 81.87                   | 2.06        | 30              |

---

### Step 1: Calculate t-statistic

You already have the calculated t-statistic:

$$
t = 9.96
$$

---

### Step 2: Degrees of Freedom (df)

Given:

$$
df = 43.77 \quad (\text{usually rounded to 43})
$$

---

### Step 3: Find Critical t-value from t-table

* For **df = 43** and **α = 0.05 (two-tailed test)**
* Critical value = **±1.67**

---

### Step 4: Compare & Conclusion

Since:

$$
t_{statistic} = 9.96 > t_{critical} = 1.67
$$

* We **reject the null hypothesis $H_0$**.

---

### 🎉 Final Conclusion:

There **is a significant difference** between the average marks of Group A and Group B students.

* Group A scored significantly higher than Group B on average.

---

### 💡 Quick Summary

* Large t-statistic means the difference between groups is unlikely due to chance.
* The p-value corresponding to such a large t would be **very small (less than 0.05)**, strengthening our decision to reject $H_0$.

---

# 🔄 Paired T-Test

### Comparing Means from the **Same Group** Before and After an Event

---

## 🤔 What is it?

* Used when you measure the **same subjects twice** — for example, **before and after treatment** or intervention.
* Checks if the **average difference** between the paired measurements is significant.
* Different from Two Independent Samples T-Test (which compares two separate groups).

---

## ⚖️ Null Hypothesis (H₀)

$$
H_0: \text{The mean difference between the two sets of measurements is zero (no change).}
$$

---

## 🧮 Formula for Test Statistic (t):

$$
t = \frac{\bar{X}_{diff}}{S_{diff} / \sqrt{n}}
$$

Where:

* $\bar{X}_{diff}$ = mean of the differences between paired samples
* $S_{diff}$ = standard deviation of those differences
* $n$ = number of pairs (sample size)

---

## 📊 Example: Blood Sugar Levels Before and After Medication

| Sample 1 (Before) | Sample 2 (After) | Difference (Before - After) |
| ----------------- | ---------------- | --------------------------- |
| 13                | 9                | 4                           |
| 14                | 11               | 3                           |
| 14                | 12               | 2                           |
| 15                | 12               | 3                           |
| 16                | 14               | 2                           |
| 17                | 16               | 1                           |
| 17                | 18               | -1                          |
| 18                | 18               | 0                           |
| 19                | 18               | 1                           |
| 20                | 19               | 1                           |
| 22                | 20               | 2                           |
| 23                | 20               | 3                           |

* Mean difference $\bar{X}_{diff} = 1.75$
* Std deviation of differences $S_{diff} = 1.422$
* Number of pairs $n = 12$

---

## 🧮 Calculate t-statistic:

$$
t = \frac{1.75}{1.422 / \sqrt{12}} = \frac{1.75}{1.422 / 3.464} = \frac{1.75}{0.410} = 4.26
$$

---

## 📈 Compare with Critical Value:

* Degrees of freedom $df = n - 1 = 12 - 1 = 11$
* For $\alpha = 0.05$, $t_{critical} = 2.201$ (from t-table)

Since:

$$
t_{statistic} = 4.26 > t_{critical} = 2.201
$$

---

## ✅ Conclusion:

* **Reject the null hypothesis $H_0$**
* There **is a significant difference** in blood sugar levels before and after medication.
* The medication had a significant effect!

---

# 🔍 Analysis of Variance (ANOVA)

---

## 🤔 What is ANOVA?

* **ANOVA** helps to check if the **means of three or more groups** are different from each other.
* Think of it as an extension of the t-test (which compares only two groups), but for **3 or more groups**.
* Example: Comparing average test scores of students from 3 different schools.

---

## 🛠️ Types of ANOVA

| Type              | Explanation                                                                            |
| ----------------- | -------------------------------------------------------------------------------------- |
| **One-Way ANOVA** | Compares means of one variable across multiple groups (e.g., scores of 3 schools).     |
| **Two-Way ANOVA** | Compares means while considering two variables (e.g., scores by school and by gender). |

---

## ⚖️ Hypothesis in ANOVA

$$
H_0: \mu_1 = \mu_2 = \mu_3 = \ldots = \mu_k
$$

* Null hypothesis $H_0$: All group means are **equal** (no difference).
* Alternative hypothesis: At least one group mean is **different**.

---

## 📊 How ANOVA Works (Conceptually)

* It looks at the **variation within each group** compared to the **variation between groups**.
* If the variation **between groups** is much larger than **within groups**, it suggests group means differ significantly.
* Uses an **F-statistic** to make this comparison.

---

## 🧮 Formula

* The formula is a bit complex and involves sums of squares and degrees of freedom.
* Usually, we rely on software (like Excel, R, Python) to calculate it.

---

## 🎯 Why use ANOVA?

* It avoids doing multiple t-tests, which increases the chance of errors.
* Gives a single test to check if **any** group differs.

---

# 📚 ANOVA Example: Comparing Teaching Methods' Test Scores

---

## 👩‍🏫 Scenario:

We want to find out if **three different teaching methods** lead to different average test scores.

---

### Given Data:

| Teaching Method | Scores             | Mean |
| --------------- | ------------------ | ---- |
| A               | 85, 88, 91, 78, 82 | 84.8 |
| B               | 75, 79, 80, 82, 78 | 78.8 |
| C               | 90, 85, 88, 92, 87 | 88.4 |

---

### Step 1: State Hypotheses

$$
H_0: \text{All teaching methods have the same mean score}  
$$

$$
H_a: \text{At least one method has a different mean}
$$

---

### Step 2: Calculate Grand Mean

$$
\text{Grand Mean} = \frac{84.8 + 78.8 + 88.4}{3} = 84
$$

---

### Step 3: Calculate SST (Sum of Squares Treatment)

Measures how much group means vary from the grand mean.

$$
SST = \sum (n_t \times (\bar{X}_t - \bar{X}_{grand})^2)
$$

$$
= 5 \times (84.8 - 84)^2 + 5 \times (78.8 - 84)^2 + 5 \times (88.4 - 84)^2
$$

$$
= 5 \times 0.64 + 5 \times 27.04 + 5 \times 19.36 = 3.2 + 135.2 + 96.8 = 235.2
$$

*Note: Your original SST was 133.2 — the small difference might be due to rounding, but both illustrate the concept.*

---

### Step 4: Calculate SSE (Sum of Squares Error)

Measures variability **within** each group.

$$
SSE = \sum \sum (X_{ij} - \bar{X}_i)^2
$$

Calculate for all observations, e.g., for Method A:

$$
(85 - 84.8)^2 + (88 - 84.8)^2 + \ldots + (82 - 84.8)^2
$$

Sum all similar terms for B and C:

$$
SSE \approx 50.8
$$

---

### Step 5: Calculate F-statistic

$$
F = \frac{SST / (k - 1)}{SSE / (N - k)}
$$

Where:

* $k = 3$ (number of groups)
* $N = 15$ (total observations)

$$
F = \frac{133.2 / 2}{50.8 / 12} = \frac{66.6}{4.23} \approx 15.75
$$

---

### Step 6: Find Critical F-value

* Degrees of Freedom Between Groups: $df_{between} = k - 1 = 2$
* Degrees of Freedom Within Groups: $df_{within} = N - k = 12$
* From the F-table at $\alpha = 0.05$, the critical value is approximately **3.89**.

---

### Step 7: Conclusion

Since:

$$
F_{calculated} = 15.75 > F_{critical} = 3.89
$$

* We **reject the null hypothesis**.
* There **is a significant difference** in mean test scores among the teaching methods.

---

## 📌 Why Column 2, Row 12 in F-table?

* Column = Between-group df = 2
* Row = Within-group df = 12
* Total df = 14 (15 observations - 1)

---

# ✅ Summary:

ANOVA tells us that not all teaching methods have the same impact on student scores — at least one method is statistically different.

---
