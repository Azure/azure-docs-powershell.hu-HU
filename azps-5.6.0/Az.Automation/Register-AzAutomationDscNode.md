---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 73E6DF02-7171-481B-966F-DECEC122A602
online version: https://docs.microsoft.com/powershell/module/az.automation/register-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
ms.openlocfilehash: ceae5a9e7dec9913d90aae836784c6bfe66b680f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010005"
---
# Register-AzAutomationDscNode

## SYNOPSIS
Egy Windows operációs rendszert futtató Azure virtuális gépet regisztrál DSC-csomópontként egy automatizálási fiókhoz.

## SZINTAXIS

```
Register-AzAutomationDscNode -AzureVMName <String> [-NodeConfigurationName <String>]
 [-ConfigurationMode <String>] [-ConfigurationModeFrequencyMins <Int32>] [-RefreshFrequencyMins <Int32>]
 [-RebootNodeIfNeeded <Boolean>] [-ActionAfterReboot <String>] [-AllowModuleOverwrite <Boolean>]
 [-AzureVMResourceGroup <String>] [-AzureVMLocation <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Register-AzAutomationDscNode** parancsmag egy Azure Automation-fiókban APS-beli kívánt államkonfigurációs (DSC) csomópontként regisztrálja az Azure virtuális gépet. Ez a parancsmag csak a Windows operációs rendszert futtató gépeket regisztrálja automatizálási DSC-csomópontként egy fiókhoz.

Ha másik előfizetésben kell regisztrálnia egy csomópontot egy automatizálási fiókban, parancsmagok helyett egy ARM kell használnia. További [részleteket](https://docs.microsoft.com/azure/automation/automation-dsc-onboarding#registering-virtual-machines-across-azure-subscriptions) az Azure Automation dokumentációjában talál.

## PÉLDÁK

### 1. példa: Azure virtuális gép regisztrálása Azure DSC-csomópontként
```
PS C:\>Register-AzAutomationDscNode -AutomationAccountName "Contoso17" -AzureVMName "VirtualMachine01" -ResourceGroupName "ResourceGroup01"-NodeConfigurationName "ContosoConfiguration.webserver"
```

Ez a parancs regisztrálja a VirtualMachine01 nevű Azure virtuális gépet DSC-csomópontként a Contoso17 nevű automatizálási fiókban.

## PARAMETERS

### -ActionAfterReboot
A virtuális gép újraindítása után szükséges műveletet adja meg.
Érvényes értékek: 
- ContinueConfiguration 
- StopConfiguration

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ContinueConfiguration, StopConfiguration

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AllowModuleOverwrite
Meghatározza, hogy az új konfigurációk, amelyek ezt a DSC-csomópontot letöltik az Azure Automation DSC letöltő kiszolgálóról, lecserélik-e a célcsomóponton már meglévő modulokat.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AutomationAccountName
Annak az automatizálási fióknak a nevét adja meg, amelyben ez a parancsmag regisztrál egy virtuális gépet.

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

### -AzureVMLocation
Az Azure VM-hely.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AzureVMName
Annak az Azure-virtuális gépnek a neve, amely regisztrál az Azure Automation DSC-val való kezeléshez.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AzureVMResourceGroup
Az Azure VM-erőforráscsoport neve.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationMode
A DSC konfigurációs módját adja meg.
Érvényes értékek: 
- ApplyAndMonitor 
- ApplyAndAutocorrect 
- ApplyOnly

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ApplyAndMonitor, ApplyAndAutocorrect, ApplyOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationModeFrequencyMins
Azt adja meg percben, hogy a DSC háttéralkalmazása milyen gyakorisággal kísérli meg implementni az aktuális konfigurációt a célcsomóponton.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés

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

### -NodeConfigurationName
Annak a csomópont-konfigurációnak a nevét adja meg, amelynél ez a parancsmag beállítja a virtuális gépet az Azure Automation DSC-ból.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RebootNodeIfNeeded
Megadja, hogy szükség esetén újraindítsa-e a virtuális gépet.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RefreshFrequencyMins
Azt adja meg percben, hogy a helyi Configuration Manager milyen gyakorisággal lép kapcsolatba az Azure Automation DSC letöltőkiszolgálóval a legújabb csomópont-konfiguráció letöltéséhez.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Egy erőforráscsoport nevét adja meg.
Az az automatizálási fiók, amellyel ez a parancsmag regisztrál egy virtuális gépet, annak az erőforráscsoportnak a tagja, amelyet ez a paraméter megad.

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

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

### System.Int32

### System.Boolean

## KIMENETEK

### System.Void

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzAutomationDscNode](./Get-AzAutomationDscNode.md)

[Set-AzAutomationDscNode](./Set-AzAutomationDscNode.md)

[Unregister-AzAutomationDscNode](./Unregister-AzAutomationDscNode.md)


