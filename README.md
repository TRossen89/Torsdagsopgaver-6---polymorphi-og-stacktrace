### Exercises med nedarvning og stacktrace


## Task 1: 
...
## Task 2: 
...

## Task 3: Nedarving
Her skal vi arbejde med tre klasser hvor de to arver fra den tredje. Vi skal se hvad der sker, når to subklasser (children) implementerer en metode forskelligt og vi skal se hvordan subklasser kan behandles som deres superklasser. 

3.1 Lav en klasse Person, med feltet name. Lav også en konstruktør og relevant getter- og setter-metode. Lav derudover metoden boolean addCourse(String course). Metoden skal ikke gøre noget, så du kan lade den returnere true og ikke gøre andet (en dummy-metode). 

EKSTRA: Den korrekte Java-måde at lave en metode, der ikke gør noget, er dog at gøre den abstract, så det kan du gøre i stedet hvis du vil. Hvis du vælger at lade metoden være abstract, skal du også lade klassen være abstract. En abstract metode har ingen {} men skrives sådan: public abstract boolean addCourse(String course);

3.2: Lav to klasser Student og Teacher, som arver fra Person. Lav konstruktører til klasserne, som kalder Persons konstruktør ved at bruge keywordet super(). 

 <details>
        <summary>
            Hint
 </summary>
         For at se hvordan man kalder en superklasses konstruktør, kan du kigge i Matadors klasse Plot. 
    </details>  

3.3 Lav to ArrayList<String> i Student kaldet passedCourses og currentCourses. Lav to ArrayList<String> i Teacher kaldet canTeach og currentCourses. Lav om i konstruktørerne, så der skal gives en ArrayList af passedCourses eller canTeach med, når objektet oprettes. 

3.4 Override metoden addCourse i Student. Når metoden bliver kaldt, skal du sikre, at kurset ikke ligger i den studerendes passedCourses-ArrayList, da en studerende ikke kan tage kurser, som allerede er bestået én gang. Hvis den studerende ikke tidligere har bestået kurset, lægges det i currentCourses. Lad metoden returnere true eller false alt efter om kurset blev tilføjet til currentCourses.

 <details>
        <summary>Hint </summary>
         Se om ikke ArrayList har en metode, der kan hjælpe dig med opgaven.
           </details> 

3.5 Override metoden addCourse i Teacher. Når metoden bliver kaldt, skal du sikre, at kurset ligger i underviserens canTeach-ArrayList, da underviseren skal være kvalificeret til at undervise for at blive sat på kurset. Hvis underviseren er kvalificeret, lægges kurset i currentCourses. Lad metoden returnere true eller false alt efter om kurset blev tilføjet til currentCourses.

3.6 Lav en klasse Main med en main-metode, hvor du tester Student og Teacher. Du skal oprette et antal studerende og et antal undervisere og give dem ArrayLists af beståede kurser eller canTeach-kurser. Gem alle dine objekter i en ArrayList<Person> persons.

3.7 Kør din persons-liste igennem med en for-løkke og tilføj kurset "Java 1.0" til dem alle (sørg for at nogle af dine studerende allerede har bestået dette og andre ikke har, samt at nogle af underviserne er kvalificerede til at undervise i det og andre ikke er). Hver gang ét af dine kald til addCourse() returnerer false, skal du printe navnet på den studerende eller underviseren. Hvis det er en Student skal du også printe " har allerede bestået dette kursus." og hvis det er en Teacher skal du også printe " kan ikke undervise i dette fag".
 <details>
        <summary>Hint </summary>
        For at finde ud af om der er tale om et Student-objekt eller et Teacher-objekt, skal du bruge instanceof. 
         </details> 