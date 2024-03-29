# Summary - Theory

## Project management triangle

1. Time:

   The actual time required for a product to be delivereable

2. Cost:

   The amount of money required to complete the project

3. Scope:

   The functional elements that make up the project deliverables.

> They are dependent on each other
>
> *Example*: If time reduces => Scope reduces || cost increases.

## Software development lifecycle

1. Requirement gathering
2. Analysis
3. Design architecture
4. Implementation
5. Testing

## WaterFall

- Requirement gathering
  - For a **good requirement**, it needs to be:
    - *Consistent*
    - *Modifiable*
    - *Traceable*
    - *Unambiguous*
    - *Complete*
    - *Verifiable* (between both parties)
    - *Feasible* (doable)
- Analysis
  - Document all the requirement
- Design
  - Structure/database/workflow/interaction/interface design.
- Implementation
  - Start coding
- Testing.

> If testing fail then have to start a gain from start.

## Spiral model

1. Risk analysis
2. Plan
3. Evaluate
4. Engineer

> From 4 loop back to 1.

## RUP

Replace requirement with **use case**

Between AGILE and Waterfall, another step from waterfall.

- **Use case driven**

- Architect **based on usecase**

- Develop bit by bit rather than the whole project.

- 4 Components

  - Worker
  - What
  - How
  - When

- Phases:

  1. Inception - *What to build?*

  2. Elaboration - *How to build?*

  3. Construction - *Build*

  4. Transition - *Test/validate*

> Problem:
>
> - Still based on document (less than waterflow)
> - Release <u>often</u> (but not enough)



## Agile

- Improve **use case** with **user stories**

  - how to write user stories:
    - As a [...], I want to[....], so I can [...]

- Increment development

- fast and flexible to change

- continuous, frequent delivery

- Popular: 

  - Scrum

    - Roles: 
      - Product Manager
      - Scrum master
      - Team member
    - Ceremonies:
      - Sprint planning
      - Sprint review
      - Sprint retrospective
      - Daily scrum meeting
    - Artefacts:
      - Product backlog *(wish list)* -> Release backlog (*selected for this release)* -> Sprint backlog (*selected for this sprint*)-> Burnt down chart *(How many more to do)*

  - XP

    - Not many document
    - Release weekly
    - **Pair programming**
    - Only keep code, test

    *Compare with RUP.*

## USE CASE

#### Use case context

| Use case name          |      |
| ---------------------- | ---- |
| Version                |      |
| Goal                   |      |
| Summary                |      |
| Actors                 |      |
| Basic course of action |      |
| Alternative path       |      |
| Post condition         |      |
| Business rules         |      |
| Notes                  |      |
| Author & Date          |      |

## ...

## Sequence diagram

> Centralised control:
>
> - Everything pass back to one main class to process.
>
> Distributed control:
>
> - Information is pass between classed to process

## State machine

Format: 

```python
event[guard]/action
// or
event[guard1 && guard2]/action
```

> *Event also known as Trigger.*
>
> **Everything is optional.**
>
> At any state, **There can only be 1 transition out that has the same event**
>
> => Guard has to make it exclusive.
>
> <u>Example:</u>
>
> - Play[CD] vs Play[noCD]

## ...

## Testing

### 5 Essentials

1. <u>Quality</u> of the test **determines** <u>success</u>
2. Prevent fault/error by using early life-cycle testing techniques
3. A person must be responsible for improving the test process.
4. Required trained/skilled people
5. Remain a positive attitude (*Don’t get mad if they destroy your program*)

### Basic definition

- Error
- Fault - *result from error*
- Failure - *result from fault*
- Incident - *sympton of failure*
- Test case - *to find failure*
- Test - the action

### Life cycle

Testing -> fault classification -> fault isolation -> fault resolution

### V-Model in Software Delopment Lifecyce

> V stands for verify (trick to remember)

| Document verification      | Acceptence test  |
| -------------------------- | ---------------- |
| Specification verification | System test      |
| Design verification        | Integration test |
| Coding verification        | Unit test        |

*Test through out the <u>development effort</u>*

> <u>Development effort:</u>
>
> - Planning
> - Configuration
> - Staffing
> - Test development
> - Test execution

### Step by Step to test

1. Plan
2. Develop test case
3. Run test case
4. Evaluate test result
5. test deliveries
   1. Report
   2. Statistics

### When can we stop

1. It’s too close to the shipping time, have to release
2. Lack of time, resources.

How to determine?

- Base on density of error
- Base on frequency of test rebugs
- Number of open bugs.

### White box vs Black box

