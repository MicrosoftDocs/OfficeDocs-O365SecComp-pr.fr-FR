---
title: "activer ou désactiver les conseils de sécurité dans Office 365" ms. Author: krowley Author: kccross Manager: laurawi ms. Date: 12/05/2018 ms. audience: admin ms. topic: article ms. service: o365-administration localization_priority: normal Search. appverid: 
- MET150 ms. AssetID: f09668bd-fe1a-4C01-89e3-e88c370e66c7 ms. collection:
    - M365-Security-Description de la conformité: "indique à Office 365 et aux administrateurs EOP comment activer et désactiver les conseils de sécurité dans les messages électroniques."
---

# <a name="enable-or-disable-safety-tips-in-office-365"></a>Activer ou désactiver les conseils de sécurité dans Office 365

Exchange Online Protection (EOP) ajoute ou horodate un Conseil de sécurité pour les messages électroniques qu'il remet. Ces conseils de sécurité fournissent aux destinataires un moyen rapide de déterminer si un message provient d'un expéditeur sécurisé et vérifié, si le message a été marqué comme courrier indésirable par Office 365, si le message contient un message suspect, tel qu'une escroquerie de type hameçonnage, ou si des images externes ont été bloquée. Les administrateurs d'Office 365 et d'EOP peuvent modifier un paramètre de stratégie de courrier indésirable pour activer ou désactiver l'affichage des conseils de sécurité dans les messages électroniques dans Outlook et d'autres clients de messagerie de bureau. 
  
Office 365 active les conseils de sécurité par défaut pour votre organisation et nous vous recommandons de les laisser activés pour combattre le courrier indésirable et les attaques par hameçonnage. Vous ne pouvez pas désactiver les conseils de sécurité pour Outlook sur le Web.
  
Pour voir des exemples et pour en savoir plus sur les informations affichées dans les conseils de sécurité, consultez la rubrique [conseils de sécurité dans les messages électroniques dans Office 365.](safety-tips-in-office-365.md)
  
Dans cet article :
  
