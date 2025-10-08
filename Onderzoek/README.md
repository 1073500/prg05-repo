##06-10-2025
Onderzoeks verslag prg05
DEADLINE: Zo 12 Okt 23:59 WEGING: 30%
Inleveren onder: 1073500_MADYA_DA_SILVA 

Cursushandleiding: https://brightspace.hr.nl/d2l/le/lessons/192850/topics/884621
Onderzoeksverslag toelichting: https://brightspace.hr.nl/d2l/le/lessons/192850/topics/853625

Toelichting:

Lever screenshots als bewijsmateriaal !!!
Laat fouten zien (Ook wanneer de installatie of het project niet gelukt is, verantwoord je de poging d.m.v.
bewijsmateriaal)
Maak vergelijkingen

Inleiding voorbeeld:
Aanpak
Samenvatting
Long list pro's n con's (8 MVC frameworks)
Short list pro's n con's (sl van Lavarel + 2 frameworks, ALLEEN MVC FRAMEWORKS)
< waarom andere frameworks niet gekozen
Persoonlijke ervaring
	Installatie (ook error)
	Leercurve
	Voorkeur en vergelijking
	Ondersteuning (denk aan officiële documentatie, tutorials, een grote of actieve 	community)
	(< op basis van ervaring vergelijk je frameworks)
Startproject
Eindconclusie (+leerdoelen)
--------------------------------------------+

* Verschil tussen een library en framework: 

- vrijheid https://www.freecodecamp.org/news/the-difference-between-a-framework-and-a-library-bd133054023f/,
- pre made structure, https://www.educative.io/blog/difference-between-library-and-framework, -  
- controle flexibiliteit en structure https://zakialawi.com/blog/2024/understanding-the-difference-between-libraries-and-frameworks

Library: bijv jQuery
- Je mag zelf kiezen waar en wanneer je het aanroept.
- The library is added to improve the features of an existing application.
- Meer controle
- Draait niet op zichzelf, set aan functionaliteiten als hulpmiddelen.
- Libraries offer flexibility and modularity, allowing developers to integrate and use them as needed.


Framework: React
- De framework is in controlle en vertelt jou wat je nodig hebt (pre-made structure).
- The framework can be used to create a new application
- Minder controle
- Frameworks offer a structured approach, which can lead to faster development but may limit flexibility.
Systeem dat op zichzelf werkt
-----------------------------------------------------------------------------------------+

* Wat betekent MVC?: Model-View-Controller
https://www.geeksforgeeks.org/software-engineering/mvc-framework-introduction/

Elk component is gebouwd om een specifiek punt van een applicatie te behandelen. Het is een web development framework om scalable en extensible projects te maken en het wordt ook gebruikt om mobile apps te designen. 

Features
Het geeft je de volledige controlle over je html en urls, zo wordt het designen van een web application makkelijker gemaakt. Ook kun je begrijpelijke en zoekbare urls bouwen.

3 componenten
** Model: M Queries, Informatie verwerking
Bewaakt de data uit de database.
Object georiënteerd opgezet, bezie het als classes (model voor bijv. user, classroom etc.)
Hij doet de CRUD


** View: V Form, wat getoond wordt
Dient voor de UI logic van de applicatie
Hoe het eruit ziet, de final render. (telkens update hij de display)
layout, styling


** Controller: C Submit, afhandelen van gebruikersinformatie
Is een intermediaire tussen de model en de views. 
Het vertelt de model wat hij moet doen. 
Hij verwerkt alle logics en request en manipuleert data via de model. 
Met de view rendert hij een een final output.
--------------------------------------------------------------------------+
Les 1 > https://brightspace.hr.nl/d2l/le/lessons/192850/topics/919243

    |
-----
    |
    |
    |

-----------------------------------------------------------------------+
Herhaling:

Functie altijd te herkennen aan: showFunction(,)

--------------------------------------------------------+
Installatie: ! Blijkbaar breeze vergeten

Eerste error, omdat ik dacht dat de tutorial vanaf scatch begon :|
Status: na 2 errors en hulp van Bob gelukt!

View aanmaken: Op string bij return view hoveren en dan in context menu view aanmaken

Controller aanmaken:
1. Open nieuwe terminal
2. Voer deze prompt uit: php artisan make:controller
3. Voer de naam in (Upper CamelCase)
4. Kies Empty controller
5. Open controller in: /app/Https/Controllers/NaamController

	Voorbeeld functie in controller:
<?php
 
namespace App\Http\Controllers;
 
use App\Http\Controllers\Controller;
use Illuminate\Routing\Controllers\HasMiddleware;
use Illuminate\Routing\Controllers\Middleware;
 
