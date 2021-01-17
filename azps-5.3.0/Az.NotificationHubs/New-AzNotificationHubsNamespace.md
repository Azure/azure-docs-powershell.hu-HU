---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3BA94976-DE88-4F07-9C06-41FEEDE1B829
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
ms.openlocfilehash: 24a42fba23427f437cb064e1915c19e36e7a71bf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467302"
---
# New-AzNotificationHubsNamespace

## SYNOPSIS
Létrehoz egy értesítési központ névterét.

## SZINTAXIS

```
New-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## LEÍRÁS
A **New-AzNotificationHubsNamespace** parancsmag létrehoz egy értesítési központ névterét.
A névterek logikai tárolók, amelyek segítenek az értesítési központok rendszerezésében és kezelésében.
Legalább egy értesítési központ névterének kell lennie.
Egyetlen névterben több központ is elterhet.
Több névteret is adhat a központ rendszerezéséhez, vagy adott személyeknek engedélyt adhat a központok kijelölt alcsoportja kezeléséhez.
Névtér létrehozásához adjon meg egyedi nevet a névtérnek; adja meg azt az adatközpontot, ahol a névtér található; és adja meg azt az erőforráscsoportot, amelyhez a névteret hozzárendeli.
A névtér létrehozása után a New-AzNotificationHubsNamespaceAuthorizationRules parancsmag segítségével engedélyezési szabályokat rendelhet a névtérhez.
Az engedélyezési szabályok a névtér engedélyeinek kezelésére használhatók.

## PÉLDÁK

### 1. példa: Értesítési központ létrehozása
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners"
```

Ez a parancs létrehoz egy ContosoPartners nevű értesítési központot.
A névtér a nyugat-amerikai adatközpontban található, és a ContosoNotificationsGroup erőforráscsoporthoz lesz hozzárendelve.

### 2. példa: Értesítési központ létrehozása címkékkel
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners" -Tags @{Name="Audience";Value="PartnerOrganizations"}
```

Ez a parancs létrehoz egy ContosoPartners nevű értesítési központot.
A névtér a nyugat-amerikai adatközpontban található, és a ContosoNotificationsGroup erőforráscsoporthoz lesz hozzárendelve.
Ez a parancs emellett létrehoz egy Címkét a Célközönség névvel és a PartnerOrganizations értékkel, és a névtérhez van rendelve.
Ez biztosítja, hogy a névtér mindig megjelenik, amikor olyan elemekre szűr, amelyeknél a Célközönség címke partnerszervezetre van állítva.

## PARAMETERS

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés

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

### -Location
A Névteret szolgáltató adatközpont megjelenítendő nevét adja meg.
Bár ezt a paramétert bármilyen érvényes helyre beállíthatja, az optimális teljesítmény érdekében érdemes lehet a felhasználók többségéhez közeli adatközpontot használni.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namespace
Az új névtér nevét adja meg.
A névterek lehetőséget nyújtanak az értesítési központok csoportosítására és kategorizálására.

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
Azt az erőforráscsoportot adja meg, amelyhez a névteret hozzá kell rendelni.
Az erőforráscsoportok olyan módon rendszerezhetik az elemeket, mint a névterek, az értesítési központok és az engedélyezési szabályok, ami egyszerű készletkezelést és felügyeletet kínál.

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

### -SkuTier
A névtér termékváltozatrétege

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Az Azure-elemek kategorizálásához és rendezéséhez használható névérték-párokat ad meg.
A címkék a kulcsszavakhoz hasonlóan működnek, és az egész telepítésben működnek.
Ha például az összes olyan elemet megkeresi, amely a Department:IT címkével van megcímkézve, a keresés az adott címkével az összes Azure-elemet visszaadja, függetlenül az elem típusától, helyétől vagy erőforráscsoporttól.
Az egyes címkék két részből áll: a *Név* és, ha lehetséges, az *Érték.*
A Department:IT (Részleg) részlegnél például a címke neve Részleg, a címke értéke pedig IT.
Címke hozzáadásához az alábbihoz hasonló hash táblázatszintaxist használjon, amely a CalendarYear:2016 címkét hozza létre:

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
A parancsmag futtatása előtt a rendszer megerősítést kér.

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
A parancsmag futtatásakor a program megjeleníti, hogy mi történik. A parancsmag nem fut.

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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

### System.Collections.Hashtable

## KIMENETEK

### Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzNotificationHubsNamespace](./Get-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)

[Set-AzNotificationHubsNamespace](./Set-AzNotificationHubsNamespace.md)


