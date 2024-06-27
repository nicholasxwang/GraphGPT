# GraphGPT
```
🚧 WORK IN PROGRESS FOR THIS DOCUMENT
```

GraphGPT is a new machine-learning model tailored for educational purposes emphasizing intuition, logic, and visual presentation. Read the paper [here (link will be added shortly)]().  In this `README.md` file, I will be going over specific details that wasn't mentioned in the paper if you would like to learn more about how GraphGPT works.

**Abstract**
> In this paper, we introduce GraphGPT, a novel machine-learning approach designed for intuitive, logical, and visual education. GraphGPT is inspired by the observation that scientific graphs help learners visualize concepts, while causal graphs enhance the logic of responses. By combining the masked prediction capabilities of GPT with transform prediction using causal graphs, we can improve explanation accuracy. GraphGPT generates logical steps alongside diagrams, significantly enhancing intuition and visual presentation compared to ChatGPT. Experimental results show that GraphGPT outperforms ChatGPT by 25\% in accuracy for multiple-choice questions. Furthermore, a vast majority of participants in the subjective tests confirmed that GraphGPT surpasses ChatGPT in all four evaluation categories. Many highlighted the diagrams and graphical explanations as key factors, giving GraphGPT a notable intuitive advantage.


## Why GraphGPT over Text-Based GPTs?
Many students learn better in a classroom with a teacher explaining or even with a peer tutor than at home, reading a textbook. Why? This is because when someone is taught a topic in person, they are learning it intuitively and often visually, on a whiteboard. Modern AI technologies such as ChatGPT cannot accomplish this as they are a text model. However, ChaGPT understands the struggles of students learning intuitively and bridges this gap in AI Education.

Learning with graphs and diagrams offers countless advantages such as
- **Graphs never lie.** Sometimes, your intuition or logic might not be the answer.
- **Graphs are memorable.** During a timed test, its much easier to draw one graph and shift the lines than going through each step, and even risk making silly mistakes.
- **Graphs are intuitive.** Often, definitions or relationships might not make sense for a student new to the subject. However, with graphs, its much more straightforward.
- **Visual Learning.** Many students are visual learners and would prefer to "see" concepts in front of them

## 💰 Macroeconomics (Example of GraphGPT)
> Credits to [Alex Chen](https://github.com/dynoscord) for helping me with this

**Macroeconomics** is a social science that studies the performance, structure, behavior, and decision-making of an economy of a country as a whole. 

There are 7 key graphs in Macroeconomics:
- Supply & Demand
- PPC (Production Possibilities Curve)
- AD/AS (Aggregate-Demand/Aggregate-Supply)
- Philips Curve
- Money Market
- Loanable Funds
- International Currency Exchange

Key Formulas
- $AD = C+I+G+X$
- $r = nIR - eIR$


### Variables
| Symbol | Meaning                 |
|--------|-------------------------|
| S      | Supply                  |
| D      | Demand                  |
| C      | Consumer Spending       |
| I      | Investment Spending     |
| G      | Government Spending     |
| X      | Exports                 |
| M      | Imports                 |
| NX     | Net Exports             |
| AD     | Aggregate Demand        |
| AS     | Aggregate Supply        |
| PL     | Price Level             |
| Y      | Output                  |
| SRPC   | Short Run Philips Curve |
| U      | Unemployment            |
| Inf    | Inflation               |
| MS     | Money Supply            |
| DR     | Discount Rate           |

### Macroeconomics Causal Graph 
```mermaid
graph TD
    S --> P
    S --> Q
    D --> P
    D --> Q
    C --> AD
    I --> AD
    G --> AD
    NX --> AD
    M --> NX
    X-->NX
    AD-->Y
    AD-->PL
    AS-->Y
    AS-->PL
    AS-->SRPC
    SRPC-->AS
    AD-->U
    AD-->Inf
    Inf-->PL
    PL-->Inf
    Y-->U
    U-->Y
    SelfAdjustment --> AS
    Fiscal-->Tax
    Fiscal-->G
    Monetary-->Bonds
    Bonds-->MS
    Monetary-->DR
    Monetary-->RR
    DR-->r
    RR-->r
    Tax-->C
    PPC-->LRAS
    LRAS-->PPC
    LRPC-->LRAS
    LRAS-->LRPC
    PPC-->LRPC
    LRPC-->PPC
    I --> Growth
    Growth-->LRAS
    MS-->nIR
    MS-->Q$
    MD-->nIR
    MD-->Q$
    SLF-->rIR
    SLF-->QLF
    DLF-->rIR
    DLF-->QLF
    IOR-->r
    nIR-->r
    rIR-->r
    r-->I
    LRAS --> SelfAdjustment
    SelfAdjustment --> AS
    Wages--> PL
    r --> Appreciation
    r --> Depreciation
    PL --> Appreciation
    PL --> Depreciation
    Appreciation --> NX
    Depreciation --> NX
    ForeignInvestment --> r
```

### Questionaire
Questionaire is linked [here](https://docs.google.com/document/d/1aQat4cVoHsBqe1YZONiW4iaPVp-nlCsoxwKSrpdNQCY/edit).

### Text-Processing and Rendering
### List of Commands

### Macroeconomics Dataset Example Questions
wip.

## Further Applications to Various Subjects
> Work in Progress

### 🛒 Microeconomics
Graphs and Diagrams in Microeconomics include:
- Supply/Demand
- PPC (Possibilities Production Curve)
- International Trade with Tarrifs
- Perfect Competition
- Monopoly
- Natural Monopoly
- Monopolistic Competition
- Game Theory
- Labor Markets
- Monospony
- Externalities

### ⚡ Physics
Graphs in Physics include:
- Position-Time
- Velocity-Time
- Acceleration-Time
- Force-Time
- Force-Displacement
...

### 🧪 Chemistry
wip.
### $\pi$ Algebra
wip.
### $\triangle$ Geometry
wip.
### $\int$ Calculus
Concepts in Calculus that can be explained visually can be:
- Integration
  - Riemann Sums
- Differentiation
  - Relationship between multiple degrees of differentiation for the same function
  - Instantaneous Slope
