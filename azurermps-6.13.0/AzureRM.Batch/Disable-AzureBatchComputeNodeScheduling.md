---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 2DF5FB4D-A5CB-439C-AC6F-DF2130AF33EC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/disable-azurebatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchComputeNodeScheduling.md
ms.openlocfilehash: 281e8a883474b3cb0f42b22de1bb00ef2f6e7249
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492019"
---
# Disable-AzureBatchComputeNodeScheduling

## Áttekintés
A megadott számítási csomóponton letiltja a tevékenység ütemezését.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### Azonosító (alapértelmezett)
```
Disable-AzureBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String>
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Disable-AzureBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>]
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **disable-AzureBatchComputeNodeScheduling** parancsmag letiltja a tevékenység ütemezését a megadott számítási csomóponton.
A számítási csomópont egy olyan Azure Virtual Machine, amely egy adott alkalmazási munkaterheléshez van hozzárendelve.
Ha egy számítási csomóponton letiltja a tevékenységek ütemezését, akkor azt is megadhatja, hogy mit szeretne tenni a csomópont tevékenység-várólistájában lévő munkahelyekről.
A **disable-AzureBatchComputeNodeScheduling** segítségével az alábbiakat végezheti el: 
- A feladatok megszüntetése és visszahelyezése a projekt várólistájába.
Ez lehetővé teszi, hogy ezek a feladatok egy másik számítási csomóponton átütemezve legyenek. 
- A feladatok megszüntetése és eltávolítása a projekt várólistájából.
Az ilyen módon leállított feladatok nem lesznek átütemezve. 
- Várjon, amíg a program végrehajtja az összes folyamatban lévő feladatot, majd tiltsa le a tevékenységek ütemezését a számítási csomóponton. 
- Várjon, amíg az összes futó tevékenység le nem fejeződik, és az összes adatmegőrzési időszak lejár, majd tiltsa le a tevékenység ütemezése beállítást a számítási csomóponton.

## Példák

### 1. példa: a tevékenység ütemezése le van tiltva egy számítási csomóponton
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Disable-AzureBatchComputeNodeScheduling -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

Ezek a parancsok letiltják a tevékenységek ütemtervét a számítási csomópont TVM – 1783593343_34 – 20151117t222514z.
Ehhez a példa első parancsa létrehoz egy objektumot a kötegelt fiók contosobatchaccount tartozó fiók kulcsaihoz.
Ez az objektum hivatkozás a $context nevű változóban tárolódik.
A második parancs ezt az objektumot használja, és a **disable-AzureBatchComputeNodeScheduling** parancsmag segítségével csatlakozik a Pool myPool, és letilthatja a TVM-1783593343_34-20151117t222514z.
Mivel a *DisableComputeNodeSchedulingOptions* paraméter nem szerepel a számítási csomóponton jelenleg futó feladatok újravárólistájában.

### 2. példa: a tevékenységek ütemezésének letiltása a teljes számítási csomóponton a készletben
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzureBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Disable-AzureBatchComputeNodeScheduling -BatchContext $Context
```

Ezekkel a parancsokkal letilthatja a tevékenységek ütemezését a köteg-Pool06 lévő összes számítógép-csomóponton.
A feladat végrehajtásához a példa első parancsa létrehoz egy objektumot a kötegelt fiók contosobatchaccount tartozó fiók kulcsaihoz.
Ez az objektum hivatkozás a $context nevű változóban tárolódik.
A példában szereplő második parancs az objektum-hivatkozással és a **Get-AzureBatchComputeNode** a Pool06 található összes számítási csomópont gyűjteményét adja eredményül.
A gyűjtemény ezután a **Letiltva, majd a le-AzureBatchComputeNodeScheduling** parancsmaggal letilthatja a tevékenységek ütemezését a gyűjtemény egyes számítási csomópontjain.
Mivel a *DisableComputeNodeSchedulingOptions* paraméter nem szerepel a számítási csomópontokon jelenleg futó feladatok újravárólistájában.

## PARAMÉTEREK

### -BatchContext
Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.
Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni. Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével. A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos. A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.

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
A számítási csomópontra mutató objektum hivatkozását adja meg, ahol a tevékenység ütemezése le van tiltva.
Ez az objektum hivatkozás az Get-AzureBatchComputeNode parancsmag használatával jön létre, és a visszaadott számítási csomópont objektumát egy változóban tárolja.

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
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableSchedulingOption
Itt adhatja meg, hogy ez a parancsmag hogyan foglalkozik az ütemezés letiltására szolgáló számítógép-csomóponton jelenleg futó feladatokkal.
A paraméter elfogadható értékei a következők:
- Újravárólista.
A feladatok azonnal leálltak, és visszatért a projekt várólistájába.
Ezzel lehetővé teszi, hogy a tevékenységeket egy másik számítási csomóponton át lehessen ütemezni.
Ez az alapértelmezett érték. 
- Lezáró.
A feladatok azonnal megszűnnek, és törlődnek a projekt várólistájáról.
Ezek a feladatok nem lesznek átütemezve. 
- TaskCompletion.
A jelenleg futó feladatok csak akkor fognak megjelenni, ha a tevékenység ütemezése le van tiltva a számítási csomóponton.
Ebben a csomópontban nem lesz új tevékenység ütemezve. 
- RetainedData.
A jelenleg futó feladatok teljes körűek és az adatmegőrzési időszakok a számítási csomóponton le lesznek tiltva, mielőtt a tevékenység ütemezése le van tiltva.
Ebben a csomópontban nem lesz új tevékenység ütemezve.

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

### -Azonosító
Annak a számítási csomópontnak az AZONOSÍTÓját adja meg, ahol a tevékenység ütemezése le van tiltva.

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
Annak a kötegelt készletnek az AZONOSÍTÓját adja meg, amely a tevékenység ütemezése letiltott számítási csomópontot tartalmazza.
Ha a *PoolId* paramétert használja, a *ComputeNode* paramétert ne használja ugyanezt a parancsot.

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Microsoft.Azure.Commands.BatCH. Modellek. PSComputeNode
Paraméterek: ComputeNode (ByValue)

### Microsoft.Azure.Commands.Batch.BatchAccountContext
Paraméterek: BatchContext (ByValue)

## KIMENETEK

### System. Void

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[Enable-AzureBatchComputeNodeScheduling](./Enable-AzureBatchComputeNodeScheduling.md)


