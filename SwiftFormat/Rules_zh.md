# 规则详解

- [规则详解](#规则详解)
  - [andOperator](#andoperator)
  - [anyObjectProtocol](#anyobjectprotocol)
  - [applicationMain](#applicationmain)
  - [assertionFailures](#assertionfailures)
  - [blankLineAfterImports](#blanklineafterimports)
  - [blankLineAfterSwitchCase](#blanklineafterswitchcase)
  - [blankLinesAroundMark](#blanklinesaroundmark)
  - [blankLinesAtEndOfScope](#blanklinesatendofscope)
  - [blankLinesAtStartOfScope](#blanklinesatstartofscope)
  - [blankLinesBetweenChainedFunctions](#blanklinesbetweenchainedfunctions)
  - [blankLinesBetweenImports](#blanklinesbetweenimports)
  - [blankLinesBetweenScopes](#blanklinesbetweenscopes)
  - [blockComments](#blockcomments)
  - [braces](#braces)

## andOperator

在 `if`, `guard` 或 `while` 条件语句中，首选 `,` 而不是 `&&`。

<details>
<summary>Examples</summary>

```diff
- if true && true {
+ if true, true {
```

```diff
- guard true && true else {
+ guard true, true else {
```

```diff
- if functionReturnsBool() && true {
+ if functionReturnsBool(), true {
```

```diff
- if functionReturnsBool() && variable {
+ if functionReturnsBool(), variable {
```

</details>
<br/>

## anyObjectProtocol

在协议定义中，首选 `AnyObject` 而不是 `class`。

<details>
<summary>Examples</summary>

```diff
- protocol Foo: class {}
+ protocol Foo: AnyObject {}
```

</details>
<br/>

**NOTE:** 首选 `AnyObject` 而不是 `class` 的建议
在 Swift 4.1 中引入，所以 `anyObjectProtocol` 规则在 Swift 4.1 前是禁用的。

## applicationMain

在 Swift 5.3 及之后，使用 `@main` 替代过时的 `@UIApplicationMain` 和 `@NSApplicationMain` 属性。

## assertionFailures

使用 `assertionFailure(...)` 替代 `assert(false, ...)`。使用 `preconditionFailure(...)` 替代 `precondition(false, ...)`。

<details>
<summary>Examples</summary>

```diff
- assert(false)
+ assertionFailure()
```

```diff
- assert(false, "message", 2, 1)
+ assertionFailure("message", 2, 1)
```

```diff
- precondition(false, "message", 2, 1)
+ preconditionFailure("message", 2, 1)
```

</details>
<br/>

## blankLineAfterImports

在 import 语句后插入空白行。

<details>
<summary>Examples</summary>

```diff
  import A
  import B
  @testable import D
+
  class Foo {
    // foo
  }
```

</details>
<br/>

## blankLineAfterSwitchCase

在多行的 switch case 语句后插入一个空白行（最后一个 case 除外，最后一个 case 后面是右大括号）。

<details>
<summary>Examples</summary>

```diff
  func handle(_ action: SpaceshipAction) {
      switch action {
      case .engageWarpDrive:
          navigationComputer.destination = targetedDestination
          await warpDrive.spinUp()
          warpDrive.activate()
+
      case let .scanPlanet(planet):
          scanner.target = planet
          scanner.scanAtmosphere()
          scanner.scanBiosphere()
          scanner.scanForArticialLife()
+
      case .handleIncomingEnergyBlast:
          await energyShields.prepare()
          energyShields.engage()
      }
  }
```

</details>
<br/>

## blankLinesAroundMark

在 `MARK:` 注释前后插入空白行。

Option | Description
--- | ---
`--lineaftermarks` | 在 `MARK:` 后插入空白行，"true" (default) or "false"

<details>
<summary>Examples</summary>

```diff
  func foo() {
    // foo
  }
  // MARK: bar
  func bar() {
    // bar
  }

  func foo() {
    // foo
  }
+
  // MARK: bar
+
  func bar() {
    // bar
  }
```

</details>
<br/>

## blankLinesAtEndOfScope

删除作用域末尾的尾随空白行。

<details>
<summary>Examples</summary>

```diff
  func foo() {
    // foo
-
  }

  func foo() {
    // foo
  }
```

```diff
  array = [
    foo,
    bar,
    baz,
-
  ]

  array = [
    foo,
    bar,
    baz,
  ]
```

</details>
<br/>

## blankLinesAtStartOfScope

删除作用域开头的空白行。

Option | Description
--- | ---
`--typeblanklines` | 从类型中删除空白行，"remove" (default) or "preserve"

<details>
<summary>Examples</summary>

```diff
  func foo() {
-
    // foo
  }

  func foo() {
    // foo
  }
```

```diff
  array = [
-
    foo,
    bar,
    baz,
  ]

  array = [
    foo,
    bar,
    baz,
  ]
```

</details>
<br/>

## blankLinesBetweenChainedFunctions

删除链式函数之间的空白行，但保留换行符。

## blankLinesBetweenImports

删除 import 语句之间的空白行。

<details>
<summary>Examples</summary>

```diff
  import A
-
  import B
  import C
-
-
  @testable import D
  import E
```

</details>
<br/>

## blankLinesBetweenScopes

在 class，struct，enum，extension，protocol 或 function 声明前插入空白行。

<details>
<summary>Examples</summary>

```diff
  func foo() {
    // foo
  }
  func bar() {
    // bar
  }
  var baz: Bool
  var quux: Int

  func foo() {
    // foo
  }
+
  func bar() {
    // bar
  }
+
  var baz: Bool
  var quux: Int
```

</details>
<br/>

## blockComments

将块注释转换为连续的单行注释。

<details>
<summary>Examples</summary>

```diff
- /*
-  * foo
-  * bar
-  */

+ // foo
+ // bar
```

```diff
- /**
-  * foo
-  * bar
-  */

+ /// foo
+ /// bar
```

</details>
<br/>

## braces

确定大括号的放置风格（K&R or Allman）。

Option | Description
--- | ---
`--allman` | 使用 Allman 风格，"true" or "false" (default)

<details>
<summary>Examples</summary>

```diff
- if x
- {
    // foo
  }
- else
- {
    // bar
  }

+ if x {
    // foo
  }
+ else {
    // bar
  }
```

</details>
<br/>

**NOTE:** K&R 风格中，左大括号在行尾；Allman 风格中，左大括号单独占一行。

