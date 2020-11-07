---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: A5697F1E-623A-4E26-96C8-6197852BFFAA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVM.md
ms.openlocfilehash: 9f594b61b1ad34a39ea0a84381f6181cadc418c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672685"
---
# Get-AzureRmSiteRecoveryVM

## Áttekintés
Információt kap a webhely-helyreállítási felügyelt virtuális gépekről.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### ByObject (alapértelmezett)
```
Get-AzureRmSiteRecoveryVM -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByObjectWithName
```
Get-AzureRmSiteRecoveryVM -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByObjectWithFriendlyName
```
Get-AzureRmSiteRecoveryVM -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmSiteRecoveryVM** parancsmag információt kap az Azure webhely-helyreállítással kezelt virtuális gépekről.

## Példák

## PARAMÉTEREK

### -Típusú megjelenített
A virtuális gép rövid nevét adja meg.

```yaml
Type: System.String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
A virtuális gép nevét adja meg.

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProtectionContainer
A webhely-helyreállítási védelem tárolójának objektumát adja meg.

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: ByObjectWithName, ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### ASRProtectionContainer
A ' ProtectionContainer ' paraméter az "ASRProtectionContainer" típusú értéket fogadja el a csővezetékről

### ASRProtectionContainer
A ' ProtectionContainer ' paraméter az "ASRProtectionContainer" típusú értéket fogadja el a csővezetékről

## KIMENETEK

### System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. SiteRecovery. ASRVirtualMachine]

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Set-AzureRmSiteRecoveryVM](./Set-AzureRmSiteRecoveryVM.md)
