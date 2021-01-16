---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 4B373447-3078-4C1F-932E-8337AB170DEB
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchpoolusagemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolUsageMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolUsageMetric.md
ms.openlocfilehash: 1700e20318a502f32386638f94a9c5c86c271d7d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322458"
---
# Get-AzBatchPoolUsageMetric

## SYNOPSIS
Készlethasználati metrikákat kap egy Batch-fiókhoz.

## SZINTAXIS

```
Get-AzBatchPoolUsageMetric [-StartTime <DateTime>] [-EndTime <DateTime>] [-Filter <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzBatchPoolUsageMetric** parancsmag a megadott fiók használati metrikákat kapja meg készlet szerint összesítve az egyes időintervallumokban.
Egy adott készlet és egy időtartomány statisztikáját is lekértheti.

## PÉLDÁK

### 1. példa: Készlethasználati metrikák lekérte egy időtartományra
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> $StartTime = Get-Date -Date "2016-05-16 00:00:00Z"
PS C:\> $EndTime = Get-Date -Date "2016-05-16 01:00:00Z"
PS C:\> Get-AzBatchPoolUsageMetric -StartTime $StartTime -EndTime $EndTime -BatchContext $context
DataEgressGiB      : 6.68875873088837E-06
DataIngressGiB     : 1.9485130906105E-05
EndTime            : 5/16/2016 12:30:00 AM
PoolId             : testpool1
StartTime          : 5/16/2016 12:00:00 AM
TotalCoreHours     : 8
VirtualMachineSize : standard_d4

DataEgressGiB      : 5.61587512493134E-06
DataIngressGiB     : 1.76150351762772E-05
EndTime            : 5/16/2016 12:30:00 AM
PoolId             : testpool2
StartTime          : 5/16/2016 12:00:00 AM
TotalCoreHours     : 12
VirtualMachineSize : standard_d4

DataEgressGiB      : 7.36676156520844E-06
DataIngressGiB     : 2.10804864764214E-05
EndTime            : 5/16/2016 1:00:00 AM
PoolId             : testpool1
StartTime          : 5/16/2016 12:30:00 AM
TotalCoreHours     : 7.99999999955555
VirtualMachineSize : standard_d4

DataEgressGiB      : 5.80586493015289E-06
DataIngressGiB     : 1.80602073669434E-05
EndTime            : 5/16/2016 1:00:00 AM
PoolId             : testpool2
StartTime          : 5/16/2016 12:30:00 AM
TotalCoreHours     : 11.9999999993333
VirtualMachineSize : standard_d4
```

Az első parancs létrehoz egy objektumhivatkozást a ContosoBatchAccount nevű kötegfiók fiókkulcsára a **Get-AzBatchAccountKey paranccsal.**
A parancs ezt az objektumhivatkozást a $Context tárolja.
A következő két parancs a **Get-Date** parancsmag használatával hoz létre DateTime-objektumokat.
A parancsok ezeket az értékeket a $StartTime és $EndTime tárolják a végleges parancshoz való használatra.
A végleges parancs a készlethasználati metrikákat adja vissza készlet szerint összesítve, a megadott kezdési és záró időpont közötti időintervallumon keresztül.

### 2. példa: Készlethasználati metrikák lekérte egy szűrő használatával
```
PS C:\>Get-AzBatchPoolUsageMetric -Filter "poolId eq 'ContosoPool'" -BatchContext $Context
DataEgressGiB      : 9.0496614575386E-06
DataIngressGiB     : 2.60043889284134E-05
EndTime            : 5/16/2016 5:30:00 PM
PoolId             : MyPool
StartTime          : 5/16/2016 5:00:00 PM
TotalCoreHours     : 12
VirtualMachineSize : standard_d4
```

Ez a parancs a ContosoPool nevű készlet használati metrikákat adja vissza.
A parancs meghatároz egy szűrő karakterláncot a készlet megadásához, és ugyanazt a $Context használja, mint az előző példában.

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

### -EndTime
Annak az időtartománynak a végét adja meg, amelyhez a parancsmag használati metrikákat kap.
Adjon meg egy legalább két órával korábban.
Ha nem ad meg záróidőt, ez a parancsmag a jelenleg rendelkezésre álló utolsó összegzési időközt használja.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Filter
Egy OData-szűrő záradékot ad meg a parancsmag által visszaadott metrikák szűréséhez.
Az egyetlen érvényes tulajdonság a **poolId** karakterlánc értékkel.
Lehetséges műveletek: eq, ge, gt, le, lt, startswith.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartTime
Azt az időtartományt adja meg, amelyhez a parancsmag használati metrikákat kap.
Adjon meg egy legalább két és fél órával korábban.
Ha nem ad meg kezdési időt, ez a parancsmag a jelenleg rendelkezésre álló utolsó összesítési időközt használja.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## KIMENETEK

### Microsoft.Azure.Commands.Bat. Models.PSPoolUsageMetrics

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Get-AzBatchPoolStatistics](./Get-AzBatchPoolStatistic.md)

[Get-AzBatchStatistics](./Get-AzBatchJobStatistic.md)
