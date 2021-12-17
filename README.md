# Gem5-Arch2
Ελευθεριάδης Ανδρέας Ευστάθιος 9649  
Κωτούλας Εμμανουήλ 9697  

### Βήμα 1ο  
  1.a.   
bzip :  
Commited instructions (system.cpu.committedInsts) : 100000001  
Executed instructions (sim_insts) : 100000001  

  mcf  :  
  Commited instructions (system.cpu.committedInsts) : 100000001  
  Executed instructions (sim_insts) : 100000001  

  hmmer :  
  Commited instructions (system.cpu.committedInsts) : 100000000  
  Executed instructions (sim_insts) : 100000000  

  sjeng :  
  Commited instructions (system.cpu.committedInsts) : 100000000  
  Executed instructions (sim_insts) : 100000000  

  libm :  
  Commited instructions (system.cpu.committedInsts) :    
  Executed instructions (sim_insts) :   

  Γιατί τα committed instructions δεν είναι ίσα με τα executed instructions?  

  Δεν φαίνεται διαφορά μεταξύ των commited και executed instructions.  
  Αν επιλέξαμε λάθος μετρική για τα Executed instructions. Θα περιμέναμε τα executed να είναι περισσότερα. Αυτό θα συνέβαινε γιατί ο CPU εκτελεί εντολές με βάση predictions για να γλιτώσει χρόνο, όταν περιμένει για να εκτελέσει άλλες εντολές και στην περίπτωσή που το prediction είναι λάθος, απορίπτει τα αποτελέσματα των εντολών.  


     1.b.  
  bzip :  
  Block replacements l1 data cache (system.cpu.dcache.replacements) : 710569  

  mcf  :  
  Block replacements l1 data cache (system.cpu.dcache.replacements) : 54452  

  hmmer :  
  Block replacements l1 data cache (system.cpu.dcache.replacements) : 65718  

  sjeng :  
  Block replacements l1 data cache (system.cpu.dcache.replacements) : 5262377    

  libm :  
  Block replacements l1 data cache (system.cpu.dcache.replacements) :   


    1.c.  
  bzip :  
  L2 cache acesses (system.l2.overall_accesses::total) : 712341  

  mcf  :  
  L2 cache acesses (system.l2.overall_accesses::total) : 724390 

  hmmer :  
  L2 cache acesses (system.l2.overall_accesses::total) : 70563  

  sjeng :  
  L2 cache acesses (system.l2.overall_accesses::total) : 5264051    

  libm :  
  L2 cache acesses (system.l2.overall_accesses::total) :  1488538

Σε περίπτωση που το gem5 δεν μας έδινε αυτήν
την πληροφορία, πώς θα μπορούσαμε να τα υπολογίσουμε από τα υπόλοιπα metrics του
gem5?  

  ?????? Δεν ξέρω. Αν αθροίσουμε όλα τα άλλα misses της L2;    


    2.(i)  
  bzip :  
  Runtime (sim_seconds) : 0.083982  

  mcf  :  
  Runtime (sim_seconds) : 0.064955  

  hmmer :  
  Runtime (sim_seconds) : 0.059396  

  sjeng :  
  Runtime (sim_seconds) : 0.513528      

  libm :  
  Runtime (sim_seconds) : 0.174671   

    2.(ii)  
  bzip :  
  CPI (system.cpu.cpi) :  1.679650  

  mcf  :  
  CPI (system.cpu.cpi) :  1.299095 

  hmmer :  
  CPI (system.cpu.cpi) : 1.187917  

  sjeng :  
  CPI (system.cpu.cpi) : 10.270554    

  libm :  
  CPI (system.cpu.cpi) : 3.493415   


    2.(iii)   
  bzip :  
  L1D miss rate (system.cpu.dcache.overall_miss_rate::total) : 0.014798  
  L1I miss rate (system.cpu.icache.overall_miss_rate::total) : 0.000077  
  L2 miss rate (system.l2.overall_miss_rate::total ) : 0.282163  

  mcf  :  
  L1D miss rate (system.cpu.dcache.overall_miss_rate::total) : 0.002108  
  L1I miss rate (system.cpu.icache.overall_miss_rate::total) : 0.023612  
  L2 miss rate (system.l2.overall_miss_rate::total ) : 0.055046  

  hmmer :  
  L1D miss rate (system.cpu.dcache.overall_miss_rate::total) : 0.001637 
  L1I miss rate (system.cpu.icache.overall_miss_rate::total) : 0.000221  
  L2 miss rate (system.l2.overall_miss_rate::total ) : 0.077760  

  sjeng :  
  L1D miss rate (system.cpu.dcache.overall_miss_rate::total) : 0.121831  
  L1I miss rate (system.cpu.icache.overall_miss_rate::total) : 0.000020  
  L2 miss rate (system.l2.overall_miss_rate::total ) : 0.999972  

  libm :  
  L1D miss rate (system.cpu.dcache.overall_miss_rate::total) : 0.060972     
  L1I miss rate (system.cpu.icache.overall_miss_rate::total) : 0.000094     
  L2 miss rate (system.l2.overall_miss_rate::total ) : 0.999944    


 Φτιάξτε γραφήματα που να απεικονίζουν αυτές τις πληροφορίες για το σύνολο των benchmarks. Τι παρατηρείτε;  

  Μεγάλα miss rate στις data caches αντιστοιχούν σε μεγάλα CPI και συνεπώς χειότερες επιδόσεις. Τα misses στην L1I δεν φαίνεται να επηρεάζουν ιδιαίτερα το CPI.  

    3. DEFAULT(2 Ghz)  
  bzip :  
  system.clk_domain.clock : 1000  
  cpu_cluster.clk_domain.clock (system.cpu_clk_domain.clock) : 500  
  sim_seconds : 0.064955 

  mcf  :  
  system.clk_domain.clock : 1000  
  cpu_cluster.clk_domain.clock (system.cpu_clk_domain.clock) : 500  
  sim_seconds : 0.059396  

  hmmer :  
  system.clk_domain.clock : 1000  
  cpu_cluster.clk_domain.clock (system.cpu_clk_domain.clock) : 500  
  sim_seconds : 0.059396

  sjeng :  
  system.clk_domain.clock : 1000  
  cpu_cluster.clk_domain.clock (system.cpu_clk_domain.clock) : 500  
  sim_seconds : 0.513528    

  libm :  
  system.clk_domain.clock : 1000  
  cpu_cluster.clk_domain.clock (system.cpu_clk_domain.clock) : 500  
  sim_seconds : 0.17467  

