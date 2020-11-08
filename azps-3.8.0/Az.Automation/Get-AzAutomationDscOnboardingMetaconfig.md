---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: FB331566-AC13-4751-A600-3A0E576308C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdsconboardingmetaconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscOnboardingMetaconfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscOnboardingMetaconfig.md
ms.openlocfilehash: 007142cb854e2e428983f95d7bb7397c5a0ace39
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012695"
---
# Get-AzAutomationDscOnboardingMetaconfig

## Áttekintés
Meta-Configuration. MOF fájlokat hoz létre.

## SZINTAXISA

```
Get-AzAutomationDscOnboardingMetaconfig [-OutputFolder <String>] [-ComputerName <String[]>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **Get-AzAutomationDscOnboardingMetaconfig** PARANCSMAG az APS-hez szükséges állapot-konfiguráció (DSC) meta-konfigurációjának (MOF) fájljait hozza létre.
Ez a parancsmag minden megadott számítógépnévhez létrehoz egy. MOF fájlt.
A parancsmag létrehoz egy mappát a. MOF fájlok számára.
A mappa Set-DscLocalConfigurationManager parancsmagját futtathatja a következő számítógépeken az Azure automatizálási fiókba a DSC csomópontok segítségével.

## Példák

### 1. példa: fedélzeti kiszolgálók automatizálási DSC-nek
```
PS C:\>Get-AzAutomationDscOnboardingMetaconfig -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ComputerName "Server01", "Server02" -OutputFolder "C:\Users\PattiFuller\Desktop" 
PS C:\> Set-DscLocalConfigurationManager -Path "C:\Users\PattiFuller\Desktop\DscMetaConfigs" -ComputerName "Server01", "Server02"
```

Az első parancs a DSC meta-konfigurációs fájlokat hozza létre két kiszolgálón a Contoso17 nevű automatizálási fiókhoz.
A parancs a fájlokat egy asztalra menti.
A második parancs a **set-DscLocalConfigurationManager** parancsmagot használva alkalmazza a meta-konfigurációt a megadott számítógépekre a DSC-csomópontok bevezetéséhez.

## PARAMÉTEREK

### -AutomationAccountName
Az automatizálási fiók nevét adja meg.
Azok a számítógépek is bejelentkezhetnek, amelyekben a *számítógépnév* paraméter a paraméter által megadott fiókhoz van meghatározva.

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

### -Számítógépnév
Azoknak a számítógépeknek a tömböket adja meg, amelyekhez a parancsmag. MOF fájlokat hoz létre.
Ha nem adja meg ezt a paramétert, a parancsmag. MOF fájlt hoz létre az aktuális számítógép (localhost) számára.

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

### -Force
Arra kényszeríti a parancsot, hogy ne kérjen megerősítést, és cserélje le a meglévő. MOF fájlokat is.

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
Annak a mappának a nevét adja meg, ahol a parancsmag. MOF fájlokat tárol.

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
Ez a parancsmag a. MOF fájlokat hozza létre az erőforráscsoport azon alaplapi számítógépeihez, amelyeket ez a paraméter határoz meg.

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

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

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
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

### System. string []

## KIMENETEK

### Microsoft. Azure. Command. Automation. Model. DscOnboardingMetaconfig

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
