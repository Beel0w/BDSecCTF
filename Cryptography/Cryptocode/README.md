# Cryptocode 

## Context

>I convert plain text to cipher text by using Cryptocode library . Always Remember BDSEC is a KEY .
>
>Attachments
> - [cipher.txt](cipher.txt)
>
>Flag Format : BDSEC{fl4g_h3r3}
>
>**Author : 1xR1FAT**

## Resolving

- Cryptocode corresponds to a library available on python.
- We know the key is BDSEC

Let's try this code on python 3 : 

```ruby
import cryptocode

cipher = 'c00EtfL9GPq2EItQrkFyPKIMfVFZy0O4ssXtr/V2Io7NMbNS*Brue6Cex4JuWkWU0lUEK2w==*f8EsezuHu2WBstRDlWZiLg==*CZ/4FNMavWZu3kznPrAyeg=='
key = 'BDSEC'
 
print(cryptocode.decrypt(cipher,key))

```
We get : BDSEC{cryp70_and_pyth0n_ar3_aw3s0me}

The Flag is : `BDSEC{cryp70_and_pyth0n_ar3_aw3s0me}`
