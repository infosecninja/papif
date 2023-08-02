# PAPIF - API endpoint fuzzer 
**Developed by:** Pramod Kumar
**Version**: 0.1
**Last updated:** 01/08/2023
**Status**: Active 

### About papif
Papif serves as an API endpoint fuzzer that operates by selecting a wordlist and subsequently sending requests to all potential endpoints. These requests utilize different methods, including POST, GET, PUT, and DELETE. The tool then analyzes the responses to identify any variations or discrepancies.


### Usage Example
`console[~/papif/]: python3 papif.py -u https://api.target.com/endpoint/ -w /opt/wordlists/api.txt -m get,post -dl 2 -ms parameter`


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
