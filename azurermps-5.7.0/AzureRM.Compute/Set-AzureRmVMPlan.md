---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: A1EA7D34-A8B4-4FA0-BD8C-3E846715AFBA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMPlan.md
ms.openlocfilehash: c6c17978840fd5c446d7d89350f1792091a5cffa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672158"
---
# Set-AzureRmVMPlan

## Áttekintés
A piactér-terv adatait egy virtuális gépen állítja be.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Set-AzureRmVMPlan [-VM] <PSVirtualMachine> [-Name] <String> [[-Product] <String>] [[-PromotionCode] <String>]
 [[-Publisher] <String>] [<CommonParameters>]
```

## Leírás
A **set-AzureRmVMPlan** parancsmag a virtuális gép Azure Marketplace csomagjának adatait állítja be.

Mielőtt a piactéren keresztül telepíteni szeretné a Piactért, a programozott hozzáférést engedélyeznie kell, vagy a virtuális gépet az Azure Portal segítségével kell telepítenie.

## Példák

## PARAMÉTEREK

### -Name (név)
A piactéren a kép nevét adja meg.
Ez a Get-AzureRmVMImageSku parancsmag által visszaadott érték.
A képinformációk megkereséséről további információt az [Azure Virtual Machine-képek, a PowerShell és az Azure CLI használata](https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) a Microsoft Azure dokumentációban című témakörben talál.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Szorzat
A piactéren a kép szorzatát adja meg.
Ez ugyanaz az információ, mint a **imageReference** elem **ajánlati** értéke.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PromotionCode
Egy előléptetési kódot ad meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Publisher
A kép közzétevőjét adja meg.
Ezeket az információkat az Get-AzureRmVMImagePublisher parancsmag segítségével találja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Annak a virtuális gépnek az objektumát adja meg, amelyhez a piactér-csomagot be szeretné állítani.
A Virtual Machine-objektum beolvasásához az Get-AzureRmVM parancsmagot használhatja.
A New-AzureRmVMConfig parancsmag segítségével létrehozhatja a virtuálisgép-objektumokat.

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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

[Get-AzureRmVM](./Get-AzureRmVM.md)

[Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md)

[Get-AzureRmVMImageSku](./Get-AzureRmVMImageSku.md)

[Új – AzureRmVMConfig](./New-AzureRmVMConfig.md)
