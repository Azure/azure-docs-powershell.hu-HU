---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 67FB5D02-4F4B-4119-B3AC-0D205247253E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchTask.md
ms.openlocfilehash: 09e2c8dd4ce1eab68eb2a4237e022034696f9769
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679746"
---
# Enable-AzureBatchTask

## Áttekintés
Tevékenység újraaktiválása

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### Azonosító
```
Enable-AzureBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObject
```
Enable-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
Az **enable-AzureBatchTask** parancsmag újraaktiválja a feladatot.
Ha egy tevékenység kimerítette az újrapróbálkozások számát, ez a parancsmag mégis lehetővé teszi a futtatását.

## Példák

### 1. példa: tevékenység újraaktiválása
```
PS C:\>Enable-AzureBatchTask -JobId "Job7" -Id "Task2" -BatchContext $Context
```

Ez a parancs újra aktiválja a tevékenység Task2 a munkahelyi Job7.

### 2. példa: tevékenység újraaktiválása a csővezeték használatával
```
PS C:\>Get-AzureBatchTask -JobId "Job8" -Id "Task3" -BatchContext $Context | Enable-AzureBatchTask -BatchContext $Context
```

Ez a parancs azt a kötegelt feladatot kapja meg, amely a Task3 azonosítóval rendelkezik, és az Get-AzureBatchTask parancsmagot használja.
A parancs a tevékenységet a pipeline operátorral továbbítja az aktuális parancsmaghoz.
A parancs újra aktiválja ezt a feladatot.

## PARAMÉTEREK

### -BatchContext
Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.
Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni. Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével. A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos. A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Azonosító
Az újraaktiválni kívánt tevékenység AZONOSÍTÓját adja meg.

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -JobId
A tevékenységet tartalmazó feladat AZONOSÍTÓját adja meg.

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tevékenység
A parancsmag által újraaktivált feladatot adja meg.
**PSCloudTask** objektum beolvasásához használja az Get-AzureBatchTask parancsmagot.

```yaml
Type: PSCloudTask
Parameter Sets: InputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
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

### BatchAccountContext
A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről

### PSCloudTask
A "tevékenység" paraméter elfogadja a "PSCloudTask" típusú értéket a csővezetékről

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[Get-AzureBatchTask](./Get-AzureBatchTask.md)

[Új – AzureBatchTask](./New-AzureBatchTask.md)

[Remove-AzureBatchTask](./Remove-AzureBatchTask.md)

[Set-AzureBatchTask](./Set-AzureBatchTask.md)

[Stop-AzureBatchTask](./Stop-AzureBatchTask.md)


