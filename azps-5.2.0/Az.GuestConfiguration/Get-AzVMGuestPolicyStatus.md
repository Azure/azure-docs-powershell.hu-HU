---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-AzVMGuestPolicyStatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
ms.openlocfilehash: 49148f1c62b71436e48b2b92a4591a7cdb36cccf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335994"
---
# Get-AzVMGuestPolicyStatus

## SYNOPSIS
A virtuális géphez hozzárendelt "Vendégkonfiguráció" típusú kezdeményezés vendégkonfigurációs házirend-állapotát (részletes) kapja meg.
A kezdeményezés a "Initiative" definíciótípusú házirend.

## SZINTAXIS

### VmScope (alapértelmezett)
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InitiativeIdScope
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InitiativeNameScope
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ReportIdScope
```
Get-AzVMGuestPolicyStatus [-ReportId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A Get-AzVMGuestPolicyStatus parancsmag vendégkonfigurációs házirend-állapotokat kap egy virtuális géphez hozzárendelt "Vendégkonfiguráció" típusú kezdeményezéshez.
A kezdeményezés a "Initiative" definíciótípusú házirend.
Ez a parancsmag megfelelőségi állapotot kap a VM-ről, és annak okait, hogy miért nem felel meg a kezdeményezésben az egyes házirendek követelményeinek.

## PÉLDÁK

### 1. példa
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```

Szerezze be a vm összes legújabb vendégkonfigurációs házirend-állapotát.
Az állapot tartalmazza a virtuális gép megfelelőségi állapotát minden olyan kezdeményezésben, amely a "Vendégkonfiguráció" típusú kezdeményezésekre vonatkozik, megfelelőségi okokat, a megfelelőségi ellenőrzés idejét, valamint a megfelelőség szempontjából ellenőrzött erőforrás-információkat.
Az eredmények közé tartoznak a legutóbbi állapotok, a korábbi előzményállapotok nem.

### 2. példa
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

A legújabb vendégkonfigurációs házirend-állapotok lekérte kezdeményezésazonosító alapján. Az állapot tartalmazza a vm megfelelőségi állapotát a kezdeményezésben az egyes házirendek esetén, megfelelőségi okokat, a megfelelőségi ellenőrzés idejét, az erőforrás-információkat, amelyeket ellenőriztünk a megfelelőség szempontjából.
Az eredmények között nem szerepel a korábban létrehozott állapot, csak a kezdeményezésben található egyes házirendek legutóbbi állapota.

### 3. példa
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

A legújabb vendégkonfigurációs házirend-állapotok lekérte a kezdeményezés neve alapján.
Az állapot tartalmazza a vm megfelelőségi állapotát a kezdeményezésben az egyes házirendek esetén, megfelelőségi okokat, a megfelelőségi ellenőrzés idejét, az erőforrás-információkat, amelyeket ellenőriztünk a megfelelőség szempontjából.
Az eredmények között nem szerepel a korábban létrehozott állapot, csak a kezdeményezésben található egyes házirendek legutóbbi állapota.

### 4. példa
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ReportId "/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac"
```

Vendégkonfigurációs házirend állapotának lekérte a ReportId alapján.
A ReportId az a ReportId tulajdonság, amely a Get-AzVMGuestPolicyStatus initiativeId vagy Initiative név alapján (további példákat is tartalmaz)

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

Required: True
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

### -ReportId
Vendégkonfigurációs házirend-állapot azonosítója.
Egy olyan házirendet, amelyben a definíció típusa Kezdeményezés, a kategória pedig Vendégkonfiguráció, egy hatókörhöz kell hozzárendelni az állapotok lekért állapotának ellenőrzéshez.

```yaml
Type: System.String
Parameter Sets: ReportIdScope
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Erőforráscsoport neve.

```yaml
Type: System.String
Parameter Sets: VmScope, InitiativeIdScope, InitiativeNameScope
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VMName
VM neve.

```yaml
Type: System.String
Parameter Sets: VmScope, InitiativeIdScope, InitiativeNameScope
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Nincs
## KIMENETEK

### Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatusDetailed
## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
