---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0EB5C25C-D0A1-4444-AEA2-C963D5069CFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: b9154b239e8d4ae2857cba18d3f7dcf9510a62b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492816"
---
# Set-AzureRmDataLakeStoreAccount

## Áttekintés
Az adattó-tároló fiók módosítása.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Set-AzureRmDataLakeStoreAccount [-Name] <String> [[-DefaultGroup] <String>] [[-Tag] <Hashtable>]
 [[-TrustedIdProviderState] <TrustedIdProviderState>] [[-FirewallState] <FirewallState>]
 [[-ResourceGroupName] <String>] [-Tier <TierType>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-KeyVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **set-AzureRmDataLakeStoreAccount** parancsmag módosította az adattó-tároló fiókját.

## Példák

### 1. példa: címke hozzáadása egy fiókhoz
```
PS C:\>Set-AzureRmDataLakeStoreAccount -Name "ContosoADL" -Tags @{"stage"="production"}
```

Ez a parancs hozzáadja a megadott címkét az ContosoADL nevű adattó-tároló fiókhoz.

## PARAMÉTEREK

### -AllowAzureIpState
Engedélyezze/tiltsa le az Azure-tól származó IP-ket a tűzfalon keresztül.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.FirewallAllowAzureIpsState]
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultGroup
Egy AzureActive-címtár-csoport AZONOSÍTÓját adja meg.
Ez a csoport a létrehozott fájlok és mappák alapértelmezett csoportja.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

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

### -FirewallState
Szükség esetén engedélyezze vagy tiltsa le a meglévő tűzfalszabályok szabályait.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.FirewallState]
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Verzió
Ha a titkosítási típus felhasználó által van hozzárendelve, a felhasználó elforgathatja a fontos verziót ezzel a paraméterrel.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (név)
Az adattó-tároló fiók nevét adja meg.

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

### -ResourceGroupName
Annak a csoportnak a neve, amely a módosítani kívánt adattó-tároló fiókot tartalmazza.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Címke
A címkéket kulcs-érték párokként adja meg.
Címkéket használhat a többi Azure-erőforrásból származó adattó-tároló fiók felismeréséhez.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tier (Tier)
A megfelelő kötelezettségvállalási szint a használni kívánt fiókhoz.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.TierType]
Parameter Sets: (All)
Aliases:
Accepted values: Consumption, Commitment1TB, Commitment10TB, Commitment100TB, Commitment500TB, Commitment1PB, Commitment5PB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TrustedIdProviderState
Szükség esetén engedélyezze vagy tiltsa le a meglévő megbízható azonosító-szolgáltatókat.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.TrustedIdProviderState]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

### System. Collections. Hashtable

### System. nulla ' 1 [[Microsoft. Azure. Management. DataLake. Store. models. TrustedIdProviderState, Microsoft. Azure. Management. DataLake. Store, Version = 2.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]

### System. nulla ' 1 [[Microsoft. Azure. Management. DataLake. Store. models. FirewallState, Microsoft. Azure. Management. DataLake. Store, Version = 2.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]

### System. nulla ' 1 [[Microsoft. Azure. Management. DataLake. Store. models. TierType, Microsoft. Azure. Management. DataLake. Store, Version = 2.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]

### System. nulla ' 1 [[Microsoft. Azure. Management. DataLake. Store. models. FirewallAllowAzureIpsState, Microsoft. Azure. Management. DataLake. Store, Version = 2.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]

## KIMENETEK

### Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmDataLakeStoreAccount](./Get-AzureRmDataLakeStoreAccount.md)

[Új – AzureRmDataLakeStoreAccount](./New-AzureRmDataLakeStoreAccount.md)

[Remove-AzureRmDataLakeStoreAccount](./Remove-AzureRmDataLakeStoreAccount.md)

[Teszt-AzureRmDataLakeStoreAccount](./Test-AzureRmDataLakeStoreAccount.md)