- [Pour activer ou désactiver les conseils de sécurité à l'aide du &amp; Centre de sécurité conformité Office 365](enable-or-disable-safety-tips.md#SandCCsafetytip)
    
- [Pour activer ou désactiver les conseils de sécurité à l'aide de PowerShell](enable-or-disable-safety-tips.md#pshellsafetytip)
    
## <a name="to-enable-or-disable-safety-tips-by-using-the-office-365-security-amp-compliance-center"></a>Pour activer ou désactiver les conseils de sécurité à l'aide du &amp; Centre de sécurité conformité Office 365
<a name="SandCCsafetytip"> </a>

1. Accédez à [https://protection.office.com](https://protection.office.com).
    
2. Connectez-vous à Office 365 à l'aide de votre compte professionnel ou scolaire.
    
3. Choisissez **** \> **stratégie**de gestion des menaces. 
    
4. Sur la page **stratégie** , choisissez **blocage du courrier**indésirable.
    
    ![Cette capture d'écran indique comment accéder à la page des paramètres de blocage du courrier &amp; indésirable dans le centre de sécurité et de conformité.](media/b8eb2ee3-2eb1-4ea2-b138-f6d7fb2e23de.png)
  
5. Sur la page **paramètres de blocage du courrier** indésirable, sélectionnez l'onglet **personnalisé** . 
    
    ![Cette capture d'écran indique l'emplacement de l'onglet personnalisé dans la page Paramètres du blocage du courrier &amp; indésirable dans le centre de sécurité et de conformité.](media/1d688d23-e6f3-4de5-84a7-e8ce31786193.png)
  
6. Si nécessaire, choisissez le commutateur **paramètres personnalisés** pour activer les paramètres personnalisés. Si le commutateur de paramètres personnalisés est **désactivé**, vous ne pourrez pas modifier les stratégies de filtrage du courrier indésirable.
    
    ![Cette capture d'écran illustre les paramètres de stratégie de filtrage anti-courrier indésirable personnalisés désactivés.](media/94f900ad-b556-4a31-a3ac-acfcd72e71b8.png)
  
7. Développez la stratégie de courrier indésirable que vous souhaitez modifier, puis choisissez **modifier la stratégie**. Par exemple, cliquez sur la flèche vers le bas en regard de **stratégie de filtrage du courrier indésirAble par défaut**. Si vous le souhaitez, vous pouvez créer une nouvelle stratégie en sélectionnant **Ajouter une stratégie**.
    
8. Développez **les actions de courrier indésirable et en bloc** . 
    
9. Pour activer les conseils de sécurité, sous **conseils de sécurité**, activez la case à cocher **activé** . Pour désactiver les conseils de sécurité, désactivez la case à cocher **activé** . 
    
10. Sélectionnez **Enregistrer**.
    
## <a name="to-enable-or-disable-safety-tips-by-using-powershell"></a>Pour activer ou désactiver les conseils de sécurité à l'aide de PowerShell
<a name="pshellsafetytip"> </a>

Les administrateurs peuvent utiliser Exchange Online PowerShell pour activer ou désactiver les conseils de sécurité. La cmdlet Set-HostedContentFilterPolicy permet d'activer ou de désactiver les conseils de sécurité dans une stratégie de filtrage du courrier indésirable.
  
1. Connectez-vous à Exchange Online PowerShell. Pour plus d'informations, consultez la rubrique [connexion à Exchange Online PowerShell](http://go.microsoft.com/fwlink/p/?LinkId=396554).
    
2. Exécutez la cmdlet Set-HostedContentFilterPolicy pour activer ou désactiver les conseils de sécurité:
    
  ```
  Set-HostedContentFilterPolicy -Identity "policy name " -InlineSafetyTipsEnabled <$true|$false>
  ```

Où :
    
  -  *nom* de la stratégie est le nom de la stratégie que vous souhaitez modifier, par exemple **par défaut**.
    
  -  `$true`active les conseils de sécurité pour la stratégie de filtrage du courrier indésirable. 
    
  -  `$false`désactive les conseils de sécurité pour la stratégie de filtrage du courrier indésirable. 
    
    Par exemple, pour désactiver les conseils de sécurité pour la stratégie de filtrage du courrier indésirable par défaut, exécutez la commande suivante:
    
  ```
  PS C:\> Set-HostedContentFilterPolicy -Identity "default" -InlineSafetyTipsEnabled $false
  ```

Pour plus d'informations sur cette cmdlet, consultez la rubrique [Set-HostedContentFilterPolicy](https://technet.microsoft.com/library/jj200781.aspx).
    
## <a name="still-need-help"></a>Vous avez encore besoin d'aide ?
<a name="pshellsafetytip"> </a>

Si vous avez désactivé les conseils de sécurité, mais que vous les voyez toujours dans vos messages électroniques, vérifiez les points suivants:
  
- Vous ne pouvez pas désactiver les conseils de sécurité pour Outlook sur le Web. Essayez d'afficher le même courrier électronique dans un autre client, tel qu'Outlook.
    
- Les conseils de sécurité sont activés par défaut pour chaque personne qui utilise EOP, y compris toutes les personnes qui disposent d'Office 365. Pour désactiver l'affichage des conseils de sécurité dans le courrier électronique, vous devez les désactiver à l'aide d'une stratégie de filtrage du courrier indésirable, comme décrit dans cette rubrique. Une fois que vous avez configuré la stratégie, vérifiez qu'elle est activée. Pour plus d'informations sur l'activation des stratégies de filtrage du courrier indésirable, voir [Configure Your Spam Filter Policies](https://technet.microsoft.com/library/jj200684.aspx).
    
Pour découvrir d'autres méthodes de lutte contre le courrier indésirable et le hameçonnage, consultez la rubrique [Office 365 E-mail anti-spam protection](anti-spam-protection.md).
  

