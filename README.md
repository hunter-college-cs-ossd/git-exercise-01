# Git Exercise 1

## The Integration Manager Workflow

This is a short exercise designed to help you to understand a very common
workflow used by small to medium-size open source projects that use a
shared, central repository. This workflow is called the 
*Integration Manager Workflow*. In this workflow, there is a single
dedicated repository, called the *blessed repository*, or the 
*canonical repository*, which contains the 
*reference version* of the project source code. All developers have read 
access to this repository, but not write access. 

To contribute to the project, the developer creates her own public clone of 
the project and "pushes" changes to it. Then the developer sends a request to 
the maintainer of the blessed project to "pull in" the changes.

When the canonical repository is located on a remote server, 
such as GitHub or GitLab, what typically happens is that, after the developer
makes her own copy of the project into her public repository, she copies that
copy, i.e., she *clones* that copy to her local host machine, works on that 
local machine, and then pushes the changes back "up" to the 
public clone on the server. That "clone" on the server is technically a 
*fork* of the blessed repository, so we would say she pushes her changes to 
"her fork of the project."

We can now summarize the steps of this workflow as they are performed by a 
contributor to the project

1. On the server (e.g. GitHub) `fork` the canonical repository to the 
contributor's public repository.

2. From the local machine, `clone` the fork of the repository to the 
local machine. On some servers, such as GitHub, there is a button that will
create a paste-able command to do this on the local machine.

3. Under `git` version control on the local machine, make the changes, verify them, and
make the commit to incorporate them into the local machine's clone of the project.
This will involve multiple `git` commands, which are detailed below.

4. Using `git`, push the changes to the fork on the server, e.g. GitHub.

5. On the server, open a `pull request` to have the work reviewed and merged
into the project.

## The Assignment
This `README.md` file is part of a GitHub repository to which you have
read access but neither write nor administrative access.
Your instructor is the project maintainer and has full access to the project.
The assignment is designed to model what you might do to contribute to an
actual software project, but you will not be writing very much code.

### Tasks

These are the steps that you must perform for this assignment.

1. Fork this repository (in GitHub).

2. Clone your fork of the repository to your local machine.

3.  Add an `upstream` remote to this repository using the `git remote add ...` 
command.

4.  Add a new file in the `sources/` directory. The filename should be named
`YOUR_GITHUB_USERNAME.cpp` where you must replace `YOUR_GITHUB_USERNAME` 
by your actual GitHub username. This file should be a succinct C++
program that will output two sentences. The first should be

    * `Hello world from YOUR_GITHUB_USERNAME`,
where `YOUR_GITHUB_USERNAME` is replaced by your actual GitHub username. 
    * The second should be a "fun fact" about yourself that you are willing to
share, not only with us, but with the world.

    Your program should be a proper program, with proper documentation, and should be as 
short as you can make it.

5. Compile and test your program to make sure it runs.

6. Track the source file using the `git add` command. Do not track the executable!

7. Commit your changes using the `git commit` command.

8. Push your changes to your fork (the `origin` remote) on GitHub.

9. Open a Pull Request to `hunter-college-cs-ossd/Git-Exercise-01` with your additions

10.  Ask the instructor to review your Pull Request - the exercise is complete once your changes have been merged.
