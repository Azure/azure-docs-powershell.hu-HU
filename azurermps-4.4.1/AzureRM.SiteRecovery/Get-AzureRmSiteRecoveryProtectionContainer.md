---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 77F1556C-323D-49CA-BD6C-75B2D4E0F894
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionContainer.md
ms.openlocfilehash: 2595d8feaa01c2f3ccd9f16ca193be195a8e303a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503939"
---
# Get-AzureRmSiteRecoveryProtectionContainer

## Áttekintés
Védett tárolók a jelenlegi webhely-helyreállítási boltozathoz.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### Alapértelmezett (alapértelmezett)
```
Get-AzureRmSiteRecoveryProtectionContainer [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByObjectWithName
```
Get-AzureRmSiteRecoveryProtectionContainer -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByObjectWithNameLegacy
```
Get-AzureRmSiteRecoveryProtectionContainer -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByObjectWithFriendlyName
```
Get-AzureRmSiteRecoveryProtectionContainer -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByObjectWithFriendlyNameLegacy
```
Get-AzureRmSiteRecoveryProtectionContainer -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByFabricObject
```
Get-AzureRmSiteRecoveryProtectionContainer -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **Get-AzureRmSiteRecoveryProtectionContainer** parancsmag védett tárolókat kap az aktuális Azure webhely-helyreállítási boltozathoz.
A védelmi tároló egy logikai tároló a védett objektumokhoz, például a virtuális gépekhez.
A védelmi házirendek definiálják a védett elemek replikációs beállításait, és a védelemmel ellátott tárolóban használhatók, és egy védett entitásra alkalmazhatók.

## Példák

## PARAMÉTEREK

### -Szövet
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: ByObjectWithName, ByObjectWithFriendlyName, ByFabricObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Típusú megjelenített
A védelmi tároló rövid nevét adja meg.

```yaml
Type: System.String
Parameter Sets: ByObjectWithFriendlyName, ByObjectWithFriendlyNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
A védelmi tároló nevét adja meg.

```yaml
Type: System.String
Parameter Sets: ByObjectWithName, ByObjectWithNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
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

### ASRFabric
A "szövet" paraméter az "ASRFabric" típusú értéket fogadja el a csővezetékről

## KIMENETEK

### System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. SiteRecovery. ASRProtectionContainer]

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

