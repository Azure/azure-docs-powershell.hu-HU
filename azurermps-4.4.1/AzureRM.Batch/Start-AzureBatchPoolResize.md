---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 82DC8DC4-D8EC-4847-A54C-B779256FD590
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Start-AzureBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Start-AzureBatchPoolResize.md
ms.openlocfilehash: 558f8c062e60f6e9f7c18c05be8f1ccb2eafa9fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499200"
---
# Start-AzureBatchPoolResize

## Áttekintés
Elkezdi átméretezni a készletet.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Start-AzureBatchPoolResize [-Id] <String> -TargetDedicated <Int32> [-ResizeTimeout <TimeSpan>]
 [-ComputeNodeDeallocationOption <ComputeNodeDeallocationOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Start-AzureBatchPoolResize** parancsmag az Azure köteg-átméretezési műveletet kezdi a készletre.

## Példák

### 1. példa: a készlet átméretezése 12 csomópontra
```
PS C:\>Start-AzureBatchPoolResize -Id "ContosoPool06" -TargetDedicated 12 -BatchContext $Context
```

A parancs átméretezési műveletet indít az azonosító ContosoPool06 tartalmazó készleten.
A művelet célja 12 dedikált kiszámított csomópont.
A Get-AzureRmBatchAccountKeys parancsmaggal társítson egy környezetet a $Context változóhoz.

### 2. példa: a készlet átméretezése kifoglalási beállítás használatával
```
PS C:\>Get-AzureBatchPool -Id "ContosoPool06" -BatchContext $Context | Start-AzureBatchPoolResize -TargetDedicated 5 -ResizeTimeout ([TimeSpan]::FromHours(1)) -ComputeNodeDeallocationOption ([Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]::Terminate) -BatchContext $Context
```

Ez a parancsmag átméretezi a készletet öt dedikált kiszámított csomópontra.
A parancs a Get-AzureBatchPool parancsmag használatával az azonosító ContosoPool06 tartalmazó készletet kapja.
A parancs a pipeline operátorral továbbítja a készlet objektumát az aktuális parancsmaghoz.
A parancs átméretezési műveletet indít a készleten.
A cél öt külön kiszámított csomópont.
A parancs egy óra elteltével adja meg az időtúllépési időszakot.
A parancs a leállítási lehetőséget adja meg.

## PARAMÉTEREK

### -BatchContext
Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.
Ha az előfizetéshez hozzáférési kulcsokat tartalmazó **BatchAccountContext** objektumot szeretne beolvasni, használja az Get-AzureRmBatchAccountKeys parancsmagot.

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

### -ComputeNodeDeallocationOption
A parancsmag által elinduló átméretezési művelet kiosztási beállítását adja meg.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]
Parameter Sets: (All)
Aliases: 
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Azonosító
A parancsmag által átméretezett készlet AZONOSÍTÓját adja meg.

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

### -ResizeTimeout
Az átméretezési művelet időtúllépési időszakát adja meg.
Ha a készlet jelenleg nem éri el a cél méretét, az átméretezés művelet leáll.

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetDedicated
A dedikált számítási csomópontok cél számát adja meg.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### BatchAccountContext
A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről

### Karakterlánc
Az ' azonosító ' paraméter a pipeline "string" típusú értékét fogadja el.

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[Get-AzureBatchPool](./Get-AzureBatchPool.md)

[Stop-AzureBatchPoolResize](./Stop-AzureBatchPoolResize.md)

[Azure-köteg parancsmagok](./AzureRM.Batch.md)


