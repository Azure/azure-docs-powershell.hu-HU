---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 1246C3AC-A123-4EA1-B99E-458A85789109
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodereport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeReport.md
ms.openlocfilehash: 81a50a8c805d05b47b934b899eff708031ac6beb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180640"
---
# Get-AzAutomationDscNodeReport

## Áttekintés
A DSC csomópontról az automatizálásra küldött jelentéseket kapja.

## SZINTAXISA

### ByAll (alapértelmezett)
```
Get-AzAutomationDscNodeReport -NodeId <Guid> [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByLatest
```
Get-AzAutomationDscNodeReport -NodeId <Guid> [-Latest] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ById
```
Get-AzAutomationDscNodeReport -NodeId <Guid> -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzAutomationDscNodeReport** PARANCSMAG az APS-nek megfelelő állapotú (DSC) csomópontról az Azure automatizálásra küldött jelentéseket kapja.

## Példák

### Példa 1: a DSC-csomópont minden jelentésének beolvasása
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup14" -AutomationAccountName "Contoso17" -NodeId $Node.Id
```

Az első parancs a Computer14 nevű számítógép DSC csomópontját kapja a Contoso17 nevű automatizálási fiókban.
A parancs az objektumot a $Node változóban tárolja.
A második parancs a Computer14 nevű DSC csomópontról a Contoso17 nevű automatizálási fiókba küldött összes jelentés metaadatait kapja.
A parancs a csomópontot a $Node objektum **ID** tulajdonságával határozza meg.

### 2. példa: jelentés kérése DSC-csomóponthoz jelentés-AZONOSÍTÓval
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

Az első parancs a Computer14 nevű számítógép DSC csomópontját kapja a Contoso17 nevű automatizálási fiókban.
A parancs az objektumot a $Node változóban tárolja.
A második parancs a Computer14 nevű DSC csomóponttól a Contoso17 nevű automatizálási fiókhoz küldött megadott azonosító által azonosított jelentés metaadatait kapja.

### 3. példa: a legújabb jelentés beszerzése DSC-csomópontról
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Latest
```

Az első parancs a Computer14 nevű számítógép DSC csomópontját kapja a Contoso17 nevű automatizálási fiókban.
A parancs az objektumot a $Node változóban tárolja.
A második parancs a Computer14 nevű DSC csomóponttól a Contoso17 nevű automatizálási fiókba küldött legutóbbi jelentés metaadatait kapja.

## PARAMÉTEREK

### -AutomationAccountName
Az automatizálási fiók nevét adja meg.
Ez a parancsmag olyan DSC csomópontokra exportál jelentéseket, amelyek a paraméter által megadott fiókba tartoznak.

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
A befejezési időpontot adja meg.
Ez a parancsmag jelentést kap, amely az adott időpont előtt kapott automatizálást.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Azonosító
Itt adhatja meg az ehhez a parancsmaghoz készült DSC Node jelentés egyedi AZONOSÍTÓját.

```yaml
Type: System.Guid
Parameter Sets: ById
Aliases: ReportId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Legújabb
Jelzi, hogy ez a parancsmag csak a megadott csomópont legújabb DSC-jelentését kapja meg.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByLatest
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NodeId
Annak a DSC-csomópontnak az egyedi azonosítója, amelyhez a parancsmag jelentést kap.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Annak a DSC-csomópontnak a neve, amelyhez a parancsmag jelentést kap.

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

### -Kezdő időpont
Megadja a kezdés időpontját.
Ez a parancsmag jelentéseket kap, amelyeket az automatizálás után kapott.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. GUID

### System. null ' 1 [[System. DateTimeOffset, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]

### System. String

## KIMENETEK

### Microsoft. Azure. Command. Automation. Model. DscNode

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzAutomationDscNode](./Get-AzAutomationDscNode.md)

[Exportálás – AzAutomationDscNodeReportContent](./Export-AzAutomationDscNodeReportContent.md)


