---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: D19488C1-9E87-4F1A-94E3-8AFDE6AFC982
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoverystorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassificationMapping.md
ms.openlocfilehash: e04f5b71fe0cc5d6872c3bdf9cd18790f4e09f7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679683"
---
# Get-AzureRmSiteRecoveryStorageClassificationMapping

## Áttekintés
Tároló besorolási megfeleltetést kap a webhely-helyreállításban.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### Alapértelmezett (alapértelmezett)
```
Get-AzureRmSiteRecoveryStorageClassificationMapping [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByName
```
Get-AzureRmSiteRecoveryStorageClassificationMapping -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **Get-AzureRmSiteRecoveryStorageClassificationMapping** parancsmag az Azure webhely-helyreállítási szolgáltatásban kapja meg a tárolási osztályozási megfeleltetést.

## Példák

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
Itt adhatja meg annak a tárolási besorolási megfeleltetésnek a nevét, amely a parancsmagot kapja.

```yaml
Type: String
Parameter Sets: ByName
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

### Nincs
Ez a parancsmag nem fogadja el a bevitelt.

## KIMENETEK

### System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. SiteRecovery. ASRStorageClassificationMapping]

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureRmSiteRecoveryStorageClassificationMapping](./New-AzureRmSiteRecoveryStorageClassificationMapping.md)

[Remove-AzureRmSiteRecoveryStorageClassificationMapping](./Remove-AzureRmSiteRecoveryStorageClassificationMapping.md)
