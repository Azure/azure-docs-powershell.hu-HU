---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 473C71A8-1DF7-487A-B239-B80E2BB63B82
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMChefExtension.md
ms.openlocfilehash: 79b16afbd6188682ff68ba5b2f2d9ccae67ff630
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144795"
---
# <span data-ttu-id="1b79b-101">Remove-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="1b79b-101">Remove-AzVMChefExtension</span></span>

## <span data-ttu-id="1b79b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b79b-102">SYNOPSIS</span></span>
<span data-ttu-id="1b79b-103">Eltávolítja a Bővítmény bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="1b79b-103">Removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="1b79b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1b79b-104">SYNTAX</span></span>

### <span data-ttu-id="1b79b-105">Linux</span><span class="sxs-lookup"><span data-stu-id="1b79b-105">Linux</span></span>
```
Remove-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Linux] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b79b-106">Windows</span><span class="sxs-lookup"><span data-stu-id="1b79b-106">Windows</span></span>
```
Remove-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Windows]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b79b-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1b79b-107">DESCRIPTION</span></span>
<span data-ttu-id="1b79b-108">A **Remove-AzVMChefExtension** parancsmag eltávolítja a Bővítmény bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="1b79b-108">The **Remove-AzVMChefExtension** cmdlet removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="1b79b-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1b79b-109">EXAMPLES</span></span>

### <span data-ttu-id="1b79b-110">1. példa: Bővítmény eltávolítása Windows virtuális gépről</span><span class="sxs-lookup"><span data-stu-id="1b79b-110">Example 1: Remove a Chef extension from a Windows virtual machine</span></span>
```
PS C:\> Remove-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="1b79b-111">Ez a parancs eltávolítja a Bővítmény bővítményt egy Windows-alapú, WindowsVM001 nevű virtuális gépről, amely az ResourceGroup001 nevű erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="1b79b-111">This command removes a Chef extension from a Windows based virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="1b79b-112">2. példa: Bővítmény eltávolítása Linux virtuális gépről</span><span class="sxs-lookup"><span data-stu-id="1b79b-112">Example 2: Remove a Chef extension from a Linux virtual machine</span></span>
```
PS C:\> Remove-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="1b79b-113">Ez a parancs eltávolítja a Bővítmény bővítményt egy Linux-alapú, LinuxVM001 nevű virtuális gépről, amely az ResourceGroup002 nevű erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="1b79b-113">This command removes a Chef extension from a Linux based virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="1b79b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b79b-114">PARAMETERS</span></span>

### <span data-ttu-id="1b79b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b79b-115">-DefaultProfile</span></span>
<span data-ttu-id="1b79b-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1b79b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b79b-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="1b79b-117">-Linux</span></span>
<span data-ttu-id="1b79b-118">Azt jelzi, hogy ez a parancsmag egy Linuxos virtuális gépet célként használ.</span><span class="sxs-lookup"><span data-stu-id="1b79b-118">Indicates that this cmdlet targets a Linux virtual machine.</span></span>

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

### <span data-ttu-id="1b79b-119">-Name</span><span class="sxs-lookup"><span data-stu-id="1b79b-119">-Name</span></span>
<span data-ttu-id="1b79b-120">Annak a bővítménynek a nevét adja meg, amelyről a parancsmag eltávolítja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="1b79b-120">Specifies the name of the Chef extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1b79b-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1b79b-121">-NoWait</span></span>
<span data-ttu-id="1b79b-122">Elindítja a műveletet, és azonnal, a művelet befejezése előtt visszatér.</span><span class="sxs-lookup"><span data-stu-id="1b79b-122">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="1b79b-123">Ha meg szeretné állapítani, hogy a művelet sikeresen befejeződött-e, használjon más mechanizmust.</span><span class="sxs-lookup"><span data-stu-id="1b79b-123">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="1b79b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b79b-124">-ResourceGroupName</span></span>
<span data-ttu-id="1b79b-125">A virtuális gépet tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1b79b-125">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="1b79b-126">-VMName</span><span class="sxs-lookup"><span data-stu-id="1b79b-126">-VMName</span></span>
<span data-ttu-id="1b79b-127">Annak a virtuális gépnek a nevét adja meg, amelynek a parancsmagja eltávolítja a Bővítmény bővítményt.</span><span class="sxs-lookup"><span data-stu-id="1b79b-127">Specifies the name of a virtual machine for which this cmdlet removes the Chef extension.</span></span>

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

### <span data-ttu-id="1b79b-128">-Windows</span><span class="sxs-lookup"><span data-stu-id="1b79b-128">-Windows</span></span>
<span data-ttu-id="1b79b-129">Azt jelzi, hogy ez a parancsmag egy windowsos virtuális gépre van kitűzve.</span><span class="sxs-lookup"><span data-stu-id="1b79b-129">Indicates that this cmdlet targets a Windows virtual machine.</span></span>

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

### <span data-ttu-id="1b79b-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1b79b-130">-Confirm</span></span>
<span data-ttu-id="1b79b-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1b79b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b79b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b79b-132">-WhatIf</span></span>
<span data-ttu-id="1b79b-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1b79b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b79b-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1b79b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b79b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b79b-135">CommonParameters</span></span>
<span data-ttu-id="1b79b-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b79b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b79b-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1b79b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b79b-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1b79b-138">INPUTS</span></span>

### <span data-ttu-id="1b79b-139">System.String</span><span class="sxs-lookup"><span data-stu-id="1b79b-139">System.String</span></span>

## <span data-ttu-id="1b79b-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1b79b-140">OUTPUTS</span></span>

### <span data-ttu-id="1b79b-141">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="1b79b-141">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="1b79b-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1b79b-142">NOTES</span></span>

## <span data-ttu-id="1b79b-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1b79b-143">RELATED LINKS</span></span>

[<span data-ttu-id="1b79b-144">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="1b79b-144">Get-AzVMChefExtension</span></span>](./Get-AzVMChefExtension.md)

[<span data-ttu-id="1b79b-145">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="1b79b-145">Set-AzVMChefExtension</span></span>](./Set-AzVMChefExtension.md)
