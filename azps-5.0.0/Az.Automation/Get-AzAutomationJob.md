---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BD32B909-296B-4E46-A24F-6E2BD4B9764B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJob.md
ms.openlocfilehash: 31390ccb19574b6b88c26828bf504dbc8ac5d924
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194830"
---
# Get-AzAutomationJob

## Áttekintés
Automatizálási runbook feladatokat kap.

## SZINTAXISA

### ByAll (alapértelmezett)
```
Get-AzAutomationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByJobId
```
Get-AzAutomationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByRunbookName
```
Get-AzAutomationJob -RunbookName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzAutomationJob** parancsmag runbook feladatokat kap az Azure automatizálásban.

## Példák

### Példa 1: konkrét runbook-feladat beszerzése
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b647
```

Ez a parancs a megadott GUID azonosítóval rendelkező feladatot kapja.

### 2. példa: a runbook minden feladatának beszerzése
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbook02"
```

Ez a parancs a Runbook02 nevű runbook társított összes feladatot megkapja.

### 3. példa: az összes futó feladat beszerzése
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Status "Running"
```

Ez a parancs a Contoso17 nevű automatizálási fiókból kapja meg az összes futó munkafolyamatot.

## PARAMÉTEREK

### -AutomationAccountName
Itt adhatja meg annak az automatizálási fióknak a nevét, amelyhez a parancsmag feladatait kapja.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

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

### -A befejezési időpont
A feladat befejezési időpontját adja meg **DateTimeOffset** -objektumként.
Megadhatja, hogy milyen karakterláncot Konvertáljon érvényes **DateTimeOffset**.
Ez a parancsmag olyan feladatokat kap, amelyeknek a záró időpontja a paramétert adja meg.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByRunbookName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Azonosító
Annak a projektnek az AZONOSÍTÓját adja meg, amely a parancsmagot kapja.

```yaml
Type: System.Guid
Parameter Sets: ByJobId
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Annak az erőforráscsoport a nevét adja meg, amelyben a parancsmag munkahelyeket kap.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RunbookName
Itt adhatja meg annak a runbook a nevét, amelynek a parancsmagja a feladatokat kapja.

```yaml
Type: System.String
Parameter Sets: ByRunbookName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kezdő időpont
A feladat kezdési időpontját adja meg **DateTimeOffset** -objektumként.
Ez a parancsmag olyan feladatokat kap, amelyeken a paraméter által megadott érték látható vagy azt követően.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByRunbookName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Állapot
Egy feladat állapotát adja meg.
Ez a parancsmag olyan munkafolyamatokat kap, amelyekhez az adott paraméter illik.
Az érvényes értékek a következők: 
- Aktiválása
- Kész
- Sikertelen
- Várólistán töltött
- Újrakezd
- Fut
- Kezdve
- Megállt
- Megállás
- Felfüggesztve
- Indokolva kéri

```yaml
Type: System.String
Parameter Sets: ByAll, ByRunbookName
Aliases:
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. GUID

### System. String

## KIMENETEK

### Microsoft. Azure. Command. Automation. Model. job

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzAutomationJobOutput](./Get-AzAutomationJobOutput.md)

[Önéletrajz – AzAutomationJob](./Resume-AzAutomationJob.md)

[Stop-AzAutomationJob](./Stop-AzAutomationJob.md)

[Felfüggesztés – AzAutomationJob](./Suspend-AzAutomationJob.md)


