---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A1EA7D34-A8B4-4FA0-BD8C-3E846715AFBA
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMPlan.md
ms.openlocfilehash: 9d3897b52d59c85caac3f68b9904878f14014606
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004550"
---
# Set-AzVMPlan

## SYNOPSIS
Beállítja a Piactér-terv adatait egy virtuális gépen.

## SZINTAXIS

```
Set-AzVMPlan [-VM] <PSVirtualMachine> [-Name] <String> [[-Product] <String>] [[-PromotionCode] <String>]
 [[-Publisher] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Set-AzVMPlan** parancsmag beállítja az Azure Piactér tervének adatait egy virtuális géphez.
Mielőtt üzembe helyezhetne egy Piactér-képet a parancssoron keresztül, engedélyeznie kell a programozott hozzáférést, vagy a virtuális gépet az Azure Portal használatával kell üzembe helyeznie.

## PÉLDÁK

## PARAMETERS

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

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

### -Name
A kép nevét adja meg a Piactérről.
Ez a parancsmag által visszaadott Get-AzVMImageSku érték.
A képinformációk keresésével kapcsolatos további információkért tekintse meg az Azure Virtuálisgép-képek navigálását és kiválasztását a PowerShell és az Azure CLI segítségével https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ (a https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) Microsoft Azure dokumentációjában).

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

### -Product
A kép termékét adja meg a Piactérről.
Ezek ugyanazok az információk, mint a **képReferencia** elem Ajánlat értéke. 

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
Megadja a promóciós kódot.

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
A kép közzétevője.
Ezek az információk a Get-AzVMImagePublisher segítségével találják meg.

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
Azt a virtuális gépobjektumot adja meg, amelyhez piactér-tervet kell beállítani.
A Get-AzVM virtuális gépi objektum beszerzéséhez használhatja a parancsmagot.
A New-AzVMConfig használhatja virtuális gépi objektum létrehozásához.

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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzVM](./Get-AzVM.md)

[Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md)

[Get-AzVMImageSku](./Get-AzVMImageSku.md)

[New-AzVMConfig](./New-AzVMConfig.md)
