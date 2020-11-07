---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-AzVMGuestPolicyStatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
ms.openlocfilehash: c1bf608c76c547360d9d7a48f4ba74c1713ee049
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836101"
---
# Get-AzVMGuestPolicyStatus

## Áttekintés
Egy VM-hez rendelt "vendég konfigurációja" típusú kezdeményezéshez (részletesen) kapja a vendégek konfigurációs házirend-állapotát.
A kezdeményezés a "kezdeményezés" típusú definíciós házirend.

## SZINTAXISA

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

## Leírás
A Get-AzVMGuestPolicyStatus parancsmagban egy VM-hez rendelt "vendég konfigurációja" típusú kezdeményezéshez kapja meg a Guest Configuration Policy állapotát.
A kezdeményezés a "kezdeményezés" típusú definíciós házirend.
Ez a parancsmag a VM megfelelőségi állapotát és annak okait kapja meg, hogy miért nem kompatibilis a kezdeményezésben szereplő egyes házirendekkel.

## Példák

### Példa 1
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```

Megtudhatja, hogy miként szerezheti be a legújabb konfiguráció házirend-állapotát egy VM-hez.
Az állapot magában foglalja a VM megfelelőségi állapotát a "vendég konfigurációja" típus minden kezdeményezéséhez, a megfelelőségi vizsgálat időpontját, a megfelelőségi vizsgálat időpontját, a megfelelőségi vizsgálat során ellenőrzött erőforrás-információkat.
Az eredmény a legújabb állapotokat tartalmazza, és nem tartalmazza az előző korábbi állapotokat.

### 2. példa
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

A legújabb konfiguráció-házirendek állapotának beszerzése kezdeményezési azonosítóval Az állapot magában foglalja a VM megfelelőségi állapotát a kezdeményezés minden házirendjéhez, megfelelőségi okok, a megfelelőségi ellenőrzés időpontja, a megfelelőségi vizsgálat során ellenőrzött erőforrás-adatok.
Az eredmény nem tartalmazza az előző állapotokat, de a kezdeményezés minden házirendjéhez csak a legújabb állapotot tartalmazza.

### 3. példa
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

A legújabb konfiguráció házirend-állapotának beszerzése a kezdeményezés neve szerint
Az állapot magában foglalja a VM megfelelőségi állapotát a kezdeményezés minden házirendjéhez, megfelelőségi okok, a megfelelőségi ellenőrzés időpontja, a megfelelőségi vizsgálat során ellenőrzött erőforrás-adatok.
Az eredmény nem tartalmazza az előző állapotokat, de a kezdeményezés minden házirendjéhez csak a legújabb állapotot tartalmazza.

### 4. példa
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ReportId "/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac"
```

A vendégek konfigurációs házirendjének állapotát ReportId érheti el.
A ReportId a ReportId tulajdonság, amely a initiativeId vagy Get-AzVMGuestPolicyStatus a kezdeményezés neve szerint (kérjük, további példákat is tartalmaz)

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

Required: True
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

### -ReportId
A vendég konfigurációja házirend-állapot azonosítója
Egy olyan házirend, ahol a definíció típusa a kezdeményezés és a kategória, a program a tartományhoz társítja a jogosultságokat.

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
Erőforráscsoporthoz tartozó név.

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
VM-név.

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs
## KIMENETEK

### Microsoft. Azure. Command. GuestConfiguration. models. PolicyStatusDetailed
## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
