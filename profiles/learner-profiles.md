---
title: Learner Profiles
---

## Who Should Take This Workshop?

This workshop is designed for researchers learning workflow automation with Make. Below are three representative learner profiles. Do you see yourself in one of these?

---

## Profile 1: Dr. Patel - Genomics Researcher with Repetitive Pipelines

### Background
Dr. Patel is a postdoctoral researcher in the biology department at Pomona running a genomics lab. Her research involves analyzing whole-genome sequencing data—a complex pipeline with 8-10 steps: quality control, alignment, variant calling, annotation, statistical testing, and visualization. She currently runs each step manually, watching for completion before starting the next. New data arrives weekly, and each analysis takes days of her time clicking between terminals and scripts.

### What She Knows
- Proficient with Unix shell and shell scripting
- Comfortable writing Python and R scripts
- Understands her analysis pipeline in detail
- Has heard of "workflow managers" but only knows shell scripts
- Can write and debug code effectively

### Why She Needs This
- Running the same 8-step pipeline weekly is wasteful
- Easy to accidentally run steps out of order
- Hard to remember which version of which script was used
- New data requires re-running entire pipeline
- Wants to delegate routine analysis to undergraduates without micromanaging

### Her Goals
- Automate her entire genomics pipeline
- Ensure reproducibility (same input = same output)
- Allow others to run the pipeline without her oversight
- Save time for actual science instead of running commands
- Document the pipeline so it's clear what happens when

### Challenges She'll Face
- Makefiles syntax is initially confusing (significant whitespace!)
- Temptation to just add more shell scripts instead of using Make
- Difficulty thinking in terms of file dependencies
- May not understand why Make is better than "just run this script"
- Getting initial Makefile setup right requires patience

### Success Indicator
After this workshop, Dr. Patel can:
- Write a Makefile for her genomics pipeline
- Run the entire analysis with one command: `make`
- Update input data and automatically re-run only necessary steps
- Share the Makefile so her team can reproduce analysis
- Add new steps without re-writing the entire pipeline

---

## Profile 2: Jackson - Physics Student Running Simulations

### Background
Jackson is a senior physics major at Pomona doing computational research on climate modeling. His thesis involves running a series of climate simulations with different parameter settings—30+ variations that take hours each. Currently, he submits each job individually to Sagehen HPC cluster, monitors which are complete, and then runs post-processing analysis scripts. Managing 30 simulations manually is tedious and error-prone.

### What He Knows
- Comfortable with Unix shell from workshop
- Written basic Python scripts
- Familiar with HPC job submission (from intro HPC workshop)
- Understands his simulation workflow conceptually
- Has multiple interdependent scripts

### Why He Needs This
- 30 parameter sweeps create 30+ jobs to track
- Post-processing must wait for all simulations to complete
- Easy to accidentally forget a simulation or re-run one unnecessarily
- Wants to submit all jobs with one command
- Thesis deadline: needs to run many variations quickly

### Her Goals
- Automate submitting all 30 simulations
- Ensure post-processing runs only after all simulations complete
- Handle job failures gracefully
- Re-run only necessary simulations if parameters change
- Graduate with actual thesis results, not administrative burden

### Challenges She'll Face
- Understanding job dependencies (simulation X must finish before post-processing)
- Coordinating HPC job submission with local Make workflow
- Dealing with long-running jobs and waiting time
- Debugging Makefiles when simulations fail
- Temptation to just write a bash script instead

### Success Indicator
After this workshop, Jackson can:
- Write a Makefile for his simulation workflow
- Submit multiple dependent jobs efficiently
- Handle failures without losing progress
- Regenerate results from the Makefile if needed
- Feel confident his thesis analysis is reproducible

---

## Profile 3: Dr. Chen - Data Scientist with Complex Workflows

### Background
Dr. Chen is a visiting lecturer in computer science at Pomona who specializes in machine learning applications. She's teaching a capstone course where student teams build machine learning projects with data cleaning, feature engineering, model training, and evaluation. Each team's workflow involves many Python scripts, data transformations, and model evaluations. Some teams accidentally run steps out of order; others re-do expensive computations unnecessarily.

