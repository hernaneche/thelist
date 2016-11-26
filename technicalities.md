<link rel="shortcut icon" href="img/favicon.ico"/>
<link href="http://fonts.googleapis.com/css?family=Open+Sans:400italic,400,700|Istok+Web:400,400italic,700,700italic" rel="stylesheet" type="text/css"/>
<link href="css/theliststyle.css" rel="stylesheet" type="text/css">   
<div style="position: fixed; top: 1em; right: 2em; text-align:right;">
<link href="css/textstyle.css" rel="stylesheet" type="text/css">
<a href="javascript:history.back();" class="linkMyPages" title="&#8469;">back</a></div>

##Technicalities
---
###How is this list made?

There are infinitely many possible lists of numbers and mappings on them, some are faster, some slower, some are longer, shorter, popular ones, and so on, for different domains, beings and purposes. This one, this list was chosen to be *as continuous as possible*, with not forbidden numbers nor inputs, you input a number and there is something there, and vice versa.   

It's made around UTF-8 coding, and Base64 for files, it allows input international encoding and some standard file formats.   For example if you input an ~ this will show the decimal value of the UTF-8 encoding for that character, i.e. 126. If you input ~~ then it "could" show 126 126, but it doesn't, because that would make the list to be *very* discontinuous, even decoding character by character won't be a **prefix code** because 126126 could be understood in many ways, for example: 12, 61, 26 or 1, 261, 26 and so on, it will not have the property of being uniquely decodable, unless we leave spaces or any special marker within codes 126[marker]126, but at doing that, we won't have a natural number any more, let alone a continuous list; so instead, if you input ~~ you get the number 32382, that is a direct conversion to decimal from hexadecimal code of UTF-8. 

**UTF-8 encoding** 

    8bits  0xxxxxxx  
    16bits 110yyyyy 10xxxxxx  
    24bits 1110zzzz 10yyyyyy 10xxxxxx  
    32bits 11110uuu 10uuzzzz 10yyyyyy 10xxxxxx   	
    
As it's a prefix code, it's possible to concatenate codes of different lengths without mixing or confusing at decoding.

UTF-8 is not a fixed bit length number to take as a base, so this is not as continuous as it wants to be, but as continuous as it can by now[any more continuous approach is welcome!]. In a way it's as taking the UTF-8 as the "base" of a **mixed radix numeral system** that is then converted to decimal and vice versa.

- First ensured chars to be in UTF-8 encoding (a prefix code! i.e no code start as any other, so there is no need for markers)  
- They are represented in individual hexadecimal numbers, and concatenated to form a whole big hexadecimal number.   
- The big hex number is converted into decimal *(this part is painfully slow)* [any faster approach is welcome!]
