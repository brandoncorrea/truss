This project uses Break Versioning (https://www.taoensso.com/break-versioning)

## `1.11.0` (2023-07-31)

> 📦 [Available on Clojars](https://clojars.org/com.taoensso/truss/versions/1.11.0)

This is a **maintenance + feature release**, and should be a non-breaking upgrade.

### New since `1.10.1`

* f42b81b [mod] Improve invariant violation output
* 02c027e [new] Add `cljdoc.edn` config (improve cljdoc output)

### Other improvements since `1.10.1`

* 9ff9d55 [nop] More reliable predicate parsing


## `1.10.1` (2023-07-15)

> 📦 [Available on Clojars](https://clojars.org/com.taoensso/truss/versions/1.10.1)

This is a **hotfix release**, please upgrade if you're using `1.10.0`.

### Fixes since `1.10.0`

* 46b2f69 [fix] Prevent `get-source` from throwing for JAR resources


## `1.10.0` (2023-07-07)

> 📦 [Available on Clojars](https://clojars.org/com.taoensso/truss/versions/1.10.0)

This is a minor **feature release**, and should be a non-breaking upgrade.

### New since `1.9.0`

* 9855aa9 [new] Add `:column` and `:file` to `:loc` data for invariant violations
* 042eb78 [nop] Add tests for GraalVM compatibility


## `1.9.0` (2023-03-15)

```clojure
[com.taoensso/truss "1.9.0"]
```

> This is a **feature release**. Should be non-breaking.
> See [here](https://github.com/taoensso/encore#recommended-steps-after-any-significant-dependency-update) for a tip re: general recommended steps when updating any Clojure/Script dependencies.

### Since `1.8.0`

- 4bbab6b [new] Add unevaluated arg `:form` info to invariant violations
- 9a572b1 [new] Add `:instance?`, `:satisfies?` special predicate forms
- e644631 [new] Experimental alternative workaround for CLJ-865


## v1.8.0 - 2022 Dec 13

```clojure
[com.taoensso/truss "1.8.0"]
```

> This is a **maintenance release**. _Should_ be non-breaking.
> See [here](https://github.com/taoensso/encore#recommended-steps-after-any-significant-dependency-update) for a tip re: general recommended steps when updating any Clojure/Script dependencies.

### Since `v1.7.2`

- e1a1fa6 [new] Document and provide workaround for CLJ-865
- 2e3fa98 [fix] [#12] Fix issue with duplicate side effects when using within another macro


## v1.7.2 - 2022 Nov 20

```clojure
[com.taoensso/truss "1.7.2"]
```

> This is a **maintenance release**. Changes may be BREAKING for some users, see relevant commits referenced below for details.  
> See [here](https://github.com/taoensso/encore#recommended-steps-after-any-significant-dependency-update) for a tip re: general recommended steps when updating any Clojure/Script dependencies.

### Changes since `v1.6.0`

- 67093d9 [mod] [BREAKING] Simplify default error output
- 09779a4 [mod] [DEPRECATE] Shorten names of dynamic assertion utils
- [nop] Update from .cljx to .cljc
- [nop] Remove unused Cljs macros


## v1.6.0 - 2020 Aug 29

```clojure
[com.taoensso/truss "1.6.0"]
```

> Minor feature release. _Should_ be non-breaking.
> See [here](https://github.com/taoensso/encore#recommended-steps-after-any-significant-dependency-update) for a tip re: general recommended steps when updating any Clojure/Script dependencies.

Identical to `1.6.0-RC1`.

#### New since `1.5.0`

* [New] Add special cardinality predicates: `:n=`, `:n>=`, `:n<=`

#### Changes since `1.5.0`

* [#9] Return verbatim input/s on successful :in
* Micro optimization: avoid unnecessary vector creation for multi-x `have?`

#### Fixes since `1.5.0`

* `have?` should return true during elision

## v1.6.0-RC1 - 2019 Mar 22

```clojure
[com.taoensso/truss "1.6.0-RC1"]
```

* [New] Add special cardinality predicates: `:n=`, `:n>=`, `:n<=`
* [Change] [#9] Return verbatim input/s on successful :in
* [Fix] `have?` should return true during elision
* [Implementation] Micro optimization: avoid unnecessary vector creation for multi-x `have?`

## v1.5.0 - 2017 Apr 09

```clojure
[com.taoensso/truss "1.5.0"]
```

* [#8] **Fix**: provide a clear error message when val eval fails (@martinklepsch)
* General improvements to help clarify error messages.

## v1.4.0 - 2017 Mar 27

```clojure
[com.taoensso/truss "1.4.0"]
```

* [#8] **Fix**: show full record values in error messages (@martinklepsch)

## v1.3.7 - 2017 Feb 13

```clojure
[com.taoensso/truss "1.3.7"]
```

* Improved some docstrings

## v1.3.6 - 2016 Sep 7

```clojure
[com.taoensso/truss "1.3.6"]
```

* Tweaked invariant-violation error message to make it clearer for beginners

## v1.3.5 - 2016 Aug 12

```clojure
[com.taoensso/truss "1.3.5"]
```

* **Hotfix**: cljs error wrapping was broken

## v1.3.3 - 2016 Jun 14

```clojure
[com.taoensso/truss "1.3.3"]
```

**BREAKING**: `error-fn` args have changed: `[msg data-map]` -> `[data-map-delay]`

## v1.2.0 - 2016 Mar 21

```clojure
[com.taoensso/truss "1.2.0"]
```

* **New**: added `set-error-fn!` [#3] to allow easier control over how invariant violations are reported

## v1.1.2 - 2016 Feb 26

* **Hotfix**: false vals were printing as "<nil>" in error messages

## v1.1.1 - 2016 Feb 18

* **Hotfix**: remove accidental encore reference [#1]

```clojure
[com.taoensso/truss "1.1.1"]
```

## v1.1.0 - 2016 Feb 17

> This is a non-breaking performance release

* **Perf**: special predicates like `[:or nil? string?]` are now compile-time transformations
* **Perf**: skip throw catching for some common predicates that are known never to throw

```clojure
[com.taoensso/truss "1.1.0"]
```

## v1.0.0 - 2015 Jan 12

> Initial public release

```clojure
[com.taoensso/truss "1.0.0"]
```
