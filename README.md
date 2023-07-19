# qrandom.lumii.lv

by Institute of Mathematics and Computer Science, University of Latvia

## Overview

The QRNG service project is a unique solution designed to serve as an alternative to `/dev/random`. The project is composed of a character device and a userspace service working together to provide a reliable source of random bytes. This repository holds all the necessary files and instructions to build and install the character device and the userspace service.

## Purpose

The prime goal of this project is to provide a fresh source of random bytes that can be accessed via `/dev/qrandom0`, effectively replacing the traditional `/dev/random`. This mechanism works by having the userspace service feed random bytes into a kernelspace character device driver.

Out of the box, the service is configured to use a Pseudorandom Number Generator (PRNG). However, it is designed to be versatile. By default, it fetches random bytes from a remote Quantum Random Number Generator (QRNG) offered by [qrng.lumii.lv](https://qrng.lumii.lv/). It's also adaptable to cater to other requirements based on your project's needs.

This project presents a significant leap forward in achieving better randomness in systems, a crucial aspect in areas like cryptography, where the strength of encryption often relies on truly random numbers. Offering a more efficient and versatile way of generating random numbers, this QRNG service brings enhanced security and robustness to your applications.
