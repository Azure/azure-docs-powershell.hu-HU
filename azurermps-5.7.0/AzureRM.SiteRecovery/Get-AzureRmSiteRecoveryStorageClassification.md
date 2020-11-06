---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 3F62A993-18BF-4189-A7C0-BB877F550AA5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoverystorageclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassification.md
ms.openlocfilehash: 4ca96961aa99a15161e9abbbc01174f97a27968e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502395"
---
# Get-AzureRmSiteRecoveryStorageClassification

## Áttekintés
Beolvashatja a tárterület besorolását a webhely-helyreállításban.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### Alapértelmezett (alapértelmezett)
```
Get-AzureRmSiteRecoveryStorageClassification [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByName
```
Get-AzureRmSiteRecoveryStorageClassification -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByFriendlyName
```
Get-AzureRmSiteRecoveryStorageClassification -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByFabricObject
```
Get-AzureRmSiteRecoveryStorageClassification -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByServerObject
```
Get-AzureRmSiteRecoveryStorageClassification -Server <ASRServer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **Get-AzureRmSiteRecoveryStorageClassification** parancsmag a tárolási besorolásokat az Azure webhely-helyreállításban kapja meg.

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

### -Szövet
```yaml
Type: ASRFabric
Parameter Sets: ByFabricObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Típusú megjelenített
Annak a tárolási osztályozásnak a rövid nevét adja meg, amelyre a parancsmag bekerül.

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
Annak a tárolási osztályozásnak a nevét adja meg, amelyre a parancsmag bekerül.

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

### -Server
```yaml
Type: ASRServer
Parameter Sets: ByServerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### ASRFabric
A "szövet" paraméter az "ASRFabric" típusú értéket fogadja el a csővezetékről

### ASRServer
A ' kiszolgáló ' paraméter elfogadja a "ASRServer" típusú értéket a csővezetékről

## KIMENETEK

### System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. SiteRecovery. ASRStorageClassification]

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

