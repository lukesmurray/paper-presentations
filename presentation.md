# Clinical Documentation as End-User Programming

## EHR Note taking over time

- Previously: physician's benefit and handwritten
- Currently: largely regulated by insurance and billing and digital
  - goal is to benefit physicians but money often comes first

## How doctors deal with documentation burden

- **copying** text
- using **forms**
- use **templates**
- **many studies deal with copying text this study deals with template and forms**

## Study

- Participants: 48 physicians and 200 staff
- Dataset: 200,000 visits over two years
- examines use of oneliner oneliners
  ![](https://i.imgur.com/fcIKhdY.png)

## Typical EHR Day

1. Providers see patients in two four hour "clinics" per day
2. Providers need to write a summary of each visit
3. Providers typically write 20-40 notes per day

## Canonical Documentation Workflow

1. Technician documents documents exam findings in clinical note.
2. Scribe documents assessment and care plan while while provider works with patient.
3. Provider reviews, edits, and signs scribe note.

_Although collaboration is typical it is not the rule._

## Oneliner Categories

helper oneliners

![](https://i.imgur.com/N16Xs1u.png)

## Oneliner Categories

signatures or attestation

![](https://i.imgur.com/avSM2yL.png)

## Oneliner Categories

full note

![](https://i.imgur.com/TvL4a83.png)

## Oneliner Features

- Data Links represented with `$LINKNAME$` syntax
- Dropdowns represented with `<option 1, option 2>` syntax
- Tab placeholder represented with `***` syntax
- Parameters `.lastbp(3)`

## Methods

- estimate percentage of note created by oneliners
- examine output of notes generated using 50 most frequent data links (`$DATALINKS$`)
- compare data links in 50 most frequent full note templates
- determine who uses oneliners (providers/staff)

## Results

- 5K unique content importing oneliners were used
- invoked 647K times in 200K visits (3.2 per visit)
- 95% of visits use at least 1 oneliner
- 82% of visits used a full note oneliner
- 50% of invocations are full note and signature oneliners
- 80% of oneliners are helper oneliners

## Note Characteristics

![](https://i.imgur.com/nMVrFe2.png)

- some data links import up to 350 words (`$MEDLIST$`) others import at most 1 word (`$AGE$`)
- many data links do the same thing (`$MEDLIST$`, `$CURRMEDLIST$`)
- half of all text in notes created with at least one oneliner is inserted by data links

## Usage Patterns

- 3 oneliners used per visit
  - 1 full note, 1 signature/attestation oneliner , 1 helpful
- staff invoke most full note oneliners (60% staff invoked)
- provider invoke most helper oneliners (74% provider invoked)
- providers invoked avg of 108 unique oneliners (max 508)
- staff invoked avg of 23 unique oneliners
- providers mostly invoked oneliners they created (71%)
- staff mostly invoked oneliners others had created (40%)
- when providers switch full length notes they dramatically reduce note length

## Takeaways

- clinical documentation relies on electronic aids
  - in one study of note contents 46% of note text was copied from prior notes, 36% was imported using tools such as templates, and just 18% was manually typed

## Takeaways

- full note templates most likely are used to meet government, regulatory, and insurance standards
- reliance on full note templates is most likely due to a need to hit a regulatory target not because it creates the best notes

## Takeaways

- oneliners perform abstraction work
- EHRs separate data by type (labs, meds, diagnosis)
- Physicians spend a lot of time aggregating data to tell a coherent story

## Takeaways

- oneliners would be better abstraction tools if they
  - offered better customizability
  - more granular search
  - more powerful synthesis

## Takeaways

- clinicians want to mix data and narrative
- clinicians could benefit from hyperlinking or tanscluding information rather than copying it

## Takeaways

- data links can produce detailed concise summaries
- data links can also bloat notes and create **information overload**
- data links could be improved to be context specific

## Takeaways

- many full note oneliners are used by only one physician and their staff
- when physicians change their full note oneliner they are shaping the process of care that they and their staff deliver

## Future Work

- within this study physicians/staff relied on IT staff to create notes
- future work could leverage end user programming paradigms to enable users to create their own oneliners
