# Fedlex metadata
As of January 2021, the Swiss Federal Chancellery renewed the backend for its official publication (e.g. acts and bills[^1]). 
These are exposed through a triple store database API and then consolidated into objects for efficient, intuitive and significantly less cryptic access.  
This repository contains the consolidated objects of the main works available in JSON format. According to the terminology used by the Federal Chancellery, the work types included in the repository are _Act_, _ConsolidationAbstract_, _TreatyProcess_ and a subset of _Draft_.

[^1]: Diritto federale, Foglio federale, Raccolta Ufficiale, Raccolta Sistematica, Trattati, Procedure di consultazione; Droit fédéral, Feuille fédérale, Recueil officiel, Recueil systématique, Traités, Procédures de consultation; Bundesrecht, Bundesblatt, Amtliche Sammlung, Systematische Rechtssammlung, Staatsverträge, Vernehmlassungen.

- Federal gazette (BBl, FF): ``/eli/fga`` (~146'000 objects[^2]).
- Official compilation (AS, RO, RU): ``/eli/oc`` (~45'000 objects[^2]).
- Classified compilation (SR, RS): ``/eli/cc`` (~17'000 objects).
- Treaties: ``/eli/treaty`` (~18'500 objects).
- Consultation procedures: ``/eli/dl/proj`` (~2'000 objects from 1992). 

Morover, the 40 vocabularies with their entries referred in the objects above are available in the directory ``/vocabularies``. 

[^2]: Some objects correspond to a work exposing multiple manifestations, while others to a single manifestation of a work (e.g Federal gazette before 1999 is presented as one object per language manifestation). The consolidation of works presented in more than one language began in the years 1998-2000 (digitalization of the official publication workflow). 

## Changes with respect to the original data
Data is provided _as is_, objects are updated and committed to this repository several times each day. Files are stored according to their URI's path with the ``.json`` extension.

Although the object structure, quality and conventions may raise some questions, the objects have not been modified, improved or corrected. The only exception is the ``timestampms`` value. This value is updated even when the object is not modified: thus, to avoid unnecessary commits, this field is always set to ``null``. 

JSON objects are prettified in order to take advantage of git to track changes.

## Additional files
- An ``/eli/updates.json`` file is preriodically generated, this include the last crawler update date for each file. 

## Feedbacks
Feedbacks are welcome. For suggestions, missing or incorrect data open an issue.

## Resources
- [www.fedlex.admin.ch](https://www.fedlex.admin.ch), where the data is officialy presented.
- [fedlex.data.admin.ch](https://fedlex.data.admin.ch), the backend public website.

## Licence
Swiss Federal Chancellery requirements for the use of the data are summarized [here](https://www.fedlex.admin.ch/fr/broadcasters). This repository is licensed under the [CC BY-NC-SA 4.0 licence](https://creativecommons.org/licenses/by-nc-sa/4.0/) and cannot be used for commercial purposes. 

Droid Factory.
