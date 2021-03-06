---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azbillingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
ms.openlocfilehash: 8c934adfd0bea950f97fbe8e8226568f9eaf57dc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922506"
---
# Get-AzBillingAccount

## SYNOPSIS
Számlázási fiókok lekérte.

## SZINTAXIS

### Lista (alapértelmezett)
```
Get-AzBillingAccount [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Single
```
Get-AzBillingAccount -Name <System.Collections.Generic.List`1[System.String]> [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-ListEntitiesToCreateSubscription]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzBillingAccount** parancsmag számlázási fiókokat kap, a felhasználónak hozzáférése van. 

## PÉLDÁK

### 1. példa
```
PS C:\> Get-AzBillingAccount
```

Szerezze be az összes számlázási fiókot, amelyhez a felhasználó hozzáfér.

### 2. példa
```
PS C:\> Get-AzBillingAccount -Name 00000000-0000-0000-0000-000000000000
```

Szerezze be a megadott nevű számlázási fiókot.

### 3. példa
```
PS C:\> Get-AzBillingAccount -IncludeAddress
```

Szerezze be az összes számlázási fiókot, amelyekhez a felhasználó hozzáfér, és az eredményben szerepeltetve tartalmazza a címet.

### 4. példa
```
PS C:\> Get-AzBillingAccount -ExpandBillingProfile
```

Szerezze be az összes olyan számlázási fiókot, amelyhez a felhasználó hozzáfér, és az eredményben szerepelteti a számlázási profilokat.

### 5. példa
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection
```

Szerezze be az összes számlázási fiókot, amelyhez a felhasználó hozzáfér, és az eredményben foglalja bele a számlázási profilokat és a számlaszakaszokat.

### 6. példa
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection -ExpandAddress -Name 00000000-0000-0000-0000-000000000000
```

Szerezze be a megadott nevű számlázási fiókot, és az eredményben adja meg a címet, a számlázási profilokat és a számlaszakaszokat.

## PARAMETERS

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

### -IncludeAddress
A számlázási fiók címét is fel kell venni.

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

### -ExpandBillingProfile
A számlázási fiókba foglalja bele a számlázási profilokat.

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

### -ExpandInvoiceSection
A számlázási profilokat a számlázási fiók és a számlák szakaszba foglalja bele.

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

### -Name
Egy adott számlázási fiók neve.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Single
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ListEntitiesToCreateSubscription
A számlázási fiókban sorolja fel azokat a számlázási entitásokat, amelyek bemenetként használhatók az előfizetés létrehozásához.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Nincs

## KIMENETEK

### Microsoft.Azure.Commands.Billing.Models.PSBillingAccount

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
