# BEARZ Desktop 0.2.4

**Présentation de la préversion.** BEARZ Desktop 0.2.4 organise des profils séparés pour Chrome, Edge et Brave sous Windows 11 x64. Les navigateurs s’installent séparément. Les profils et leurs téléchargements restent sur le poste. Pour transférer des profils, utiliser les fonctions de sauvegarde et récupération. Cette préversion est destinée à des essais avec des données fictives.

**Notes 0.2.4.** La construction retire les symboles de débogage et les chemins locaux de compilation de la livraison. Le fonctionnement des profils reste celui de la 0.2.3. L’édition ZIP et l’édition installée utilisent la même bibliothèque de profils. Fermer complètement l’une avant d’ouvrir l’autre.

**Installer et vérifier.** Vérifier le SHA-256 du ZIP, extraire la totalité de l’archive dans un dossier local neuf, puis lancer `BEARZ-Desktop.exe` sous un compte Windows standard. Le runtime .NET de Desktop est inclus. Dans **Diagnostics**, vérifier la version 0.2.4 et la signature du navigateur utilisé, puis ouvrir et fermer un profil fictif. Windows peut afficher un titre générique pour la fenêtre du navigateur. Pour une future édition Store, installer depuis l’invitation avec le compte Microsoft invité, puis vérifier dans Diagnostics que l’application est installée par un paquet Windows.

**Erreurs et désinstallation.**

| Situation | Action |
|---|---|
| SHA-256 différent ou archive incomplète | Interrompre l’installation et récupérer une copie auprès du canal autorisé. |
| Erreur de lancement ou navigateur absent | Relever la version Windows, le canal ZIP/Store et le message exact. Vérifier dans Diagnostics la présence d’un navigateur accepté si l’application s’ouvre. Relire tout rapport avant de le transmettre et retirer les chemins, noms et identifiants personnels. |
| Blocage Smart App Control ou SmartScreen | Préserver les protections et arrêter le lancement. Le ZIP non signé a été bloqué sur la configuration Windows 11 Famille avec Smart App Control actif testée. Le canal Store pourra être essayé une fois le paquet certifié disponible. |
| Poste professionnel, App Control for Business ou AppLocker | S’adresser à l’équipe informatique avec le nom, la version, l’empreinte et le message de blocage. Le ZIP ou le Store peut être indisponible selon la politique du poste. |
| Liste illisible ou restauration refusée | Utiliser **Diagnostics → Réparer la liste des profils** pour une liste illisible. En cas de phrase incorrecte ou sauvegarde corrompue, garder l’original et vérifier la phrase ou utiliser une autre sauvegarde vérifiée. |
| Retrait du ZIP ou du Store | Fermer BEARZ et vérifier la sauvegarde si les profils doivent être conservés. Pour le ZIP, retirer uniquement le dossier des binaires extraits. Pour le Store, ouvrir **Paramètres → Applications → Applications installées → BEARZ Desktop → Désinstaller**. Les profils et téléchargements sont stockés séparément. Leur éventuelle suppression relève d’une action distincte. |

[Smart App Control, Microsoft](https://support.microsoft.com/en-gb/windows/security/threat-malware-protection/smart-app-control-frequently-asked-questions) · [Politiques de contrôle des applications, Microsoft](https://learn.microsoft.com/en-us/windows/security/application-security/application-control/app-control-for-business/appcontrol-and-applocker-overview)

**Contenu exact du futur `SHA256SUMS.txt`**, vérifié sur le ZIP qualifié de 63 222 340 octets.

```text
C66577A5F2D9E5DE4E4199DA1DF4F53F9422A1ACB32DB36A3A763F279C9A476C  BEARZ-Desktop-0.2.4.0-win-x64.zip
```

```powershell
Get-FileHash -Algorithm SHA256 -LiteralPath '.\BEARZ-Desktop-0.2.4.0-win-x64.zip'
```

## Canaux de diffusion

Le ZIP communautaire vise les environnements Windows compatibles, après autorisation de diffusion. Le Microsoft Store est la voie prévue pour un paquet signé et certifié, après validation officielle.

## Licences des composants redistribués

Le dossier `licences/` du ZIP contient les licences MIT de .NET et de WPF et les avis des composants tiers embarqués. Conservez ces fichiers avec le paquet. Les conditions de diffusion de BEARZ Desktop seront précisées avec la préversion approuvée. [Licence .NET](https://github.com/dotnet/runtime/blob/main/LICENSE.TXT) · [Licence WPF](https://github.com/dotnet/wpf/blob/main/LICENSE.TXT)
