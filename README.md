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



### Βήμα 3ο


