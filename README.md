# Email Addresses are Special

So you want to build an email address validator?

Here is some information that can be helpful.

## DO NOT USE REGEX

Regular Expressions are powerful however, it is truly the wrong tool for the job.

This is Perl's Regular Expression For [Email Validation](https://metacpan.org/release/RJBS/Email-Valid-1.200/source/lib/Email/Valid.pm#L390)

So as you can see to get a fully complete email validator is a messy process in Regex and I am assuming that the performance is not that great

## Emails are very permissive

For Example, These Are Some of my favorite valid emails

```text
// It is in between quotes and the characters are escaped
"very.(),:;<>[]\".VERY.\"very@\ \"very\".unusual"@strange.example.com
// Yes this is valid. 
#!$%&'*+-/=?^_`{}|~@example.org
// Empty Space Between Quotes is allowed
" "@example.org
```

## Implementing an Email Validator

If you decide to implement an email validator I recommend you read these resources first

- [RFC5322](https://datatracker.ietf.org/doc/html/rfc5322#section-3.4)

Then have a ton of tests. This Repository Contains some JSON files with tests to help you test your email validator.

Feel free to add more tests.

## Libraries that can do it for you

Find a Library to validate you because implementing it yourself is a mess

### Rust

- [Lettre](https://github.com/lettre/lettre)
- [mail_lib_types](https://github.com/nitro-mail/mail_lib/)

Feel free to PR more libraries

### Thank You

[kenorb](https://stackoverflow.com/a/38787343) for their invalid and valid emails on StackOverFlow.
