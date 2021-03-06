# What's new in ILAng

## 1.0.4 - 2020-06-17

#### Updates

* Revamp filesystem utilities with `c++17` features.
* Set off \(default\) the synthesis engine interface for future OS \(due to the deprecation of Python2\).
* Update CI setups accordingly.
* Regular maintenance, e.g., clean up redundant unit tests and leaving temporary files.

## 1.0.3 - 2020-06-02

#### Updates

* Include `smt-switch` interface support.
* New external library `fmt` for string formatting.
* New ILA passes for optimization and simplification.

## 1.0.2 - 2020-01-09

#### Updates

* Include invariant synthesis support.
* New external project - SMT parser.
* New external project - VCD parser.

## 1.0.1 - 2019-11-01

#### Updates 

* Change numeric of bit-vector constant from `int` to `uint64_t`
* Several improvements on the Verilog parser

## 1.0.0 - 2019-09-18

#### Updates

* ILA modeling
* Importing from ItSy \(synthesized abstraction\)
* Importing/exporting ILA portables
* Exporting ILA to Verilog
* Unrolling and exporting ILA to SMT
* Generate verification targets based on the provided refinement relation

## 0.9.0 - 2019-02-05 \(pre-release if v1.0.0\)

#### Updates

* Hard-fix Bison version in Travis CI OS X test since Verilog parser does not build for 3.3.1.
* Re-detect language in LGTM analysis. 
* Restructure: move examples to PrincetonUniversity/IMDb.
* Improve code quality and clean up the repository. 
* Backward compatibility for z3 below 4.6.0. 

