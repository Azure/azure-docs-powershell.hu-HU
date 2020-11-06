---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6493186F-064B-45B7-8DFD-7799B1F2E5C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNode.md
ms.openlocfilehash: a902c88c53736f1e0db238cdb53ea381e5e887a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492042"
---
# Get-AzureRmAutomationDscNode

## Áttekintés
Az automatizálásból kapja a DSC csomópontokat.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### ByAll (alapértelmezett)
```
Get-AzureRmAutomationDscNode [-Status <DscNodeStatus>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ById
```
Get-AzureRmAutomationDscNode -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByName
```
Get-AzureRmAutomationDscNode [-Status <DscNodeStatus>] -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByNodeConfiguration
```
Get-AzureRmAutomationDscNode [-Status <DscNodeStatus>] -NodeConfigurationName <String>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByConfiguration
```
Get-AzureRmAutomationDscNode -ConfigurationName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmAutomationDscNode** parancsmag az Azure automatizálási rendszerének megfelelő állami konfigurációs (DSC) csomópontokat kapja.

## Példák

### 1. példa: az összes DSC csomópont beolvasása
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

Ez a parancs a Contoso17 nevű automatizálási fiók összes DSC csomópontjának metaadatait kapja.

### 2. példa: a DSC-csomópontok beszerzése DSC-konfigurációhoz
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

Ez a parancs a Contoso17 nevű automatizálási fiók összes DSC csomópontjának metaadatait kapja, amelyeket a DSC konfigurációs ContosoConfiguration generált DSC csomópont-konfigurációhoz társítanak.

### 3. példa: DSC-csomópont beszerzése AZONOSÍTÓval
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

Ez a parancs a Contoso17 nevű automatizálási fiókban megadott azonosítót tartalmazó DSC-csomópont metaadatait kapja.

### Példa 4: DSC csomópont beszerzése név alapján
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
```

Ez a parancs egy DSC-csomópont metaadatait kapja, a Computer14 nevű Contoso17 nevű automatizálási fiókban.

### Példa 5: az összes DSC csomópont beolvasása DSC-csomópont konfigurációjához
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeConfigurationName "ContosoConfiguration.webserver"
```

Ez a parancs metaadatokat kap a Contoso17 nevű automatizálási fiók összes DSC csomópontján, amelyek egy ContosoConfiguration. webszerver nevű DSC csomópont-konfigurációhoz vannak rendelve.

## PARAMÉTEREK

### -AutomationAccountName
Itt adhatja meg annak az automatizálási fióknak a nevét, amely a parancsmag által kapott DSC csomópontokat tartalmazza.

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

### -ConfigurationName
A DSC-konfiguráció nevét adja meg.
Ez a parancsmag olyan DSC csomópontokat kap, amelyek megfelelnek a paraméter által definiált konfigurációból létrehozott csomópont-konfigurációknak.

```yaml
Type: System.String
Parameter Sets: ByConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

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

### -Azonosító
Annak a DSC-csomópontnak az egyedi AZONOSÍTÓját adja meg, amelyre a parancsmag bekerül.

```yaml
Type: System.Guid
Parameter Sets: ById
Aliases: NodeId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (név)
Itt adhatja meg annak a DSC-csomópontnak a nevét, amely a parancsmagot kapja.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: NodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NodeConfigurationName
Itt adhatja meg annak a csomópont-konfigurációnak a nevét, amely a parancsmagot kapja.

```yaml
Type: System.String
Parameter Sets: ByNodeConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Annak a csoportnak a nevét adja meg, amelyben ez a parancsmag a DSC csomópontokat kapja.

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

### -Állapot
A parancsmag által kapott DSC csomópontok állapotát adja meg.
Az érvényes értékek a következők: 
- Kompatibilis 
- NotCompliant
- Sikertelen
- Függőben 
- Kapott
- Hűvös

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.DscNodeStatus
Parameter Sets: ByAll, ByName, ByNodeConfiguration
Aliases:
Accepted values: Compliant, NotCompliant, Failed, Pending, Received, Unresponsive

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. GUID

### System. String

## KIMENETEK

### Microsoft. Azure. Command. Automation. Model. DscNode

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Register-AzureRmAutomationDscNode](./Register-AzureRmAutomationDscNode.md)

[Set-AzureRmAutomationDscNode](./Set-AzureRmAutomationDscNode.md)

[Regisztráció törlése – AzureRmAutomationDscNode](./Unregister-AzureRmAutomationDscNode.md)


