---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: FB331566-AC13-4751-A600-3A0E576308C7
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationdsconboardingmetaconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscOnboardingMetaconfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscOnboardingMetaconfig.md
ms.openlocfilehash: e520fec3d0299ca2b5f74bb2a8a8b7de437d7a2a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008150"
---
# Get-AzAutomationDscOnboardingMetaconfig

## SYNOPSIS
Metakonfigurációs .mof fájlokat hoz létre.

## SZINTAXIS

```
Get-AzAutomationDscOnboardingMetaconfig [-OutputFolder <String>] [-ComputerName <String[]>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzAutomationDscOnboardingMetaconfig** parancsmag létrehozza az APS-hez szükséges államkonfigurációs (DSC) metakonfigurációs Felügyelt objektumformátum (MOF) fájlokat.
Ez a parancsmag minden megadott számítógépnévhez létrehoz egy .mof fájlt.
A parancsmag létrehoz egy mappát az .mof fájloknak.
A mappa Set-DscLocalConfigurationManager futtatásával egy Azure Automation-fiókba, DSC-csomópontokként használhatja ezeket a számítógépeket.

## PÉLDÁK

### 1. példa: Onboard-kiszolgálók az Automatizálási DSC-nek
```
PS C:\>Get-AzAutomationDscOnboardingMetaconfig -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ComputerName "Server01", "Server02" -OutputFolder "C:\Users\PattiFuller\Desktop" 
PS C:\> Set-DscLocalConfigurationManager -Path "C:\Users\PattiFuller\Desktop\DscMetaConfigs" -ComputerName "Server01", "Server02"
```

Az első parancs a Contoso17 nevű automatizálási fiók két kiszolgálójának DSC-metakonfigurációs fájljait hozza létre.
A parancs ezeket a fájlokat asztali gépre menti.
A második parancs a **Set-DscLocalConfigurationManager** parancsmag segítségével alkalmazza a metakonfigurációt a megadott számítógépekre, hogy DSC-csomópontokként használják őket.

## PARAMETERS

### -AutomationAccountName
Egy automatizálási fiók nevét adja meg.
A Számítógépnév paraméter által  megadott számítógépek be vannak adva a paraméterben megadott fiókba.

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

### -ComputerName
Azoknak a számítógépeknek a tömbje, amelyekhez ez a parancsmag .mof fájlokat hoz létre.
Ha nem adja meg ezt a paramétert, a parancsmag .mof fájlt hoz létre az aktuális számítógéphez (localhost).

```yaml
Type: System.String[]
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

### -Force
A parancs futtatását kényszeríti anélkül, hogy megerősítést kérné, és lecseréli az azonos nevű meglévő .mof fájlokat.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OutputFolder
Annak a mappának a nevét adja meg, amelyben ez a parancsmag .mof fájlokat tárol.

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

### -ResourceGroupName
Egy erőforráscsoport nevét adja meg.
Ez a parancsmag .mof fájlokat hoz létre a számítógépére a paraméterként megadott erőforráscsoportban.

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

### -Confirm
A parancsmag futtatása előtt a rendszer megerősítést kér.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
A parancsmag futtatásakor a program megjeleníti, hogy mi történik.
A parancsmag nem fut.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

### System.String[]

## KIMENETEK

### Microsoft.Azure.Commands.Automation.Model.DscOnboardingMetaconfig

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
