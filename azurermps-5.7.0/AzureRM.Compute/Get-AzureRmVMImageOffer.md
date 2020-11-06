---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImageOffer.md
ms.openlocfilehash: ccdc7ee8a63c0a633caf162f8549fd1ba737ce8e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503855"
---
# Get-AzureRmVMImageOffer

## Áttekintés
Beolvassa a VMImage kínálati típust.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Get-AzureRmVMImageOffer -Location <String> -PublisherName <String> [<CommonParameters>]
```

## Leírás
A **Get-AzureRmVMImageOffer** parancsmag a VMImage ajánlatok típusait kapja.

## Példák

### 1. példa: ajánlati típusok beszerzése Publisherhez
```
PS C:\> Get-AzureRmVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

Ez a parancs a közép-amerikai régióban a megadott közzétevőhöz tartozó ajánlati típusokat kapja meg.

## PARAMÉTEREK

### -Hely
A VMImage helyét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublisherName
A VMImage közzétevő nevét adja meg.
Publisher beolvasásához használja az Get-AzureRmVMImagePublisher parancsmagot.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs
Ez a parancsmag nem fogadja el a bevitelt.

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmVMImage](./Get-AzureRmVMImage.md)

[Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md)

[Get-AzureRmVMImageSku](./Get-AzureRmVMImageSku.md)

[Mentés-AzureRmVMImage](./Save-AzureRmVMImage.md)


