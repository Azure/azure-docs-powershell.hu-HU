---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B2B4E132-4A71-4DB8-A7B9-9ED3FE7EB292
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbginfoextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBginfoExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBginfoExtension.md
ms.openlocfilehash: d49fae13c69e194f0b31c702670639ce486dad81
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671237"
---
# <span data-ttu-id="69f39-101">Set-AzVMBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="69f39-101">Set-AzVMBginfoExtension</span></span>

## <span data-ttu-id="69f39-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="69f39-102">SYNOPSIS</span></span>
<span data-ttu-id="69f39-103">A BGInfo bővítmény felvétele egy virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="69f39-103">Adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="69f39-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="69f39-104">SYNTAX</span></span>

```
Set-AzVMBginfoExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69f39-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="69f39-105">DESCRIPTION</span></span>
<span data-ttu-id="69f39-106">A **set-AzVMBGInfoExtension** parancsmag hozzáadja a BGInfo bővítményt egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="69f39-106">The **Set-AzVMBGInfoExtension** cmdlet adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="69f39-107">Példák</span><span class="sxs-lookup"><span data-stu-id="69f39-107">EXAMPLES</span></span>

### <span data-ttu-id="69f39-108">Példa 1: a BGInfo bővítmény felvétele virtuális gépre</span><span class="sxs-lookup"><span data-stu-id="69f39-108">Example 1: Add the BGInfo extension for a virtual machine</span></span>
```
PS C:\> Set-AzVMBgInfoExtension -ResourceGroupName "ContosoRG" -VMName "ContosoVM" -Name "ExtensionName" -TypeHandlerVersion "2.1" -Location "West Europe"
```

<span data-ttu-id="69f39-109">Ez a parancs hozzáadja a BGInfo bővítményt a ContosoVM nevű virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="69f39-109">This command adds the BGInfo extension to virtual machine named ContosoVM.</span></span>
<span data-ttu-id="69f39-110">A parancs a virtuális gép erőforrás csoportját és helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="69f39-110">The command specifies the resource group and location of the virtual machine.</span></span>
<span data-ttu-id="69f39-111">A parancs a bővítmény nevét és verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="69f39-111">The command specifies the name and version of the extension.</span></span>

## <span data-ttu-id="69f39-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="69f39-112">PARAMETERS</span></span>

### <span data-ttu-id="69f39-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69f39-113">-DefaultProfile</span></span>
<span data-ttu-id="69f39-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="69f39-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69f39-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="69f39-115">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="69f39-116">Jelzi, hogy ez a parancsmag megakadályozza, hogy az Azure Guest Agent automatikusan frissítse a bővítményt egy újabb alverzióra.</span><span class="sxs-lookup"><span data-stu-id="69f39-116">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extension to a newer minor version.</span></span>
<span data-ttu-id="69f39-117">Ez a parancsmag alapértelmezés szerint lehetővé teszi, hogy a Guest Agent frissítse a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="69f39-117">By default, this cmdlet enables the guest agent to update the extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69f39-118">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="69f39-118">-ForceRerun</span></span>
<span data-ttu-id="69f39-119">Azt adja meg, hogy a bővítményt ugyanazzal a nyilvános vagy védett beállításokkal kell futtatni.</span><span class="sxs-lookup"><span data-stu-id="69f39-119">Specifies that the extension should be run again with the same public or protected settings.</span></span>
<span data-ttu-id="69f39-120">Az érték tetszőleges karakterlánc lehet, amely az aktuális értéktől eltérő lehet.</span><span class="sxs-lookup"><span data-stu-id="69f39-120">The value can be any string different from the current value.</span></span>
<span data-ttu-id="69f39-121">Ha a forceUpdateTag nem változik, a kezelő továbbra is alkalmazza a nyilvános vagy a védett beállításokra vonatkozó frissítéseket.</span><span class="sxs-lookup"><span data-stu-id="69f39-121">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="69f39-122">-Hely</span><span class="sxs-lookup"><span data-stu-id="69f39-122">-Location</span></span>
<span data-ttu-id="69f39-123">A virtuális gép helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="69f39-123">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="69f39-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="69f39-124">-Name</span></span>
<span data-ttu-id="69f39-125">Megadja annak a BGInfo-kiterjesztésnek a nevét, amelyet a parancsmag a virtuális gépre ad.</span><span class="sxs-lookup"><span data-stu-id="69f39-125">Specifies the name of the BGInfo extension that this cmdlet adds to a virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69f39-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69f39-126">-ResourceGroupName</span></span>
<span data-ttu-id="69f39-127">Annak a virtuális gépnek az erőforráscsoport nevét adja meg, amelyre a parancsmag hozzáadja a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="69f39-127">Specifies the name of the resource group of the virtual machine to which this cmdlet adds an extension.</span></span>

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

### <span data-ttu-id="69f39-128">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="69f39-128">-TypeHandlerVersion</span></span>
<span data-ttu-id="69f39-129">Annak a bővítménynek a verziószámát adja meg, amelyet a parancsmag a virtuális gépre ad.</span><span class="sxs-lookup"><span data-stu-id="69f39-129">Specifies the version of the extension that this cmdlet adds to the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69f39-130">-VMName</span><span class="sxs-lookup"><span data-stu-id="69f39-130">-VMName</span></span>
<span data-ttu-id="69f39-131">Annak a virtuális gépnek a neve, amelyhez a parancsmag hozzáadja az BGInfo bővítményt.</span><span class="sxs-lookup"><span data-stu-id="69f39-131">Specifies the name of the virtual machine to which this cmdlet adds the BGInfo extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69f39-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="69f39-132">-Confirm</span></span>
<span data-ttu-id="69f39-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="69f39-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69f39-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69f39-134">-WhatIf</span></span>
<span data-ttu-id="69f39-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="69f39-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69f39-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="69f39-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69f39-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69f39-137">CommonParameters</span></span>
<span data-ttu-id="69f39-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="69f39-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69f39-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69f39-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69f39-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="69f39-140">INPUTS</span></span>

### <span data-ttu-id="69f39-141">System. String</span><span class="sxs-lookup"><span data-stu-id="69f39-141">System.String</span></span>

### <span data-ttu-id="69f39-142">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="69f39-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="69f39-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="69f39-143">OUTPUTS</span></span>

### <span data-ttu-id="69f39-144">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="69f39-144">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="69f39-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="69f39-145">NOTES</span></span>

## <span data-ttu-id="69f39-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="69f39-146">RELATED LINKS</span></span>
