---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A1EA7D34-A8B4-4FA0-BD8C-3E846715AFBA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMPlan.md
ms.openlocfilehash: 40ecbc3c5b949ae8eda51f61637b515910e4c2cb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671225"
---
# Set-AzVMPlan

## Áttekintés
A piactér-terv adatait egy virtuális gépen állítja be.

## SZINTAXISA

```
Set-AzVMPlan [-VM] <PSVirtualMachine> [-Name] <String> [[-Product] <String>] [[-PromotionCode] <String>]
 [[-Publisher] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **set-AzVMPlan** parancsmag a virtuális gép Azure Marketplace csomagjának adatait állítja be.
Mielőtt a piactéren keresztül telepíteni szeretné a Piactért, a programozott hozzáférést engedélyeznie kell, vagy a virtuális gépet az Azure Portal segítségével kell telepítenie.

## Példák

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### -Name (név)
A piactéren a kép nevét adja meg.
Ez a Get-AzVMImageSku parancsmag által visszaadott érték.
A képinformációk megkereséséről további információt az Azure Virtual Machine-képek – a PowerShell és az Azure CLI https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ ( https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) a Microsoft Azure-dokumentáció) című témakörben talál.

```yaml
Type: System.String
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
Type: System.String
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
Type: System.String
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
Ezeket az információkat az Get-AzVMImagePublisher parancsmag segítségével találja meg.

```yaml
Type: System.String
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
A Virtual Machine-objektum beolvasásához az Get-AzVM parancsmagot használhatja.
A New-AzVMConfig parancsmag segítségével létrehozhatja a virtuálisgép-objektumokat.

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
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

### Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine

### System. String

## KIMENETEK

### Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzVM](./Get-AzVM.md)

[Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md)

[Get-AzVMImageSku](./Get-AzVMImageSku.md)

[Új – AzVMConfig](./New-AzVMConfig.md)
