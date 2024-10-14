
- [默认开启规则](#默认开启规则)
  - [andOperator](#andoperator)
  - [anyObjectProtocol](#anyobjectprotocol)
  - [applicationMain](#applicationmain)
  - [assertionFailures](#assertionfailures)
  - [blankLineAfterImports](#blanklineafterimports)
  - [blankLinesAroundMark](#blanklinesaroundmark)
  - [blankLinesAtEndOfScope](#blanklinesatendofscope)
  - [blankLinesAtStartOfScope](#blanklinesatstartofscope)
  - [blankLinesBetweenChainedFunctions](#blanklinesbetweenchainedfunctions)
  - [blankLinesBetweenScopes](#blanklinesbetweenscopes)
  - [braces](#braces)
  - [conditionalAssignment](#conditionalassignment)
  - [consecutiveBlankLines](#consecutiveblanklines)
  - [consecutiveSpaces](#consecutivespaces)
  - [consistentSwitchCaseSpacing](#consistentswitchcasespacing)
  - [duplicateImports](#duplicateimports)
  - [elseOnSameLine](#elseonsameline)
  - [emptyBraces](#emptybraces)
  - [enumNamespaces](#enumnamespaces)
  - [extensionAccessControl](#extensionaccesscontrol)
  - [fileHeader](#fileheader)
  - [genericExtensions](#genericextensions)
  - [headerFileName](#headerfilename)
  - [hoistAwait](#hoistawait)
  - [hoistPatternLet](#hoistpatternlet)
  - [hoistTry](#hoisttry)
  - [indent](#indent)
  - [initCoderUnavailable](#initcoderunavailable)
  - [leadingDelimiters](#leadingdelimiters)
  - [linebreakAtEndOfFile](#linebreakatendoffile)
  - [linebreaks](#linebreaks)
  - [modifierOrder](#modifierorder)
  - [numberFormatting](#numberformatting)
  - [opaqueGenericParameters](#opaquegenericparameters)
  - [preferForLoop](#preferforloop)
  - [preferKeyPath](#preferkeypath)
  - [redundantBackticks](#redundantbackticks)
  - [redundantBreak](#redundantbreak)
  - [redundantClosure](#redundantclosure)
  - [redundantExtensionACL](#redundantextensionacl)
  - [redundantFileprivate](#redundantfileprivate)
  - [redundantGet](#redundantget)
  - [redundantInit](#redundantinit)
  - [redundantInternal](#redundantinternal)
  - [redundantLet](#redundantlet)
  - [redundantLetError](#redundantleterror)
  - [redundantNilInit](#redundantnilinit)
  - [redundantObjc](#redundantobjc)
  - [redundantOptionalBinding](#redundantoptionalbinding)
  - [redundantParens](#redundantparens)
  - [redundantPattern](#redundantpattern)
  - [redundantRawValues](#redundantrawvalues)
  - [redundantReturn](#redundantreturn)
  - [redundantSelf](#redundantself)
  - [redundantStaticSelf](#redundantstaticself)
  - [redundantType](#redundanttype)
  - [redundantTypedThrows](#redundanttypedthrows)
  - [redundantVoidReturnType](#redundantvoidreturntype)
  - [semicolons](#semicolons)
  - [sortDeclarations](#sortdeclarations)
  - [sortImports](#sortimports)
  - [sortTypealiases](#sorttypealiases)
  - [spaceAroundBraces](#spacearoundbraces)
  - [spaceAroundBrackets](#spacearoundbrackets)
  - [spaceAroundComments](#spacearoundcomments)
  - [spaceAroundGenerics](#spacearoundgenerics)
  - [spaceAroundOperators](#spacearoundoperators)
  - [spaceAroundParens](#spacearoundparens)
  - [spaceInsideBraces](#spaceinsidebraces)
  - [spaceInsideBrackets](#spaceinsidebrackets)
  - [spaceInsideComments](#spaceinsidecomments)
  - [spaceInsideGenerics](#spaceinsidegenerics)
  - [spaceInsideParens](#spaceinsideparens)
  - [strongOutlets](#strongoutlets)
  - [strongifiedSelf](#strongifiedself)
  - [todos](#todos)
  - [trailingClosures](#trailingclosures)
  - [trailingCommas](#trailingcommas)
  - [trailingSpace](#trailingspace)
  - [typeSugar](#typesugar)
  - [unusedArguments](#unusedarguments)
  - [void](#void)
  - [wrap](#wrap)
  - [wrapArguments](#wraparguments)
  - [wrapAttributes](#wrapattributes)
  - [wrapLoopBodies](#wraploopbodies)
  - [wrapMultilineStatementBraces](#wrapmultilinestatementbraces)
  - [wrapSingleLineComments](#wrapsinglelinecomments)
  - [yodaConditions](#yodaconditions)
- [默认关闭规则](#默认关闭规则)
  - [acronyms](#acronyms)
  - [blankLineAfterSwitchCase](#blanklineafterswitchcase)
  - [blankLinesBetweenImports](#blanklinesbetweenimports)
  - [blockComments](#blockcomments)
  - [docComments](#doccomments)
  - [isEmpty](#isempty)
  - [markTypes](#marktypes)
  - [noExplicitOwnership](#noexplicitownership)
  - [organizeDeclarations](#organizedeclarations)
  - [redundantProperty](#redundantproperty)
  - [sortSwitchCases](#sortswitchcases)
  - [wrapConditionalBodies](#wrapconditionalbodies)
  - [wrapEnumCases](#wrapenumcases)
  - [wrapMultilineConditionalAssignment](#wrapmultilineconditionalassignment)
  - [wrapSwitchCases](#wrapswitchcases)
- [已弃用规则](#已弃用规则)
  - [sortedImports](#sortedimports)
  - [sortedSwitchCases](#sortedswitchcases)
  - [specifiers](#specifiers)

----------

# 默认开启规则

## andOperator

在 `if`, `guard` 或 `while` 条件中，首选 `,` 而不是 `&&`。

<details>
<summary>示例</summary>

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
<summary>示例</summary>

```diff
- protocol Foo: class {}
+ protocol Foo: AnyObject {}
```

**NOTE:** 首选 `AnyObject` 而不是 `class` 的建议在 Swift 4.1 中引入，所以 `anyObjectProtocol` 规则在 Swift 4.1 前是禁用的。

</details>
<br/>

## applicationMain

在 Swift 5.3 及以上版本中，使用 `@main` 替代过时的 `@UIApplicationMain` 和 `@NSApplicationMain` 特性。

## assertionFailures

用 `assertionFailure(...)` 替换 `assert(false, ...)`，用 `preconditionFailure(...)` 替换 `precondition(false, ...)`。

<details>
<summary>示例</summary>

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

在 `import` 语句后插入空白行。

<details>
<summary>示例</summary>

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

## blankLinesAroundMark

在 `MARK:` 注释前后插入空白行。

选项 | 描述
--- | ---
`--lineaftermarks` | Insert blank line after "MARK:": "true" (default) or "false"

<details>
<summary>示例</summary>

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

移除作用域末尾的尾随空白行。

<details>
<summary>示例</summary>

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

移除作用域开头的空白行。

选项 | 描述
--- | ---
`--typeblanklines` | "remove" (default) or "preserve" blank lines from types

<details>
<summary>示例</summary>

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

移除链式函数之间的空白行，但保留换行符。

## blankLinesBetweenScopes

在 `class`，`struct`，`enum`，`extension`，`protocol` 或 `function` 声明前插入空白行。

<details>
<summary>示例</summary>

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

## braces

根据选定样式确定大括号位置（K&R 或 Allman）。

选项 | 描述
--- | ---
`--allman` | 使用 Allman 缩进样式: "true" or "false" (default)

<details>
<summary>示例</summary>

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

**NOTE:** K&R 样式中，左大括号在行尾；Allman 样式中，左大括号单独一行。

## conditionalAssignment

使用 `if` / `switch` 表达式给属性赋值。

选项 | 描述
--- | ---
`--condassignment` | Use cond. assignment: "after-property" (default) or "always"

<details>
<summary>示例</summary>

```diff
- let foo: String
- if condition {
+ let foo = if condition {
-     foo = "foo"
+     "foo"
  } else {
-     foo = "bar"
+     "bar"
  }

- let foo: String
- switch condition {
+ let foo = switch condition {
  case true:
-     foo = "foo"
+     "foo"
  case false:
-     foo = "bar"
+     "bar"
  }

// With --condassignment always (disabled by default)
- switch condition {
+ foo.bar = switch condition {
  case true:
-     foo.bar = "baaz"
+     "baaz"
  case false:
-     foo.bar = "quux"
+     "quux"
  }
```

</details>
<br/>

## consecutiveBlankLines

将连续的空白行替换为单个空白行。

<details>
<summary>示例</summary>

```diff
  func foo() {
    let x = "bar"
-

    print(x)
  }

  func foo() {
    let x = "bar"

    print(x)
  }
```

</details>
<br/>

## consecutiveSpaces

将连续的空格替换为单个空格。

<details>
<summary>示例</summary>

```diff
- let     foo = 5
+ let foo = 5
```

</details>
<br/>

## consistentSwitchCaseSpacing

确保 `switch` 语句中所有 `case` 之间的间距一致。

<details>
<summary>示例</summary>

```diff
  func handle(_ action: SpaceshipAction) {
      switch action {
      case .engageWarpDrive:
          navigationComputer.destination = targetedDestination
          await warpDrive.spinUp()
          warpDrive.activate()

      case .enableArtificialGravity:
          artificialGravityEngine.enable(strength: .oneG)
+
      case let .scanPlanet(planet):
          scanner.target = planet
          scanner.scanAtmosphere()
          scanner.scanBiosphere()
          scanner.scanForArtificialLife()

      case .handleIncomingEnergyBlast:
          energyShields.engage()
      }
  }
```

```diff
  var name: PlanetType {
  switch self {
  case .mercury:
      "Mercury"
-
  case .venus:
      "Venus"
  case .earth:
      "Earth"
  case .mars:
      "Mars"
-
  case .jupiter:
      "Jupiter"
  case .saturn:
      "Saturn"
  case .uranus:
      "Uranus"
  case .neptune:
      "Neptune"
  }
```

</details>
<br/>

## duplicateImports

移除重复的 `import` 语句。

<details>
<summary>示例</summary>

```diff
  import Foo
  import Bar
- import Foo
```

```diff
  import B
  #if os(iOS)
    import A
-   import B
  #endif
```

</details>
<br/>

## elseOnSameLine

根据选定样式确定 `else`，`catch` 或 `while` 关键字位置（同一行或换行）。

选项 | 描述
--- | ---
`--elseposition` | else / catch 位置: "same-line" (default) or "next-line"
`--guardelse` | Guard else 位置: "same-line", "next-line" or "auto" (default)

<details>
<summary>示例</summary>

```diff
  if x {
    // foo
- }
- else {
    // bar
  }

  if x {
    // foo
+ } else {
    // bar
  }
```

```diff
  do {
    // try foo
- }
- catch {
    // bar
  }

  do {
    // try foo
+ } catch {
    // bar
  }
```

```diff
  repeat {
    // foo
- }
- while {
    // bar
  }

  repeat {
    // foo
+ } while {
    // bar
  }
```

</details>
<br/>

## emptyBraces

移除空大括号里的空白。

选项 | 描述
--- | ---
`--emptybraces` | Empty braces: "no-space" (default), "spaced" or "linebreak"

<details>
<summary>示例</summary>

```diff
- func foo() {
-
- }

+ func foo() {}
```

</details>
<br/>

## enumNamespaces

将仅用于托管静态成员的类型转为枚举（空枚举是在 Swift 中创建命名空间的规范方法，因为不能被实例化）。

选项 | 描述
--- | ---
`--enumnamespaces` | Change type to enum: "always" (default) or "structs-only"

## extensionAccessControl

配置 `extension` 的访问控制关键字位置。

选项 | 描述
--- | ---
`--extensionacl` | Place ACL "on-extension" (default) or "on-declarations"

<details>
<summary>示例</summary>

`--extensionacl on-extension` (default)

```diff
- extension Foo {
-     public func bar() {}
-     public func baz() {}
  }

+ public extension Foo {
+     func bar() {}
+     func baz() {}
  }
```

`--extensionacl on-declarations`

```diff
- public extension Foo {
-     func bar() {}
-     func baz() {}
-     internal func quux() {}
  }

+ extension Foo {
+     public func bar() {}
+     public func baz() {}
+     func quux() {}
  }
```

</details>
<br/>

**NOTE:** 待讨论

## fileHeader

对所有文件使用指定的源文件头模版。

选项 | 描述
--- | ---
`--header` | Header comments: "strip", "ignore", or the text you wish use
`--dateformat` | "system" (default), "iso", "dmy", "mdy" or custom
`--timezone` | "system" (default) or a valid identifier/abbreviation

<details>
<summary>示例</summary>

You can use the following tokens in the text:

Token | Description
--- | ---
`{file}` | File name
`{year}` | Current year
`{created}` | File creation date
`{created.year}` | File creation year
`{author}` | Name and email of the user who first committed the file
`{author.name}` | Name of the user who first committed the file
`{author.email}` | Email of the user who first committed the file

**Example**:

`--header \n {file}\n\n Copyright © {created.year} {author.name}.\n`

```diff
- // SomeFile.swift

+ //
+ //  SomeFile.swift
+ //  Copyright © 2023 Tim Apple.
+ //
```

You can use the following built-in formats for `--dateformat`:

Token | Description
--- | ---
system | Use the local system locale
iso | ISO 8601 (yyyy-MM-dd)
dmy | Date/Month/Year (dd/MM/yyyy)
mdy | Month/Day/Year (MM/dd/yyyy)

Custom formats are defined using
[Unicode symbols](https://www.unicode.org/reports/tr35/tr35-31/tr35-dates.html#Date_Field_Symbol_Table).

`--dateformat iso`

```diff
- // Created {created}
+ // Created 2023-08-10
```

`--dateformat dmy`

```diff
- // Created {created}
+ // Created 10/08/2023
```

`--dateformat mdy`

```diff
- // Created {created}
+ // Created 08/10/2023
```

`--dateformat 'yyyy.MM.dd.HH.mm'`

```diff
- // Created {created}
+ // Created 2023.08.10.11.00
```

Setting a time zone enforces consistent date formatting across environments
around the world. By default the local system locale is used and for convenience
`gmt` and `utc` can be used. The time zone can be further customized by
setting it to a abbreviation/time zone identifier supported by the Swift
standard library.

`--dateformat 'yyyy-MM-dd HH:mm ZZZZ' --timezone utc`

```diff
- // Created {created}
+ // Created 2023-08-10 11:00 GMT
```

`--dateformat 'yyyy-MM-dd HH:mm ZZZZ' --timezone Pacific/Fiji`

```diff
- // Created 2023-08-10 11:00 GMT
+ // Created 2023-08-10 23:00 GMT+12:00
```

</details>
<br/>

## genericExtensions

对泛型类型的扩展使用尖括号 (`extension Array<Foo>`)，而不是类型约束 (`extension Array where Element == Foo`)。

选项 | 描述
--- | ---
`--generictypes` | Semicolon-delimited list of generic types and type parameters

<details>
<summary>示例</summary>

```diff
- extension Array where Element == Foo {}
- extension Optional where Wrapped == Foo {}
- extension Dictionary where Key == Foo, Value == Bar {}
- extension Collection where Element == Foo {}
+ extension Array<Foo> {}
+ extension Optional<Foo> {}
+ extension Dictionary<Key, Value> {}
+ extension Collection<Foo> {}

// With `typeSugar` also enabled:
- extension Array where Element == Foo {}
- extension Optional where Wrapped == Foo {}
- extension Dictionary where Key == Foo, Value == Bar {}
+ extension [Foo] {}
+ extension Foo? {}
+ extension [Key: Value] {}

// Also supports user-defined types!
- extension LinkedList where Element == Foo {}
- extension Reducer where
-     State == FooState,
-     Action == FooAction,
-     Environment == FooEnvironment {}
+ extension LinkedList<Foo> {}
+ extension Reducer<FooState, FooAction, FooEnvironment> {}
```

</details>
<br/>

## headerFileName

确保头部注释中的文件名与实际文件名匹配。

## hoistAwait

将内联的 `await` 关键字移动到表达式开头。

选项 | 描述
--- | ---
`--asynccapturing` | List of functions with async @autoclosure arguments

<details>
<summary>示例</summary>

```diff
- greet(await forename, await surname)
+ await greet(forename, surname)
```

```diff
- let foo = String(try await getFoo())
+ let foo = await String(try getFoo())
```

</details>
<br/>

## hoistPatternLet

在模式匹配中重新定位 `let` 或 `var` 绑定。

选项 | 描述
--- | ---
`--patternlet` | let/var placement in patterns: "hoist" (default) or "inline"

<details>
<summary>示例</summary>

```diff
- (let foo, let bar) = baz()
+ let (foo, bar) = baz()
```

```diff
- if case .foo(let bar, let baz) = quux {
    // inner foo
  }

+ if case let .foo(bar, baz) = quux {
    // inner foo
  }
```

</details>
<br/>

**NOTE:** 待讨论

## hoistTry

将内联的 `try` 关键字移动到表达式开头。

选项 | 描述
--- | ---
`--throwcapturing` | List of functions with throwing @autoclosure arguments

<details>
<summary>示例</summary>

```diff
- foo(try bar(), try baz())
+ try foo(bar(), baz())
```

```diff
- let foo = String(try await getFoo())
+ let foo = try String(await getFoo())
```

</details>
<br/>

## indent

根据作用域级别缩进代码。

选项 | 描述
--- | ---
`--indent` | Number of spaces to indent, or "tab" to use tabs
`--tabwidth` | The width of a tab character. Defaults to "unspecified"
`--smarttabs` | Align code independently of tab width. defaults to "enabled"
`--indentcase` | Indent cases inside a switch: "true" or "false" (default)
`--ifdef` | #if indenting: "indent" (default), "no-indent" or "outdent"
`--xcodeindentation` | Match Xcode indenting: "enabled" or "disabled" (default)
`--indentstrings` | Indent multiline strings: "false" (default) or "true"

<details>
<summary>示例</summary>

```diff
  if x {
-     // foo
  } else {
-     // bar
-       }

  if x {
+   // foo
  } else {
+   // bar
+ }
```

```diff
  let array = [
    foo,
-     bar,
-       baz
-   ]

  let array = [
    foo,
+   bar,
+   baz
+ ]
```

```diff
  switch foo {
-   case bar: break
-   case baz: break
  }

  switch foo {
+ case bar: break
+ case baz: break
  }
```

</details>
<br/>

## initCoderUnavailable

在未实现的 `init(coder:)` 构造函数上添加 `@available(*, unavailable)` 属性。

选项 | 描述
--- | ---
`--initcodernil` | 在不可用的 `` 构造函数中，将 fatalError 替换为 nil。

<details>
<summary>示例</summary>

```diff
+ @available(*, unavailable)
  required init?(coder aDecoder: NSCoder) {
    fatalError("init(coder:) has not been implemented")
  }

// --initcodernil
+ @available(*, unavailable)
  required init?(coder aDecoder: NSCoder) {
    nil
  }
```

</details>
<br/>

## leadingDelimiters

将开头的分隔符移动到上一行的末尾。

<details>
<summary>示例</summary>

```diff
- guard let foo = maybeFoo // first
-     , let bar = maybeBar else { ... }

+ guard let foo = maybeFoo, // first
+      let bar = maybeBar else { ... }
```

</details>
<br/>

## linebreakAtEndOfFile

在文件末尾添加空白行。

## linebreaks

对所有换行使用指定换行字符。

选项 | 描述
--- | ---
`--linebreaks` | 换行字符: "cr", "crlf" or "lf" (default)

## modifierOrder

Use consistent ordering for member modifiers.

选项 | 描述
--- | ---
`--modifierorder` | Comma-delimited list of modifiers in preferred order

<details>
<summary>示例</summary>

```diff
- lazy public weak private(set) var foo: UIView?
+ public private(set) lazy weak var foo: UIView?
```

```diff
- final public override func foo()
+ override public final func foo()
```

```diff
- convenience private init()
+ private convenience init()
```

**NOTE:** 如果 `--modifierorder` 选项未设置，默认排序为:
`override`, `private`, `fileprivate`, `internal`, `package`, `public`, `open`, `private(set)`, `fileprivate(set)`, `internal(set)`, `package(set)`, `public(set)`, `open(set)`, `final`, `dynamic`, `optional`, `required`, `convenience`, `indirect`, `isolated`, `nonisolated`, `nonisolated(unsafe)`, `lazy`, `weak`, `unowned`, `static`, `class`, `borrowing`, `consuming`, `mutating`, `nonmutating`, `prefix`, `infix`, `postfix`

</details>
<br/>

## numberFormatting

对数字字面量进行一致分组，使用 `_` 作为分隔符以提高可读性。你可以为每种数值类型指定分组大小（每组的位数）和阈值（在达到最小位数时应用分组）。

选项 | 描述
--- | ---
`--decimalgrouping` | Decimal grouping,threshold (default: 3,6) or "none", "ignore"
`--binarygrouping` | Binary grouping,threshold (default: 4,8) or "none", "ignore"
`--octalgrouping` | Octal grouping,threshold (default: 4,8) or "none", "ignore"
`--hexgrouping` | Hex grouping,threshold (default: 4,8) or "none", "ignore"
`--fractiongrouping` | Group digits after '.': "enabled" or "disabled" (default)
`--exponentgrouping` | Group exponent digits: "enabled" or "disabled" (default)
`--hexliteralcase` | Casing for hex literals: "uppercase" (default) or "lowercase"
`--exponentcase` | Case of 'e' in numbers: "lowercase" or "uppercase" (default)

<details>
<summary>示例</summary>

```diff
- let color = 0xFF77A5
+ let color = 0xff77a5
```

```diff
- let big = 123456.123
+ let big = 123_456.123
```

</details>
<br/>

**NOTE:** 待讨论

## opaqueGenericParameters

使用不透明的泛型参数 `(some Protocol)` 替代具有约束的泛型参数 `(T where T: Protocol)`，并支持使用主要关联类型来简化标准库类型的定义。

选项 | 描述
--- | ---
`--someany` | Use `some Any` types: "true" (default) or "false"

<details>
<summary>示例</summary>

```diff
- func handle<T: Fooable>(_ value: T) {
+ func handle(_ value: some Fooable) {
      print(value)
  }

- func handle<T>(_ value: T) where T: Fooable, T: Barable {
+ func handle(_ value: some Fooable & Barable) {
      print(value)
  }

- func handle<T: Collection>(_ value: T) where T.Element == Foo {
+ func handle(_ value: some Collection<Foo>) {
      print(value)
  }

// With `--someany enabled` (the default)
- func handle<T>(_ value: T) {
+ func handle(_ value: some Any) {
      print(value)
  }
```

</details>
<br/>

## preferForLoop

Convert functional `forEach` calls to for loops.

选项 | 描述
--- | ---
`--anonymousforeach` | Convert anonymous forEach: "convert" (default) or "ignore"
`--onelineforeach` | Convert one-line forEach: "convert" or "ignore" (default)

<details>
<summary>示例</summary>

```diff
  let strings = ["foo", "bar", "baaz"]
- strings.forEach { placeholder in
+ for placeholder in strings {
      print(placeholder)
  }

  // Supports anonymous closures
- strings.forEach {
+ for string in strings {
-     print($0)
+     print(string)
  }

- foo.item().bar[2].baazValues(option: true).forEach {
+ for baazValue in foo.item().bar[2].baazValues(option: true) {
-     print($0)
+     print(baazValue)
  }

  // Doesn't affect long multiline functional chains
  placeholderStrings
      .filter { $0.style == .fooBar }
      .map { $0.uppercased() }
      .forEach { print($0) }
```

</details>
<br/>

**NOTES:** 待讨论

## preferKeyPath

将简单的 `map { $0.foo }` 闭包转换为基于 keyPath 的语法。

<details>
<summary>示例</summary>

```diff
- let barArray = fooArray.map { $0.bar }
+ let barArray = fooArray.map(\.bar)

- let barArray = fooArray.compactMap { $0.optionalBar }
+ let barArray = fooArray.compactMap(\.optionalBar)
```

</details>
<br/>

## redundantBackticks

移除标识符周围不必要的反引号。

<details>
<summary>示例</summary>

```diff
- let `infix` = bar
+ let infix = bar
```

```diff
- func foo(with `default`: Int) {}
+ func foo(with default: Int) {}
```

</details>
<br/>

## redundantBreak

移除 switch case 中的冗余 `break`。

<details>
<summary>示例</summary>

```diff
  switch foo {
    case bar:
        print("bar")
-       break
    default:
        print("default")
-       break
  }
```

</details>
<br/>

## redundantClosure

移除包含单个语句的立即调用闭包体。

<details>
<summary>示例</summary>

```diff
- let foo = { Foo() }()
+ let foo = Foo()
```

```diff
- lazy var bar = {
-     Bar(baaz: baaz,
-         quux: quux)
- }()
+ lazy var bar = Bar(baaz: baaz,
+                    quux: quux)
```

</details>
<br/>

## redundantExtensionACL

移除冗余的访问控制修饰符。

<details>
<summary>示例</summary>

```diff
  public extension URL {
-   public func queryParameter(_ name: String) -> String { ... }
  }

  public extension URL {
+   func queryParameter(_ name: String) -> String { ... }
  }
```

</details>
<br/>

## redundantFileprivate

在等效的情况下，优先使用 `private` 而不是 `fileprivate`。

<details>
<summary>示例</summary>

```diff
-  fileprivate let someConstant = "someConstant"
+  private let someConstant = "someConstant"
```

在 Swift 4.0 及以上版本中，当成员仅在同一个文件中的扩展中访问时，可以使用 `private` 来替代 `fileprivate`:

```diff
  class Foo {
-   fileprivate var foo = "foo"
+   private var foo = "foo"
  }

  extension Foo {
    func bar() {
      print(self.foo)
    }
  }
```

</details>
<br/>

## redundantGet

移除计算属性中不需要的 `get`。

<details>
<summary>示例</summary>

```diff
  var foo: Int {
-   get {
-     return 5
-   }
  }

  var foo: Int {
+   return 5
  }
```

</details>
<br/>

## redundantInit

移除不必要的显式 `init`。

<details>
<summary>示例</summary>

```diff
- String.init("text")
+ String("text")
```

</details>
<br/>

## redundantInternal

移除冗余的 `internal` 访问控制修饰符。

<details>
<summary>示例</summary>

```diff
- internal class Foo {
+ class Foo {
-     internal let bar: String
+     let bar: String

-     internal func baaz() {}
+     func baaz() {}

-     internal init() {
+     init() {
          bar = "bar"
      }
  }
```

</details>
<br/>

## redundantLet

移除被忽略变量前的 `let` / `var`。

<details>
<summary>示例</summary>

```diff
- let _ = foo()
+ _ = foo()
```

</details>
<br/>

## redundantLetError

移除 `catch` 语句中冗余的 `let error`。

<details>
<summary>示例</summary>

```diff
- do { ... } catch let error { log(error) }
+ do { ... } catch { log(error) }
```

</details>
<br/>

## redundantNilInit

移除/插入冗余的 `nil` 默认值（可选类型变量默认值是 nil）

选项 | 描述
--- | ---
`--nilinit` | "remove" (default) redundant nil or "insert" missing nil

<details>
<summary>示例</summary>

`--nilinit remove`

```diff
- var foo: Int? = nil
+ var foo: Int?
```

```diff
// doesn't apply to `let` properties
let foo: Int? = nil
```

```diff
// doesn't affect non-nil initialization
var foo: Int? = 0
```

`--nilinit insert`

```diff
- var foo: Int?
+ var foo: Int? = nil
```

</details>
<br/>

## redundantObjc

移除冗余的 `@objc` 注释。

<details>
<summary>示例</summary>

```diff
- @objc @IBOutlet var label: UILabel!
+ @IBOutlet var label: UILabel!
```

```diff
- @IBAction @objc func goBack() {}
+ @IBAction func goBack() {}
```

```diff
- @objc @NSManaged private var foo: String?
+ @NSManaged private var foo: String?
```

</details>
<br/>

## redundantOptionalBinding

移除可选绑定条件中冗余的标识符。

<details>
<summary>示例</summary>

```diff
- if let foo = foo {
+ if let foo {
      print(foo)
  }

- guard let self = self else {
+ guard let self else {
      return
  }
```

</details>
<br/>

## redundantParens

移除冗余的括号。

<details>
<summary>示例</summary>

```diff
- if (foo == true) {}
+ if foo == true {}
```

```diff
- while (i < bar.count) {}
+ while i < bar.count {}
```

```diff
- queue.async() { ... }
+ queue.async { ... }
```

```diff
- let foo: Int = ({ ... })()
+ let foo: Int = { ... }()
```

</details>
<br/>

## redundantPattern

移除冗余的模式匹配参数语法。

<details>
<summary>示例</summary>

```diff
- if case .foo(_, _) = bar {}
+ if case .foo = bar {}
```

```diff
- let (_, _) = bar
+ let _ = bar
```

</details>
<br/>

## redundantRawValues

移除枚举中冗余的原始字符串值。

<details>
<summary>示例</summary>

```diff
  enum Foo: String {
-   case bar = "bar"
    case baz = "quux"
  }

  enum Foo: String {
+   case bar
    case baz = "quux"
  }
```

</details>
<br/>

## redundantReturn

移除不需要的 `return` 关键字。

<details>
<summary>示例</summary>

```diff
- array.filter { return $0.foo == bar }
+ array.filter { $0.foo == bar }

  // Swift 5.1+ (SE-0255)
  var foo: String {
-     return "foo"
+     "foo"
  }

  // Swift 5.9+ (SE-0380) and with conditionalAssignment rule enabled
  func foo(_ condition: Bool) -> String {
      if condition {
-         return "foo"
+         "foo"
      } else {
-         return "bar"
+         "bar"
      }
  }
```

</details>
<br/>

## redundantSelf

根据适用情况插入或移除显式的 `self`。

选项 | 描述
--- | ---
`--self` | 显式的 `self`: "insert", "remove" (default) or "init-only"
`--selfrequired` | Comma-delimited list of functions with @autoclosure arguments

<details>
<summary>示例</summary>

```diff
  func foobar(foo: Int, bar: Int) {
    self.foo = foo
    self.bar = bar
-   self.baz = 42
  }

  func foobar(foo: Int, bar: Int) {
    self.foo = foo
    self.bar = bar
+   baz = 42
  }
```

In the rare case of functions with `@autoclosure` arguments, `self` may be
required at the call site, but SwiftFormat is unable to detect this
automatically. You can use the `--selfrequired` command-line option to specify
a list of such methods, and the `redundantSelf` rule will then ignore them.

An example of such a method is the `expect()` function in the Nimble unit
testing framework (https://github.com/Quick/Nimble), which is common enough that
SwiftFormat excludes it by default.

There is also an option to always use explicit `self` but *only* inside `init`,
by using `--self init-only`:

```diff
  init(foo: Int, bar: Int) {
    self.foo = foo
    self.bar = bar
-   baz = 42
  }

  init(foo: Int, bar: Int) {
    self.foo = foo
    self.bar = bar
+   self.baz = 42
  }
```

</details>
<br/>

## redundantStaticSelf

移除不必要的显式 `Self`。

## redundantType

移除变量声明中的冗余类型。

选项 | 描述
--- | ---
`--redundanttype` | "inferred", "explicit", or "infer-locals-only" (default)

<details>
<summary>示例</summary>

```diff
// inferred
- let view: UIView = UIView()
+ let view = UIView()

// explicit
- let view: UIView = UIView()
+ let view: UIView = .init()

// infer-locals-only
  class Foo {
-     let view: UIView = UIView()
+     let view: UIView = .init()

      func method() {
-         let view: UIView = UIView()
+         let view = UIView()
      }
  }

// Swift 5.9+, inferred (SE-0380)
- let foo: Foo = if condition {
+ let foo = if condition {
      Foo("foo")
  } else {
      Foo("bar")
  }

// Swift 5.9+, explicit (SE-0380)
  let foo: Foo = if condition {
-     Foo("foo")
+     .init("foo")
  } else {
-     Foo("bar")
+     .init("foo")
  }
```

</details>
<br/>

## redundantTypedThrows

将 `throws(any Error)` 转换为 `throws`，并将 `throws(Never)` 转换为非抛出异常函数。

<details>
<summary>示例</summary>

```diff
- func foo() throws(Never) -> Int {
+ func foo() -> Int {
      return 0
  }

- func foo() throws(any Error) -> Int {
+ func foo() throws -> Int {
      throw MyError.foo
  }
```

</details>
<br/>

## redundantVoidReturnType

移除冗余的 `Void` 返回类型。

选项 | 描述
--- | ---
`--closurevoid` | Closure void returns: "remove" (default) or "preserve"

<details>
<summary>示例</summary>

```diff
- func foo() -> Void {
    // returns nothing
  }

+ func foo() {
    // returns nothing
  }
```

</details>
<br/>

## semicolons

移除不必要的分号。

选项 | 描述
--- | ---
`--semicolons` | Allow semicolons: "never" or "inline" (default)

<details>
<summary>示例</summary>

```diff
- let foo = 5;
+ let foo = 5
```

```diff
- let foo = 5; let bar = 6
+ let foo = 5
+ let bar = 6
```

```diff
// semicolon is not removed if it would affect the behavior of the code
return;
goto(fail)
```

</details>
<br/>

## sortDeclarations

对带有 // swiftformat:sort 注释的声明和在 // swiftformat:sort:begin 与 // swiftformat:sort:end 注释之间的声明进行排序。

<details>
<summary>示例</summary>

```diff
  // swiftformat:sort
  enum FeatureFlags {
-     case upsellB
-     case fooFeature
-     case barFeature
-     case upsellA(
-         fooConfiguration: Foo,
-         barConfiguration: Bar)
+     case barFeature
+     case fooFeature
+     case upsellA(
+         fooConfiguration: Foo,
+         barConfiguration: Bar)
+     case upsellB
  }

  enum FeatureFlags {
      // swiftformat:sort:begin
-     case upsellB
-     case fooFeature
-     case barFeature
-     case upsellA(
-         fooConfiguration: Foo,
-         barConfiguration: Bar)
+     case barFeature
+     case fooFeature
+     case upsellA(
+         fooConfiguration: Foo,
+         barConfiguration: Bar)
+     case upsellB
      // swiftformat:sort:end

      var anUnsortedProperty: Foo {
          Foo()
      }
  }
```

</details>
<br/>

## sortImports

按字母顺序对 `import` 语句进行排序。

选项 | 描述
--- | ---
`--importgrouping` | "testable-first/last", "alpha" (default) or "length"

<details>
<summary>示例</summary>

```diff
- import Foo
- import Bar
+ import Bar
+ import Foo
```

```diff
- import B
- import A
- #if os(iOS)
-   import Foo-iOS
-   import Bar-iOS
- #endif
+ import A
+ import B
+ #if os(iOS)
+   import Bar-iOS
+   import Foo-iOS
+ #endif
```

</details>
<br/>

## sortTypealiases

按字母顺序对协议组合类型别名进行排序。

<details>
<summary>示例</summary>

```diff
- typealias Placeholders = Foo & Bar & Baaz & Quux
+ typealias Placeholders = Baaz & Bar & Foo & Quux

  typealias Dependencies
-     = FooProviding
+     = BaazProviding
      & BarProviding
-     & BaazProviding
+     & FooProviding
      & QuuxProviding
```

</details>
<br/>

## spaceAroundBraces

在大括号周围添加或移除空格。

<details>
<summary>示例</summary>

```diff
- foo.filter{ return true }.map{ $0 }
+ foo.filter { return true }.map { $0 }
```

```diff
- foo( {} )
+ foo({})
```

</details>
<br/>

## spaceAroundBrackets

在中括号周围添加或移除空格。

<details>
<summary>示例</summary>

```diff
- foo as[String]
+ foo as [String]
```

```diff
- foo = bar [5]
+ foo = bar[5]
```

</details>
<br/>

## spaceAroundComments

在注释前后添加或移除空格。

<details>
<summary>示例</summary>

```diff
- let a = 5// assignment
+ let a = 5 // assignment
```

```diff
- func foo() {/* ... */}
+ func foo() { /* ... */ }
```

</details>
<br/>

## spaceAroundGenerics

移除尖括号周围的空格。

<details>
<summary>示例</summary>

```diff
- Foo <Bar> ()
+ Foo<Bar>()
```

</details>
<br/>

## spaceAroundOperators

在运算符或分隔符周围添加或移除空格。

选项 | 描述
--- | ---
`--operatorfunc` | Spacing for operator funcs: "spaced" (default) or "no-space"
`--nospaceoperators` | Comma-delimited list of operators without surrounding space
`--ranges` | Spacing for ranges: "spaced" (default) or "no-space"
`--typedelimiter` | "space-after" (default), "spaced" or "no-space"

<details>
<summary>示例</summary>

```diff
- foo . bar()
+ foo.bar()
```

```diff
- a+b+c
+ a + b + c
```

```diff
- func ==(lhs: Int, rhs: Int) -> Bool
+ func == (lhs: Int, rhs: Int) -> Bool
```

</details>
<br/>

## spaceAroundParens

在括号周围添加或移除空格。

<details>
<summary>示例</summary>

```diff
- init (foo)
+ init(foo)
```

```diff
- switch(x){
+ switch (x) {
```

</details>
<br/>

**NOTES:** 待讨论

## spaceInsideBraces

在大括号内添加空格。

<details>
<summary>示例</summary>

```diff
- foo.filter {return true}
+ foo.filter { return true }
```

</details>
<br/>

## spaceInsideBrackets

移除中括号内的空格。

<details>
<summary>示例</summary>

```diff
- [ 1, 2, 3 ]
+ [1, 2, 3]
```

</details>
<br/>

## spaceInsideComments

在注释的开头和/或结尾添加空格。

<details>
<summary>示例</summary>

```diff
- let a = 5 //assignment
+ let a = 5 // assignment
```

```diff
- func foo() { /*...*/ }
+ func foo() { /* ... */ }
```

</details>
<br/>

## spaceInsideGenerics

移除尖括号内的空格。

<details>
<summary>示例</summary>

```diff
- Foo< Bar, Baz >
+ Foo<Bar, Baz>
```

</details>
<br/>

## spaceInsideParens

移除括号内的空格。

<details>
<summary>示例</summary>

```diff
- ( a, b)
+ (a, b)
```

</details>
<br/>

## strongOutlets

从 `@IBOutlet` 属性中移除 `weak` 修饰符。

<details>
<summary>示例</summary>

As per Apple's recommendation
(https://developer.apple.com/videos/play/wwdc2015/407/ @ 32:30).

```diff
- @IBOutlet weak var label: UILabel!
+ @IBOutlet var label: UILabel!
```

</details>
<br/>

## strongifiedSelf

在可选解包表达式中移除围绕 `self` 的反引号。

<details>
<summary>示例</summary>

```diff
- guard let `self` = self else { return }
+ guard let self = self else { return }
```

**NOTE:** 在 Swift 4.2 及以上版本中，允许对未转义的 `self` 进行赋值操作，因此 `strongifiedSelf` 规则只有在 Swift 4.2 或更高时才启用。

</details>
<br/>

## todos

使用正确的格式来标记 `TODO:`，`MARK:` 或 `FIXME:` 注释。

<details>
<summary>示例</summary>

```diff
- /* TODO fix this properly */
+ /* TODO: fix this properly */
```

```diff
- // MARK - UIScrollViewDelegate
+ // MARK: - UIScrollViewDelegate
```

</details>
<br/>

## trailingClosures

在适用的地方使用尾随闭包语法。

选项 | 描述
--- | ---
`--trailingclosures` | Comma-delimited list of functions that use trailing closures
`--nevertrailing` | List of functions that should never use trailing closures

<details>
<summary>示例</summary>

```diff
- DispatchQueue.main.async(execute: { ... })
+ DispatchQueue.main.async {
```

```diff
- let foo = bar.map({ ... }).joined()
+ let foo = bar.map { ... }.joined()
```

</details>
<br/>

## trailingCommas

在集合字面量的最后一项后添加或移除尾随逗号。

选项 | 描述
--- | ---
`--commas` | 在集合字面量中使用正确的逗号: "always" (default) or "inline"

<details>
<summary>示例</summary>

```diff
  let array = [
    foo,
    bar,
-   baz
  ]

  let array = [
    foo,
    bar,
+   baz,
  ]
```

</details>
<br/>

**NOTE:** 待确定

## trailingSpace

移除行尾的空格。

选项 | 描述
--- | ---
`--trimwhitespace` | Trim trailing space: "always" (default) or "nonblank-lines"

## typeSugar

优先使用数组、字典和可选类型的简写语法。

选项 | 描述
--- | ---
`--shortoptionals` | Use ? for optionals "always" or "except-properties" (default)

<details>
<summary>示例</summary>

```diff
- var foo: Array<String>
+ var foo: [String]
```

```diff
- var foo: Dictionary<String, Int>
+ var foo: [String: Int]
```

```diff
- var foo: Optional<(Int) -> Void>
+ var foo: ((Int) -> Void)?
```

</details>
<br/>

## unusedArguments

用 `_` 标记未使用函数参数。

选项 | 描述
--- | ---
`--stripunusedargs` | "closure-only", "unnamed-only" or "always" (default)

<details>
<summary>示例</summary>

```diff
- func foo(bar: Int, baz: String) {
    print("Hello \(baz)")
  }

+ func foo(bar _: Int, baz: String) {
    print("Hello \(baz)")
  }
```

```diff
- func foo(_ bar: Int) {
    ...
  }

+ func foo(_: Int) {
    ...
  }
```

```diff
- request { response, data in
    self.data += data
  }

+ request { _, data in
    self.data += data
  }
```

</details>
<br/>

## void

在类型声明中使用 Void，在值表示中使用 ()。

选项 | 描述
--- | ---
`--voidtype` | How void types are represented: "void" (default) or "tuple"

<details>
<summary>示例</summary>

```diff
- let foo: () -> ()
+ let foo: () -> Void
```

```diff
- let bar: Void -> Void
+ let bar: () -> Void
```

```diff
- let baz: (Void) -> Void
+ let baz: () -> Void
```

```diff
- func quux() -> (Void)
+ func quux() -> Void
```

```diff
- callback = { _ in Void() }
+ callback = { _ in () }
```

</details>
<br/>

## wrap

将超过指定最大宽度的行进行换行。

选项 | 描述
--- | ---
`--maxwidth` | Maximum length of a line before wrapping. defaults to "none"
`--nowrapoperators` | Comma-delimited list of operators that shouldn't be wrapped
`--assetliterals` | Color/image literal width. "actual-width" or "visual-width"
`--wrapternary` | Wrap ternary operators: "default", "before-operators"

## wrapArguments

对齐换行的函数参数或集合元素。

选项 | 描述
--- | ---
`--wraparguments` | Wrap all arguments: "before-first", "after-first", "preserve"
`--wrapparameters` | Wrap func params: "before-first", "after-first", "preserve"
`--wrapcollections` | Wrap array/dict: "before-first", "after-first", "preserve"
`--closingparen` | Closing paren position: "balanced" (default) or "same-line"
`--callsiteparen` | Closing paren at call sites: "balanced" or "same-line"
`--wrapreturntype` | Wrap return type: "if-multiline", "preserve" (default)
`--wrapconditions` | Wrap conditions: "before-first", "after-first", "preserve"
`--wraptypealiases` | Wrap typealiases: "before-first", "after-first", "preserve"
`--wrapeffects` | Wrap effects: "if-multiline", "never", "preserve"

<details>
<summary>示例</summary>

**NOTE:** For backwards compatibility with previous versions, if no value is
provided for `--wrapparameters`, the value for `--wraparguments` will be used.

`--wraparguments before-first`

```diff
- foo(bar: Int,
-     baz: String)

+ foo(
+   bar: Int,
+   baz: String
+ )
```

```diff
- class Foo<Bar,
-           Baz>

+ class Foo<
+   Bar,
+   Baz
+ >
```

`--wrapparameters after-first`

```diff
- func foo(
-   bar: Int,
-   baz: String
- ) {
    ...
  }

+ func foo(bar: Int,
+          baz: String)
+ {
    ...
  }
```

`--wrapcollections before-first`:

```diff
- let foo = [bar,
             baz,
-            quuz]

+ let foo = [
+   bar,
    baz,
+   quuz
+ ]
```

</details>
<br/>

## wrapAttributes

将 `@attributes` 属性换到单独一行，或保持在同一行。

选项 | 描述
--- | ---
`--funcattributes` | Function @attributes: "preserve", "prev-line", or "same-line"
`--typeattributes` | Type @attributes: "preserve", "prev-line", or "same-line"
`--storedvarattrs` | Stored var @attribs: "preserve", "prev-line", or "same-line"
`--computedvarattrs` | Computed var @attribs: "preserve", "prev-line", "same-line"
`--complexattrs` | Complex @attributes: "preserve", "prev-line", or "same-line"
`--noncomplexattrs` | List of @attributes to exclude from complexattrs rule

<details>
<summary>示例</summary>

`--funcattributes prev-line`

```diff
- @objc func foo() {}

+ @objc
+ func foo() { }
```

`--funcattributes same-line`

```diff
- @objc
- func foo() { }

+ @objc func foo() {}
```

`--typeattributes prev-line`

```diff
- @objc class Foo {}

+ @objc
+ class Foo { }
```

`--typeattributes same-line`

```diff
- @objc
- enum Foo { }

+ @objc enum Foo {}
```

</details>
<br/>

## wrapLoopBodies

将内联循环语句的主题换到新行。

<details>
<summary>示例</summary>

```diff
- for foo in array { print(foo) }
+ for foo in array {
+     print(foo)
+ }
```

```diff
- while let foo = bar.next() { print(foo) }
+ while let foo = bar.next() {
+     print(foo)
+ }
```

</details>
<br/>

## wrapMultilineStatementBraces

将多行语句的左大括号换到新行。

<details>
<summary>示例</summary>

```diff
  if foo,
-   bar {
    // ...
  }

  if foo,
+   bar
+ {
    // ...
  }
```

```diff
  guard foo,
-   bar else {
    // ...
  }

  guard foo,
+   bar else
+ {
    // ...
  }
```

```diff
  func foo(
    bar: Int,
-   baz: Int) {
    // ...
  }

  func foo(
    bar: Int,
+   baz: Int)
+ {
    // ...
  }
```

```diff
  class Foo: NSObject,
-   BarProtocol {
    // ...
  }

  class Foo: NSObject,
+   BarProtocol
+ {
    // ...
  }
```

</details>
<br/>

**NOTE:** 待讨论

## wrapSingleLineComments

将超过 `--maxwidth` 的单行注释 `//` 换行。

## yodaConditions

优先将常量放在表达式的右侧。

选项 | 描述
--- | ---
`--yodaswap` | Swap yoda values: "always" (default) or "literals-only"

# 默认关闭规则

## acronyms

当首字母大写时，将缩写词也大写。

选项 | 描述
--- | ---
`--acronyms` | 自动大写的首字母，默认是 "ID,URL,UUID"

<details>
<summary>示例</summary>

```diff
- let destinationUrl: URL
- let urlRouter: UrlRouter
- let screenId: String
- let entityUuid: UUID

+ let destinationURL: URL
+ let urlRouter: URLRouter
+ let screenID: String
+ let entityUUID: UUID
```

</details>
<br/>

**NOTES:** 开启后，Codable 模型需要检查下字段。

## blankLineAfterSwitchCase

在多行的 switch case 语句后插入一个空白行（最后一个 case 除外，它后面跟右大括号）。

<details>
<summary>示例</summary>

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

## blankLinesBetweenImports

移除 import 语句之间的空白行。

<details>
<summary>示例</summary>

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

## blockComments

将块注释转换为连续的单行注释。

<details>
<summary>示例</summary>

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

## docComments

对 API 声明使用文档注释 `///`，否则使用常规注释 `//`。

选项 | 描述
--- | ---
`--doccomments` | 文档注释: "before-declarations" (default) or "preserve"

<details>
<summary>示例</summary>

```diff
- // A placeholder type used to demonstrate syntax rules
+ /// A placeholder type used to demonstrate syntax rules
  class Foo {
-     // This function doesn't really do anything
+     /// This function doesn't really do anything
      func bar() {
-         /// TODO: implement Foo.bar() algorithm
+         // TODO: implement Foo.bar() algorithm
      }
  }
```

</details>
<br/>

## isEmpty

首选 `isEmpty` 而不是用 `count` 跟零进行对比。

<details>
<summary>示例</summary>

```diff
- if foo.count == 0 {
+ if foo.isEmpty {

- if foo.count > 0 {
+ if !foo.isEmpty {

- if foo?.count == 0 {
+ if foo?.isEmpty == true {
```

**NOTE:** 在少数情况下，`isEmpty` 规则可能会对不实现该属性的类型插入 `isEmpty` 调用，从而导致程序出错。因此，该规则默认情况下是禁用的，必须通过 `--enable isEmpty` 选项手动启用。

</details>
<br/>

## markTypes

在顶级类型和扩展之前添加 MARK 注释。

选项 | 描述
--- | ---
`--marktypes` | Mark types "always" (default), "never", "if-not-empty"
`--typemark` | Template for type mark comments. Defaults to "MARK: - %t"
`--markextensions` | Mark extensions "always" (default), "never", "if-not-empty"
`--extensionmark` | Mark for standalone extensions. Defaults to "MARK: - %t + %c"
`--groupedextension` | Mark for extension grouped with extended type. ("MARK: %c")

<details>
<summary>示例</summary>

```diff
+ // MARK: - FooViewController
+
 final class FooViewController: UIViewController { }

+ // MARK: UICollectionViewDelegate
+
 extension FooViewController: UICollectionViewDelegate { }

+ // MARK: - String + FooProtocol
+
 extension String: FooProtocol { }
```

</details>
<br/>

## noExplicitOwnership

不要使用显式的所有权修饰符 (borrowing / consuming)。

<details>
<summary>示例</summary>

```diff
- borrowing func foo(_ bar: consuming Bar) { ... }
+ func foo(_ bar: Bar) { ... }
```

</details>
<br/>

## organizeDeclarations

组织 `class`，`struct`，`enum`，`actor` 和 `extension` 内的声明。

选项 | 描述
--- | ---
`--categorymark` | Template for category mark comments. Defaults to "MARK: %c"
`--markcategories` | Insert MARK comments between categories (true by default)
`--beforemarks` | Declarations placed before first mark (e.g. `typealias,struct`)
`--lifecycle` | Names of additional Lifecycle methods (e.g. `viewDidLoad`)
`--organizetypes` | Declarations to organize (default: `class,actor,struct,enum`)
`--structthreshold` | Minimum line count to organize struct body. Defaults to 0
`--classthreshold` | Minimum line count to organize class body. Defaults to 0
`--enumthreshold` | Minimum line count to organize enum body. Defaults to 0
`--extensionlength` | Minimum line count to organize extension body. Defaults to 0
`--organizationmode` | Organize declarations by "visibility" (default) or "type"

<details>
<summary>示例</summary>

`--organizationmode visibility` (default)

```diff
  public class Foo {
-     public func c() -> String {}
-
-     public let a: Int = 1
-     private let g: Int = 2
-     let e: Int = 2
-     public let b: Int = 3
-
-     public func d() {}
-     func f() {}
-     init() {}
-     deinit() {}
 }

  public class Foo {
+
+     // MARK: Lifecycle
+
+     init() {}
+     deinit() {}
+
+     // MARK: Public
+
+     public let a: Int = 1
+     public let b: Int = 3
+
+     public func c() -> String {}
+     public func d() {}
+
+     // MARK: Internal
+
+     let e: Int = 2
+
+     func f() {}
+
+     // MARK: Private
+
+     private let g: Int = 2
+
 }
```

`--organizationmode type`

```diff
  public class Foo {
-     public func c() -> String {}
-
-     public let a: Int = 1
-     private let g: Int = 2
-     let e: Int = 2
-     public let b: Int = 3
-
-     public func d() {}
-     func f() {}
-     init() {}
-     deinit() {}
 }

  public class Foo {
+
+     // MARK: Properties
+
+     public let a: Int = 1
+     public let b: Int = 3
+
+     let e: Int = 2
+
+     private let g: Int = 2
+
+     // MARK: Lifecycle
+
+     init() {}
+     deinit() {}
+
+     // MARK: Functions
+
+     public func c() -> String {}
+     public func d() {}
+
 }
```

</details>
<br/>

## redundantProperty

简化那些立即返回的冗余属性定义。

<details>
<summary>示例</summary>

```diff
  func foo() -> Foo {
-   let foo = Foo()
-   return foo
+   return Foo()
  }
```

</details>
<br/>

## sortSwitchCases

按字母顺序排列 switch 语句中的 case。

## wrapConditionalBodies

将内联条件语句的主体部分换到新的一行。

<details>
<summary>示例</summary>

```diff
- guard let foo = bar else { return baz }
+ guard let foo = bar else {
+     return baz
+ }
```

```diff
- if foo { return bar }
+ if foo {
+    return bar
+ }
```

</details>
<br/>

## wrapEnumCases

将用 `,` 分隔的枚举 case 重写为每个 case 占一行。

选项 | 描述
--- | ---
`--wrapenumcases` | Wrap enum cases: "always" (default) or "with-values"

<details>
<summary>示例</summary>

```diff
  enum Foo {
-   case bar, baz
  }

  enum Foo {
+   case bar
+   case baz
  }
```

</details>
<br/>

## wrapMultilineConditionalAssignment

在赋值运算符后将多行条件赋值表达式换行。

<details>
<summary>示例</summary>

```diff
- let planetLocation = if let star = planet.star {
-     "The \(star.name) system"
- } else {
-     "Rogue planet"
- }
+ let planetLocation =
+     if let star = planet.star {
+         "The \(star.name) system"
+     } else {
+         "Rogue planet"
+     }
```

</details>
<br/>

## wrapSwitchCases

将 switch 语句中有 `,` 的多个 case 换行。

<details>
<summary>示例</summary>

```diff
  switch foo {
-   case .bar, .baz:
      break
  }

  switch foo {
+   case .foo,
+        .bar:
      break
  }
```

</details>
<br/>

# 已弃用规则

## sortedImports

按字母顺序排列 import 语句。

*Note: sortedImports rule is deprecated. Use sortImports instead.*

## sortedSwitchCases

按字母顺序排列 switch 语句中的 case。

*Note: sortedSwitchCases rule is deprecated. Use sortSwitchCases instead.*

## specifiers

为成员修饰符使用一致的顺序。

*Note: specifiers rule is deprecated. Use modifierOrder instead.*