| white box                                               | black box                       |
| ------------------------------------------------------- | ------------------------------- |
| Need to understand coding                               | Don’t need to understand coding |
| Test based on functionality of the code, system related | Usability test                  |
|                                                         | Performance test                |
|                                                         | Stress test                     |
|                                                         | Configuration                   |
|                                                         | Other non-functional test.      |
|                                                         |                                 |

### Testing activities

1. Initiation phase - *Document verification*
2. Requirement phase - *Review all the document, begin designing acceptence test*
3. Software architecture phase - *Review the architecture design, start designing system test*
4. Detail design phase - *Review the design document, start designing integration testing*
5. Implementation phase - *Code inspect, design/implement unit test*
6. Integration and testing phase - *Intergrate the tested unit*
7. Acceptence and transition phase - *Do system testing dessigned in phase 3, black box testing*
8. Acceptence testing and review.

### Test case specification

| identifier                    | uniqueID                               |
| ----------------------------- | -------------------------------------- |
| test items                    | components / feature being test        |
| input specification           |                                        |
| out put specification         | expected output                        |
| environment need              |                                        |
| special procedure requirement | contraint or special need              |
| iner-case dependencies        | any dependencies (any extra libraries) |

### Why bug not fixed

- Not enough time
- Not real bug
- Too risky to fix
- Not worth to fix
- bug reporting is <u>not good</u>
  - **TO BE GOOD:**
    - non-judgement, non-personal
    - well described
    - following up on bug reports.

### Bug report sample

| title              |      |
| ------------------ | ---- |
| Description        |      |
| Severity/ Priority |      |
| Reproduction steps |      |
| Expected result    |      |
| Actual result      |      |

### Bug life cycle

1. Open - *Waiting to be fixed*
2. Resolved - *Fixed, waiting to be tested*
3. Closed - *Tested and approved*

### Rationale testing

- Equivalence class testing:
  - Divide test cases into different group of test case:
    - < 18; 18 - 50; > 50
- Boundary Value testing
  - Test a specific **boundary value** instead of a group
  - Boundary value could be the boundaries where the two value meet.
  - For example:
    - Testing for under 16, boundary could be
    - Age = 15, 16

### Validation vs Verification

- Validation: to be valid
  - Are we building the right product?
  - Unit testing, integration testing, system testing, acceptance testing.
- Verification: 
  - Are we building the product right?

### Regression testing

Involves detecting new bugs or defects.

Through changes that attempt to fix existing bugs

### JUnit test

```java
public class carTest {
 @Before
  public void setUp() throws Exception{
    car = new Car(100,100,10);
  }
  @After
  public void tearDown() throws Exception {

  }

  @Test
  public void testMove1() {
    car.move();
    assertEquals(120, car.getX());
  }
  @Test
  public void testMove2() throws SpeedException {
    car.move();
    assertEquals(120, car.getSpeed());
  }
  @Test (expected = SpeedException.class)
  public void testAccelerate() throws SpeedException {
    car.accelerate();
    car.accelerate();
    car.accelerate();
  } 
}
```

#### @BeforeClass

`@BeforeClass` is used when you want to execute it *just once* when the class is first loaded.

Handy for connecting to the database.

```java
@BeforeClass
public static void setupClass() throws Exception {
  // Do stuff
}
```

#### @AfterClass

`@AfterClass` will be execute *just once* when the class finished. Suitable for cleaning up the test.

```java
@AfterClass
public static void cleanUp() throws Exception {
  // Do stuff
}
```

#### @Before

`@Before` is used ==before the class is test==. Suitable for *Setting up, initialise variables.*

```java
@Before
public void setup() throws Exception {
  int a = 10;
  Program p = new Program();
}
```

#### @After

`@After` is used ==After the class is test==. Suitable for *releasing resources such as files*

```java
@After
public void free() throws Exception {
  a = null;
  Program p = null;
}
```

> You can have @Before and @After as many times as you want.

#### @Test

`@Test` is used <u>to test the class.</u> Use `assertTrue(condition)` or `assertEquals(constant, variable)` to test.

```java
@Test
public void testCase1 throws Exception() {
  a += 10;
  assertEquals(10,a);
  assertTrue(a>=10);
}
```

##### Specify how long the method is gonna take

```java
@Test(timeout = 10) 
public void testCase2 throws Exception() {
  assertTrue(a*999999 > 200000);
}
```

##### Specify what exception class expecting

```java
@Test(expected = SomeOtherException.class)
public void testCase3 throws Exception() {
 	a/=0;
}
```

