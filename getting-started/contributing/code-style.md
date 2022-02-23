# Code Style

To keep the code base clean and uniform this document should be referenced if you are planning to submit a pull request or work on the repository.

Windows line endings should be used at all times and files should all have an empty new line at the bottom.

**British English must be used, no arguments will be had over American English word spelling.**

### Name Style

| Entity               | Style                                         |
| -------------------- | --------------------------------------------- |
| Types and Namespaces | Pascal                                        |
| Methods              | Pascal                                        |
| Properties           | Pascal                                        |
| Local variables      | lowerCamel                                    |
| Parameters           | lowerCamel                                    |
| Fields (public)      | Pascal                                        |
| Fields (other)       | lowerCamel                                    |
| Enumerations         | Pascal                                        |
| Interfaces           | IPascal (Pascal with I prefix, IFooInterface) |

### Braces and Brace Code Style

The overall global indent style is Allman with a few exceptions on where braces should be placed or added at all (redundant braces), see examples below.

```csharp
class FooClass
{
    // empty simple methods with no body should have the braces on separate lines
    public virtual void SomeVirtualMethod()
    {
    }

    // properties with default setter or getters should have the braces on the same line
    public uint EmptyProperty { get; set; }
    public uint EmptyProperty2 { get; init; }

    // setters or getters that have multiple lines should have the braces on seperate lines
    public uint SomeProperty
    {
        get => someValue;
        set
        {
            DoSomething();
            someValue = value;
        }
    }

    public void StandardMethod()
    {
        Foo();
        DoSomethingElse();
        ThirdForGoodMeasure();
    }

    public void RedundantBraces()
    {
        // no braces required
        for (uint i = 0u; i < 5u; i++)
            DoSomething(i);

        foreach (var foo in bar)
            DoSomething(foo);

        // braces only required for the if block as it has multiple lines
        if (Foo())
        {
            FooBar();
            SecondFunction();
        }
        else
            return;

        // no braces required for either as both are single line
        if (Foo())
            FooBar();
        else
            FooBar2();
    }
}
```

### Comments

All public methods should contain a summary description, private methods do not require a description.

The description at minimum should contain summary information, return, parameter, exception, etc... comments are optional.

```csharp
class FooClass
{
    /// <summary>
    /// Does something cool.
    /// </summary>
    public void SomePublicMethod()
    {
    }
}
```

### Enumerations

Enumeration and value names should both be PascalCase, if specifying index values these should be spaced out to the match to length of the longest value name (see example), the final value in any enumeration should not have the ending comma.

_Note: enumerations should be ordered by their values unless specified otherwise with a comment (ex: opcode enumerations)_

```csharp
[Flags]
enum FooFlag
{
    None          = 0x00,
    Foo           = 0x01, // comment
    SomeOtherFlag = 0x02  // final value comment has an extra space due to missing comma
}

// ordered enumeration values do not need to be indexed, this is up to your discretion
enum FooValues
{
    None,
    Foo,
    SomeOtherValue
}

enum FooValues
{
    None           = 0,
    Foo            = 1,
    SomeOtherValue = 2
}
```

### Attributes

Attributes must be placed on a separate line to the entity they are intended to effect (the exception is parameters which have the attribute on the line, see example below), custom attributes must adhere to the standard class name style of PascalCase.

```csharp
[FooAttribute]
class FooClass
{
    [FooAttribute]
    public uint FooValue { get; }

    [FooAttribute]
    public void FooMember()
    {
    }
    
    public void FooParameters([FooAttribute] bla, [FooAttribute] bla2)
    {
    }
    
    public void FooParameters2(
        [FooAttribute]
        bla,
        [FooAttribute]
        bla2)
    {
    }
}

enum FooEnum
{
    None,
    [FooAttribute]
    Foo
}
```
