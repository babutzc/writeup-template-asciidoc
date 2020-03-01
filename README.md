# writeup-template-asciidoc

This template can be used if you dont like the standard ascidoctor-pdf default theme. I tried to make it a dynamic document, so you have minimale changes to make. 

Customize the theme yourself
* ![AsciiDoctor PDf Theming Guide](https://github.com/asciidoctor/asciidoctor-pdf/blob/master/docs/theming-guide.ado)



# Required 

* asciidoctor 
* ascidoctor-pdf 

# Changes 
__Template location__
If you want to place writeup-theme.yml in a different folder than your template you need to adjust the template as followed: 

```
:pdf-theme: writeup
:pdf-themesdir: <<folder path>> 
```

__Image__
If you want a different image you can change the URL

```
:title-logo-image: image::https://pbs.twimg.com/media/EROZoCLWsAEL99X?format=jpg[align=center]
```

# Create PDF 
Use the following syntac to create a pdf. If you do not usea picture from the internet you can exclude the ``-a`` flag

```
asciidoctor-pdf -b pdf -o template.pdf -D ../pdf  -a allow-uri-read template.adoc```

```
-b	which backend
-o	name of the output file
-D 	Location where to place output file
-a 	allow to fetch the image from a remote target
```

