# V1: आर्किटेक्चर, डिजाइन और थ्रेट मॉडलिंग आवश्यकताएं

## उद्देश्य नियंत्रण

 एक संपूर्ण दुनिया में, विकास के सभी चरणों में सुरक्षा पर विचार किया जाएगा। हालांकि वास्तविकता में, सुरक्षा अक्सर एसडीएलसी (SDLC) में एक देर के चरण में एक विचार है। तकनीकी नियंत्रणों के अलावा, MASVS को ऐसी प्रक्रियाओं की आवश्यकता होती है जो यह सुनिश्चित करती हैं कि मोबाइल ऐप की वास्तुकला (architecture) की योजना बनाते समय सुरक्षा स्पष्ट रूप से संबोधित की गई है, और यह कि सभी घटकों (components) की कार्यात्मक और सुरक्षा भूमिकाएं ज्ञात हैं। चूंकि अधिकांश मोबाइल एप्लिकेशन दूरस्थ सेवाओं के लिए ग्राहकों के रूप में कार्य करते हैं, इसलिए यह सुनिश्चित किया जाना चाहिए कि उन सेवाओं के लिए उपयुक्त सुरक्षा मानक भी लागू हों - अलग से मोबाइल ऐप का परीक्षण करना पर्याप्त नहीं है।

"V1" श्रेणी, आर्किटेक्चर और ऐप के डिजाइन से संबंधित आवश्यकताओं को सूचीबद्ध करती है। इस प्रकार, यह एकमात्र श्रेणी है जो ओडब्ल्यूएएसपी(OWASP) मोबाइल टेस्टिंग गाइड में तकनीकी परीक्षण मामलों के लिए मैप नहीं करता है। थ्रेट मॉडलिंग, सुरक्षित एसडीएलसी( Secure SDLC) या मुख्य प्रबंधन (Key Management) जैसे विषयों को कवर करने के लिए, MASVS के उपयोगकर्ताओं को संबंधित OWASP योजना और / या अन्य मानकों से परामर्श करना चाहिए जैसे नीचे दिए गए लिंक।

## सुरक्षा सत्यापन आवश्यकताएँ

MASVS-L1 और MASVS-L2 की आवश्यकताएं नीचे सूचीबद्ध हैं।

| # | MSTG-ID | विवरण | L1 | L2 |
| -- | ---------- | ---------------------- | - | - |
| **1.1** | MSTG-ARCH-1 | सभी एप्लिकेशन घटकों की पहचान की जाती है और आवश्यक होने के लिये जाना जाता है। | x | x |
| **1.2** | MSTG-ARCH-2 | सुरक्षा नियंत्रण केवल ग्राहक पक्ष पर ही नहीं बल्कि संबंधित दूरस्थ समापन बिंदुओं पर भी लागू किए जाते हैं। | x | x |
| **1.3** | MSTG-ARCH-3 | मोबाइल एप्लिकेशन और सभी कनेक्टेड दूरस्थ सेवाओं के लिए एक उच्च-स्तरीय वास्तुकला (architecture) को परिभाषित किया गया है और उस वास्तुकला में सुरक्षा को संबोधित किया गया है। | x | x |
| **1.4** | MSTG-ARCH-4 | मोबाइल ऐप के संदर्भ में संवेदनशील माना जाने वाला डेटा स्पष्ट रूप से पहचाना जाता है। | x | x |
| **1.5** | MSTG-ARCH-5 | सभी ऐप घटकों (components) को उनके द्वारा प्रदान किये जाने वाले व्यावसायिक कार्यों और / या सुरक्षा कार्यों के संदर्भ में परिभाषित किया गया है। |  | x |
| **1.6** | MSTG-ARCH-6 | मोबाइल ऐप और संबंधित दूरस्थ सेवाओं के लिए एक थ्रेट मॉडल को प्रस्तुत किया गया है, जो संभावित खतरों और प्रतिकारों (countermeasure) की पहचान करता है। |  | x |
| **1.7** | MSTG-ARCH-7 | सभी सुरक्षा नियंत्रणों का केंद्रीयकृत कार्यान्वयन है।|  | x |
| **1.8** | MSTG-ARCH-8 | क्रिप्टोग्राफ़िक कुंजियाँ (यदि कोई हो) प्रबंधित की जाती हैं, और क्रिप्टोग्राफ़िक कुंजियों का जीवनचक्र कैसे लागू किया जाता है, इसके लिए एक स्पष्ट नीति है। आदर्श रूप से, NIST SP 800-57 जैसे प्रमुख प्रबंधन मानक का पालन करें। |  | x |
| **1.9** | MSTG-ARCH-9 | मोबाइल ऐप के अपडेट को लागू करने के लिए एक तंत्र मौजूद है। |  | x |
| **1.10** | MSTG-ARCH-10 | सॉफ्टवेयर विकास जीवनचक्र के सभी भागों के भीतर सुरक्षा को संबोधित किया जाता है। |  | x |
| **1.11** | MSTG-ARCH-11 | एक जिम्मेदार प्रकटीकरण नीति लागू होती है और प्रभावी रूप से लागू होती है। |  | x |
| **1.12** | MSTG-ARCH-12 | एप्लिकेशन को गोपनीयता कानूनों और नियमों का पालन करना चाहिए। | x | x |

## संदर्भ

अधिक जानकारी के लिए, यह भी देखें:

- OWASP मोबाइल टॉप 10: M10 (एक्सट्रोनस फंक्शनलिटी) - <https://owasp.org/www-project-mobile-top-10/2016-risks/m10-extraneous-functionality>
- OWASP थ्रेट मॉडलिंग - <https://owasp.org/www-community/Application_Threat_Modeling>
- Microsoft SDL - <https://www.microsoft.com/en-us/securityengineering/sdl/>
- NIST SP 800-57 - <https://csrc.nist.gov/publications/detail/sp/800-57-part-1/rev-5/final>
- security.txt - <https://securitytxt.org/>
