---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVM.md
ms.openlocfilehash: 6e733bfecea9a054bbab3794ca61778894c613fe
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346314"
---
# <span data-ttu-id="04ff0-101">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="04ff0-101">Remove-AzVM</span></span>

## <span data-ttu-id="04ff0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04ff0-102">SYNOPSIS</span></span>
<span data-ttu-id="04ff0-103">Eltávolít egy virtuális gépet az Azure-ból.</span><span class="sxs-lookup"><span data-stu-id="04ff0-103">Removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="04ff0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="04ff0-104">SYNTAX</span></span>

### <span data-ttu-id="04ff0-105">ResourceGroupNameParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="04ff0-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzVM [-Name] <String> [-Force] [-NoWait] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04ff0-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="04ff0-106">IdParameterSetName</span></span>
```
Remove-AzVM [-Force] [-NoWait] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04ff0-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="04ff0-107">DESCRIPTION</span></span>
<span data-ttu-id="04ff0-108">A **Remove-AzVM** parancsmag eltávolít egy virtuális gépet az Azure-ból.</span><span class="sxs-lookup"><span data-stu-id="04ff0-108">The **Remove-AzVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="04ff0-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="04ff0-109">EXAMPLES</span></span>

### <span data-ttu-id="04ff0-110">1. példa: Virtuális gép eltávolítása</span><span class="sxs-lookup"><span data-stu-id="04ff0-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="04ff0-111">Ez a parancs eltávolítja a VirtualMachine07 nevű virtuális gépet az ResourceGroup11 erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="04ff0-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="04ff0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04ff0-112">PARAMETERS</span></span>

### <span data-ttu-id="04ff0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="04ff0-113">-AsJob</span></span>
<span data-ttu-id="04ff0-114">Futtasa a parancsmagot a háttérben, és adja vissza a feladatot az előrehaladás nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="04ff0-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="04ff0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04ff0-115">-DefaultProfile</span></span>
<span data-ttu-id="04ff0-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="04ff0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04ff0-117">-Force</span><span class="sxs-lookup"><span data-stu-id="04ff0-117">-Force</span></span>
<span data-ttu-id="04ff0-118">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="04ff0-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04ff0-119">-Id</span><span class="sxs-lookup"><span data-stu-id="04ff0-119">-Id</span></span>
<span data-ttu-id="04ff0-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="04ff0-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04ff0-121">-Name</span><span class="sxs-lookup"><span data-stu-id="04ff0-121">-Name</span></span>
<span data-ttu-id="04ff0-122">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="04ff0-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04ff0-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="04ff0-123">-NoWait</span></span>
<span data-ttu-id="04ff0-124">Elindítja a műveletet, és azonnal, a művelet befejezése előtt visszatér.</span><span class="sxs-lookup"><span data-stu-id="04ff0-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="04ff0-125">Ha meg szeretné állapítani, hogy a művelet sikeresen befejeződött-e, használjon más mechanizmust.</span><span class="sxs-lookup"><span data-stu-id="04ff0-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="04ff0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04ff0-126">-ResourceGroupName</span></span>
<span data-ttu-id="04ff0-127">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="04ff0-127">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04ff0-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="04ff0-128">-Confirm</span></span>
<span data-ttu-id="04ff0-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="04ff0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04ff0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04ff0-130">-WhatIf</span></span>
<span data-ttu-id="04ff0-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="04ff0-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04ff0-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="04ff0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04ff0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04ff0-133">CommonParameters</span></span>
<span data-ttu-id="04ff0-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04ff0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04ff0-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="04ff0-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04ff0-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="04ff0-136">INPUTS</span></span>

### <span data-ttu-id="04ff0-137">System.String</span><span class="sxs-lookup"><span data-stu-id="04ff0-137">System.String</span></span>

## <span data-ttu-id="04ff0-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="04ff0-138">OUTPUTS</span></span>

### <span data-ttu-id="04ff0-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="04ff0-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="04ff0-140">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="04ff0-140">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="04ff0-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="04ff0-141">NOTES</span></span>

## <span data-ttu-id="04ff0-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="04ff0-142">RELATED LINKS</span></span>

[<span data-ttu-id="04ff0-143">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="04ff0-143">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="04ff0-144">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="04ff0-144">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="04ff0-145">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="04ff0-145">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="04ff0-146">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="04ff0-146">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="04ff0-147">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="04ff0-147">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="04ff0-148">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="04ff0-148">Update-AzVM</span></span>](./Update-AzVM.md)


