# CRS-000 Faculty Resources

Welcome Faculty!

This directory contains faculty-only course materials, including:

- Answer keys and exemplar solutions
- Grading checklists and guidance
- Faculty teaching resources

All contents are confidential and must remain in this private repository.

## Table of Contents <!-- omit from toc -->

1. [Getting Started](#getting-started)

## Getting Started

1. [**Set up your GitHub account**](https://github.com/GC-STEM/atlas/wiki/GitHub-Setup) once for SNHU teaching assignments. Skip this step if you have already done so.

    {{SME TODO: How do we know the instructor's GitHub username so we can add them to the CRS000-Faculty team?}}

2. **Set up the Course-specific overlay** (CSO) once per device. Skip this step if you have already done so. Otherwise, follow the instructions for your operating system:

   - [**Windows**](https://github.com/GC-STEM/crs000/wiki/CSO-Setup-on-Windows)
   - [**macOS**](https://github.com/GC-STEM/crs000/wiki/CSO-Setup-on-macOS)
   - [**Linux**](https://github.com/GC-STEM/crs000/wiki/CSO-Setup-on-Linux)

    {{SME/AI TODO: Add option to launch the CSO directly from the Vagrantfile. [Virtualization Technologies](https://github.com/GC-STEM/atlas/wiki/Virtualization-Technologies)}}

    <!-- ci:command-test id=setup-personal-repo fixture=empty-repos expect=repo -->
    ```bash
    cd "$HOME/Repos/crs000-faculty"
    vagrant up
    ```

3. **Clone the faculty repository** to your local machine. This repository contains faculty-only course materials.

    Copy and run the following command block to a terminal in your CSO. For help using a terminal, see [**Terminal Basics**](https://github.com/GC-STEM/atlas/wiki/Terminal-Basics).

    <!-- ci:command-test id=setup-personal-repo fixture=empty-repos expect=repo -->
    ```bash
    cd "$HOME/Repos"
    git clone git@github.com:GC-STEM/crs000-faculty.git
    ```

Student-facing course materials are maintained in GC-STEM/crs000 and synchronized into this repository.

- Main course repository: https://github.com/GC-STEM/crs000
- Faculty repository: https://github.com/GC-STEM/crs000-faculty
