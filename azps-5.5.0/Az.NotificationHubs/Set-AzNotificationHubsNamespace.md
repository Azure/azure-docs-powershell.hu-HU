---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 1B2AA717-ECD6-4CC0-AB6D-A199AF21A4A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
ms.openlocfilehash: c367c4b4f7ebe7c9d6d51b832eed22249f262864
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158722"
---
# Set-AzNotificationHubsNamespace

## SYNOPSIS
Beállítja egy értesítési központ névterének tulajdonságértékét.

## SZINTAXIS

```
Set-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-State] <NamespaceState>] [[-Critical] <Boolean>] [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
A **Set-AzNotificationHubsNamespace** parancsmag beállítja egy meglévő értesítési központ névterének tulajdonságértékét.
A névterek logikai tárolók, amelyek segítenek az értesítési központok rendszerezésében és kezelésében.
Legalább egy értesítési központ névterének kell lennie.
Ezenkívül minden értesítési központhoz hozzá kell rendelni egy névteret.
Ez a parancsmag elsősorban a névterek engedélyezésére és letiltására használható.
Ha egy névtér le van tiltva, a felhasználók nem tudnak csatlakozni a névtér egyik értesítési központjához sem, és a rendszergazdák sem tudnak leküldéses értesítéseket küldeni.
Ha újra engedélyezni szeretné a letiltott névteret, ezzel a parancsmaggal állítsa a névtér **State** tulajdonságát Aktívra.
Ez a parancsmag egy névteret is kritikusként címkézhet meg.
Ez megakadályozza a névtér törlését.
A kritikus névterek eltávolításához először el kell távolítania a kritikus címkét.

## PÉLDÁK

### 1. példa: Névtér letiltása
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Disabled"
```

Ez a parancs letiltja a ContosoPartners nevű névteret, amely az Amerikai Egyesült Államok nyugati részén található, és a ContosoNotificationsGroup erőforráscsoporthoz van rendelve.

### 2. példa: Névtér engedélyezése
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Active"
```

Ez a parancs engedélyezi a ContosoPartners nevű névteret, amely az Amerikai Egyesült Államok nyugati részén található, és a ContosoNotificationsGroup erőforráscsoporthoz van rendelve.

## PARAMETERS

### -Critical
Azt jelzi, hogy a névtér kritikus névtér-e.
A kritikus névterek nem törölhetők.
A kritikus névterek törléséhez a tulajdonság értékét Hamis értékre kell állítania ahhoz, hogy a névteret ne kritikusként jelölje meg.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -Force
Ne kérjen megerősítést.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Location
A névteret tartalmazó adatközpont megjelenítendő nevét adja meg.
Bár ezt a paramétert bármilyen érvényes Azure-helyre beállíthatja, az optimális teljesítmény érdekében a legtöbb felhasználó közelében található adatközpontot kell használnia.
Az Azure-helyek naprakész listájának lekértért futtatásához futtassa az alábbi parancsot: `Get-AzLocation | Select-Object DisplayName`

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
A parancsmag által módosítható névteret adja meg.
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
Azt az erőforráscsoportot adja meg, amelyhez a névteret hozzárendelték.
Az erőforráscsoportok a készletkezelést és az Azure felügyeletét segítő módon rendszerezhetik az elemeket, például a névtereket, az értesítési központokat és az engedélyezési szabályokat.

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

### -State
A névtér aktuális állapotát adja meg.
A paraméter elfogadható értékei: Aktív és Letiltva.

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, Active, Disabled

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Az Azure-elemek kategorizálására és rendezésére használható névérték-párokat ad meg.
A címkék a kulcsszavakhoz hasonlóan működnek, és az egész telepítésben működnek.
Ha például az összes olyan elemet megkeresi, amely a Department:IT címkével van megcímkézve, a keresés az adott címkével az összes Azure-elemet visszaadja, függetlenül az elem típusától, helyétől vagy erőforráscsoporttól.
Az egyes címkék két részből áll: a *Név* és (tetszés szerint) az *Érték.*
A Department:IT (Részleg) címke neve például Részleg, a címke értéke pedig IT.
Címke hozzáadásához ehhez hasonló hash táblázatszintaxist használjon, amely létrehozza a CalendarYear:2016 címkét: -Tags @{Name="CalendarYear"; Value="2016"} Ha több címkét szeretne hozzáadni egy parancshoz, az egyes címkéket vesszővel válassza el egymástól: -Tag @{Name="CalendarYear"; Value="2016"}, @{Name="FiscalYear"; Value="2017"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

### Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState

### System.Boolean

### System.Collections.Hashtable

## KIMENETEK

### Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzNotificationHubsNamespace](./Get-AzNotificationHubsNamespace.md)

[New-AzNotificationHubsNamespace](./New-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)


