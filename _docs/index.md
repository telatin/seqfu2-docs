---
title: SeqFu 2.0
description: "A suite of utilities for FASTA/FASTQ file manipulation"
tags: [seqfu, fasta, fastq, bioinformatics, sequence]
permalink: /
---

[![Seqfu-Nim-Build](https://github.com/telatin/seqfu2/actions/workflows/nim-2.yaml/badge.svg)](https://github.com/telatin/seqfu2/actions/workflows/nim-2.yaml)
[![Latest release](https://img.shields.io/github/v/release/telatin/seqfu2)](https://github.com/telatin/seqfu2/releases)
[![Bioconda Downloads](https://img.shields.io/conda/dn/bioconda/seqfu?label=Bioconda%20Downloads)](https://anaconda.org/bioconda/seqfu)

😺 **[Repository](https://github.com/telatin/seqfu2)** | 📦 **[Releases](https://github.com/telatin/seqfu2/releases)** | 📃 **[Paper](https://www.mdpi.com/resolver?pii=bioengineering8050059)**

SeqFu is a general-purpose program to manipulate and parse information from FASTA/FASTQ files, supporting gzipped input files. It includes functions to interleave and de-interleave FASTQ files, rename sequences, and count and print statistics on sequence lengths. SeqFu is available for Linux and macOS.

![Seqfu splash]({{ site.baseurl }}/assets/img/screenshot-seqfu.svg)

## Features

- A compiled program delivering high-performance analyses
- Supports FASTA/FASTQ files, including gzip-compressed files
- A growing collection of handy utilities for quick inspection of datasets
- UNIX-like commands specific to sequences: `seqfu cat`, `seqfu head`, `seqfu tail`, `seqfu grep`
- Terminal-friendly reports from `seqfu stats` or `seqfu count`

## Quick install

Install via conda:

```bash
conda install -c conda-forge -c bioconda "seqfu>1.10"
```

See the [Get started](/get-started/) page for more installation options.

## Citation

> Telatin A, Fariselli P, Birolo G. *SeqFu: A Suite of Utilities for the Robust and Reproducible Manipulation of Sequence Files*. Bioengineering 2021, 8, 59. [doi.org/10.3390/bioengineering8050059](https://doi.org/10.3390/bioengineering8050059)
