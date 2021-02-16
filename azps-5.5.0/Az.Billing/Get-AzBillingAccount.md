---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
ms.openlocfilehash: 21914793295f8ff000d02355fead1df718fcf052
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149250"
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
A **Get-AzBillingAccount** parancsmag számlázási fiókokat kap, és a felhasználó rendelkezik hozzáféréssel. 

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
Tartalmazza a számlázási fiók címét.

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
