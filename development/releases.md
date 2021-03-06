# Release Notes

## 1.1.4 - 2020-09-29

#### Updates

* Renaming namespace `AbsKnob` to `absknob` for consistency
* Bug fixes in `Ilator`

## 1.1.3 - 2020-08-24

#### Updates

* New `PathUnroller` that takes templated `SmtShim` for broader SMT support
* Bug fixes in `smt-switch` interface

## 1.1.2 - 2020-07-20

#### Updates

* New `SmtShim` to provide a unified interface for both z3 and smt-switch
* Update smt-switch interface for their new releases
* New pass `SanityCheckAndFix` for checking instruction set completeness and determinism \(hierarchically\)
* Unify `ExprFuse` and `ast_fuse` into namespace `asthub`

## 1.1.1 - 2020-07-14

#### Updates

* New pass `SimplifySyntactic`
* ILAtor support for initial condition setup using SMT queries
* ILAtor bug fix in cascaded conditional memory update
* Unroller support external interpretation of uninterpreted function
* Redesign expression node hashing \(`ExprMngr`\)

## 1.1.0 - 2020-07-08

#### Updates

* New simulator generation \(class `ilator`\) to optimize compile time and simulation time.
* Enrich top-level interface to help unrolling SMT \(z3 specifically\) of program fragments.
* Misc. utilities \(e.g., `util` and `AbsKnob`\).

## 1.0.5 - 2020-06-18

#### Updates

* Support CMake build system for ILAtor generated simulators.
* Performance profiling and improvements.
* Regular maintenance and bug fixes.

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

