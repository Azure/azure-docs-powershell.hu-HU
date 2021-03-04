---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A39A415A-B403-48D3-AF80-CF7CFE382577
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchlocationquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchLocationQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchLocationQuota.md
ms.openlocfilehash: 297b862cb9491c0659d5fd2ec5ab0da4fc071e4b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922121"
---
# Get-AzBatchLocationQuota

## SYNOPSIS
Az adott helyen megkapja az előfizetés kötegszolgáltatásra vonatkozó kvótáját.

## SZINTAXIS

```
Get-AzBatchLocationQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A megadott előfizetés kötegszolgáltatáskvótáját kapja meg a megadott helyen.

## PÉLDÁK

### 1. példa: Az előfizetés kötegszolgáltatásra vonatkozó kvótáinak lekérte a nyugat-amerikai régiót
```
PS C:\>Get-AzBatchLocationQuota -Location "westus"
          AccountQuota Location
          ------------ --------
          1            westus
```

Ez a parancs a nyugat-amerikai régió aktuális előfizetésének kvótáját kapja meg.
A visszatérési érték azt jelzi, hogy ez az előfizetés csak egy Batch-fiókot hozhat létre az adott régióban.

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

### -Location
Azt a régiót adja meg, amelyhez a parancsmag a kvótát ellenőrzi.
További információt az Azure Régiók https://azure.microsoft.com/regions) ( .

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

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.Bat. Models.PSBatchLocationQuotas

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
