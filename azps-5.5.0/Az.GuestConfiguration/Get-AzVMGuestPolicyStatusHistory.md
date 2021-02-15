---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-azvmguestpolicystatushistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
ms.openlocfilehash: 929bc417cf4b84800635b85e7f503972509aa7fc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204038"
---
# Get-AzVMGuestPolicyStatusHistory

## SYNOPSIS
A virtuális géphez hozzárendelt "Vendégkonfiguráció" típusú kezdeményezéshez a vendégkonfigurációs házirendek megfelelőségi állapotelőzményeit kapja meg.
A kezdeményezés a "Initiative" definíciótípusú házirend.

## SZINTAXIS

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

## LEÍRÁS
A Get-AzVMGuestPolicyStatusHistory parancsmag a virtuális géphez hozzárendelt "Vendégkonfiguráció" típusú kezdeményezéshez lekérte a vendégkonfigurációs házirendek megfelelőségi állapotelőzményeit.
A kezdeményezés a "Initiative" definíciótípusú házirend.
Egy Get-AzVMGuestPolicyStatus parancsmaggal lekértheti egyetlen megfelelőségi állapot részleteit a ReportId segítségével, amely egy parancsmag kimenetében Get-AzVMGuestPolicyStatusHistory található.

## PÉLDÁK

### 1. példa
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af" -ShowOnlyChange
```

Megfelelőségi állapotelőzményeket kap kezdeményezésazonosító alapján. A ShowOnlyChange kapcsoló csak a korábbi állapotváltozásokat jeleníti meg.
Kihagyja az állapotokat, amelyek nem változtak két megfelelőségi ellenőrzés között.

### 2. példa
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17" -ShowOnlyChange
```

Megfelelőségi állapotelőzményeket kap kezdeményezésnév szerint.
A ShowOnlyChange kapcsoló csak a korábbi állapotváltozásokat jeleníti meg.
Kihagyja az állapotokat, amelyek nem változtak két megfelelőségi ellenőrzés között.

### 3. példa
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -ShowOnlyChange
```

Megfelelőségi állapotelőzményeket kap a virtuális géphez rendelt összes vendégkonfigurációs házirendhez.
A ShowOnlyChange kapcsoló csak a korábbi állapotváltozásokat jeleníti meg.
Kihagyja az állapotokat, amelyek nem változtak két megfelelőségi ellenőrzés között.

### 4. példa
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

Megfelelőségi állapotelőzményeket kap kezdeményezésazonosító alapján.

### 5. példa
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

Megfelelőségi állapotelőzményeket kap kezdeményezésnév szerint.

### 6. példa
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```
Megfelelőségi állapotelőzményeket kap a virtuális géphez rendelt összes vendégkonfigurációs házirendhez.

### 7. példa
```powershell
PS C:\>$x = Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
PS C:\>$x[10].ReportId
/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac
PS C:\> Get-AzVMGuestPolicyStatus -ReportId $x[10].ReportId
```

Vendégkonfigurációs házirend állapotának lekérte a ReportId alapján.
A ReportId a ReportId tulajdonság, amely a Get-AzVMGuestPolicyStatusHistory eredményében található. (kérjük, adjon meg további példákat)

## PARAMETERS

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

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
Annak a házirendnek a definícióazonosítója, amelyben a definíció típusa Kezdeményezés, a kategória pedig vendégkonfiguráció

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
Annak a házirendnek a neve, amelyben a definíció típusa Kezdeményezés, a kategória pedig vendégkonfiguráció

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
Erőforráscsoport neve.

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
Csak a vendégkonfigurációs házirendek előzményállapot-módosításait jeleníti meg.
Kihagyja az olyan állapotokat, amelyek nem változtak két megfelelőségi állapot-ellenőrzés futtatása között.

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
VM neve.

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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Nincs
## KIMENETEK

### Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatus
## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
