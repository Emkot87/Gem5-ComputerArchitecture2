# Gem5-Arch2
Ελευθεριάδης Ανδρέας Ευστάθιος 9649  
Κωτούλας Εμμανουήλ 9697  

### Βήμα 1ο  


### Βήμα 2ο
#### SpecBzip

Σε αυτό το benchmark παρατηρούμε βελτίωση με την αύξηση οποιασδήποτε παραμέτρου  

![image](https://user-images.githubusercontent.com/49078291/146423629-a24f592c-f66a-4717-96db-ea7b8bb3a9c2.png)
Ωστόσο το CPI φαίνεται να σταματάει να μειώνεται σημαντικά για associativity άνω του 4  

![image](https://user-images.githubusercontent.com/49078291/146425541-fc725f8f-c053-40fc-b12d-8748c6f5dd78.png)
![image](https://user-images.githubusercontent.com/49078291/146425776-d28afcc7-b971-4d4e-abbc-c42a7e1ff434.png)

Με την αύξηση της L2 cache βλέπουμε συνεχή μείωση του CPI και του L2 miss rate αυξάνεται σημαντικά όμως το κόστος  

![image](https://user-images.githubusercontent.com/49078291/146426017-c7d668ec-1aac-4a1a-8c29-4195d73b8ed4.png)
Με παρόμοιο τρόπο βλέπουμε οτι με την αύξηση του Cacheline size μειώνεται το CPI  

#### SpecHmmer  

Σε αυτό το benchmark παρατηρούμε σχεδόν μηδενική βελτίωση από την αλλαγή οποιουδήποτε μεγέθους όσο οι τιμές είναι πάνω απο ένα κάτω όριο με μικρή εξαίρεση το Cacheline Size    
![image](https://user-images.githubusercontent.com/49078291/146426976-746a87de-c6ce-4efe-bc26-18dcbfcda817.png)
![image](https://user-images.githubusercontent.com/49078291/146427134-1e9a6c1f-16b3-434c-ad34-1031a3ff95b4.png)

#### SpecLibm 

Σε αυτό το Benchmark παρατηρήσαμε οτι το Cacheline size επηρέασε σημαντικά το CPI ρίχνοντας το miss rate της L1. Μικρή ήταν επιρροή του μεγέθους της L2 Cache.  
![image](https://user-images.githubusercontent.com/49078291/146428414-cc5b09ab-77a0-4f36-8ee0-e23aa4568690.png)
![image](https://user-images.githubusercontent.com/49078291/146428430-03fc9730-ebaa-4130-be81-c1912c49cde0.png)
![image](https://user-images.githubusercontent.com/49078291/146428655-ecfc7a4b-8f77-4960-93a7-8ed7bf04c21e.png)

#### SpecMcf  

![image](https://user-images.githubusercontent.com/49078291/146428772-0292d177-2da9-42c0-8c0f-0e50724d8790.png)
![image](https://user-images.githubusercontent.com/49078291/146428803-640e9856-dc3b-457e-8202-1281b52fa1ed.png)

#### SpecSjeng

![image](https://user-images.githubusercontent.com/49078291/146428874-9ce0b799-1118-4840-a57b-378ebc1ab623.png)




### Βήμα 3ο


