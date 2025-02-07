Phrases de passe et bonnes pratiques
####################################

:date: 2015-05-09
:headline: Communiquer de manière chiffrée n'est pas aisée, et nécessite de
           mémoriser des phrases de passes complexes. Comment s'en sortir ?


.. epigraph::

    Au contraire des autres mots de passe, les mots de passe cryptographiques
    ont specifiquement besoin d'être longs et extremement difficiles à deviner.
    La raison est qu'un ordinateur (ou un cluster de plusieurs ordinateurs)
    peut être programmé pour faire des trillions d'essais de manière
    automatique. Si le mot de passe choisi est trop faible ou construit d'une
    manière trop prédictible, cette attaque par la force pourrait se revéler
    fructueuse en essayant toutes les possibilités.

    -- `The Electronic Frontier Foundation
    <https://www.eff.org/wp/defending-privacy-us-border-guide-travelers-carrying-digital-devices>`_ (traduction de mon fait)

Comprendre les concepts et l'écosystème qui permettent d'avoir une vie
numérique chiffrée n'est pas quelque chose d'aisé. `Plusieurs
<https://emailselfdefense.fsf.org/fr/>`_ `guides
<http://www.controle-tes-donnees.net/outils/GnuPG.html>`_ ont été écrits à ce
propos, et pour autant je me rends compte que naïvement il est possible de
mal utiliser les outils existants.

.. epigraph::

    Utilisez un *bon* mot de passe pour votre session utilisateur et une
    *bonne* phrase de passe pour proteger votre clé privée. Cette phrase de
    passe est la partie la plus fragile de tout le système.

    -- La page de manuel de GPG.

Une phrase de passe devrait:

- Être suffisamment longue pour être difficile à deviner;
- Ne pas être une citation connue (littérature, livres sacrés etc);
- Difficile à deviner même pour vos proches;
- Facile à se souvenir et à taper;
- être unique et non partagée entre différents sites / applications etc.

Une des techniques consiste à utiliser des mots du dictionnaire, sélectionnés de
manière aléatoire, puis modifiés.

.. figure:: https://imgs.xkcd.com/comics/password_strength.png

Micah Lee `travaille également sur un outil
<https://github.com/micahflee/passphrases>`_ qui vise à rendre la mémorisation
des phrases de passe plus aisée, de par leur répétition avec des pauses de plus
en plus longues.

.. figure:: {filename}/static/passphrases.png
    :alt: Capture d'écran du logiciel de génération et de mémorisation des
          phrases de passe.

Oui, ce n'est pas aussi simple que ce qu'il y parait. Pour ma part, j'ai une
copie en local de mes clés, dans un fichier chiffré avec une autre clé que j'ai
généré pour l'occasion et que je ne partagerait pas. J'ai par ailleurs
`configuré <https://github.com/jamessan/vim-gnupg>`_ mon éditeur de texte pour
pouvoir chiffrer les documents textes par défaut.

J'ai donc regénéré une nouvelle fois mes clés de travail et personnelles, en
utilisant des phrases de passe plus complexes.

Reste encore la question de la sauvegarde de ces clés privées de manière
chiffrée, que je n'ai pas encore résolue. Bref, tout cela me semble bien
compliqué pour réussir à l'expliquer à des novices, qui pour certains ne sont
même pas sur de l'intérêt de la chose.
