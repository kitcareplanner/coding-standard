# CarePlanner Coding Standard

The CarePlanner Coding Standard is a set of [PHP_CodeSniffer](https://github.com/squizlabs/PHP_CodeSniffer) rules applied to all CarePlanner Symfony projects. It is  based on [Doctrine Coding Standard](https://github.com/doctrine/coding-standard) with a heavily influence by [Slevomat Coding Standard](https://github.com/slevomat/coding-standard).

Code MUST follow all rules outlined in [PSR-12](https://www.php-fig.org/psr/psr-12/).

## Differences to Doctrine Coding Standard
### Additions
#### Severity 4
- Exactly 1 empty line must be between class members. (SlevomatCodingStandard.Classes.ClassMemberSpacing)
- Exactly 1 empty line before a constant with a comment, and up to 1 empty line between constants without a comment. (SlevomatCodingStandard.Classes.ConstantSpacing)
- Exactly 1 empty line between methods. (SlevomatCodingStandard.Classes.MethodSpacing)
- Exactly 1 empty line before a property with a comment, and up to 1 empty line between properties without a comment. (SlevomatCodingStandard.Classes.PropertySpacing)
- Union type hints must not contain spaces between types, and `null` must be in the last position. (SlevomatCodingStandard.TypeHints.UnionTypeHintFormat)
#### Severity 3
- A trailing comma in function declarations is required. (SlevomatCodingStandard.Functions.RequireTrailingCommaInDeclaration)
- A method signature must be a one-liner where possible. (SlevomatCodingStandard.Classes.RequireSingleLineMethodSignature)
- A function call must be a one-liner where possible. (SlevomatCodingStandard.Classes.RequireSingleLineCall)
- Class members must be present in the following order: (SlevomatCodingStandard.Classes.ClassStructure)
  - uses
  - public constants
  - constants
  - public static properties
  - static properties
  - public properties
  - properties
  - constructor
  - magic methods
  - methods
- Arrow functions must be used where possible. (SlevomatCodingStandard.Functions.RequireArrowFunction)
- Non-capturing catch statements must be used when applicable. (SlevomatCodingStandard.Exceptions.RequireNonCapturingCatch)
- `@deprecated` annotations must have a description. (SlevomatCodingStandard.Commenting.DeprecatedAnnotationDeclaration)
- `continue` in switch without integer operand is not allowed. (SlevomatCodingStandard.ControlStructures.DisallowContinueWithoutIntegerOperandInSwitch)
- When creating objects with `new`, there must be parentheses after the class name. (SlevomatCodingStandard.ControlStructures.NewWithParentheses)
#### Severity 2
- Unused variables are not allowed. (SlevomatCodingStandard.Variables.UnusedVariable)
- Using `$strict = true` is required for PHP functions that have such a parameter. (SlevomatCodingStandard.Functions.StrictCall)
- Numeric literal separators are required in large numbers. (SlevomatCodingStandard.Numbers.RequireNumericLiteralSeparator)
- Increment and decrement operators must be standalone. (SlevomatCodingStandard.Operators.RequireOnlyStandaloneIncrementAndDecrementOperators)
- Short ternary operator (`?:`) must be used where possible. (SlevomatCodingStandard.ControlStructures.RequireShortTernaryOperator)
- Ternary operator must be used where possible. (SlevomatCodingStandard.ControlStructures.RequireTernaryOperator)
- Functions with no statements must contain a comment. (SlevomatCodingStandard.Functions.DisallowEmptyFunction)
- Useless parameter default values are not allowed. (SlevomatCodingStandard.Functions.UselessParameterDefaultValue)
#### Severity 1
- Implicit array creation is not allowed. (SlevomatCodingStandard.Arrays.DisallowImplicitArrayCreation)
- References are not allowed. (SlevomatCodingStandard.PHP.DisallowReference)
- Multiple namespaces in a single file are not allowed. (SlevomatCodingStandard.Namespaces.RequireOneNamespaceInFile)
- Parameters with no uses are not allowed. (SlevomatCodingStandard.Functions.UnusedParameter)
- Functions may not be longer than 40 lines. (SlevomatCodingStandard.Functions.FunctionLength)
### Exclusions
- Aligning assignment statements (Generic.Formatting.MultipleStatementAlignment)
- Force space after `!` (Generic.Formatting.SpaceAfterNot)
- Early exits are not required when the if statement is standalone, or last in scope with only one instruction. (SlevomatCodingStandard.ControlStructures.EarlyExit)
- Doc comment alignment. (Squiz.Commenting.DocCommentAlignment)
- Function phpDoc parameter alignment. (Squiz.Commenting.FunctionComment.SpacingAfterParamType) 

## Severity 5 (default)
- `else if` is not allowed, `elseif` must be used instead. (PSR2.ConstrolStructures.ElseIfDeclaration.NotAllowed)
- Multi-line arrays must have a comma after the last element. (SlevomatCodingStandard.Arrays.TrailingArrayComma)
- Constants must state their visibility. (SlevomatCodingStandard.Classes.ClassConstantVisibility)
- There must be no empty lines before or between trait uses, and exactly 1 line after the last. (SlevomatCodingStandard.Classes.TraitUseSpacing)
- Null safe operator (`?->`) must be used when possible. (SlevomatCodingStandard.ControlStructures.RequireNullSafeObjectOperator)
- Use statements must be sorted alphabetically. (SlevomatCodingStandard.Namespaces.AlphabeticallySortedUses)
- Namespaces must be separated by empty lines. (SlevomatCodingStandard.Namespaces.NamespaceSpacing)
- There must be exactly 1 empty line before the first use statement, exactly 1 empty line after the last use statement, and exactly 1 empty line between types of use statements. Use statements of the same type must not have any empty lines between them. (SlevomatCodingStandard.Namespaces.UseSpacing)
- `declare(strict_types=1)` must be present as shown with exactly 1 empty line before and after. (SlevomatCodingStandard.TypeHints.DeclareStrictTypes)
- Type hints must include the nullability sign (`?`) when the default value is null. (SlevomatCodingStandard.TypeHints.NullableTypeForNullDefaultValue)
- There must be one space between type hints and the variable, and no space after the nullability sign. (SlevomatCodingStandard.TypeHints.ParameterTypeHintSpacing)
- There must be no space before the colon in return types. (SlevomatCodingStandard.TypeHints.ReturnTypeHintSpacing)
- Doc comments must be one line when there's only 1 annotation present. (SlevomatCodingStandard.Commenting.RequireOneLineDocComment)
- Class name must match the file name. (Squiz.Classes.ClassFileName)
- `AND` and `OR` are not allowed, `&&` and `||` must be used instead. (Squiz.Operators.ValidLogicalOperators)
- PHP function calls must be in lowercase. (Squiz.PHP.LowercasePHPFunctions)
- There must be exactly 1 space or a new line (with the required indentation) before and after the concatenation operator. (Squiz.Strings.ConcatenationSpacing)
- There must be exactly 1 space around logical operators. (Squiz.WhiteSpace.LogicalOperatorSpacing)

### The following are NOT allowed:
- Multiple classes with the same name. (Generic.Classes.DuplicateClassName)
- Final methods in final classes (redundant). (Generic.CodeAnalysis.UnnecessaryFinalModifier)
- Inline HTML. (Generic.Files.InlineHTML)
- PHP 4 constructors. (Generic.NamingConventions.ConstructorName)
- Content before PHP opening tag. (Generic.PHP.CharacterBeforePHPOpeningTag)
- Using deprecated PHP functions. (Generic.PHP.DeprecatedFunctions)
- Backtick operator. (Generic.PHP.BacktickOperator)
- Uppercase param or return types. (Generic.PHP.LowerCastType)
- Multiple constants declared in a statement. (SlevomatCodingStandard.Classes.DisallowMultiConstantDefinition)
- Empty lines around type declarations. (SlevomatCodingStandard.Classes.EmptyLinesAroundClassBraces)
- Uses of multiple traits seprated by a comma. (SlevomatCodingStandard.Classes.TraitUseDeclaration)
- Usage of a boolean-only ternary operator (e.g. `$foo ? true : false`). (SlevomatCodingStandard.ControlStructures.UselessTernaryOperator)
- Unreachable catch blocks. (SlevomatCodingStandard.Exceptions.DeadCatch)
- Unused variables passed to closures via `use` (SlevomatCodingStandard.Functions.UnusedInheritedVariablePassedToClosure)
- Group uses. (SlevomatCodingStandard.Namespaces.DisallowGroupUse)
- Multiple use statements on the same line. (SlevomatCodingStandard.Namespaces.MultipleUsesPerLine)
- Unused use statements. (SlevomatCodingStandard.Namespaces.UnusedUses)
- Leading backslash in use statements. (SlevomatCodingStandard.Namespaces.UseDoesNotStartWithBackslash)
- Useless aliases for classes, constants, or functions (SlevomatCodingStandard.Namespaces.UselessAlias)
- Weak comparisions (`==`, `!=`). (SlevomatCodingStandard.Operators.DisallowEqualOperators)
- Spacing after the spread operator. (SlevomatCodingStandard.Operators.SpreadOperatorSpacing)
- Argument unpacking for functions specialized by the PHP VM. (SlevomatCodingStandard.PHP.OptimizedFunctionsWithoutUnpacking)
- Longhand cast operators. (SlevomatCodingStandard.PHP.TypeCast)
- Useless semicolons. (SlevomatCodingStandard.PHP.UselessSemicolon)
- Duplicate variable assignments. (SlevomatCodingStandard.Variables.DuplicateAssignmentToVariable)
- Global functions. (Squiz.Functions.GlobalFunction)
- Global keyword. (Squiz.PHP.GlobalKeyword)
- Nested functions. (Squiz.PHP.InnerFunctions)
- Usage of `$this` inside a static function. (Squiz.Scope.StaticThisUsage)
- Braces around string in `echo`. (Squiz.Strings.EchoedStrings)
- Spaces in type casts. (Squiz.WhiteSpace.CastSpacing)
- Spaces between increment/decrement operator and its operand. (Generic.WhiteSpace.IncrementDecrementSpacing)
- Spaces around the `->` operator. (Squiz.WhiteSpace.ObjectOperatorSpacing)

## Severity 4
- A single space must come after a type cast. (Generic.Formatting.SpaceAfterCast)
- Single line arrays must not have space around brackets, and have a space after commas. (SlevomatCodingStandard.Arrays.SingleLineArrayWhitespace)
- Doc comments must be formatted as such:
  - No empty lines before the first line of content
  - No empty lines after the last line of content
  - An empty line between annotations and the description
  - An empty line between each annotation group (defined below)
  - Annotations to be ordered by groups: (SlevomatCodingStandard.Commenting.DocCommentSpacing)
    - `@internal`, `@deprecated`
    - `@link`, `@see`, `@uses`
    - `@ORM`, `@ODM`, `@PHPCR`
    - `@param`, `@psalm-param`, `@phpstan-param`
    - `@return`, `@psalm-return`, `@phpstan-return`
    - `@throws`
    - Any remaining annotations that aren't in a previous group
- The following annotations are forbidden: (SlevomatCodingStandard.Commenting.ForbiddenAnnotations)
  - `@api`
  - `@author`
  - `@category`
  - `@copyright`
  - `@created`
  - `@license`
  - `@package`
  - `@since`
  - `@subpackage`
  - `@version`
- The following comments are forbbiden: (SlevomatCodingStandard.Commenting.ForbiddenComments)
  - "private constructor", "protected constructor", "static constructor", "constructor"
  - "private destructor", "protected destructor", "static destructor", "destructor"
  - "Created by ..."
  - "User: ...", "Date: ...", "Time: ..."
  - "... getter", "... setter"
  - "Class ...", "Interface ...", "Trait ..."
- Comments with single line content must be written as one-liners. (SlevomatCodingStandard.Commenting.RequireOneLinePropertyDocComment)
- Block structures (`if`, `do`, `while`, `for`, `foreach`, `switch`, `try`, `default`) must have consistent spacing. (SlevomatCodingStandard.ControlStructures.BlockControlStructureSpacing)
- Jump statements (`return`, `throw`, `yield`, `yield_from`) must have consistent spacing. (SlevomatCodingStandard.ControlStructures.JumpStatementsSpacing)
- Arrow functions must have exactly 1 space after keyword, and exactly 1 space before and after the arrow. (SlevomatCodingStandard.Functions.ArrowFunctionDeclaration)
- The `null` type hint must be in the last position of annotations. (SlevomatCodingStandard.TypeHints.NullTypeHintOnLastPosition) 
- Function comments must be formatted consistently. (Squiz.Commenting.FunctionComment)
- Functions must have exactly 1 line before and after, except at the top and bottom. (Squiz.Whitespace.FunctionSpacing)
- There must be exactly 1 space after language constructs. (Squiz.Whitespace.LanguageConstructSpacing)

### The following are NOT allowed:
- Comments starting with `#`. (PEAR.Commenting.InlineComment)
- Empty comments. (SlevomatCodingStandard.Commenting.EmptyComment)
- A space after the negative operator `-`. (SlevomatCodingStandard.Operators.NegationOperatorSpacing)
- Useless `@var` annotation on constants. (SlevomatCodingStandard.TypeHints.UselessConstantTypeHint)
- Useless phpDocs for functions. (SlevomatCodingStandard.Commenting.UselessFunctionDocComment)
- Useless inherit doc comments. (SlevomatCodingStandard.Commenting.UselessInheritDocComment)
- Spaces around square brackets. (Squiz.Arrays.ArrayBracketSpacing)
- A blank line after the opening brace on a function. (Squiz.Whitespace.FunctionOpeningBraceSpace)
- A space before the semicolon. (Squid.WhiteSpace.SemicolonSpacing)
- Superfluous empty lines. (Squiz.WhiteSpace.SuperfluousWhitespace.EmptyLines)

## Severity 3
- Array elements in multi-line arrays must be indented by 4 spaces. (Generic.Arrays.ArrayIndent)
- `array(...)` is not allowed, `[ ... ]` must be used instead. (Generic.Arrays.DisallowLongArraySyntax)
- Late static binding for constants is not allowed. (SlevomatCodingStandard.Classes.DisallowLateStaticBindingForConstants)
- `__CLASS__`, `get_class()`, `get_called_class()` and `get_parent_class()` are not allowed, `::class` must be used instead (SlevomatCodingStandard.Classes.ModernClassNameReference)
- Early exit must be used when possible. (SlevomatCodingStandard.ControlStructures.EarlyExit)
- Null coalesce equal operator (`??=`) must be used when possible. (SlevomatCodingStandard.ControlStructures.RequireNullCoalesceEqualOperator)
- Null coalesce operator (`??`) must be used when possible. (SlevomatCodingStandard.ControlStructures.RequireNullCoalesceOperator)
- Catching Throwable must be used instead of Exception. (SlevomatCodingStandard.Exceptions.ReferenceThrowableOnly)
- Closures not referencing `$this` must be declared as `static`. (SlevomatCodingStandard.Functions.StaticClosure)
- Combined assignment operators (e.g. `+=`) must be used when possible. (SlevomatCodingStandard.Operators.RequireCombinedAssignmentOperator)
- `list(...)` is not allowed, `[ ... ]` must be used instead. (SlevomatCodingStandard.PHP.ShortList)
- `/* @var type $foo */` and similar simple inline annotations must be written as `assert($foo instanceof type)`. (SlevomatCodingStandard.PHP.RequireExplicitAssertion)
- Short versions of scalar types must be used over their long counterparts. (SlevomatCodingStandard.TypeHints.LongTypeHints)
- Array declarations must be consistently formatted. (Squiz.Arrays.ArrayDeclaration)
- Self reference must use `self::` with no spaces. (Squiz.Classes.SelfMemberReference)
- Double quotes may only be used when necessary, and may not include variables to be expanded. (Squiz.Strings.DoubleQuoteUsage)

### The following are NOT allowed:
- Empty statements. (Generic.CodeAnaylsis.EmptyStatement)
- Useless inline string concatenation. (Generic.Strings.UnnecessaryStringConcat)
- [Yoda conditions](https://en.wikipedia.org/wiki/Yoda_conditions). (SlevomatCodingStandard.ControlStructures.DisallowYodaComparison)
- Language constructs with parentheses. (SlevomatCodingStandard.ControlStructures.LanguageConstructWithParentheses)
- Conditions when a simple return can be used. (SlevomatCodingStandard.ControlStructures.UselessIfConditionWithReturn)
- Using absolute class name references except for collisions. (SlevomatCodingStandard.Namespaces.ReferenceUsedNamesOnly)
- Uses of the same namespace. (SlevomatCodingStandard.Namespaces.UseFromSameNamespace)
- Useless parentheses. (SlevomatCodingStandard.PHP.UselessParentheses)
- Useless variables. (SlevomatCodingStandard.Variables.UselessVariable)

## Severity 2
- The following functions are forbidden: (Generic.PHP.ForbiddenFunctions and Generic.PHP.SAPIUsage)
  - `compact`
  - `extract`
  - `is_null`
  - `settype`
  - `php_sapi_name`
- The following alias functions are forbidden: (Generic.PHP.ForbiddenFunctions)
  - `chop` (use `rtrim` instead)
  - `close` (use `closedir` instead)
  - `delete` (use `unset` instead)
  - `doubleval` (use `floatval` instead)
  - `fputs` (use `fwrite` instead)
  - `ini_alter` (use `ini_set` instead)
  - `is_double` (use `is_float` instead)
  - `is_integer` (use `is_int` instead)
  - `is_long` (use `is_int` instead)
  - `is_real` (use `is_float` instead)
  - `is_writeable` (use `is_writable` instead)
  - `join` (use `implode` instead)
  - `key_exists` (use `array_key_exists` instead)
  - `pos` (use `current` instead)
  - `show_source` (use `highlight_file` instead)
  - `sizeof` (use `count` instead)
  - `strchr` (use `strstr` instead)
  - `user_error` (use `trigger_error` instead)
- Inline phpDocs with `@var` must be correctly formatted. (SlevomatCodingStandard.Commenting.InlineDocCommentDeclaration)
- Parameter type hints must be written natively when possible. (SlevomatCodingStandard.TypeHints.ParameterTypeHint)
- Property type hints must be written natively when possible. (SlevomatCodingStandard.TypeHints.PropertyTypeHint)
- Return type hints must be written natively when possible. (SlevomatCodingStandard.TypeHints.ReturnTypeHint)
- Variables must be named using camelCase. (Squiz.NamingConventions.ValidVariableName)

### The following are NOT allowed:
- Assigning variables within a condition. (SlevomatCodingStandard.ControlStructures.AssignmentInCondition)
- Function comments missing parameter names. (Squiz.Commenting.FunctionComment.MissingParamName)
- Unexecutable code. (Squiz.PHP.NonExecutableCode)

## Severity 1

### The following are NOT allowed:
- Useless method overriding. (Generic.CodeAnaylsis.UselessOverridingMethod)
- Prefix or suffix "Abstract" in an abstract class. (SlevomatCodingStandard.Classes.SuperfluousAbstractClassNaming)
- Prefix or suffix "Exception" in an exception class. (SlevomatCodingStandard.Classes.SuperfluousExceptionNaming)
- Prefix or suffix "Interface" in an interface. (SlevomatCodingStandard.Classes.SuperfluousInterfaceNaming)
- Suffix "Trait" in a trait. (SlevomatCodingStandard.Classes.SuperfluousTraitNaming)
