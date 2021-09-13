# ![left 100%](https://raw.githubusercontent.com/thierry-laval/archives/master/images/logo-portfolio.png)

## Auteur

👤**Thierry LAVAL** [🇫🇷 Contactez moi 🇬🇧](<contact@thierrylaval.dev>)

* Github: [@Thierry Laval](https://github.com/thierry-laval)
* LinkedIn: [@Thierry Laval](https://www.linkedin.com/in/thierry-laval)

***

### 📎 Projet 19 - Paramètrage de [Firefox développeur](https://www.mozilla.org/fr/firefox/developer/)

![left 100%](firefox.png?raw=true)

_`Début du projet le 20/05/2021`_

Liste des paramètres à modifier dans le menu de Firefox :  about:config

***

### Paramètrage automatique

Le fichier `user.js`, fournis dans l'archive, est un profil pour Mozilla Firefox basé sur les paramètres de PrivacyTools afin d'améliorer la vie privée et la confidentialité sur Internet.

Attention le profil actuel va être supprimé, n'oubliez pas de sauvegarder vos données, telles que les marque-pages, mots de passe, etc.

- Ouvrez Firefox et tapez about:profiles dans la barre d'adresse.
- Une fois sur la page, cliquez sur Créer un nouveau profil.
- Dès que le nouveau profil est créé, cliquez sur Ouvrir le répertoire dans Répertoire racine du nouveau profil.
- Déplacez le fichier user.js dans ce répertoire et cliquez sur Lancer le profil dans un nouveau navigateur.
- Fermez l'ancien navigateur et le répertoire, tapez about:profiles et une fois sur la page, cliquez sur Supprimer.
- Ça y est, votre profil est configuré et vous êtes mieux protégé sur Internet !

***

### Paramètrage manuel


#### Vie privée et sécurité

##### Désactiver le Safe Browsing

| Attribut | Valeur | Description |
| :-: | :-: | --- |
| `browser.safebrowsing.malware.enabled`          | **false** | Désactive le safebrowsing, fourni par Google.   |
| `browser.safebrowsing.phishing.enabled`         | **false** | Désactive le safebrowsing.                      |
| `browser.safebrowsing.blockedURIs.enabled`         | **false** | Désactive le safebrowsing.                      |
| `browser.safebrowsing.downloads.remote.enabled` | **false** | Désactive la mise à jour des listes de blocage. |
| `browser.safebrowsing.provider.google.updateURL` | **blanc** | Désactive la mise à jour des listes de blocage. |
| `browser.safebrowsing.provider.google4.updateURL` | **blanc** | Désactive la mise à jour des listes de blocage. |
| `browser.safebrowsing.provider.google4.dataSharingURL` | **blanc** | Désactive le partage de données. |
| `browser.safebrowsing.provider.google4.gethashURL` | **blanc** | Désactive le partage de données. |

##### Gestion du referer

| Attribut | Valeur | Description |
| :-: | :-: | --- |
| `network.http.referer.spoofSource`           | **true** | Envoie comme referer le site que vous visitez, si vous visitez mozilla.org, Firefox enverra comme referer mozilla.org. |

##### Désactiver le préchargement

| Attribut | Valeur | Description |
| :-: | :-: | --- |
| `network.dns.disablePrefetch`               | **true**  | Désactive le préchargement DNS des liens, si vous avez confiance en votre serveur DNS ne désactivez pas cette option utile à l'amélioration des performances. |
| `network.prefetch-next`                     | **false** | Désactive le préchargement des pages. |
| `browser.urlbar.speculativeConnect.enabled` | **false** | Désactive le préchargement dans la barre "intelligente" de Firefox. |
| `network.http.speculative-parallel-limit`   | **0**     | Désactive le préchargement. |

##### Désactiver la télémétrie

Tapez `telemetry` dans la barre de recherche, supprimez tous les liens et passez tout à `false`.

| Attribut | Valeur | Description |
| :-: | :-: | --- |
| `toolkit.telemetry.enabled` | **false** | Désactive la télémétrie. |
| `toolkit.telemetry.server` | **blanc** | Désactive la télémétrie. |
| `dom.ipc.plugins.flash.subprocess.crashreporter.enabled` | **false** | Désactive la télémétrie. |
| `app.normandy.enabled`                                   | **false** | Désactive la télémétrie. |
| `app.normandy.first_run`                                 | **false** | Désactive la télémétrie. |
| `app.normandy.api_url`                                   | **blanc** | Désactive la télémétrie. |
| `beacon.enabled`                                         | **false** | Désactive la télémétrie. |

##### Désactiver la géolocalisation

| Attribut | Valeur | Description |
| :-: | :-: | --- |
| `geo.enabled`              | **false** | Désactive la géolocalisation. |
| `geo.wifi.uri`             | **blanc** | Désactive la géolocalisation via énumération des points Wi-Fi. |
| `geo.provider.network.url` | **blanc** | Désactive la géolocalisation. |

##### Désactiver les notifications push

Les notifications push permettent aux sites de vous envoyer des notifications même s'ils ne sont pas ouverts, si vous les y autorisez. Pour ce faire Mozilla utilise ses serveurs. Cela peut poser des problèmes de confidentialité.

| Attribut | Valeur |
| :-: | :-: |
| `dom.push.connection.enabled` | **false** |
| `dom.push.enabled`            | **false** |
| `dom.push.serverURL`          | **blanc**  |

#### Autres

| Attribut | Valeur | Description |
| :-: | :-: | --- |
| `security.OCSP.enabled` | **0** | Désactive l'[OCSP](https://fr.wikipedia.org/wiki/Online_Certificate_Status_Protocol). |
| `browser.cache.offline.enable` | **false** | Désactive le cache hors-ligne, c'est pas terrible d'autoriser les sites à enregistrer tout et n'importe quoi sur votre ordi. |
| `browser.cache.offline.capacity` | **0** | Désactive le cache hors-ligne. |
| `extensions.pocket.enabled` | **false** | Désactive pocket. Si vous ne vous en servez pas autant le désactiver. |
| `extensions.pocket.api` | **blanc** | Désactive pocket.
| `extensions.pocket.site` | **blanc** | Désactive pocket. |
| `browser.send_pings` | **false** | Désactive le pistage des cliques. |
| `browser.send_pings.max_per_link` | **0** | Autorise 0 envoie de notification lors d'un clic sur la page. |
| `dom.battery.enabled` | **false** | Empêche les sites de voir l'état de votre batterie. |
| `dom.event.clipboardevents.enabled` | **false** | Empêche les sites de savoir lorsque vous coper un élément dans le presse-papier. |
| `media.navigator.enabled`| **false** | Empêche les sites de pister l'état du micro et de la caméra. |
| `webgl.disabled` | **true** | WebGL pourrait être source de problèmes de sécurité. Peut casser certains sites. |
| `network.captive-portal-service.enabled` | **false** | Désactive la recherche de portail captif. C'est utilisé notamment pour se connecter aux réseaux Wi-Fi publics. |
| `captivedetect.canonicalURL` | **blanc** | Désactive la recherche de portails captifs. |
| `layout.css.visited_links_enabled` | **false** |[Trop long à expliquer](https://hacks.mozilla.org/2010/03/privacy-related-changes-coming-to-css-vistited/).|
| `device.sensors.enabled` | **false** | |
| `browser.newtabpage.activity-stream.feeds.snippets` | **false** | Désactive l'affichage des snippets, ou "brèves" en Français, de Mozilla. Firefox contacte les serveurs de Mozilla pour les afficher. |
| `privacy.firstparty.isolate` | **true** | Isole chacun de vos onglets. |
| `network.IDN_show_punycode` | **true** | Certains liens contiennent des caractères unicodes. Ceci donne de plus grandes possibilités pour l'hameçonnage. Ces caractères unicode sont encodés avec le code "punycode". Activer ce paramètres force Firefox à afficher le punycode plutôt que le caractère unicode. |
| `media.peerconnection.enabled` | **false** | Désactive WebRTC qui peut poser des problèmes de sécurité et de vie privée, comme révéler votre adresse IP. |
| `signon.autofillForms` | **false** | Désactive le remplissage automatique des identifiants. |
| `network.security.esni.enabled` | **true** | Active la prise en charge de l'[ESNI](https://lafibre.info/cryptographie/encrypted-sni/). |

#### Performances

***Vérifier l'impact réel de la modification de ces paramètres, si vous ne savez pas ce que vous faites ne les modifiez pas.***

| Attribut | Valeur | Description |
| :-: | :-: | --- |
| `browser.cache.memory.enable` | **true** | Active le cache mémoire (RAM). Pour tous les paramètres concernant le cache, pensez à activer le nettoyage automatique du cache à la fin de la session pour des raisons de confidentialité. Le mieux étant d'utiliser une extension comme cookies autodelete et d'activer le nettoyage automatique à la fermeture de l'onglet et au bout d'un intervalle d'une dizaine de secondes. |
| `browser.cache.memory.capacity` | **512000** | Taille du cache mémoire (en octets, 512000 = 512 mo). Mettre -1 pour que Firefox gére automatiquement cette valeur en fonction de votre quantiter de mémoire. |
| `browser.cache.memory.max_entry_size` | **-1** | Mettre -1 pour supprimer toute limite de taille. |
| `browser.cache.disk.enable` | **true** | Autorise l'utilisation du cache disque. Pour des raisons de confidentialité désactiver le cache disque au profit du cache mémoire peut être une bonne chose ; cela permet de s'assurer qu'aucune donnée n'est enregistrée sur votre ordinateur à la fermeture de Firefox. |
| `browser.cache.disk.capacity` | **512000** | Taille du cache disque. |
| `network.dnsCacheEntries` | **4000** | Nombre d'entrées du cache DNS. Pour des raisons de confidentialité, si quelqu'un peut avoir accès à votre ordinateur laisser le paramètre par défaut. |
| `network.dnsCacheExpiration` | **43200** | Temps avant expiration, nettoyage, d'une entrée présente dans le cache DNS (en secondes). Pour des raisons de confidentialité, si quelqu'un peut avoir accès à votre ordinateur laissez le nombre par défaut. |
| `network.dnsCacheExpirationGracePeriod` | **43200** | Mettre la même valeur que pour `network.dnsCacheExpiration`. |
| `browser.sessionstore.interval` | **60000** | Firefox sauvegarde toutes les 15 secondes vos onglets et leurs données. Ça lui permet en cas de plantage de restaurer votre session. Ici on fait passer de une sauvegarde toutes les 15 secondes (15 000 ms) à une sauvegarde toutes les 60 secondes (60 000 ms). Une sauvegarde par minute c'est largement suffisant et ça permet de diminuer les accès au disque fait par Firefox. |

#### Pratique

| Attribut | Valeur | Description |
| :-: | :-: | --- |
| `browser.tabs.closeWindowWithLastTab` | **false** | Désactive la fermeture de Firefox lorsque vous fermez le dernier onglet. |
| `browser.backspace_action` | **1** | La touche retour arrière de votre clavier ne vous fera plus revenir au lien précédent. |
| `security.secure_connection_icon_color_gray` | **false** | Remet le cadenas de la barre d'adresse en vert plutôt qu'en gris. Parce que c'est plus joli :-) |
| `accessibility.blockautorefresh` | **true** | Bloque le rafraichissement automatique de la page. |
| `dom.event.contextmenu.enabled` | **false** | Empêche les sites de bloquer l'utilisation du clic-droit. |
| `browser.tabs.allowTabDetach` | **false** | Désactive la possibilité de déplacer un onglet vers une nouvelle fenêtre en tirant dessus. |
| `ui.SpellCheckerUnderlineStyle` | **3** | Créez cette entrée dans le about:config et mettez le nombre 3 afin que Firefox souligne les mots mal orthographiés au lieu de dessiner une petite vaguelette rouge. [Un autre chiffre donnera une autre forme](http://kb.mozillazine.org/Ui.SpellCheckerUnderlineStyle). |
| `full-screen-api.warning.timeout` | **0** | Firefox affiche un popup lorsque vous passez en plein écran. Passer ce paramètre à 0 permet de ne plus afficher ce paramètre. |
| `browser.preferences.experimental` | **true** | Active l'onglet "Expérimental" dans les paramètres de Firefox. |

#### N'hésitez pas à aller voir les sources pour en apprendre plus

https://www.dsfc.net/logiciel-libre/firefox-logiciel-libre/firefox-plus-rapide-respectueux-vie-privee/#Utiliser_la_memoire

https://www.privacytools.io/browsers/#about_config

https://support.mozilla.org/fr/kb/comment-empecher-firefox-etablir-automatiquement-connexions#w_mises-aa-jour-automatiques-et-saecuritae

https://sebsauvage.net/wiki/doku.php?id=firefox

https://wiki.mozilla.org/Privacy/Privacy_Task_Force/firefox_about_config_privacy_tweeks

https://www.kali-linux.fr/configuration/configurer-firefox-optimiser-securite-performances

https://lehollandaisvolant.net/?d=2020/01/02/11/28/39-ma-liste-des-tweaks-aboutconfig-dans-firefox

https://theprivacyguide1.github.io/about_config.html

https://www.ghacks.net/overview-firefox-aboutconfig-security-privacy-preferences/

https://librewolf-community.gitlab.io/

https://lehollandaisvolant.net/?d=2020/01/02/11/28/39-ma-liste-des-tweaks-aboutconfig-dans-firefox

http://kb.mozillazine.org/

https://www.malekal.com/mozilla-firefox-les-reglages-ultimes-anti-tracking-et-contre-le-pistage/

***

### Utilisé dans ce projet

| Langages       | et Applications        |
| :-------------: |:--------------:        |
| Firefox développeur | Visual Studio Code |
| Git/GitHub          |                    |

***N'hésitez pas à contribuer, en ouvrant une issue.***

#### Merci à tous

***

&hearts;&nbsp;&nbsp;&nbsp;&nbsp;Love Markdown
