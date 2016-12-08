##Différents types de pages :

  * page en markdown avec un layout

##Layout :

  * default :

   * nav_bar.html
   * footer.html   


##Architecture du site :

  * page d'accueil : index.html = carousel + welcome (= petit texte + icones)
  * page About : about/index.html
  * page People : people/index.html 
  * page Projects : projects/index.html
  * pages projets individuels : projects/sobums.md
  * page Code : code.md
  * page Data : data.md
  * page Publications : publications/index.html
  * page Job Offers : jobs.md
  * page News : blog/index.html
  * page Contact : contact/index.html
  * pages scientifiques :
    * unravel.md
    * forecast.md
    * climate.md
    

##Rajouter une image dans le carousel :

  * dans _includes/carousel.html :  rajouter ou modifier le nombre d'images


<pre><code>    <li data-target="#carousel-generic" data-slide-to="4"></li> </code></pre>

  * dans _data/carousel.yml : rajouter un paragraphe 


    - title :
      pic : assets/img/carousel/chaos3.png
      picg : assets/img/carousel/chaos3g.png
      picm : assets/img/carousel/chaos3m.png
      pics : assets/img/carousel/chaos3s.png
      text : Quantifying chaos and uncertainties in the ocean evolution
      link : forecast
      colorf : black
      colorb : white

dans lequel il faut donner le nom des 4 images (tailles 2052x340, 1000x340, 500x340, 250x340) , le texte, un lien sous le "Read more", la couleur du texte et la couleur en fond du texte.

  - dans assets/img/carousel : déposer les images 

##Rajouter une personne dans la page people :

 * si membre permanent :

    - dans _data/group.yml : rajouter un paragraphe

"- name : Thierry Penduff
  title : Head of the Team
  email : penduff.png
  image_nb : Penduff_nb.jpg
  image_color : Penduff_color.jpg
  post : Researcher (CNRS)
  website : http://lgge.osug.fr/personnels/penduff_thierry/FRANCAIS/
  phone : +33 (0) 4 76 82 86 54"

dans lequel on indique le nom, si besoin le titre, le nom de l'image qui montre l'adresse mail (à générer avec script email2gif), le nom des photos n&b et couleur, le poste, si besoin l'adresse du site web perso et le numero de téléphone.

     - dans assets/img/people : deposer les photos et l'image de l'adresse mail

  * si membre non-permanent : mêmes manips mais dans le fichier _data/nonperm.yml


##Rajouter un projet dans la liste des projets :

  - dans _data/projects.yml : rajouter un paragraphe

"- title : AtlantOS
  image :
  date : 2015-2019
  text : The vision of AtlantOS is to improve and innovate Atlantic observing by using the Framework of Ocean Observing to obtain an international, more sustainable, more efficient, more integrated, and fit-for-purpose system. Hence, the AtlantOS initiative will have a long-lasting and sustainable contribution to the societal, economic and scientific benefit arising from this integrated approach. This will be achieved by improving the value for money, extent, completeness, quality and ease of access to Atlantic Ocean data required by industries, product supplying agencies, scientist and citizens.
  link : https://www.atlantos-h2020.eu/
  ancre : atlantos"

dans lequel on indique le titre du projet, si besoin le nom d'une image, les dates du projet, un texte descriptif, un lien et un mot-clé pour désigner le projet (permet de naviguer à l'intérieur de la page)

  - dans _includes/navbar.html : rajouter une ligne

"<li><a href="{{site.baseurl}}/projects/nouveau_projet" class={{researchDropdownClass}}>Nouveau Projet</a></li>"

permet d'accéder à la page du projet, ou rajouter la ligne

"<li><a href="{{site.baseurl}}/projects#ancre" class={{researchDropdownClass}}>Nouveau Projet</a></li>"

pour accéder dans la page all projects au paragraphe correspondant au nouveau projet.

##Créer une page projet indépendante (type page SOBUMS) :

  - dans le dossier projects, rajouter un document markdown :

"
---
layout: pagemd
title: SOBUMS
permalink: /projects/sobums/
---

The Southern Ocean (oceans south of 30°S) plays a key role in global biogeochemical cycles. But large environmental changes are ongoing in the Southern Ocean physical and biogeochemical properties. These changes reflect widespread environmental changes that are occurring throughout the southern hemisphere and over the Southern Ocean (changes in surface winds, solar radiation, sea ice cover and glacial melt from Antarctica). How the Southern Ocean primary production and carbon cycle will respond to these changing climate stressors is a matter of concern in the climate science community.


<img class="img-responsive img-centered" src="https://meom-group.github.io/assets/img/projects/sobums-meijers.png" alt="A changing Southern Ocean."/> "

en indiquant le titre du projet, l'adresse de la page et le texte en markdown.

##Rajouter une offre d'emploi :

  - dans jobs.md, ajouter un paragraphe du type :

"### PhD grants

 - [Stochastic variability of oceanic water masses](http://www.adum.fr/as/ed/voirproposition.pl?langue=fr&site=edtue&matricule_prop=11736);  contact : Thierry Penduff."


##Rajouter une news :

  - dans le dossier _posts, créer un fichier dans le nom commence par la date : year-month-day-title-of-the-news.md et le remplir comme suit : 

"---
title: New MEOM website !
featured:
layout: page
link:
---

We are proud to open our new public website today.

Thank to all the team members that contributed to this effort !"


en indiquant le titre de la news, une éventuelle image, un éventuel lien et le texte en syntaxe markdown

