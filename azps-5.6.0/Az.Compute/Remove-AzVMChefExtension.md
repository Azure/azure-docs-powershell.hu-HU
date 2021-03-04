---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 473C71A8-1DF7-487A-B239-B80E2BB63B82
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMChefExtension.md
ms.openlocfilehash: 56973d23e59a3d34b2caadce3677ca0bfd5f3c5e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929073"
---
# <span data-ttu-id="0023a-101">Remove-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="0023a-101">Remove-AzVMChefExtension</span></span>

## <span data-ttu-id="0023a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0023a-102">SYNOPSIS</span></span>
<span data-ttu-id="0023a-103">Eltávolítja a Bővítmény bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="0023a-103">Removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="0023a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0023a-104">SYNTAX</span></span>

### <span data-ttu-id="0023a-105">Linux</span><span class="sxs-lookup"><span data-stu-id="0023a-105">Linux</span></span>
```
Remove-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Linux] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0023a-106">Windows</span><span class="sxs-lookup"><span data-stu-id="0023a-106">Windows</span></span>
```
Remove-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Windows]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0023a-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0023a-107">DESCRIPTION</span></span>
<span data-ttu-id="0023a-108">A **Remove-AzVMChefExtension** parancsmag eltávolítja a Bővítmény bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="0023a-108">The **Remove-AzVMChefExtension** cmdlet removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="0023a-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0023a-109">EXAMPLES</span></span>

### <span data-ttu-id="0023a-110">1. példa: Bővítmény eltávolítása Windows virtuális gépről</span><span class="sxs-lookup"><span data-stu-id="0023a-110">Example 1: Remove a Chef extension from a Windows virtual machine</span></span>
```
PS C:\> Remove-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="0023a-111">Ez a parancs eltávolítja a Bővítmény bővítményt egy Windows-alapú, WindowsVM001 nevű virtuális gépről, amely az ResourceGroup001 nevű erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="0023a-111">This command removes a Chef extension from a Windows based virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="0023a-112">2. példa: Bővítmény eltávolítása Linux virtuális gépről</span><span class="sxs-lookup"><span data-stu-id="0023a-112">Example 2: Remove a Chef extension from a Linux virtual machine</span></span>
```
PS C:\> Remove-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="0023a-113">Ez a parancs eltávolítja a Bővítmény bővítményt egy Linux-alapú, LinuxVM001 nevű virtuális gépről, amely az ResourceGroup002 nevű erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="0023a-113">This command removes a Chef extension from a Linux based virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="0023a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0023a-114">PARAMETERS</span></span>

### <span data-ttu-id="0023a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0023a-115">-DefaultProfile</span></span>
<span data-ttu-id="0023a-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0023a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0023a-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="0023a-117">-Linux</span></span>
<span data-ttu-id="0023a-118">Azt jelzi, hogy ez a parancsmag egy Linuxos virtuális gépet célként használ.</span><span class="sxs-lookup"><span data-stu-id="0023a-118">Indicates that this cmdlet targets a Linux virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0023a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="0023a-119">-Name</span></span>
<span data-ttu-id="0023a-120">Annak a bővítménynek a nevét adja meg, amelyről a parancsmag eltávolítja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="0023a-120">Specifies the name of the Chef extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0023a-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0023a-121">-NoWait</span></span>
<span data-ttu-id="0023a-122">Elindítja a műveletet, és azonnal, a művelet befejezése előtt visszatér.</span><span class="sxs-lookup"><span data-stu-id="0023a-122">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="0023a-123">Ha meg szeretné állapítani, hogy a művelet sikeresen befejeződött-e, használjon más mechanizmust.</span><span class="sxs-lookup"><span data-stu-id="0023a-123">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="0023a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0023a-124">-ResourceGroupName</span></span>
<span data-ttu-id="0023a-125">A virtuális gépet tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0023a-125">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="0023a-126">-VMName</span><span class="sxs-lookup"><span data-stu-id="0023a-126">-VMName</span></span>
<span data-ttu-id="0023a-127">Annak a virtuális gépnek a nevét adja meg, amelynek a parancsmagja eltávolítja a Bővítmény bővítményt.</span><span class="sxs-lookup"><span data-stu-id="0023a-127">Specifies the name of a virtual machine for which this cmdlet removes the Chef extension.</span></span>

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

### <span data-ttu-id="0023a-128">-Windows</span><span class="sxs-lookup"><span data-stu-id="0023a-128">-Windows</span></span>
<span data-ttu-id="0023a-129">Azt jelzi, hogy ez a parancsmag egy Windows-virtuális gépre van kitűzve.</span><span class="sxs-lookup"><span data-stu-id="0023a-129">Indicates that this cmdlet targets a Windows virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0023a-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0023a-130">-Confirm</span></span>
<span data-ttu-id="0023a-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0023a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0023a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0023a-132">-WhatIf</span></span>
<span data-ttu-id="0023a-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0023a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0023a-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0023a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0023a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0023a-135">CommonParameters</span></span>
<span data-ttu-id="0023a-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0023a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0023a-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0023a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0023a-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0023a-138">INPUTS</span></span>

### <span data-ttu-id="0023a-139">System.String</span><span class="sxs-lookup"><span data-stu-id="0023a-139">System.String</span></span>

## <span data-ttu-id="0023a-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0023a-140">OUTPUTS</span></span>

### <span data-ttu-id="0023a-141">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0023a-141">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="0023a-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0023a-142">NOTES</span></span>

## <span data-ttu-id="0023a-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0023a-143">RELATED LINKS</span></span>

[<span data-ttu-id="0023a-144">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="0023a-144">Get-AzVMChefExtension</span></span>](./Get-AzVMChefExtension.md)

[<span data-ttu-id="0023a-145">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="0023a-145">Set-AzVMChefExtension</span></span>](./Set-AzVMChefExtension.md)
