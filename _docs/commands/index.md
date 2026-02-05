---
title: Commands
permalink: /commands/
---

Each of the following tools can be invoked as a subcommand of *SeqFu*.

Invoking `seqfu` will display a list of internal commands:

```text
SeqFu 1.24.0 - FASTX Tools

      ____             _____
     / ___|  ___  __ _|  ___|   _
     \___ \ / _ \/ _` | |_ | | | |
      ___) |  __/ (_| |  _|| |_| |
     |____/ \___|\__, |_|   \__,_|
                    |_|
  · bases               : count bases in FASTA/FASTQ files
  · check               : check FASTQ file for errors
  · count [cnt]         : count FASTA/FASTQ reads, pair-end aware
  · deinterleave [dei]  : deinterleave FASTQ
  · derep [der]         : feature-rich dereplication of FASTA/FASTQ files
  · interleave [ilv]    : interleave FASTQ pair ends
  · lanes [mrl]         : merge Illumina lanes
  · list [lst]          : print sequences from a list of names
  · metadata [met]      : print a table of FASTQ reads (mapping files)
  · rotate [rot]        : rotate a sequence with a new start position
  · sort [srt]          : sort sequences by size (uniques)
  · stats [st]          : statistics on sequence lengths
  · tofasta             : convert multiple formats to FASTA
  · trim                : trim FASTQ sequences based on quality

  · cat                 : concatenate FASTA/FASTQ files
  · grep                : select sequences with patterns
  · head                : print first sequences
  · less                : interactive viewer for sequences (like less)
  · rc                  : reverse complement strings or files
  · tab                 : tabulate reads to TSV (and viceversa)
  · tail                : view last sequences
  · view                : view sequences with colored quality and oligo matches

Type 'seqfu version' or 'seqfu cite' to print the version and paper, respectively.
Add --help after each command to print its usage.
```



