# very-secure-php-ini
how to properly and securely configure the entire php.ini file for the latest version of PHP

# Most Important Values - (Draft)

expose_php = Off # prevents disclosure of PHP version from being sent in HTTP Headers

display_errors = Off
- displays whether errors should be printed on the screen to everyone visiting the site, disable

allow_url_include = Off
- allows risky website loading function
- use with some caution

session.cookie_httponly = 1
- disables access to cookies via Javascript APIs
- use with some caution; might break something 

session.use_strict_mode   = 1
- prevents session fixation  attacks

session.cookie_secure     = 1
- requires cookies to be transmitted over HTTPS only

session.cookie_samesite   = Strict
- prevents cross-origin attacks

session.use_trans_sid = 0
- you don't need this always make sure this is off

session.sid_length = 128
- length of session string, prevents brute force attacks

session.sid_bits_per_character = 6
- increases randomness of session string, prevents brute force attack

# Further Info:

1. This is the single best place to go to look up php.ini values: http://php.net/manual/en/ini.list.php. See what each value that you want to learn about does, if current values in your php.ini file have been deprecated in the current release, etc.
