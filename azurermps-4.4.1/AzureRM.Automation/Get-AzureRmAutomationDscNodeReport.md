---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 1246C3AC-A123-4EA1-B99E-458A85789109
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeReport.md
ms.openlocfilehash: c3ae9da7959d606ec8ab92ed7a05e502d03b12a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498003"
---
# Get-AzureRmAutomationDscNodeReport

## Áttekintés
A DSC csomópontról az automatizálásra küldött jelentéseket kapja.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### ByAll (alapértelmezett)
```
Get-AzureRmAutomationDscNodeReport -NodeId <Guid> [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByLatest
```
Get-AzureRmAutomationDscNodeReport -NodeId <Guid> [-Latest] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ById
```
Get-AzureRmAutomationDscNodeReport -NodeId <Guid> -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmAutomationDscNodeReport** PARANCSMAG az APS-nek megfelelő állapotú (DSC) csomópontról az Azure automatizálásra küldött jelentéseket kapja.

## Példák

### Példa 1: a DSC-csomópont minden jelentésének beolvasása
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup14" -AutomationAccountName "Contoso17" -NodeId $Node.Id
```

Az első parancs a Computer14 nevű számítógép DSC csomópontját kapja a Contoso17 nevű automatizálási fiókban.
A parancs az objektumot a $Node változóban tárolja.

A második parancs a Computer14 nevű DSC csomópontról a Contoso17 nevű automatizálási fiókba küldött összes jelentés metaadatait kapja.
A parancs a csomópontot a $Node objektum **ID** tulajdonságával határozza meg.

### 2. példa: jelentés kérése DSC-csomóponthoz jelentés-AZONOSÍTÓval
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

Az első parancs a Computer14 nevű számítógép DSC csomópontját kapja a Contoso17 nevű automatizálási fiókban.
A parancs az objektumot a $Node változóban tárolja.

A második parancs a Computer14 nevű DSC csomóponttól a Contoso17 nevű automatizálási fiókhoz küldött megadott azonosító által azonosított jelentés metaadatait kapja.

### 3. példa: a legújabb jelentés beszerzése DSC-csomópontról
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Latest
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

## KIMENETEK

### Microsoft. Azure. Command. Automation. Model. DscNode

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmAutomationDscNode](./Get-AzureRmAutomationDscNode.md)

[Exportálás – AzureRmAutomationDscNodeReportContent](./Export-AzureRmAutomationDscNodeReportContent.md)


