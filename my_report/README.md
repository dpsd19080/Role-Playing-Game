# Lesson: Digital & Serious Games

### First and Last Name: Ανδρέας Μπιρμπίλης | Andreas Birmpilis
### University Registration Number: dpsd19080
### GitHub Personal Profile: [URL](https://github.com/dpsd19080)
### Digital & Serious Games Personal Repository: [URL](https://github.com/dpsd19080/Role-Playing-Game)

# Introduction
Στα πλαίσια του μαθήματος "Ψηφιακά Παιχνίδια και Παιγνιώδης Μάθηση" καλούμε να υλοποιήσω μια ατομική εργασία με θέμα την δημιουργία ενός 2D RPG video game (ελεύθερης θεματολογίας), η οποία αντιστοιχεί στο 60% του τελικού μου βαθμού.
# Summary
Η ατομική εργασία χωρίζεται σε τρία παραδοτέα: 
#### [1st Deliverable](https://github.com/dpsd19080/Role-Playing-Game/tree/main/my_report#1st-deliverable):
#### [2st Deliverable](https://github.com/dpsd19080/Role-Playing-Game/tree/main/my_report#2nd-deliverable):
#### [3st Deliverable](https://github.com/dpsd19080/Role-Playing-Game/tree/main/my_report#3nd-deliverable):

