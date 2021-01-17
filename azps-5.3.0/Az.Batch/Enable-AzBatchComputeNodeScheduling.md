---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 36EB9CE6-EAC9-471C-97D6-14E882E0F710
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 9969388d51abb337030a8a732805ee1a15368ea7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478397"
---
# Enable-AzBatchComputeNodeScheduling

## SYNOPSIS
Engedélyezi a tevékenységek ütemezését a megadott számítási csomóponton.

## SZINTAXIS

### Id (Default)
```
Enable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Enable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
Az **Enable-AzBatchComputeNodeScheduling parancsmag** lehetővé teszi a feladat ütemezését a megadott számítási csomóponton.
A számítási csomópont egy adott alkalmazásterheléshez dedikált Azure virtuális gép.

## PÉLDÁK

### 1. példa: Feladatütemezés engedélyezése számítási csomóponton
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Enable-AzBatchComputeNodeScheduling  -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

Ezek a parancsok lehetővé teszik a feladatok ütemezését a számítási csomópont tvm-1783593343_34-20151117t22514z.
Ehhez a példában az első parancs létrehoz egy objektumhivatkozást, amely tartalmazza a contosobatchaccount kötegfiók fiókkulcsait.
Ezt az objektumhivatkozást egy $context.
A második parancs ezután ezt az objektumhivatkozást és az **Enable-AzBatchComputeNodeScheduling parancsmagot** használva csatlakozik a sajátPool készlethez, és engedélyezi a feladatok ütemezését a tvm-1783593343_34-20151117t22514z.

### 2. példa: Tevékenységütemezés engedélyezése egy készlet számítási csomópontjain
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Enable-AzBatchComputeNodeScheduling  -BatchContext $Context
```

Ezek a parancsok lehetővé teszik a tevékenység ütemezését a készlet Pool06-ban található összes számítási csomóponton.
A feladat végrehajtásához a példában az első parancs létrehoz egy objektumhivatkozást, amely tartalmazza a contosobatchaccount kötegfiók fiókkulcsait.
Ezt az objektumhivatkozást egy $context.
A példában a második parancs ezt az objektumhivatkozást és **a Get-AzBatchComputeNode-ot** használva visszaadja a Pool06-ban található összes számítási csomópont gyűjteményét.
Ez a gyűjtemény ezután az **Enable-AzBatchComputeNodeScheduling** parancsmagba lesz becsatolt, amely lehetővé teszi a feladat ütemezését a gyűjtemény minden egyes számítási csomópontján.

## PARAMETERS

### -BatchContext
Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatáshoz való interakcióhoz.
Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor a Batch szolgáltatás használata során az Azure Active Directory-hitelesítést fogja használni a rendszer. Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse ki a BatchAccountContext objektumot a hozzáférési kulcsokkal. Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja. A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.

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

### -ComputeNode
Objektumhivatkozást ad meg arra a számítási csomópontra, ahol engedélyezve van a tevékenységütemezés.
Ez az objektumhivatkozás a Get-AzBatchComputeNode segítségével jön létre, és a visszaadott számítási csomópont-objektumot egy változóban tárolja.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject
Aliases:

Required: False
Position: 0
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
Annak a számítási csomópontnak az azonosítója, ahol engedélyezve van a feladatütemezés.

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PoolId
Annak a kötegkészletnek az azonosítója, amely azt a számítási csomópontot tartalmazza, ahol a tevékenységütemezés engedélyezve van.

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.Commands.Bat. Models.PSComputeNode

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## KIMENETEK

### System.Void

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Disable-AzBatchComputeNodeScheduling](./Disable-AzBatchComputeNodeScheduling.md)


