# Sound's Good

## Context

>Challenge can give you intention sound can give you direction.
>
>Attachments
>
>- [file.txt](file.txt)
>
>Flag Format : BDSEC{fl4g_h3r3}
>
>**Author : pmsiam**

## Resolving

- By decoding the first line of this message, we notice that it is an audio :

| Encoding | Value |
|------------|:------:|
|Base 64 | <details><summary>`texte`</summary>SUQzBAAAAAACFVRYWFgAAAASAAADbWFqb3JfYnJhbmQAaXNvbQBUWFhYAAAAEwAAA21pbm9yX3ZlcnNpb24ANTEyAFRYWFgAAAAkAAADY29tcGF0aWJsZV9icmFuZHMAaXNvbWlzbzJhdmMxbXA0MQBUWFhYAAABAQAAA2NvbW1lbnQAQ3JlYXRlIHZpZGVvcyB3aXRoIGh0dHBzOi8vY2xpcGNoYW1wLmNvbS9lbi92aWRlby1lZGl0b3IgLSBmcmVlIG9ubGluZSB2aWRlbyBlZGl0b3IsIHZpZGVvIGNvbXByZXNzb3IsIHZpZGVvIGNvbnZlcnRlc</details> |
|To text | <details><summary>`text`</summary>ID3.......TXXX.......major_brand.isom.TXXX.......minor_version.512.TXXX...$...compatible_brands.isomiso2avc1mp41.TXXX.......comment.Create videos with https://clipchamp.com/en/video-editor - free online video editor, video compressor, video converter</details> |

- We use the [ipvoid](https://www.ipvoid.com/base64-to-mp3/) online tool to convert the base 64 to mp3.

  - Here is the audio file obtained : [song.mp3](song.mp3)

- We hear the following numbers : 4110 4246 4250 33665 44633 4657 53 1140 5253 72164 75242 76521 501465 75063 332 107 1027 6175

- To decode the message we can use the following script:

```ruby
print(bytes.fromhex(hex(int("41104246425033665446334657531140525372164752427652150146575063303210710276175",8))[2:]))
```
*The result is : b'BDSEC{Y3s_Y0U_GOT_Th3_Fl4G!|}'*

The Flag is : `BDSEC{Y3s_Y0U_GOT_Th3_Fl4G!|}`


