---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 7D0D8B46-4BF0-47D5-9261-3306AEB9E7DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchsubtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSubtask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSubtask.md
ms.openlocfilehash: 463f19b5ed459f0c2b2f4a4fdeff40bf69db2682
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671465"
---
# Get-AzBatchSubtask

## Áttekintés
A megadott tevékenység altevékenység-információit kapja.

## SZINTAXISA

### ODataFilter (alapértelmezett)
```
Get-AzBatchSubtask [-JobId] <String> [-TaskId] <String> [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ParentObject
```
Get-AzBatchSubtask [[-Task] <PSCloudTask>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzBatchSubtask** parancsmag kikeresi a megadott tevékenység altevékenységi adatait.
Az altevékenységek párhuzamos feldolgozást biztosítanak az egyes tevékenységekhez, és lehetővé teszik a tevékenységek végrehajtásának és előrehaladásának pontos figyelését.

## Példák

### Példa 1: adott tevékenység összes altevékenységének visszaadása
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchSubtask -JobId "Job-01" -TaskID "myTask" -BatchContext $Context
```

Ezek a parancsok a tevékenységhez tartozó összes altevékenységet visszaadja az azonosító myTask.
Ehhez a példa első parancsa létrehoz egy objektumot a kötegelt fiók contosobatchaccount tartozó fiók kulcsaihoz.
Ez az objektum hivatkozás a $context nevű változóban tárolódik.
A második parancs ezt követően az Object Reference és a **Get-AzBatchSubtask** parancsmagot használja az myTask összes altevékenységének visszaadására, egy olyan tevékenységre, amely a projektfeladat-01 részeként fut.

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

### -JobId
Annak a tevékenységnek az AZONOSÍTÓját adja meg, amely a parancsmag altevékenységeit tartalmazza.

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxCount
A visszaadni kívánt altevékenységek maximális számát adja meg.
Ha a nulla (0) vagy annál kisebb értéket adja meg, a parancsmag nem használ felső határértéket.
Az alapértelmezett érték a 1000.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tevékenység
Megadja az objektum hivatkozását arra a tevékenységre, amely a parancsmag által visszaadott altevékenységeket tartalmazza.
Ez az objektum hivatkozás az Get-AzBatchTask parancsmag használatával jön létre, és a visszaadott objektumot egy változóban tárolja.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -TaskId
Annak a tevékenységnek az AZONOSÍTÓját adja meg, amelynek az altevékenysége ezt a parancsmagot adja eredményül.

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

### Microsoft.Azure.Commands.BatCH. Modellek. PSCloudTask

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## KIMENETEK

### Microsoft.Azure.Commands.BatCH. Modellek. PSSubtaskInformation

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzBatchTask](./Get-AzBatchTask.md)


