# Chinese2wordlist
Python package to convert chinese text to a word list. 
- Simplified and Traditional
- English and Dutch
- Json and Markdown response 


### Usage
```
usage: chinese2wordlist.py [-h]
                           [--character-input-type traditional or simplified)]
                           [--response-type json or markdown]
                           [--language (en or nl]
                           chinese

Convert Chinese text to a word list

positional arguments:
  chinese               chinese text

optional arguments:
  -h, --help            show this help message and exit
  --character-input-type (traditional or simplified)
                        input type of the characters
  --response-type json or markdown
                        return type
  --language (en or nl)
                        language to translate to


```

### Example
Returns a json response, for simplified characters, in English 
> `python chinese2wordlist.py 我是荷蘭人 `

With arguments for a markdown response, with traditional characters, in Dutch
> `python chinese2wordlist.py 我是荷蘭人 --response-type=markdown --character-input-type=traditional --language=nl`

Or with xargs
> `echo  '我是' | xargs python chinese2wordlist.py` 

With xargs from a file
> `cat 'chinese.txt' | xargs -n 1 python chinese2wordlist.py`

With xargs appending to a file
> `cat input.txt |  xargs -n 1 python chinese2wordlist.py --response-type=markdown >> output.txt` 



### Info

Uses CEDICT for Chinese to English

Uses NLDICT (work in progress) for Chinese to Dutch

[Issues or feature requests can be submitted are welcome](https://github.com/JorisKok/chinese2wordlist/issues)