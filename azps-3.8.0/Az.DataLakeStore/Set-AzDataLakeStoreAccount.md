---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 0EB5C25C-D0A1-4444-AEA2-C963D5069CFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreAccount.md
ms.openlocfilehash: 4db6ceb0f806aeffd4dc69580da891de567e4e83
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94015036"
---
# Set-AzDataLakeStoreAccount

## Áttekintés
Az adattó-tároló fiók módosítása.

## SZINTAXISA

```
Set-AzDataLakeStoreAccount [-Name] <String> [[-DefaultGroup] <String>] [[-Tag] <Hashtable>]
 [[-TrustedIdProviderState] <TrustedIdProviderState>] [[-FirewallState] <FirewallState>]
 [[-ResourceGroupName] <String>] [-Tier <TierType>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-KeyVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **set-AzDataLakeStoreAccount** parancsmag módosította az adattó-tároló fiókját.

## Példák

### 1. példa: címke hozzáadása egy fiókhoz
```
PS C:\>Set-AzDataLakeStoreAccount -Name "ContosoADL" -Tags @{"stage"="production"}
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

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
Aliases:

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

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

[Get-AzDataLakeStoreAccount](./Get-AzDataLakeStoreAccount.md)

[Új – AzDataLakeStoreAccount](./New-AzDataLakeStoreAccount.md)

[Remove-AzDataLakeStoreAccount](./Remove-AzDataLakeStoreAccount.md)

[Teszt-AzDataLakeStoreAccount](./Test-AzDataLakeStoreAccount.md)

