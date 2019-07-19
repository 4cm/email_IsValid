# email_IsValid
PHP function to validate if an email address is valid or not.

This function includes checking for email injections, [syntax formatting](https://gist.github.com/johnabela/9a41191e9946ed59addae447b3c72206), dns checking, and a few basic TLD corrections.


## Usage

Here is how you use the `email_IsValid()` function:

```php
$Email = 'foo@.com';
//
if ( !email_IsValid($Email) ) {
    //
    die('The email address you entered does not appear to be a valid email address.');
    //
}
```

## Requirements

This function requires that you have access to the [idn_to_ascii()](https://www.php.net/manual/en/function.idn-to-ascii.php) function, which requires your PHP server have [intl](https://www.php.net/manual/en/intl.installation.php) installed, if you want the dns check to perform.

## License

The MIT License (MIT). Please see [License File](LICENSE) for more information.
