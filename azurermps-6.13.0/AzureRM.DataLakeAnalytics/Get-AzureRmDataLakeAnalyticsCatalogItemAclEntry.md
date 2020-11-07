---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: 349fe79bf3ff3bea0097542ee0189b5a1999bd35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679580"
---
# Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry

## Áttekintés
Megadhat egy bejegyzést az adattó-elemzési katalógus vagy katalógus elemeinek hozzáférés-vezérlési területén.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### GetCatalogAclEntry (alapértelmezett)
```
Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetCatalogAclEntryForUserOwner
```
Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetCatalogAclEntryForGroupOwner
```
Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetCatalogItemAclEntry
```
Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> -ItemType <String>
 -Path <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetCatalogItemAclEntryForUserOwner
```
Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -ItemType <String>
 -Path <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetCatalogItemAclEntryForGroupOwner
```
Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -ItemType <String>
 -Path <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry** parancsmag az adattó-elemzések katalógusa vagy katalógusa hozzáférés-vezérlési listájában (ACE) tartalmazza a bejegyzések (ACE-EK) listáját.

## Példák

### Példa 1: a katalógushoz tartozó hozzáférés-vezérlési lista beszerzése
```powershell
PS C:\> Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla"

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
```

Ez a parancs beilleszti a megadott adattó-fiók katalógusának hozzáférés-vezérlési listáját.

### 2. példa: a felhasználó hozzáférés-vezérlési bejegyzésének beszerzése egy katalógusban
```powershell
PS C:\> Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

Ez a parancs beolvassa a felhasználó tulajdonosának ACL-bejegyzését a megadott adat-tó Analytics-fiókja katalógusához.

### Példa: a csoport tulajdonosának hozzáférés-vezérlési bejegyzésének beszerzése katalógushoz
```powershell
PS C:\> Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -GroupOwner

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

Ez a parancs beilleszti a csoport tulajdonosának hozzáférés-vezérlési bejegyzését a megadott adat-tó Analytics-fiókja katalógusához.

### Példa 4: az adatbázis-hozzáférés-vezérlés beszerzése
```powershell
PS C:\> Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -ItemType Database -Path "databaseName"

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
```

Ez a parancs beilleszti a megadott Data Lake Analytics-fiók adatbázisának hozzáférés-vezérlési listáját.

### Példa 5: az adatbázis felhasználói tulajdonosának hozzáférés-vezérlési bejegyzésének beszerzése
```powershell
PS C:\> Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -ItemType Database -Path "databaseName"

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

Ez a parancs beilleszti a felhasználó tulajdonosának hozzáférés-vezérlési bejegyzését a megadott adattó-alapú adatkezelési fiók adatbázisához.

### Példa 6: a csoport tulajdonosának hozzáférés-vezérlési bejegyzésének beszerzése egy adatbázishoz
```powershell
PS C:\> Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -GroupOwner -ItemType Database -Path "databaseName"

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

Ez a parancs beolvassa a csoport tulajdonosának hozzáférés-vezérlési bejegyzését a megadott adattó Analytics-fiók adatbázisához.

## PARAMÉTEREK

### -Fiók
A Lake Analytics-fiók nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GroupOwner
A katalógus ACL-bejegyzésének beszerzése a csoport tulajdonosai számára

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetCatalogAclEntryForGroupOwner, GetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ItemType
A katalógus vagy a katalógus elem (ek) típusát adja meg. A paraméter elfogadható értékei a következők:
- Katalógus
- Adatbázis

```yaml
Type: System.String
Parameter Sets: GetCatalogItemAclEntry, GetCatalogItemAclEntryForUserOwner, GetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path (elérési út)
Egy katalógus vagy katalógusfájl adattó-elemzési útvonalát adja meg.
Az elérési út egyes részeit ponttal (.) kell elválasztani.

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: GetCatalogItemAclEntry, GetCatalogItemAclEntryForUserOwner, GetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UserOwner
ACL-bejegyzés kérése a felhasználó tulajdonosának.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetCatalogAclEntryForUserOwner, GetCatalogItemAclEntryForUserOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

### Microsoft. Azure. Command. DataLakeAnalytics. models. CatalogPathInstance

## KIMENETEK

### Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Az U-SQL most az adatbázis szintű hozzáférés-vezérlést kínálja](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)

[Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry](Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md)

[Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry](Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md)
