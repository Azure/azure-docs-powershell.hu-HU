---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 8C5D29AD-0B15-4CD4-8637-86ABD19F41C8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlCapability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlCapability.md
ms.openlocfilehash: 98d45109af99658f8f6bd7847646818b30469a78
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503924"
---
# Get-AzureRmSqlCapability

## Áttekintés
Az SQL-adatbázis funkciói az aktuális előfizetéshez.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### FilterResults (alapértelmezett)
```
Get-AzureRmSqlCapability [-LocationName] <String> [-ServerVersionName <String>] [-EditionName <String>]
 [-ServiceObjectiveName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### DefaultResults
```
Get-AzureRmSqlCapability [-LocationName] <String> [-Defaults] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmSqlCapability** parancsmag az Azure SQL-adatbázis elérhető funkcióit kapja meg a jelenlegi előfizetésben egy régióban.
Ha megadja a *ServerVersionName* , a *EditionName* vagy a *ServiceObjectiveName* paramétert, ez a parancsmag a megadott értékeket és a megelőzőket adja eredményül.

## Példák

### Példa 1: a meglévő előfizetéshez tartozó funkciók beszerzése egy adott régióban
```
PS C:\>Get-AzureRmSqlCapability -LocationName "Central US"
Location                : Central US
Status                  : Available
SupportedServerVersions : {12.0, 2.0}
```

Ez a parancs a közép-amerikai régió aktuális előfizetésének SQL-adatbázis-példányait jeleníti meg.

### 2. példa: a jelenlegi előfizetéshez tartozó alapértelmezett funkciók beszerzése egy régióban
```
PS C:\>Get-AzureRmSqlCapability -LocationName "Central US" -Defaults
Location        : Central US
Status          : Available
ExpandedDetails : Version: 2.0 (Default) -> Edition: Standard (Default) -> Service Objective: S0 (Default)
```

Ez a parancs a közép-amerikai régió jelenlegi előfizetésének alapértelmezett funkcióit számítja ki az SQL-adatbázisokban.

### 3. példa: a szolgáltatási cél részleteinek beolvasása
```
PS C:\>Get-AzureRmSqlCapability -LocationName "Central US" -ServiceObjectiveName "S1"
Location        : Central US
Status          : Available
ExpandedDetails : Version: 12.0 (Available) -> Edition: Standard (Default) -> Service Objective: S1 (Available) 
                  Version: 2.0 (Default) -> Edition: Standard (Default) -> Service Objective: S1 (Available)
```

Ez a parancs a jelenlegi előfizetéshez megadott szolgáltatási célhoz tartozó alapértelmezett funkciókat kapja meg az SQL-adatbázisokban.

## PARAMÉTEREK

### – Alapértelmezett beállítások
Azt jelzi, hogy ez a parancsmag csak alapértelmezés szerint válik elérhetővé.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultResults
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EditionName
Annak az adatbázis-kiadásnak a nevét adja meg, amelynek a parancsmagja elérhetővé válik.

```yaml
Type: System.String
Parameter Sets: FilterResults
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LocationName
Annak a helynek a nevét adja meg, amelyre a parancsmag lehetőségeket ad.
További információ: Azure Regions https://azure.microsoft.com/en-us/regions/ ( https://azure.microsoft.com/en-us/regions/) .

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

### -ServerVersionName
Annak a kiszolgálói verziónak a nevét adja meg, amelynek a parancsmagja elérhetővé válik.

```yaml
Type: System.String
Parameter Sets: FilterResults
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceObjectiveName
Annak a szolgáltatási célnak a nevét adja meg, amelyre ez a parancsmag lehetőségeket kap.

```yaml
Type: System.String
Parameter Sets: FilterResults
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
A parancsmag nem fut.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### Microsoft.Azure.Commands.Sql.Location_Capabilities. Model. LocationCapabilityModel

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

