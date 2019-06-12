# data-desensitization

Data desensitization: mobile phone number, id card number, bank card number, etc.

数据脱敏：手机号、身份证号、银行卡号等。

Easy and safe desensitize way

Don’t Panic! ... Ddz

## What is Ddz?

Ddz is a library to desensitize sensitive data such as mobile phone number, id number and bank card number.

## Why use Ddz?

When working with sensitive data you often need to desensitize it. DDZ provides a very simple, straightforward and convenient library to handle it.

If you're struggling with data desensitization, you’ll need an easy way to handle it. This is the library for you.

If you are taking in desensitization data from string, number, or Boolean, or other formats which lack full types, then Ddz is the library for you.

## Usage

```
import "github.com/kankanreno/ddz"

str := ddz.ToDz("12345678")
```

Ddz will always return the desired string without error.

The following examples are merely a sample of what is available. Please review
the code for a complete set.

### Example:

    ddz.ToDz(12345678, 4, 2)                // "1234**78"
    ddz.ToDz(12345678, 4, 4)                // "12345678"
    ddz.ToDz(12345678, 4, 5)                // "12345678"
    ddz.ToDz(12345678, 9, 5)                // "12345678"
    ddz.ToDz(12345678, 0, 0)                // "********"
    ddz.ToDz(12345678, 0, 3}                // "*****678"
    ddz.ToDz(12345678, -2, 0)               // "********"
    ddz.ToDz(123456.78, 4, 2)               // "1234***78"
    ddz.ToDz(-123456.78, 4, 3)              // "-123***.78"
    ddz.ToDz("12345678", 4, 2)              // "1234**78"
    ddz.ToDz([]byte("123 45678"), 4, 2)     // "123 ***78"
    ddz.ToDz(true, 0, 0)                    // "****"
    ddz.ToDz(nil, 0, 5)                     // ""
    
