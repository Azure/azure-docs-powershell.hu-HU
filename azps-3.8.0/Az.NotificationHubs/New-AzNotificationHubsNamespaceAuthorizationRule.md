---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3F59F7E8-CD32-40CB-9DE0-3FB044439DD0
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: eaf34373cb17fea94c498e16f623cef4bf65e937
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012779"
---
# New-AzNotificationHubsNamespaceAuthorizationRule

## Áttekintés
Létrehoz egy engedélyezési szabályt, és hozzárendeli a szabályt egy értesítési hub-névtérhez.

## SZINTAXISA

### InputFileParameterSet
```
New-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SASRuleParameterSet
```
New-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Leírás
A **New-AzNotificationHubsNamespaceAuthorizationRule** parancsmag létrehoz egy megosztott hozzáférés-aláírási (SA) engedélyezési szabályt, és hozzárendeli az értesítési hub névteréhez.
Az engedélyezési szabályok a névtérhez és az adott névtérhez tartozó értesítési hubokhoz való felhasználói jogokat kezelik.
Ez a parancsmag két lehetőséget kínál új engedélyezési szabály létrehozására és névtérhez rendeléséhez.
Létrehozhat egy példányt a **SharedAccessAuthorizationRuleAttributes** objektumból, majd beállíthatja az objektum azon tulajdonsági értékeit, amelyeket az új szabálynak meg kell jelenítenie.
Ez a funkció a .NET Framework segítségével végezhető el.
A *SASRule* paraméterrel átmásolhatja ezeket a tulajdonságértékeket az új szabályba.
Azt is megteheti, hogy a megfelelő konfigurációs értékeket tartalmazó JSON (JavaScript-objektum jelölése) fájlt hoz létre, majd a *InputFile* paraméterrel alkalmazza ezeket az értékeket.
A JSON-fájl egy szöveges fájl, amely a következőhöz hasonló szintaxist használ: {  
    "Név": "ContosoAuthorizationRule";  
    "PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =";  
    "Jogok": \[  
        "Figyelj",  
        Küldése  
    \]  
} Ha a **New-AzNotificationHubsNamespaceAuthorizationRule** parancsmaggal együtt használja, az előző JSON-minta létrehoz egy ContosoAuthorizationRule nevű engedélyezési szabályt, amely lehetővé teszi, hogy a felhasználók meghallgassák és elküldjék a névteret.
A hitelesítéshez használt *PrimaryKey* a következő Windows PowerShell-paranccsal lehet véletlenszerűen generált: \[ Convert \] :: ToBase64String (((1.. 32 |% { \[ byte/] (Get-Random-minimum 0-Max 255)}))

## Példák

### Példa 1: engedélyezési szabály létrehozása és hozzárendelése egy névtérhez
```
PS C:\>New-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\NamespaceAuthorizationRules.json"
```

A parancs létrehoz egy engedélyezési szabályt, és hozzárendeli a szabályt a névtér ContosoNamespace.
A szabály létrehozásakor meg kell adnia a megfelelő névteret és azt az erőforráscsoport-csoportot, amelyhez a névtér hozzá van rendelve.
Nem kell azonban a szabályra vonatkozó információkat megadni: a szabály adatait a program a bemeneti fájlból C:\Configuration\NamespaceAuthorizationRules.js.

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputFile
Az új engedélyezési szabály konfigurációs adatait tartalmazó JSON-fájl elérési útját adja meg.

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namespace
Azt a névteret adja meg, amelyre az engedélyezési szabályokat hozzárendeli.
A névterek lehetőséget nyújtanak az értesítési hubok csoportosítására és kategorizálására.
Az új szabályokat egy meglévő névtérhez kell rendelni.
A **New-AzNotificationHubsNamespaceAuthorizationRule** parancsmag nem tud új névteret létrehozni.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroup
Azt az erőforráscsoportot adja meg, amelyhez a névtér van társítva.
Az erőforráscsoportok elemek (például névterek, értesítési hubok és engedélyezési szabályok) rendszerezése olyan módon, hogy egyszerűen csak a Készletkezelés és az Azure felügyeletet segítse elő.
Egy meglévő erőforráscsoportot kell használnia.
Ez a parancsmag nem tud új erőforráscsoportot létrehozni.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SASRule
Az új szabályok konfigurációs adatait tartalmazó **SharedAccessAuthorizationRuleAttributes** -objektumot adja meg.

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut. A parancsmag nem fut.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

## KIMENETEK

### Microsoft. Azure. Command. NotificationHubs. models. SharedAccessAuthorizationRuleAttributes

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzNotificationHubAuthorizationRule](./Get-AzNotificationHubAuthorizationRule.md)

[Remove-AzNotificationHubAuthorizationRule](./Remove-AzNotificationHubAuthorizationRule.md)

[Set-AzNotificationHubAuthorizationRule](./Set-AzNotificationHubAuthorizationRule.md)


