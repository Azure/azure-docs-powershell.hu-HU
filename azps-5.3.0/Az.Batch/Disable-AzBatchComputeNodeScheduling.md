---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2DF5FB4D-A5CB-439C-AC6F-DF2130AF33EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 9e93d6fd17d4ba308e6d5752554fb03639fce769
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478425"
---
# Disable-AzBatchComputeNodeScheduling

## SYNOPSIS
Letiltja a tevékenységütemezést a megadott számítási csomóponton.

## SZINTAXIS

### Id (Default)
```
Disable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String>
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Disable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>]
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Disable-AzBatchComputeNodeScheduling** parancsmag letiltja a feladatütemezést a megadott számítási csomóponton.
A számítási csomópont egy adott alkalmazásterheléshez dedikált Azure virtuális gép.
Ha egy számítási csomóponton letiltja a tevékenységütemezést, eldöntheti azt is, hogy mit kell tenni a csomópont feladatsorában lévő feladatokkal.
**Az Disable-AzBatchComputeNodeScheduling** segítségével az alábbi lehetőségek közül választhat: 
- Bontsa le a tevékenységeket, és helyezze vissza őket a várólistára.
Ez lehetővé teszi, hogy ezeket a feladatokat átütemezték egy másik számítási csomóponton. 
- Bontsa le a feladatokat, és távolítsa el őket a várólistáról.
Az ily módon leállított tevékenységeket a projekt nem ütemezi át. 
- Várja meg, amíg az összes jelenleg végrehajtott feladat befejeződik, majd tiltsa le a tevékenységütemezést a számítási csomóponton. 
- Várja meg, amíg az összes futó feladat befejeződik, az adatmegőrzési időszakok lejárnak, majd tiltsa le a tevékenységütemezést a számítási csomóponton.

## PÉLDÁK

### 1. példa: Feladatütemezés letiltása számítási csomóponton
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Disable-AzBatchComputeNodeScheduling -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

Ezek a parancsok letiltják a tevékenység ütemezését a számítási csomópont tvm-1783593343_34-20151117t22514z.
Ehhez a példában az első parancs létrehoz egy objektumhivatkozást a contosobatchaccount kötegfiók fiókkulcsára.
Ezt az objektumhivatkozást egy $context.
A második parancs ezután ezt az objektumhivatkozást és a **Disable-AzBatchComputeNodeScheduling** parancsmagot használva csatlakozik a sajátPool készlethez, és letiltja a feladatok ütemezését a node tvm-1783593343_34-20151117t22514z.
Mivel a *DisableComputeNodeSchedulingOptions* paraméter nem tartalmazta a számítási csomóponton jelenleg futó feladatokat, a rendszer újra le fogja tiltani.

### 2. példa: Tevékenységütemezés letiltása egy készlet összes számítási csomópontja számára
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Disable-AzBatchComputeNodeScheduling -BatchContext $Context
```

Ezek a parancsok letiltják a tevékenység ütemezését a készlet Pool06 összes számítógépcsomópontját.
A feladat végrehajtásához a példában az első parancs létrehoz egy objektumhivatkozást a contosobatchaccount kötegfiók fiókkulcsára.
Ezt az objektumhivatkozást egy $context.
A példában a második parancs ezt az objektumhivatkozást és **a Get-AzBatchComputeNode-ot** használva visszaadja a Pool06-ban található összes számítási csomópont gyűjteményét.
Ezt a gyűjteményt ezután a **Disable-AzBatchComputeNodeScheduling** parancsmagra kapcsolja a rendszer, hogy letiltsa a feladatütemezést a gyűjtemény minden egyes számítási csomópontján.
Mivel a *DisableComputeNodeSchedulingOptions* paraméter nem tartalmazta a számítási csomópontokon jelenleg futó feladatokat, a rendszer újraszámít.

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
Objektumhivatkozást ad meg arra a számítási csomópontra, ahol a tevékenységütemezés le van tiltva.
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

### -DisableSchedulingOption
Azt adja meg, hogy ez a parancsmag hogyan foglalkozik a számítógép csomópontján jelenleg futó olyan feladatokkal, amelyekben az ütemezés le van tiltva.
A paraméter elfogadható értékei a következőek:
- Újraérték.
A feladatok azonnal leállnak, és visszakerülnek a várólistára.
Ez lehetővé teszi a feladatok átütemezét egy másik számítási csomóponton.
Ez az alapértelmezett érték. 
- Lezárás.
A tevékenységeket a rendszer azonnal leállja, és eltávolítja őket a várólistáról.
Ezek a tevékenységek nem lesznek átütemezve. 
- TaskCompletion.
A jelenleg futó feladatok még azelőtt befejeződnek, hogy a tevékenységütemezés le lenne tiltva a számítási csomóponton.
Ezen a csomóponton nem lesznek új feladatok ütemezve. 
- RetainedData.
A jelenleg futó feladatok befejeződnek, az adatmegőrzési időszakok pedig le fognak járni, mielőtt a tevékenységütemezés le lenne tiltva a számítási csomóponton.
Ezen a csomóponton nem lesznek új feladatok ütemezve.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.DisableComputeNodeSchedulingOption]
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, TaskCompletion

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id
Annak a számítási csomópontnak az azonosítója, ahol a tevékenységütemezés le van tiltva.

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
Annak a kötegkészletnek az azonosítója, amely azt a számítási csomópontot tartalmazza, ahol a tevékenységütemezés le van tiltva.
Ha a *PoolId paramétert használja,* ne használja a *ComputeNode* paramétert ugyanabban a parancsban.

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

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Enable-AzBatchComputeNodeScheduling](./Enable-AzBatchComputeNodeScheduling.md)


