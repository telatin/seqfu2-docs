---
title: Get started
description: "Install SeqFu and learn the basics"
tags: [seqfu, installation, usage, fasta, fastq]
---

This page covers installation and basic usage of SeqFu.

## Installation

### Install via Miniconda (recommended)

The recommended installation method is via BioConda, which supports both Linux and macOS. If you have conda installed ([how to install it](https://docs.conda.io/en/latest/miniconda.html)):

```bash
conda install -c conda-forge -c bioconda "seqfu>1.10"
```

:::note
Windows compilation is possible but not officially supported.
:::

### Pre-compiled binaries

Pre-compiled core binaries are distributed with the [releases](https://github.com/telatin/seqfu2/releases), as zip files containing all the tools. Files are labeled "Linux" and "Darwin" for Linux and macOS respectively. When possible, install SeqFu via Miniconda as it provides the full set of tools.

### Manual compilation

1. Install `nim` if not already installed ([see instructions](https://nim-lang.org/install_unix.html)). The `choosenim` method is recommended when available.
2. Clone the repository: `git clone https://github.com/telatin/seqfu2`
3. Compile with `nimble build` (this downloads the required packages)
4. The binaries are available in the `./bin` directory

## Overview

SeqFu consists of core programs, accessible as subcommands, and a set of corollary utilities with the prefix `fu-`.

Type `seqfu` alone to list the core subprograms, and `seqfu {command} --help` to access the help for each specific subcommand.

To print the version, type `seqfu version`. To print the citation, type `seqfu cite`.

## Basic commands

### File operations: cat, head, tail, grep, rc

These commands are inspired by common GNU commands and can read from standard input.

**[seqfu cat](/commands/cat/)** reads mixed FASTA and FASTQ files and outputs in either format. It includes manipulations like:
- Forcing FASTA or FASTQ output
- Manipulating sequence names (prefix, suffix, prepend filename, remove comments)
- Adding info in the header (length, GC content, original name)
- Filtering by length (minimum, maximum, trim bases)

**[seqfu grep](/commands/grep/)** extracts sequences by matching oligonucleotides, scanning the reverse strand and allowing mismatches or partial matches. The oligo can use IUPAC alphabet with ambiguous bases.

**[seqfu head](/commands/head/)** can skip sequences (print the first N sequences, taking one every M) to extract a small subset sampling deeper.

**[seqfu rc](/commands/rc/)** computes the reverse complement, taking both files and sequences as input, and supports IUPAC degenerate bases.

### Inspection: view, qual, stats, count

**[seqfu view](/commands/view/)** provides visual feedback on quality values and oligonucleotide presence (for interactive use).

**[seqfu stats](/commands/stats/)** prints the total number of sequences, bases, average, N50, N75, N90, AuN, minimum and maximum length. Output is available in TSV format or a console-oriented table:

```text
┌────────────────────┬───────┬──────────┬───────┬─────┬─────┬─────┬────────┬─────┬─────┐
│ File               │ #Seq  │ Total bp │ Avg   │ N50 │ N75 │ N90 │ auN    │ Min │ Max │
├────────────────────┼───────┼──────────┼───────┼─────┼─────┼─────┼────────┼─────┼─────┤
│ filt.fa.gz         │ 78730 │ 24299931 │ 308.6 │ 316 │ 316 │ 220 │ 0.385  │ 180 │ 485 │
│ illumina_1.fq.gz   │ 7     │ 630      │ 90.0  │ 90  │ 90  │ 90  │ 12.857 │ 90  │ 90  │
└────────────────────┴───────┴──────────┴───────┴─────┴─────┴─────┴────────┴─────┴─────┘
```

### Dataset management: interleave, deinterleave, lanes

**[seqfu interleave](/commands/interleave/)** and **[seqfu deinterleave](/commands/deinterleave/)** handle paired-end Illumina sequences with high speed and low corruption risk.

**[seqfu lanes](/commands/lanes/)** merges multiple Illumina lanes.

### Sorting and dereplication

**[seqfu sort](/commands/sort/)** sorts sequences by length.

**[seqfu derep](/commands/derep/)** dereplicates datasets, printing the number of identical sequences. It can also process previously dereplicated files while tracking sequence counts.
