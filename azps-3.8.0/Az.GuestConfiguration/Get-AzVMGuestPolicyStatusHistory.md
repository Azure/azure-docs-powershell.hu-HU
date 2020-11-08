---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-azvmguestpolicystatushistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
ms.openlocfilehash: 929bc417cf4b84800635b85e7f503972509aa7fc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011152"
---
# Get-AzVMGuestPolicyStatusHistory

## Áttekintés
A vendég konfigurációja házirend megfelelőségi előzményeit kapja egy VM-hez rendelt "Guest Configuration" típusú kezdeményezéshez.
A kezdeményezés a "kezdeményezés" típusú definíciós házirend.

## SZINTAXISA

### InitiativeNameScope (alapértelmezett)
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InitiativeIdScope
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [[-InitiativeId] <String>]
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A Get-AzVMGuestPolicyStatusHistory parancsmag a vendég konfigurációs házirendjeinek megfelelőségi előzményeit kapja egy VM-hez rendelt "Guest Configuration" típusú kezdeményezéshez.
A kezdeményezés a "kezdeményezés" típusú definíciós házirend.
Az Get-AzVMGuestPolicyStatus parancsmaggal az Get-AzVMGuestPolicyStatusHistory parancsmag kimenetében található ReportId használatával kaphat egyetlen megfelelőségi állapotot.

## Példák

### Példa 1
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af" -ShowOnlyChange
```

A megfelelőségi előzményeket a kezdeményezési azonosítóval kapja meg. a ShowOnlyChange kapcsoló csak a múltbeli állapotokat jeleníti meg.
Kihagyja azokat az állapotokat, amelyek nem változtak két megfelelőségi vizsgálat között.

### 2. példa
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17" -ShowOnlyChange
```

A megfelelőségi előzményeket a kezdeményezés neve alapján kapja meg.
A ShowOnlyChange-kapcsoló csak a múltbeli állapotok változásait jeleníti meg.
Kihagyja azokat az állapotokat, amelyek nem változtak két megfelelőségi vizsgálat között.

### 3. példa
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -ShowOnlyChange
```

A VM-be rendelt összes vendégfiók-konfigurációs házirend megfelelőségi előzményeit kapja.
A ShowOnlyChange-kapcsoló csak a múltbeli állapotok változásait jeleníti meg.
Kihagyja azokat az állapotokat, amelyek nem változtak két megfelelőségi vizsgálat között.

### 4. példa
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

A megfelelési előzményeket kezdeményezési azonosítóval kapja meg.

### Példa 5
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

A megfelelőségi előzményeket a kezdeményezés neve alapján kapja meg.

### 6. példa
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```
A VM-be rendelt összes vendégfiók-konfigurációs házirend megfelelőségi előzményeit kapja.

### 7. példa
```powershell
PS C:\>$x = Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
PS C:\>$x[10].ReportId
/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac
PS C:\> Get-AzVMGuestPolicyStatus -ReportId $x[10].ReportId
```

A vendégek konfigurációs házirendjének állapotát ReportId érheti el.
A ReportId a ReportId tulajdonság, amely a Get-AzVMGuestPolicyStatusHistory eredményei között található. (kérjük, olvassa el a további példákat)

## PARAMÉTEREK

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### -InitiativeId
Definíciós azonosító egy olyan házirendhez, amelyben a definíció típusa a kezdeményezés, a kategória pedig a vendég konfigurációja

```yaml
Type: System.String
Parameter Sets: InitiativeIdScope
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InitiativeName
Annak a házirendnek a neve, ahol a definíció típusa a kezdeményezés és a kategória a Guest Configuration

```yaml
Type: System.String
Parameter Sets: InitiativeNameScope
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Erőforráscsoporthoz tartozó név.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShowOnlyChange
A múltbeli állapot módosításait csak a vendégek konfigurációs házirendjeihez jeleníti meg.
Kihagyja azokat az állapotokat, amelyek nem változtak két megfelelőségi állapot naplózása között.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -VMName
VM-név.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs
## KIMENETEK

### Microsoft. Azure. Command. GuestConfiguration. models. PolicyStatus
## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