class UserController extends Controller implements HasMiddleware
{
    /**
     * Get the middleware that should be assigned to the controller.
     */
    public static function middleware(): array
    {
        return [
            'auth',
            new Middleware('log', only: ['index']),
            new Middleware('subscribed', except: ['store']),
        ];
    }
 
    // ...
}

----------------------------------------------------------------+
Verloop:

Ondezoek Lavarel:
Onderzoek Lavarel was eerst nog onduidelijk, omdat het compleet nieuw voor mij was. 
Alles liep uiteindelijk goed, maar het aanmaken van de controller is nog onduidelijk voor mij.

Onderzoek frameworks:

Ik ga eerst kijken naar 8 mogelijke frameworks om er 6 te laten vallen.
De taal is belangrijk, want ik ben bijvoorbeeld niet bekend met Ruby of Python, dus gaat mijn voorkeur naar frameworks die met js werken.

Mogelijke frameworks: React, Vue, Angular.js, Backbone.js...
*https://astro.deployn.de/blog/comparing-mvc-frameworks/
*https://centralsoft.io/en/blog/posts/what-are-some-of-the-frameworks-that-follow-mvc-architectural-pattern#laravel
*https://squashapps.com/blog/javascript-mvc-frameworks/
*https://acropolium.com/blog/most-popular-backend-frameworks-in-2021-2022-pros-and-cons-what-to-choose/
*https://www.geeksforgeeks.org/blogs/php-frameworks/#cakephp
--------------------------------------------------------------------------------+
Les 2
 -----
|     |
   ---
|
-------
------------------------------------------+
*Longlist: Waarom ...? + pro's en con's

reserve voor longlist: Phalcon, FuelPHP, Symfony

1. CakePHP:
+ heeft SQL injection preventie en CSRF protection.
- Minder flexibel, kan langzaam zijn bij veel inspanning.
2. Spring
+ Weinig tijd nodig
- Java, te complex
3. Ruby on Rails
+ een oke leercurve, oke performance, goed voor web applications en een grote community
- kan langzaam zijn
4. Flask
+ lightweight, makkelijke leercurve, flexibel
- python, kan snel lastig worden, meerdere requests tegelijk kan langzaam zijn.
5. Django
+ lage leercurve dus makkelijk te gebruiken, heeft een build in bescherming tegen sql injections en cross-scripting. 
- kost tijd en je hebt kennis nodig, python
6. ASP.NET
+ snelle app development omdat je minder hoeft te coderen, C# levert een gemakkelijke gebruikers ervaring.
- gebruikt C#, minder controle, licentie kost geld.
7. Express (met Node.js)
+ Makkelijke leercurve vooral als je al met js werkt, high performance, code kan gerunt worden op elke platform.
- Asynchronous programming
8. Nest.js: https://medium.com/@emperorbrains/advantages-and-disadvantages-of-node-js-reasons-to-choose-or-avoid-node-js-ed93cc895b48
+ gebruikt typescript (js), efficient, asynchronous, grote community
- security problemen, errors zijn lastig te debuggen.
9. Codelgniter: https://www.savvyonweb.com/blog/pros-and-cons-of-codeigniter-framework
+ Makkelijke leercurve, geen zware files, built in security features, flexibel, volledig php
- libraries zijn niet zo extended als moderne libraries, het bied alleen simpele features.

Wat valt op?: 


*Shortlist: Waarom ...? + pro's en con's

Laravel:
+ beste backend framework van 2023, gebruikers authenticatie is simpel, API integrations voor mail service, simpele data catching
- heel veel functies zijn lastig, waardoor de leercurve moeilijker wordt.

CakePHP: 
...

Nest.js: 
Codelgniter is snel te leren en niet complex aan de andere kant biedt het weinig dus ben ik benieuwd wat ik allemaal kan met deze framework.

Wat valt op?: 
-------------------------------------------------------------------------------------------+
Verkenning 2 frameworks + laravel
Vertel over installatiegemak, leercurve, gebruikte ondersteuning (documentatie, tutorial, community)

*Laravel

Installatie:

Leercurve:

Ondersteuning:

*CakePHP

Installatie:
De installatie verliep gemakkelijk, vooral door de turtorial. Ook waren de problemen makkelijk op te lossen.

Leercurve: 

Ondersteuning:
> https://www.youtube.com/watch?v=lZweiKSw1cI
Installatie pagina cakephp

----------------+

*Codelgniter

Installatie: 
Over het algemeen verliep de installatie goed. Het was wel een beetje prutsen met de localhost, maar uiteindelijk kwam dat goed.

Leercurve: 

Ondersteuning:
https://www.youtube.com/watch?v=VkMozngSyew
https://www.youtube.com/watch?v=UrVzAp01_3w
ChatGPT
https://codeigniter.com/user_guide/installation/running.html

