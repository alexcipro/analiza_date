# Introducere {.unnumbered}

> "Numerele au fost inventate pentru a măsura grânele și pentru a administra bogățiile regatului."
> --- Mesopotamia antică

> "Datele sunt noul petrol. (en.Data is the new oil.)"
> --- Clive Humby (2006)

> “...acum nu mai e nimic nou de descoperit;\
> tot ce rămâne e doar măsurătoarea din ce în ce mai precisă”
>
> --- Lord Kelvin (1894)

"Cartea tipărită merită răsfoită", spunea Nicoleta Caragea, în anul 2018, unul dintre apreciații profesori și profesioniști statisticieni ai României, în introducerea cărții [Statistica. Concepte, tehnici si instrumente softwaRe](https://www.ujmag.ro/economie/statistica-economica/statistica-concepte-tehnici-si-instrumente-software). Deși internetul ne oferă aproape tot doar la un click distanță, informația fiind disponibilă oricând și oricum, sezația unei cărți tipărite rămâne de neegalat. Dacă lângă carte adăugăm o coală de hârtie și un creion, putem spune că într-adevăr studiem. Și mai mult, dacă adormim în gând cu o problemă de rezolvat și ne trezim plini de speranță că vom găsi rezolvarea, atunci am început activitatea de cercetare științifică.\

Obiectivul principal al cărții pe care o propun este de a fi un ghid cuprinzător, în termeni de concepte și tehnici, reprezentativ și, mai ales, practic, în ceea ce privește utilizarea instrumentelor software de analiză statistică, R fiind principalul software utilizat pentru aplicațiile propuse. Ca abordare generală, cartea prezintă principalele concepte utilizate în statistică, cu exemple și explicații descriptive. Exemplele din viața economică - cele mai multe dintre ele bazate pe date statistice reale - problemele rezolvate, dar și cele propuse, acoperă o arie cuprinzătoare de tematici, cititorul având șansa de a fi introdus în sfera aplicativă a conceptelor teoretice parcurse.\
Cartea este destinată tuturor celor care doresc să înțeleagă, prin mijloace științifice, fenomenele economice și sociale, sub aspectul măsurării cantitative și din perspectiva determinării cauzale. Deși se adresează, în principal, studenților care se pregătesc să devină specialiști în științele economice, lucrarea este utilă și celor care își propun să cunoască un domeniu atât de frumos și de captivant. Tocmai nevoia de informații, din ce în ce mai complexe, dar și posibilitățile de calcul avansat cu ajutorul soft-urilor tot mai performante, au condus la crearea unui bazin imens de date care pot fi cu ușurință exploatate pe baza analizei statistice. Poate că acesta este și motivul pentru care statistica rămâne o disciplină percepută ca fiind adesea prea matematizată, destinată specialiștilor. Pentru mulți cititori, mai ales dintre cei care nu au o formare bazată pe un aparat matematic, studiul fenomenelor economice prin metode statistice și matematice, presupune un efort deosebit. Din acest motiv, am încercat să tratez aspectele teoretice, dar și problemele cu aplicație practică din sfera economică, într-o manieră simplă, accesibilă. Așadar, lucrarea are menirea de a facilita înțelegerea conceptelor fundamentale cu care operează statistica, utilizarea adecvată a metodelor de analiză statistică, precum și interpretarea corectă a rezultatelor, în vederea cunoașterii modului de manifestare a fenomenelor.

\begin{flushright}
Ciprian Alexandru \\
Noiembrie, 2024
\end{flushright}

\newpage

## Quarto {.unnumbered}

Această carte a fost editată cu ajutorul pachetului R **bookdown** [@xie2015].\
Cartea are la bază manualul *Statistică - concepte și metode de analiză a datelor*[@caragea2015].

Pachetul R **bookdown** este integrat R Markdown (http://rmarkdown.rstudio.com). Documentele elaborate pe baza acestui tip de instrumentar de editare sunt pe deplin reproductibile și dau posibilitatea creării unor formate de ieșire diverse (PDF/HTML/Word/...). Informații suplimentare referitoare la utilizarea pachetului **bookdown** se pot găsi la adresa: https://bookdown.org.

\includegraphics[width=0.2\textwidth]{images/logo.png}













## Informații despre software {.unnumbered}

Software-ul \textsf{R} a devenit în prezent unul dintre cele mai utilizate instrumente de analiză statistică, fiind utilizat în statisticile oficiale, în mediile universitare și de cercetare academică, dar și în mediul de afaceri. Acest manual este destinat tuturor celor care doresc să învețe statistica, fiind un material introductiv de studiu, care prezintă un spectru larg de exemple, prezentări grafice și analiză a datelor, dezvoltate cu ajutorul \textsf{R}.\
Aplicațiile din această carte utilizează \textsf{R}, ceea ce înseamnă că pentru reproducerea acestora va fi nevoie de instalarea \textsf{R} pe calculatorul pe care lucrați.\
\textsf{R} este un sistem pentru analize statistice și reprezentare grafică creat de către Ross Ihaka și Robert Gentleman, profesori de statistică la Universitatea Auckland din Noua Zeelandă\footnote{Ihaka R. \& Gentleman R. 1996. R: a language for data analysis and graphics. {\it Journal of Computational and Graphical Statistics} 5: 299--314.}.\
\index{limbajul S}\textsf{R} este considerat un dialect al limbajului \textsf{S} creat de AT&T Bell Laboratories. \textsf{S} este disponibil sub forma software-ului S-PLUS, comercializat de compania Insightful. Există diferențe importante între cele două limbaje, \textsf{R} și \textsf{S}: acestea sunt documentate de către Ihaka & Gentleman (1996) sau se regăsesc în R-FAQ\footnote{\href{http://cran.r-project.org/doc/FAQ/R-FAQ.html\#What-are-the-differences-between-R-and-S_003f}{R-FAQ}}.\
Astfel, numele limbajului R provine de la inițiala prenumelui creatorilor, dar este totodată și un omagiu adus limbajului \textsf{S}.\
În primul rând, \textsf{R} este open-source, fiind distribuit în mod gratuit sub licență \textit{GNU - General Public Licence}\footnote{\href{http://www.gnu.org/}{GNU}}; dezvoltarea și distribuirea sunt în grija câtorva profesori și statisticieni, afiliați companiilor și universităților, cunoscuți sub denumirea generică de \textit{R Development Core Team}.\
Conform filosofiei \textit{GNU}\footnote{\href{http://www.gnu.org/philosophy/free-sw.ro.html\#exportcontrol}{GNU Philosophy}}, software-ul open-source este caracterizat de libertatea acordată utilizatorilor săi de a-l utiliza, copia, distribui, studia, modifica și îmbunătăți. Mai exact, este vorba de patru forme de libertate acordate utilizatorilor[@dusa2015]:

\begin{itemize}
\item Libertatea de a utiliza programul, în orice scop (libertatea 0);
\item Libertatea de a studia modul de funcționare a programului, și de a-l adapta nevoilor proprii (libertatea 1). Accesul la codul-sursă este o precondiție pentru aceasta;
\item Libertatea de a redistribui copii, în scopul ajutorării aproapelui tău (libertatea 2);
\item Libertatea de a îmbunătăți programul, și de a pune îmbunătățirile la dispoziția publicului, în folosul întregii societăți (libertatea 3). Accesul la codul-sursă este o precondiție pentru aceasta.
\end{itemize}

Faptul că este gratuit atrage automat avantajul competitiv în fața altor software-uri de analiză statistică, precum Stata, SAS și SPSS. Astfel, costurile alocate licenței de software dispar. \textsf{R} este denumit de către Norman Nie, unul dintre fondatorii SPSS și CEO al Revolution Analytics, "cel mai puternic și flexibil limbaj de programare statistică din lume" (în engleză \textit{"the most powerful and flexible statistical programming language in the world"}).\footnote{\href{http://blog.revolutionanalytics.com/2010/10/r-is-hot.html}{Smith, D., 2010,"R is Hot", Revolution Analytics}} Dovadă a succesului pe care \textsf{R} îl are în știința datelor, s-au dezvoltat medii de integrare a acestuia în SAS și chiar SPSS. Este vorba despre modulul SAS/IML\footnote{\href{http://www.sas.com/en_us/software/analytics/iml.html\#close}{SAS/IML Module}}, care integrează limbajul \textsf{R} în SAS, și despre \textit{translate2R}, un serviciu de translatare a codului SPSS direct în \textsf{R} dezvoltat de compania \textit{eoda}\footnote{\href{http://www.eoda.de/en/translate2R.html}{translate2R - eoda}}. \textsf{R} are susținerea comunității științifice, dar și a multor companii internaționale. Dintre acestea, menționăm: Google, Facebook, Mozilla, Twitter, The New York Times, The Economist, NewScientist, Lloyd's, Bing, Johnson&Johnson, Pfizer, Shell, Bank of America, Ford.\footnote{\href{http://www.revolutionanalytics.com/what-is-open-source-r/companies-using-r.php}{Revolution Analytics, "Companies Using R"}} \index{open-source}\textsf{R} este susținut și de mediul academic. Marile universități din lume sprijină \textsf{R}, la fel cum sprijină și alte inițiative sau software-uri open-source, precum sistemul de operare Linux sau sistemul de preparare a documentelor \LaTeX.