# 1st Deliverable
Ξεκίνησα την εργασία ακολουθώντας τις οδηγίες που μας δόθηκαν για το πρώτο [παραδοτέο](https://github.com/merkourisa/Role-Playing-Game/issues/1). Όταν ξεκίνησα να υλοποιώ τις οδηγίες για το [World Design - Tilemaps](https://learn.unity.com/tutorial/world-design-tilemaps?uv=2020.3&projectId=5c6166dbedbc2a0021b1bc7c) αντιμετώποισα πρόβλημα επειδή οι οδηγίες ήταν outdated, πιο συγκεκριμένα έχει αλλάξει ο τρόπως δημιουργίας των Tilemaps. Παρ ολ' αυτά, με μια γρήγορη αναζήτηση στο YouTube βρήκα αύτο το [βίντεο](https://www.youtube.com/watch?v=DTp5zi8_u1U) που μου έλυσε το πρόβλημα! Ένα επιπλέον πρόβλημα που δημιουργήθηκε ακολουθώντας τις οδηγίες για το [Decorating the World](https://learn.unity.com/tutorial/decorating-the-world?uv=2020.3&projectId=5c6166dbedbc2a0021b1bc7c#) ήταν πως στο βήμα 3 μου ζήταγε να ορίσω τις εξής Transparency Sort Axis συντεταγμένες: 
- x = 0
- y = 1
- z = 0 

Όταν το έκανα έτσι γινόταν αυτό:

![Alt Text](https://github.com/dpsd19080/Role-Playing-Game/blob/main/my_report/problem1.gif)

Αυτό επιλύθηκε απλά ορίζοντα τις συντεταγμένες έτσι:
- x = 0
- y = 0
- z = 1


Αφού ολοκλήρωσα το πρώτο παραδοτέο μια φόρα με τα assets του [Ruby's Adventure](https://assetstore.unity.com/packages/templates/tutorials/2d-beginner-tutorial-resources-140167) για να καταλάβω την λογική, ξανά έκανα όλη την διαδικασία με τα εξής assets: 
- [Spider-Man Sheets](https://gr.pinterest.com/pin/298504281561510034/)
- [City Tilemaps](https://www.artstation.com/marketplace/p/yr9p8/city-tileset-pack)
- [Crates](https://www.istockphoto.com/vector/pixelated-wooden-box-set-pixel-art-isometric-projection-3d-vector-illustration-gm1210024697-350374351)

Το τελικό αποτέλεσμα πλέον μετά το Bulid and Run είναι αυτό: 

![Alt Text](https://github.com/dpsd19080/Role-Playing-Game/blob/main/my_report/deliverable_1_final.gif)

#### Extra προσθήκες που δεν ήταν υποχρεωτικές ακόμα: 
- Προσθήκη Public float speed, με σκοπό να μπορώ να αλλάζω την ταχύτητα ανά πάσα στιγμή, χωρίς να χρειάζεται συνεχής επεξεργασία του script αρχείου για τον χειρισμό του Spider-Man.
![ScreenShot](public_float_speed.jpg)
 
- Προσθήκη walking animations στον Spider-Man 

![Alt Text](https://github.com/dpsd19080/Role-Playing-Game/blob/main/my_report/walking_animation.gif)

# 2nd Deliverable
Σε αυτό το παραδοτέο τα πράγματα πήραν μια πιο ενδιαφέρουσα τροπή.

Πρώτη μου δουλειά (με βάση τις [οδηγίες](https://learn.unity.com/tutorial/world-interactions-blocking-movement?uv=2020.3&projectId=5c6166dbedbc2a0021b1bc7c)) ήταν να διορθώσω το γεγονός ότι ο Spider-Man πέρναγε πάνω από τα boxes στο περιβάλλον αντί να συγκρούεται με αυτά. Αυτό επιτυγχάνεται με την βοήθεια των Colliders.
Κατ ουσίαν, έπρεπε να προσθέσω ένα box collider 2D στον χαρακτήρα μου και αντίστοιχα ένα στο αντικείμενο με το οποίο θέλω να συγκρούεται (στην συγκεκριμένη περίπτωση τα boxes)
![Alt Text](https://github.com/dpsd19080/Role-Playing-Game/blob/main/my_report/box_collider.gif)

Επιπλέον, πρόσθεσα ένα Rigidbody 2D στον Spidey έτσι ώστε να συμπεριφέρεται με βάση την φυσική. Ομως, απενεργοποιώ την βαρύτητα του γιατί δεν θέλω να πέφτει κάτω μιας και το παιχνίδι μου θέλω να είναι Top-Down. ![ScreenShot](Spidey's_Rigidbody.jpg)

Αμέσως μετά τοποθέτησα ένα box collider 2D και στο Tilemap με σκοπό να ορίσω τα όρια που θα μπορεί να κινείται ο Spider-Man.
![Alt Text](https://github.com/dpsd19080/Role-Playing-Game/blob/main/my_report/map_boundaries.gif)

Στην συνέχεια μου ζητήθηκε (από την εκφώνηση του δεύτερου [παραδοτέου](https://github.com/merkourisa/Role-Playing-Game/issues/2)) να φτιάξω Health Collectables τα οποία θα μπορεί να συλλέγει ο χαρακτήρας μου κάθε φορά που "δέχεται" κάποιο damage.
Αρχικά, με την βοήθεια του [World Interactions - Collectibles](https://learn.unity.com/tutorial/world-interactions-collectibles?uv=2020.3&projectId=5c6166dbedbc2a0021b1bc7c) συμπλήρωσα το C# Script "SpiderManController" με στόχο να ορίσω κάποιο Health Stat στον Spider-Man.
![ScreenShot](health_stat1_fixed.jpg)
![ScreenShot](health_stat2_fixed.jpg)
![ScreenShot](health_stat3.jpg)

#### Πολύ συνοπτικά, ορίζω μια μεταβλητή int με όνομα maxHealth η οποία αντιστοιχεί στην αρχική και μέγιστη ζωή του χαρακτήρα. Αμέσως μετά, ορίζω μια int currentHealth η οποία θα μου επιστρέφει πάντα την τιμή που αντιστοιχεί στην ζωή που έχει ο χαρακτήρας κάθε στιγμή του παιχνιδιού. Όταν ξεκινάει το παιχνίδι, προφανώς η currentHealth είναι ίση με την maxHealth μιας και ο Spider-Man δεν θα έχει δεχθεί κανένα damage κατά την έναρξη του παιχνιδιού. Επιπλέον, έχει δημιουργηθεί μια συνάρτηση ChangeHealth η οποία υπολογίζει συνέχεια την τιμή της currentHealth και την εμφανίζει στο Console.

Έπειτα, βρήκα και τοποθέτησα στα sprites μου το εξής asset για Health Collectable: [Pizza](https://weheartit.com/entry/103348799) 

Του βάζω ένα box collider 2D αλλά αυτή την φορά με την διαφορά ότι "κλικαρω" την επιλογή is Trigger γιατί στην συγκεκριμένη περίπτωση δεν θέλω ο χαρακτήρας να συγκρούεται με το αντικείμενο αλλά κάθε φορά που περνάει από πάνω του να γίνεται Trigger κάποια ενέργεια που θέλω. Ο σκοπό μου είναι κάθε φορά που έχει χάσει ζωή και περνάει από πάνω του να το "μαζεύει" κια να του συμπληρώνετε μια μονάδα ζωής.
Για να το πετύχω αυτό, δημιουργώ ένα ακόμα C# Script με όνομα HealthCollectible:
![ScreenShot](healthcollectible_script.jpg)

#### Πολύ συνοπτικά, κάθε φορά που η τρέχουσα ζωή του Spider-Man είναι μικρότερη από την μέγιστη ζωή του, τότε απλά αυξάνει την ζωή κατά 1 και καταστρέφει το object του HealthCollectible.

Όμως, για να δουλέψει όντως αυτό πρέπει να κάνω define κάποιο property στο C# Script του Spider-Man, δηλαδή στο SpiderManController και μετά χρησιμοποιώ αυτό το property στο HealthCollectible.
![ScreenShot](spidermancontroller_property1.jpg)
![ScreenShot](spidermancontroller_property2.jpg)

Κλείνοντας, έκανα prefab το asset Health Collectible έτσι ώστε να μπορώ να το ξανατοποθετήσω στο map όσες φορές θέλω χωρίς να χρειαστεί να το "σετάρω" ξανά και ξανά.

Στη συνέχεια, αφού έχω φτιάξει Health Collectible και έχω ορίσει ζωή στον πρωταγωνιστή μου, ήρθε η ώρα να φτιάξω περιοχές και εχθρούς που θα προκαλούν damage.

Πρώτη κίνηση, δημιουργία νέου C# Script με όνομα DamageZone. Δηλαδή, δημιουργία του κώδικα που θα αφαιρεί 1 πόντο από την ζωή του χαρακτήρα.
![ScreenShot](damagezone_script.jpg)
Όπως και στο asset για το health έτσι και εδώ, προσθέτουμε box collider 2D με επιλεγμένο το is Trigger. Οι διαφορές όμως στην συγκεκριμένη περίπτωση είναι: 
- Πως δεν θέλουμε να εξαφανίζεται το object (γι' αυτό λείπει και από τον κώδικα η εντολή "Destroy(game.Object);")
- Στο Rigidbody 2D που προσθέσαμε κατά την διάρκεια του tutorial, ορίζουμε το sleeping mode σε never sleep για να βεβαιωθούμε πως ο πρωταγωνιστής μας θα δέχεται ζημιά και όταν κάθεται ακίνητος στο damage zone.

Επειτα, κατά την υλοποίηση παρατήρησα πως ο Spider-Man χάνει με την μια όλες τις ζωές του. Για να το φτιάξω αυτό τροποποίησα τον κώδικα του SpiderManController ως εξής:
![ScreenShot](damage_fix1.jpg)
![ScreenShot](damage_fix3.jpg)
![ScreenShot](damage_fix2.jpg)

Για να ολοκληρώσω τα damage zones έμενε πλέον μονάχα να βάλω ένα στο map να του προσθέσω το DamageZone Script και να το κάνω prefab.

#### Σημείωση: Tο asset του DamageZone: [Broken Glass Pixel Art](https://www.pngkey.com/detail/u2y3q8w7w7i1i1e6_820-x-400-4-broken-glass-pixel-art/)

Επόμενη κίνηση, προσθήκη των εχθρών. 
Παρόμοια λογική και εδώ όπως και με τα προηγούμενα, δημιουργία EnemyController Script και προσθήκη αυτού, προσθήκη Rigidbody 2D και box collider 2D.
Σε αυτή την φάση το EnemyController Script ήταν κάπως έτσι:
![ScreenShot](enemycontroller_script1.jpg)
![ScreenShot](enemycontroller_script2.jpg)
![ScreenShot](enemycontroller_script3.jpg)
Απλά ορίζεται μια ταχύτητα και κατ ουσίαν ακολουθεί μια κατεύθυνση αριστερά και δεξιά ή πάνω και κάτω. 

Τέλος, για προκαλούν και οι εχθροί damage όταν τους ακουμπάει ο πρωταγωνιστής απλώς πρόσθεσα τον παρακάτω κώδικα στο script των εχθρών μου:
![ScreenShot](enemycontroller_script4.jpg)

#### Σημείωση: Τα assets των εχθρών: [Enemy 1 Sheets](https://twitter.com/creeperofsteam/status/1505997629817331716), [Enemy 2 Sheets](https://www.mediafire.com/convkey/0455/2ojme8ya5fmg7ypzg.jpg?size_id=5)

Επόμενο βήμα, βήμα σιδηρόδρομος, τα Animations. Βήμα εξερετικά απαραίτητο για κάθε game μιας και του δίνει ζωντάνια, χωρίς αυτό το παιχνίδι θα έδειχνε άδειο και αχανές.
Για να μην χαθώ, ακολούθησα κατά γράμμα τις οδηγίες που μας δόθηκαν δόθηκαν για τα [Sprite Animations](https://learn.unity.com/tutorial/sprite-animation?uv=2020.3&projectId=5c6166dbedbc2a0021b1bc7c#). 

Ξεκίνησα (όπως και στο tutorial) με την εξής σειρά:
- Προσθήκη Animator στους εχθρούς μου 
- Δημιουργία Walking (Right and Left) και Death ("Fixed" στο tutorial) animations για τον πρώτο εχθρό.
![Alt Text](https://github.com/dpsd19080/Role-Playing-Game/blob/main/my_report/enemy1_animations.gif)
- Δημιουργία Walking (Up and Down) και Death ("Fixed" στο tutorial) animations για τον δεύτερο εχθρό.
(Προσθήκη gif)
- Δημιουργία Blend Tree 
(Προσθήκη gif)
#### Σημείωση 1: Όπως φάνηκε, δημιούργησα και επεξεργάστικα ένα κοινό Blend Tree και για τους δύο εχθρούς και όχι δύο διαφορετικά. Η αρχική μου προσέγγιση ήταν ο κάθε ένας να έχει το δικό του αλλά υπήρχαν μικροπροβλήματα όπως να μην αλλάζει από WalkingRight σε WalkingLeft. Οπότε σκέφτηκα πως, αφού στο tutorial τα robots θα έκαναν μόνο οριζόντια ή κάθετη κίνηση ανάλογα με τον αν θα έχεις "τσεκαρισμένο" το Vertical στον Inspecot στο κομμάτι που αφορά το EnemyController Script, θα μπορούσα απλά να βάλω στον ένα άξονα τον πρώτο εχθρό και στον άλλον τον δεύτερο(ούτως ή άλλως, σκόπευα να έχουν στον έναν μόνο άξονα κίνηση ο κάθε ένας εχθρός).


#### Σημείωση 2: Η εμπειρία, μου έδειξε πως αν γίνει το παραμικρό λάθος σε οποιαδήποτε στάδιο του Blend Tree απλά όλα τα animation σχεδόν γίνονται προβληματικά ή μπερδεμένα.


- Προσθήκη των εξής εντολών στο EnemyController Script:
![ScreenShot](enemycontroller_animator1.jpg)
![ScreenShot](enemycontroller_animator2.jpg)
Σκοπός είναι να καλέσω των Animator έτσι ώστε κάθε φορά που θα περνάει ένα χρονικό διάστημα και θα έχει διανύσει μια απόσταση να αλλάζει κατεύθυνση και να αλλάζει μαζί και το animation.
- Δημιουργία Idle, Walking (Left and Right), Hit και Launch (θα χρειαστούν για τα projectiles, θα εξηγηθεί αργότερα) animations
(Προσθήκη gif)
- Δημιουργία τεσσάρων Blend Tree (Idle, Walking, Hit, Launch) για την διαχείριση των animations του Spider-Man 
(Προσθήκη gif)
- Προσθήκη των εξής εντολών στο SpiderManController Script:
![ScreenShot](spideycontroller_animator1.jpg)
![ScreenShot](spideycontroller_animator2.jpg)

Πλέον, μετά από όλα αυτά τα βήματα, τα animations του χαρακτήρας και των εχθρών μου αλλάζουν όποτε πρέπει και σωστά

Προτελευταία απαίτηση ηταν ο χαρακτήρας μου να "πετάει" σφαίρες οι οποίες θα προκαλούν Damage στους εχθρούς. Μιας και ο πρωταγωνιστής μου είναι ο Spider-Man, σαν σφαίρες έφτιαξα στο photoshop ιστούς.
Ξεκίνησα να προσεγγίζω το θέμα ως εξής. Αρχικά, πρόσθεσα το spite μου στο map προσωρινά για να του βάλω Rigidbody 2D και box collider 2D. Έπειτα, συμβουλεύτικα κάποιες ρυθμίσεις από το tutorial που μας είχε υποδεχθεί. Μετά, δημιούργησα ξανά ένα νέο C# Script με όνομα Projectile:
![ScreenShot](projectile.jpg)
Κάπου εδώ πρόσθεσα στον κώδικα του SpiderManController, την εντολή "animator.SetTrigger("Launch");" με σκοπό να αξιοποίησω το animation που ανέφερα πριν. 
![ScreenShot](launch2.jpg)
Τώρα, το μόνο που έλειπε ήταν να ορίσω ένα κουμπί στο Script και να καλέσω την Launch(); με στόχο να εκτοξεύει το projectile και να παίζει το animation:
![ScreenShot](launch1.jpg)
Όμως, δεν είχα τελειώσει ακόμη. Υπήρχαν δύο πρόβλημα που έπρεπε να λύσω ακόμα:
- Το projectile παρότι είχε force και direction έμενε ακίνητο. Αυτό το έλυσα αλλάζοντας την Void start() σε void Awake() στο Projectile Script 
- To projectile έκανε collide με τον χαρακτήρα. Αυτό λύθηκε ορίζοντας "Character" και "Projectile" layers από πάνω δεξιά στον Inspector (προσθέτοντας νέα layers μέσω του layer manager) και πηγαίνοντας στα Project Setting > Physics 2d και κάνοντας uncheck το intersection ανάμεσα σε Character και Projectile.
Τελειώνοντας, έμενε μονάχα να "σκοτώνω" τους εχθρούς όταν τους βρίσκει το projectile και να παίζει το Death animation. 
Αυτό το κατάφερα προσθέτοντας τις έξεις εντολές στα EnemyController και Projectile Scripts αντίστοιχα:
![ScreenShot](enemy_death1.jpg)
![ScreenShot](enemy_death2.jpg)
![ScreenShot](enemy_death3.jpg)
![ScreenShot](enemy_death4.jpg)

Τέλος, για να ολοκληρωθεί το παραδοτέο έμενε να "φτιάξω" την κάμερα με τέτοιο τρόπο έτσι ώστε να έχει σαν επίκεντρο και να ακολουθεί τον πρωταγωνιστή μου.

Ξεκίνησα κάνοντας εγκατάσταση μέσα από το unity το Cinemachina. Έπειτα έμενε απλά να το ρυθμίσω με βάση τις οδηγίες και να το βάλω να ακολουθεί τον Spider-Man. 
(Προσθήκη εικόνας και gif)

![ScreenShot](cam_follow.jpg)
Το τελικό αποτέλεσμα πλέον μετά το Bulid and Run είναι αυτό: 
(Προσθήκη gif)
# 3rd Deliverable 


# Conclusions


# Sources
#### 1st Deliverable:
- [Get started with Ruby’s Adventure](https://learn.unity.com/tutorial/main-character-and-first-script?uv=2020.3&projectId=5c6166dbedbc2a0021b1bc7c)
- [Character Controller and Keyboard Input](https://learn.unity.com/tutorial/character-controller-and-keyboard-input?uv=2020.3&projectId=5c6166dbedbc2a0021b1bc7c)
- [World Design - Tilemaps](https://learn.unity.com/tutorial/world-design-tilemaps?uv=2020.3&projectId=5c6166dbedbc2a0021b1bc7c)
- [Decorating the World](https://learn.unity.com/tutorial/decorating-the-world?uv=2020.3&projectId=5c6166dbedbc2a0021b1bc7c)
- [Creating Tilemaps For Your 2D Game in Unity 2021 - Tutorial](https://www.youtube.com/watch?v=DTp5zi8_u1U)
- [Ruby's Adventure](https://assetstore.unity.com/packages/templates/tutorials/2d-beginner-tutorial-resources-140167)
- [Spider-Man Sheets](https://gr.pinterest.com/pin/298504281561510034/)
- [City Tilemaps](https://www.artstation.com/marketplace/p/yr9p8/city-tileset-pack)
- [Crates](https://www.istockphoto.com/vector/pixelated-wooden-box-set-pixel-art-isometric-projection-3d-vector-illustration-gm1210024697-350374351)