### What She Knows
- Strong programming background (Python, shell)
- Understands machine learning workflows
- Experienced with complex data pipelines
- Has heard of tools like Snakemake but wants to start simple
- Wants to teach best practices to her students

### Why She Needs This
- Student projects need documented, reproducible workflows
- Teams are duplicating effort and making mistakes
- Wants to require "proper workflow management" as a learning objective
- Needs to teach her students automation best practices
- Complex pipelines are good practice for industry careers

### Her Goals
- Teach workflow automation as a course requirement
- Ensure student projects are fully reproducible
- Have students learn professional practices early
- Create templates so students start with good structure
- Demonstrate that automation is a key skill

### Challenges She'll Face
- Make isn't the trendiest tool; students might ask "why not Snakemake?"
- Convincing students that workflow automation is worth learning
- Teaching Make syntax while also teaching ML content
- Helping students who are new to shell and Make simultaneously
- Balancing simplicity with realistic, complex workflows

### Success Indicator
After this workshop, Dr. Chen can:
- Write Makefiles that model ML workflows
- Create templates for her students
- Teach workflow automation in her capstone course
- Help students debug their Makefiles
- Show students how to think about dependencies and automation

---

## Using These Profiles

**During teaching:**
- Reference Dr. Patel when discussing pipelines: "Like her genomics workflow, this has multiple steps..."
- Use Jackson's example for dependencies: "You can't process results until simulations finish..."
- Draw on Dr. Chen's teaching perspective: "Your future employers expect this..."

**When explaining concepts:**
- Use realistic, multi-step workflows (not toy examples)
- Show time-saving benefits: "Instead of 30 commands, just type `make`"
- Emphasize reproducibility and delegation

**For pacing:**
- Dr. Patel needs depth for a real pipeline
- Jackson needs to understand job submission integration
- Dr. Chen wants practical teaching examples

---

## Common Threads

Despite different backgrounds, all three learners share:

1. **Repetitive workflows**: Running same steps over and over
2. **Complex dependencies**: Steps that must happen in order
3. **Significant time investment**: Workflows take hours or days
4. **Multiple people involved**: Want to delegate/share work
5. **Desire for reproducibility**: Need to recreate results

## Teaching to Diverse Learner Types

### What Works Well

- **Real workflows**: Use actual research pipelines, not toy examples
- **Time savings focus**: Show how Make reduces command-line overhead
- **Dependency visualization**: Draw diagrams showing what depends on what
- **Practical exercises**: Have learners automate parts of their own work
- **Troubleshooting together**: Make Makefile debugging a collaborative activity
- **Celebrate automation wins**: "You just saved an hour of manual work!"

### Pacing Tips

- **For ambitious researchers like Dr. Patel**: Show advanced Make features, how to scale
- **For HPC-focused learners like Jackson**: Explain Make + job submission interaction
- **For educators like Dr. Chen**: Provide teaching templates and examples
- **For all**: Normalize Makefile confusion ("Whitespace is weird at first!")

---

## After the Workshop

These learners won't be Make experts, but they will:

- Understand when to use Make vs. shell scripts
- Write Makefiles for realistic workflows
- Think in terms of file dependencies
- Automate repetitive analysis tasks
- Know how to maintain and update pipelines

Many will return for:
- **Advanced Make** (pattern rules, more complex dependencies)
- **Workflow Managers** (Snakemake, Nextflow) if they outgrow Make
- **Workshop 0: Introduction to HPC** (integrating Make with cluster jobs)
- **Git and Make together** (version control for pipelines)

Your role is to show them that the initial time investment in a Makefile pays off immediately and multiplies as they run the workflow again and again.

---

## Real Impact

Emphasize that:

- **Dr. Patel's genomics pipeline** goes from "one day to set up" to "one command"
- **Jackson's 30 simulations** are managed automatically; no human tracking
- **Dr. Chen's students** graduate with professional workflow skills
- **All their research** becomes more efficient, more reproducible, and shareable
