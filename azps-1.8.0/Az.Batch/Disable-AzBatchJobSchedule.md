---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B4737AE8-F57C-4B95-B81E-74802EF8E7AE
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJobSchedule.md
ms.openlocfilehash: 59afa8f2ad5b1cf8739bece249d63574c8db6e4c
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93671909"
---
# Disable-AzBatchJobSchedule

## Áttekintés
Letilt egy kötegelt feladatok ütemezését.

## SZINTAXISA

```
Disable-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **disable-AzBatchJobSchedule** parancsmag letiltja az Azure-alapú kötegelt feladatok ütemezését.
Ha letiltja az ütemtervet, a feladatok nem az adott ütemterv szerint jönnek létre.
Később is engedélyezheti a letiltott ütemtervet.

## Példák

### 1. példa: munkabeosztás letiltása
```
PS C:\>Disable-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

Ez a parancs letiltja a JobSchedule17 azonosító munkabeosztást.
A **Get-AzBatchAccountKeys** parancsmaggal rendelhet környezetet a $Context változóhoz.

## PARAMÉTEREK

### -BatchContext
Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.
Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni. Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével. A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos. A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.

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
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### -Azonosító
Annak az ütemezésnek az AZONOSÍTÓját adja meg, amelyre a parancsmag letiltja.

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## KIMENETEK

### System. Void

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Enable-AzBatchJobSchedule](./Enable-AzBatchJobSchedule.md)

[Get-AzBatchAccountKeys](./Get-AzBatchAccountKey.md)

[Get-AzBatchJobSchedule](./Get-AzBatchJobSchedule.md)

[Új – AzBatchJobSchedule](./New-AzBatchJobSchedule.md)

[Remove-AzBatchJobSchedule](./Remove-AzBatchJobSchedule.md)

[Stop-AzBatchJobSchedule](./Stop-AzBatchJobSchedule.md)

[Azure-köteg parancsmagok](/powershell/module/az.batch)


