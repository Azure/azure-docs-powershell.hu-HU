---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: DBA02017-8372-4A91-A4F1-985777DEDAB9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchnodefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchNodeFile.md
ms.openlocfilehash: a81d77ac1761c37dc3042394a4a70bda6848cc83
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672487"
---
# Remove-AzureBatchNodeFile

## Áttekintés
Törli a tevékenység vagy a számítási csomópont csomópont-fájlját.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### Tevékenység
```
Remove-AzureBatchNodeFile -JobId <String> -TaskId <String> -Path <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ComputeNode
```
Remove-AzureBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> -Path <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### InputObject
```
Remove-AzureBatchNodeFile [[-InputObject] <PSNodeFile>] [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Leírás
A **Remove-AzureBatchNodeFile** parancsmag egy Azure kötegfájl-csomópontot töröl egy tevékenységhez vagy egy kiszámított csomóponthoz.

## Példák

### 1. példa: assocated tartalmazó fájl törlése
```
PS C:\>Remove-AzureBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "wd\testFile.txt" -BatchContext $Context
```

Ez a parancs törli a wd\testFile.txt nevű csomópontot.
A fájl társítva van azzal a tevékenységgel, amelynek azonosító Task26 a Job Job-000001.

### 2. példa: fájl törlése egy számítási csomópontból
```
PS C:\>Remove-AzureBatchNodeFile -PoolId "Pool07" -ComputeNodeId "tvm-2316545714_1-20150725t213220z" -Path "startup\testFile.txt" -BatchContext $Context
```

Ez a parancs törli a startup\testFile.txt nevű csomópontot az azonosító Pool07 tartalmazó készlet meghatározott számítási csomópontról.

### 3. példa: fájl eltávolítása a csővezeték használatával
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "wd\testFile2.txt" -BatchContext $Context | Remove-AzureBatchNodeFile -Force -BatchContext $Context
```

Ez a parancs a **Get-AzureBatchNodeFile** használatával kapja meg a csomópontot.
A fájl társítva van azzal a tevékenységgel, amelynek azonosító Task26 a Job Job-000001.
A parancs a fájlt átadja az aktuális parancsmagnak a csővezeték használatával.
Az aktuális parancsmag eltávolítja a csomópontot tartalmazó fájlt.
A parancs az *erő* paramétert adja meg.
Ezért a parancs nem kér megerősítést.

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

### -ComputeNodeId
Annak a számítási csomópontnak az AZONOSÍTÓját adja meg, amely a parancsmag által törölt köteg csomópont-fájlt tartalmazza.

```yaml
Type: System.String
Parameter Sets: ComputeNode
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Force
Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Azt a **PSNodeFile** objektumot adja meg, amely a parancsmag által törölt csomópont-fájlt jelképezi.
Ha **PSNodeFile** szeretne beolvasni, használja az Get-AzureBatchNodeFile parancsmagot.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSNodeFile
Parameter Sets: InputObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -JobId
A tevékenységet tartalmazó feladat AZONOSÍTÓját adja meg.

```yaml
Type: System.String
Parameter Sets: Task
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path (elérési út)
A törlendő csomópont fájljának elérési útja.

```yaml
Type: System.String
Parameter Sets: Task, ComputeNode
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PoolId
Annak a készletnek az AZONOSÍTÓját adja meg, amely azokat a számítási csomópontokat tartalmazza, amelyeknek a parancsmagja eltávolítja a fájlt.

```yaml
Type: System.String
Parameter Sets: ComputeNode
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Rekurzív
Azt jelzi, hogy ez a parancsmag törli a mappát és az összes almappát és fájlt a megadott elérési úttal.
Ez a parancsmag csak akkor érvényes, ha az elérési út egy mappa.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TaskId
A tevékenység AZONOSÍTÓját adja meg.

```yaml
Type: System.String
Parameter Sets: Task
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
A parancsmag nem fut.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

### Microsoft.Azure.Commands.BatCH. Modellek. PSNodeFile
Paraméterek: InputObject (ByValue)

### Microsoft.Azure.Commands.Batch.BatchAccountContext
Paraméterek: BatchContext (ByValue)

## KIMENETEK

### System. Void

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[Get-AzureBatchNodeFile](./Get-AzureBatchNodeFile.md)

[Get-AzureBatchNodeFileContent](./Get-AzureBatchNodeFileContent.md)


