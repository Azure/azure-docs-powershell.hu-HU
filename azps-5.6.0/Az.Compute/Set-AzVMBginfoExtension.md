---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B2B4E132-4A71-4DB8-A7B9-9ED3FE7EB292
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmbginfoextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBginfoExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBginfoExtension.md
ms.openlocfilehash: 9b8eafaead04c2e2f727676c78bd717b1c6e97c2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941281"
---
# <span data-ttu-id="a9a90-101">Set-AzVMBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="a9a90-101">Set-AzVMBginfoExtension</span></span>

## <span data-ttu-id="a9a90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9a90-102">SYNOPSIS</span></span>
<span data-ttu-id="a9a90-103">Hozzáadja a BGInfo bővítményt egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="a9a90-103">Adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="a9a90-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a9a90-104">SYNTAX</span></span>

```
Set-AzVMBginfoExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9a90-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a9a90-105">DESCRIPTION</span></span>
<span data-ttu-id="a9a90-106">A **Set-AzVMBGInfoExtension** parancsmag hozzáadja a BGInfo kiterjesztést egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="a9a90-106">The **Set-AzVMBGInfoExtension** cmdlet adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="a9a90-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a9a90-107">EXAMPLES</span></span>

### <span data-ttu-id="a9a90-108">1. példa: A BGInfo bővítmény hozzáadása virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="a9a90-108">Example 1: Add the BGInfo extension for a virtual machine</span></span>
```
PS C:\> Set-AzVMBgInfoExtension -ResourceGroupName "ContosoRG" -VMName "ContosoVM" -Name "ExtensionName" -TypeHandlerVersion "2.1" -Location "West Europe"
```

<span data-ttu-id="a9a90-109">Ez a parancs hozzáadja a BGInfo bővítményt a ContosoVM nevű virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="a9a90-109">This command adds the BGInfo extension to virtual machine named ContosoVM.</span></span>
<span data-ttu-id="a9a90-110">A parancs megadja a virtuális gép erőforráscsoportját és helyét.</span><span class="sxs-lookup"><span data-stu-id="a9a90-110">The command specifies the resource group and location of the virtual machine.</span></span>
<span data-ttu-id="a9a90-111">A parancs a bővítmény nevét és verzióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a9a90-111">The command specifies the name and version of the extension.</span></span>

## <span data-ttu-id="a9a90-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9a90-112">PARAMETERS</span></span>

### <span data-ttu-id="a9a90-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9a90-113">-DefaultProfile</span></span>
<span data-ttu-id="a9a90-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a9a90-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9a90-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="a9a90-115">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="a9a90-116">Ez a parancsmag megakadályozza, hogy az Azure vendégügynök automatikusan frissítse a bővítményt egy újabb alverzióra.</span><span class="sxs-lookup"><span data-stu-id="a9a90-116">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extension to a newer minor version.</span></span>
<span data-ttu-id="a9a90-117">Ez a parancsmag alapértelmezés szerint lehetővé teszi a vendégügynöknek a bővítmény frissítését.</span><span class="sxs-lookup"><span data-stu-id="a9a90-117">By default, this cmdlet enables the guest agent to update the extension.</span></span>

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

### <span data-ttu-id="a9a90-118">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="a9a90-118">-ForceRerun</span></span>
<span data-ttu-id="a9a90-119">Azt adja meg, hogy a bővítményt újra futtatni kell ugyanazokkal a nyilvános vagy védett beállításokkal.</span><span class="sxs-lookup"><span data-stu-id="a9a90-119">Specifies that the extension should be run again with the same public or protected settings.</span></span>
<span data-ttu-id="a9a90-120">Az érték bármilyen karakterlánc lehet, amely nem az aktuális érték.</span><span class="sxs-lookup"><span data-stu-id="a9a90-120">The value can be any string different from the current value.</span></span>
<span data-ttu-id="a9a90-121">Ha a forceUpdateTag nem változik, a nyilvános vagy védett beállítások frissítéseit továbbra is alkalmazza a kezelő.</span><span class="sxs-lookup"><span data-stu-id="a9a90-121">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="a9a90-122">-Location</span><span class="sxs-lookup"><span data-stu-id="a9a90-122">-Location</span></span>
<span data-ttu-id="a9a90-123">A virtuális gép helyét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="a9a90-123">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="a9a90-124">-Name</span><span class="sxs-lookup"><span data-stu-id="a9a90-124">-Name</span></span>
<span data-ttu-id="a9a90-125">Annak a BGInfo kiterjesztésnek a nevét adja meg, amely a parancsmag virtuális géphez ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="a9a90-125">Specifies the name of the BGInfo extension that this cmdlet adds to a virtual machine.</span></span>

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

### <span data-ttu-id="a9a90-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a9a90-126">-NoWait</span></span>
<span data-ttu-id="a9a90-127">Elindítja a műveletet, és azonnal, a művelet befejezése előtt visszatér.</span><span class="sxs-lookup"><span data-stu-id="a9a90-127">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="a9a90-128">Ha meg szeretné állapítani, hogy a művelet sikeresen befejeződött-e, használjon más mechanizmust.</span><span class="sxs-lookup"><span data-stu-id="a9a90-128">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="a9a90-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9a90-129">-ResourceGroupName</span></span>
<span data-ttu-id="a9a90-130">Annak a virtuális gépnek az erőforráscsoportját adja meg, amelyhez a parancsmag bővítményt ad.</span><span class="sxs-lookup"><span data-stu-id="a9a90-130">Specifies the name of the resource group of the virtual machine to which this cmdlet adds an extension.</span></span>

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

### <span data-ttu-id="a9a90-131">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="a9a90-131">-TypeHandlerVersion</span></span>
<span data-ttu-id="a9a90-132">A bővítménynek azt a verzióját adja meg, amely a parancsmag hozzáadható a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="a9a90-132">Specifies the version of the extension that this cmdlet adds to the virtual machine.</span></span>

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

### <span data-ttu-id="a9a90-133">-VMName</span><span class="sxs-lookup"><span data-stu-id="a9a90-133">-VMName</span></span>
<span data-ttu-id="a9a90-134">Annak a virtuális gépnek a nevét adja meg, amelyhez ez a parancsmag hozzáadja a BGInfo kiterjesztést.</span><span class="sxs-lookup"><span data-stu-id="a9a90-134">Specifies the name of the virtual machine to which this cmdlet adds the BGInfo extension.</span></span>

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

### <span data-ttu-id="a9a90-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a9a90-135">-Confirm</span></span>
<span data-ttu-id="a9a90-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a9a90-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9a90-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9a90-137">-WhatIf</span></span>
<span data-ttu-id="a9a90-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a9a90-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9a90-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a9a90-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9a90-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9a90-140">CommonParameters</span></span>
<span data-ttu-id="a9a90-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9a90-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9a90-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a9a90-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9a90-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a9a90-143">INPUTS</span></span>

### <span data-ttu-id="a9a90-144">System.String</span><span class="sxs-lookup"><span data-stu-id="a9a90-144">System.String</span></span>

### <span data-ttu-id="a9a90-145">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a9a90-145">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a9a90-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9a90-146">OUTPUTS</span></span>

### <span data-ttu-id="a9a90-147">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="a9a90-147">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="a9a90-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a9a90-148">NOTES</span></span>

## <span data-ttu-id="a9a90-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a9a90-149">RELATED LINKS</span></span>
