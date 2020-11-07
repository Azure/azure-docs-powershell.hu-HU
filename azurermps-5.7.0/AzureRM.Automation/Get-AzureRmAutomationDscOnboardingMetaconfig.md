---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: FB331566-AC13-4751-A600-3A0E576308C7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdsconboardingmetaconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscOnboardingMetaconfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscOnboardingMetaconfig.md
ms.openlocfilehash: 34dcb85de9520882b9202edd38ae2e44d1bcafee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680203"
---
# Get-AzureRmAutomationDscOnboardingMetaconfig

## Áttekintés
Meta-Configuration. MOF fájlokat hoz létre.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Get-AzureRmAutomationDscOnboardingMetaconfig [-OutputFolder <String>] [-ComputerName <String[]>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmAutomationDscOnboardingMetaconfig** PARANCSMAG az APS-hez szükséges állapot-konfiguráció (DSC) meta-konfigurációjának (MOF) fájljait hozza létre.
Ez a parancsmag minden megadott számítógépnévhez létrehoz egy. MOF fájlt.
A parancsmag létrehoz egy mappát a. MOF fájlok számára.
A mappa Set-DscLocalConfigurationManager parancsmagját futtathatja a következő számítógépeken az Azure automatizálási fiókba a DSC csomópontok segítségével.

## Példák

### 1. példa: fedélzeti kiszolgálók automatizálási DSC-nek
```
PS C:\>Get-AzureRmAutomationDscOnboardingMetaconfig -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ComputerName "Server01", "Server02" -OutputFolder "C:\Users\PattiFuller\Desktop" 
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
Type: String
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
Type: String[]
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Arra kényszeríti a parancsot, hogy ne kérjen megerősítést, és cserélje le a meglévő. MOF fájlokat is.

```yaml
Type: SwitchParameter
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
Type: String
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
Type: String
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
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs
Ez a parancsmag nem fogadja el a bevitelt.

## KIMENETEK

### Microsoft. Azure. Command. Automation. Model. DscOnboardingMetaconfig

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