![εικόνα](https://user-images.githubusercontent.com/49563194/146544468-72364f74-1241-46d9-823c-4f06111ceb78.png)  

![εικόνα](https://user-images.githubusercontent.com/49563194/146544494-0772e369-aa40-40a9-9573-d54c69cb9ea4.png)  

![εικόνα](https://user-images.githubusercontent.com/49563194/146544523-d0b620b1-33a5-4988-bcbf-7fca812da306.png)  

![εικόνα](https://user-images.githubusercontent.com/49563194/146544543-06991a88-ef26-4f0c-8547-c9f18dbeb043.png)  

![εικόνα](https://user-images.githubusercontent.com/49563194/146544567-cd70092a-e707-4557-bc82-83eca365cfcc.png)  



      3. 1.5 Ghz  
  bzip :  
  system.clk_domain.clock : 1000  
  cpu_cluster.clk_domain.clock (system.cpu_clk_domain.clock) : 667  
  sim_seconds : 0.109754 

  mcf  :  
  system.clk_domain.clock : 1000  
  cpu_cluster.clk_domain.clock (system.cpu_clk_domain.clock) : 667  
  sim_seconds : 0.086162


  hmmer :  
  system.clk_domain.clock : 1000  
  cpu_cluster.clk_domain.clock (system.cpu_clk_domain.clock) : 667  
  sim_seconds : 0.079149

  sjeng :  
  system.clk_domain.clock : 1000  
  cpu_cluster.clk_domain.clock (system.cpu_clk_domain.clock) : 667  
  sim_seconds : 0.581937    

  libm :  
  system.clk_domain.clock : 1000  
  cpu_cluster.clk_domain.clock (system.cpu_clk_domain.clock) : 667  
  sim_seconds : 0.205034 

  Μπορείτε να εξηγήσετε τελικά τι χρονίζεται στα 1,5GHz και τι χρονίζεται στα default GHz;   
  Το cpu clock, ενώ το system clock μένει σταθερό.  

Αναζητώντας πληροφορίες για το ρολόι, μπορείτε να δώσετε μια πιο σαφή απάντηση;   
???????????Ξερω γω    

Αν προσθέσουμε άλλον έναν επεξεργαστή, ποια εικάζετε ότι θα είναι η συχνότητα του;  
Ίδια με το cpu clock που ορίζουμε  

Υπάρχει τέλειο scaling; Μπορείτε να δώσετε μια εξήγηση αν δεν υπάρχει τέλειο scaling;  
Τα benchmarks bzip, mcf και hmmer που έχουν χαμηλά memory miss rates και συνεπώς CPI ~ 1 κάνουν scale γραμμικά και συνεπώς η μείωση του cpu clock έχει άυξηση χρόνου κατά περίπου το ίδιο ποσοστό.  
Τα benchmark sjeng και libm έχουν υψηλά memory miss rates και συνεπώς CPI πολύ μεγαλύτερα του 1 και συνεπώς η διαφορά στο cpu clock δεν έχει αντίστοιχη ποσοστιακή αύξηση του απαιτούμενου χρόνου. 

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

Σε αυτό το benchmark παρατηρήσαμε σημαντική βελτίωση για Cacheline size 32 και μια περίεργη αύξηση του CPI για associativity 2.  
To CPI μειώθηκε το περισσότερο κατά 0.1 με την αύξηση των μεγεθών των Cache.  

![image](https://user-images.githubusercontent.com/49078291/146428772-0292d177-2da9-42c0-8c0f-0e50724d8790.png)

![image](https://user-images.githubusercontent.com/49078291/146428803-640e9856-dc3b-457e-8202-1281b52fa1ed.png)

![image](https://user-images.githubusercontent.com/49078291/146525614-576ea31d-b3b4-4c85-932f-395c3ae17443.png)

#### SpecSjeng
Αυτό το benchmark έμεινε ανεπηρέαστο μεταβάλλοντας οποιαδήποτε μεταβλητή πέρα του Cacheline Size με την αύξηση του οποίου έπεσαν σημαντικά τα misses της L1 data Cache.

![image](https://user-images.githubusercontent.com/49078291/146428874-9ce0b799-1118-4840-a57b-378ebc1ab623.png)

![image](https://user-images.githubusercontent.com/49078291/146529970-ea2de7cb-c7a5-4a5a-81f6-141457c0f04b.png)


### Βήμα 3ο


