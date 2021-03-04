---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3E736E85-0488-4D10-BEA1-4F9B8DA54C4B
online version: https://docs.microsoft.com/powershell/module/az.batch/stop-azbatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchPoolResize.md
ms.openlocfilehash: 339c3a537e84ff63a6eac0a6f1f63669ce4567ae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922529"
---
# Stop-AzBatchPoolResize

## SYNOPSIS
A készlet átméretezésének leállítja a műveletet.

## SZINTAXIS

```
Stop-AzBatchPoolResize [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Stop-AzBatchPoolResize** parancsmag leállít egy Azure Batch-átméretezési műveletet egy készleten.

## PÉLDÁK

### 1. példa: Készlet átméretezésének vége
```
PS C:\>Stop-AzBatchPoolResize -Id "ContosoPool06" -BatchContext $Context
```

Ez a parancs leállít egy átméretezési műveletet a ContosoPool06 azonosítójú készleten.
A Get-AzBatchAccountKey parancsmag használatával kontextust rendelhet a $Context változóhoz.

### 2. példa: Készlet átméretezésének leállítása a folyamat használatával
```
PS C:\>Get-AzBatchPool -Id "ContosoPool06" -BatchContext $Context | Stop-AzBatchPoolResize -BatchContext $Context
```

Ez a parancs leállítja a készlet átméretezését a folyamat műveleti operátorával.
A parancs a ContosoPool06 azonosítót használó készletet a Get-AzBatchPool parancsmag használatával kapja meg.
A parancs átadja a készletobjektumot az aktuális parancsmagnak.
A parancs leállítja az átméretezést a készleten.

## PARAMETERS

### -BatchContext
Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatáshoz való interakcióhoz.
Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor a Batch szolgáltatás használata során az Azure Active Directory-hitelesítést fogja használni a rendszer. Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse le a BatchAccountContext objektumot a hozzáférési kulcsokkal. Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja. A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

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

### -Id
Annak a készletnek az azonosítója, amelynek a parancsmagja leállítja az átméretezést.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## KIMENETEK

### System.Void

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Get-AzBatchPool](./Get-AzBatchPool.md)

[Start-AzBatchPoolResize](./Start-AzBatchPoolResize.md)

[Azure Batch-parancsmagok](/powershell/module/Az.Batch/)
