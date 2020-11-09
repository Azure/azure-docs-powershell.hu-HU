---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
ms.openlocfilehash: 21914793295f8ff000d02355fead1df718fcf052
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302123"
---
# Get-AzBillingAccount

## Áttekintés
Számlázási fiókok beszerzése

## SZINTAXISA

### Lista (alapértelmezett)
```
Get-AzBillingAccount [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Egyetlen
```
Get-AzBillingAccount -Name <System.Collections.Generic.List`1[System.String]> [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-ListEntitiesToCreateSubscription]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzBillingAccount** parancsmag számlázási fiókokat kap, a felhasználónak hozzáférése van. 

## Példák

### Példa 1
```
PS C:\> Get-AzBillingAccount
```

Az összes számlázási fiók beszerzése: a felhasználónak hozzáférése van.

### 2. példa
```
PS C:\> Get-AzBillingAccount -Name 00000000-0000-0000-0000-000000000000
```

A megadott nevű számlázási fiók beszerzése

### 3. példa
```
PS C:\> Get-AzBillingAccount -IncludeAddress
```

Az összes számlázási fiók beszerzése: a felhasználó hozzáféréssel rendelkezik, és felveheti a címet az eredménybe.

### 4. példa
```
PS C:\> Get-AzBillingAccount -ExpandBillingProfile
```

Az összes számlázási fiók beszerzése: a felhasználó hozzáférhet az eredményhez, és felveszi a számlázási profilokat.

### Példa 5
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection
```

Az összes számlázási fiók beszerzése: a felhasználó hozzáféréssel rendelkezik, és belefoglalhatja a számlázási profilokat és a számla szakaszokat az eredményben.

### 6. példa
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection -ExpandAddress -Name 00000000-0000-0000-0000-000000000000
```

Adja meg a megadott nevű számlázási fiókot, és adja meg a cím, a számlázási profilok és a számla szakaszt az eredményben.

## PARAMÉTEREK

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

### -IncludeAddress
Adja meg a Számlázási fiók címét.

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
Adja meg a számlázási profilokat a Számlázási fiók csoportban.

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
Adja meg a számlázási profilokat az alatta lévő számlázási fiók és számlák szakaszban.

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

### -Name (név)
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
A számlázási entitások listája a Számlázási fiók csoportban, amelyet az előfizetés létrehozásakor a bemenetként használhat.

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs

## KIMENETEK

### Microsoft. Azure. commands. számlázás. modellek. PSBillingAccount

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
