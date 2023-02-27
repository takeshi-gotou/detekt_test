# detekt

## Metrics

* 4 number of properties

* 1 number of functions

* 1 number of classes

* 1 number of packages

* 1 number of kt files

## Complexity Report

* 345 lines of code (loc)

* 332 source lines of code (sloc)

* 315 logical lines of code (lloc)

* 0 comment lines of code (cloc)

* 14 cyclomatic complexity (mcc)

* 91 cognitive complexity

* 7 number of total code smells

* 0% comment source ratio

* 44 mcc per 1,000 lloc

* 22 code smells per 1,000 lloc

## Findings (7)

### complexity, LongMethod (1)

One method should have one responsibility. Long methods tend to handle many things at once. Prefer smaller methods to make them easier to understand.

[Documentation](https://detekt.dev/docs/rules/complexity#longmethod)

* logging/logback/src/main/kotlin/jp/co/sample/LogbackJobNetLogging.kt:11:9
```
The function nestCheck is too long (324). The maximum length is 60.
```
```kotlin
8          private val loggerFactory = ""
9      }
10 
11     fun nestCheck(inputstr: String) {
!!         ^ error
12         var i = 0
13 
14         if (inputstr == "aa") {

```

### complexity, NestedBlockDepth (1)

Excessive nesting leads to hidden complexity. Prefer extracting code to make it easier to understand.

[Documentation](https://detekt.dev/docs/rules/complexity#nestedblockdepth)

* logging/logback/src/main/kotlin/jp/co/sample/LogbackJobNetLogging.kt:11:9
```
Function nestCheck is nested too deeply.
```
```kotlin
8          private val loggerFactory = ""
9      }
10 
11     fun nestCheck(inputstr: String) {
!!         ^ error
12         var i = 0
13 
14         if (inputstr == "aa") {

```

### style, MayBeConst (2)

Usage of `vals` that can be `const val` detected.

[Documentation](https://detekt.dev/docs/rules/style#maybeconst)

* logging/logback/src/main/kotlin/jp/co/sample/LogbackJobNetLogging.kt:7:21
```
loggerMap can be a `const val`.
```
```kotlin
4  class LogbackJobNetLogging {
5      companion object {
6          private const val DELIMITER = ":"
7          private val loggerMap = ""
!                      ^ error
8          private val loggerFactory = ""
9      }
10 

```

* logging/logback/src/main/kotlin/jp/co/sample/LogbackJobNetLogging.kt:8:21
```
loggerFactory can be a `const val`.
```
```kotlin
5      companion object {
6          private const val DELIMITER = ":"
7          private val loggerMap = ""
8          private val loggerFactory = ""
!                      ^ error
9      }
10 
11     fun nestCheck(inputstr: String) {

```

### style, UnusedPrivateMember (3)

Private member is unused and should be removed.

[Documentation](https://detekt.dev/docs/rules/style#unusedprivatemember)

* logging/logback/src/main/kotlin/jp/co/sample/LogbackJobNetLogging.kt:6:27
```
Private property `DELIMITER` is unused.
```
```kotlin
3  
4  class LogbackJobNetLogging {
5      companion object {
6          private const val DELIMITER = ":"
!                            ^ error
7          private val loggerMap = ""
8          private val loggerFactory = ""
9      }

```

* logging/logback/src/main/kotlin/jp/co/sample/LogbackJobNetLogging.kt:7:21
```
Private property `loggerMap` is unused.
```
```kotlin
4  class LogbackJobNetLogging {
5      companion object {
6          private const val DELIMITER = ":"
7          private val loggerMap = ""
!                      ^ error
8          private val loggerFactory = ""
9      }
10 

```

* logging/logback/src/main/kotlin/jp/co/sample/LogbackJobNetLogging.kt:8:21
```
Private property `loggerFactory` is unused.
```
```kotlin
5      companion object {
6          private const val DELIMITER = ":"
7          private val loggerMap = ""
8          private val loggerFactory = ""
!                      ^ error
9      }
10 
11     fun nestCheck(inputstr: String) {

```

generated with [detekt version 1.22.0](https://detekt.dev/) on 2023-02-27 07:57:36 UTC
