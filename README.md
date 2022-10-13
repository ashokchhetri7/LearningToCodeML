# Setting up GitHub Library: libindic/indic-trans

## DISCLAIMER !!!
I don't have the code, nor do I have rights, but I am writing this to help the users correctly download and use the indic-trans code in the system.
#### How to setup the git hub code indictrans | import error: ctranxn | from: can't read /var/mail/indictrans | libindic indic-trans code clone

## Steps

### 1. Download or use this code to clone: 
[link]: https://github.com/libindic/indic-trans



      git clone https://github.com/libindic/indic-trans.git 
      
      OR
      
      git clone https://github.com/irshadbhat/indictrans.git
------------------------------------------------------------------------------------------------------------------------
### 2. Now go to the directory through cmd / terminal

    cd indic-trans
      pip install -r requirements.txt
      python setup.py install  
------------------------------------------------------------------------------------------------------------------------
### 3. Now check if you have installed it correct or not, using:

      indictrans -v
------------------------------------------------------------------------------------------------------------------------
### 4. Then access the code library. Note you need come out of the source code directory to access the below commands;

    
     from indictrans import Transliterator
     trn = Transliterator(source='hin', target='eng', build_lookup=True)

     hin = """कांग्रेस पार्टी अध्यक्ष सोनिया गांधी, तमिलनाडु की मुख्यमंत्री
     जयललिता और रिज़र्व बैंक के गवर्नर रघुराम राजन के बीच एक समानता
     है. ये सभी अलग-अलग कारणों से भारतीय जनता पार्टी के राज्यसभा सांसद
     सुब्रमण्यम स्वामी के निशाने पर हैं. उनके जयललिता और सोनिया गांधी के
     पीछे पड़ने का कारण कथित भ्रष्टाचार है."""

     eng = trn.transform(hin)
     print(eng)
------------------------------------------------------------------------------------------------------------------------
### 5. The output should be like this:

    congress party adhyaksh sonia gandhi, tamilnadu kii mukhyamantri
    jayalalita or reserve bank ke governor raghuram rajan ke bich ek samanta
    he. ye sabhi alag-alag kaarnon se bhartiya janata party ke rajyasabha saansad
    subramanyam swami ke nishane par hai. unke jayalalita or sonia gandhi ke
    peeche padane kaa kaaran kathith bhrashtachar he.
------------------------------------------------------------------------------------------------------------------------
### 6. The library can translate this back to original through following code:
    
    trn = Transliterator(source='eng', target='hin')
    hin_ = trn.transform(eng)

------------------------------------------------------------------------------------------------------------------------
I have writting this all from the source https://github.com/libindic/indic-trans
Please refer to this [link] for more details. Enjoy!!!
