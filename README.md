# very-secure-php-ini
how to properly and securely configure the entire php.ini file for the latest version of PHP

# Most Important Values - (Draft)

expose_php = Off

display_errors = Off

allow_url_include = Off

session.cookie_httponly = 1

session.use_strict_mode   = 1

session.cookie_secure     = 1

session.cookie_samesite   = Strict

session.use_trans_sid = 0

session.sid_length = 128

session.sid_bits_per_character = 6

# Further Info:

1. This is the single best place to go to look up php.ini values: http://php.net/manual/en/ini.list.php. See what each value that you want to learn about does, if current values in your php.ini file have been deprecated in the current release, etc.
