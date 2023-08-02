# PAPIF - API endpoint fuzzer 
**Developed by:** Pramod Kumar
**Version**: 0.1
**Last updated:** 01/08/2023
**Status**: Active 

### About papif
papif is an API endpoint fuzzer, once a wordlist has been selected it'll send a request to each possible endpoint using various request methods (POST, GET, PUT and DELETE) and then look for differences within the responses.

### Usage Example
`console[~/papif/]: python3 papif.py -u https://api.target.com/api/ -w /opt/wordlists/api-endpoints.txt -m get,post -dl 2 -ms parameter`


### Help Output
```
usage: papif.py [-h] -u <example url> [<example url> ...] -w <wordlist> -m <method> [-dl]
               [-ms <string> [<string> ...]] [-v] [-k] [--version]

options:
  -h, --help                                                    Display the help options.
  -u <example url> [<example url> ...], --url <example url> [<example url> ...]
                                                                Specify the target url after the -u
                                                                flag.
  -w <wordlist>, --wordlist <wordlist>                          Specify your chosen wordlist after the
                                                                -w flag.
  -m <method>, --method <method>                                Specify the desired request methods,
                                                                accepted methods are
                                                                get,post,put,delete or all.
  -dl , --default_testing_length                                Specify the testing length thats tested
                                                                against.
  -ms <string> [<string> ...], --match_string <string> [<string> ...]
                                                                Match a specific string within the
                                                                response text.
  -v, --verbose                                                 Verbose mode
  -k, --ignore_certificates                                     Ignore SSL certificate verification.
  --version                                                     Show papif.py version number

```
