---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/repair-azvmssservicefabricupdatedomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Repair-AzVmssServiceFabricUpdateDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Repair-AzVmssServiceFabricUpdateDomain.md
ms.openlocfilehash: 43e92594d8a67dbb3ade0b66a065b8c6c097d60d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477701"
---
# <span data-ttu-id="d86ae-101">Repair-AzVmssServiceFabricUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="d86ae-101">Repair-AzVmssServiceFabricUpdateDomain</span></span>

## <span data-ttu-id="d86ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d86ae-102">SYNOPSIS</span></span>
<span data-ttu-id="d86ae-103">Manuális platformfrissítési tartomány walk to update virtual machines in a service fabric virtual machine scale set.</span><span class="sxs-lookup"><span data-stu-id="d86ae-103">Manual platform update domain walk to update virtual machines in a service fabric virtual machine scale set.</span></span>

## <span data-ttu-id="d86ae-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d86ae-104">SYNTAX</span></span>

### <span data-ttu-id="d86ae-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d86ae-105">DefaultParameter (Default)</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-PlatformUpdateDomain] <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d86ae-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="d86ae-106">ResourceIdParameter</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-PlatformUpdateDomain] <Int32> [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d86ae-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="d86ae-107">ObjectParameter</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-PlatformUpdateDomain] <Int32>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d86ae-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d86ae-108">DESCRIPTION</span></span>
<span data-ttu-id="d86ae-109">Kényszerítheti a manuális platformfrissítési tartománylépést virtuális gépek frissítésére egy szolgáltatáshálózat virtuális gépméret-készletében.</span><span class="sxs-lookup"><span data-stu-id="d86ae-109">Force manual platform update domain walk to update virtual machines in a service fabric virtual machine scale set.</span></span>

## <span data-ttu-id="d86ae-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d86ae-110">EXAMPLES</span></span>

### <span data-ttu-id="d86ae-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="d86ae-111">Example 1</span></span>
```
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -ResourceGroupName $rgname -VMScaleSetName $vmssName -PlatformUpdateDomain 0
```

<span data-ttu-id="d86ae-112">Ez a parancs kényszeríti a szolgáltatáshálózati háló frissítését az UD 0-on az erőforráscsoport neve és a méretkészlet neve által megadott virtuális gépi méretarányhoz.</span><span class="sxs-lookup"><span data-stu-id="d86ae-112">This command forces service fabric update walk on UD 0 for the virtual machine scale set specified by resource group name and scale set name.</span></span>

### <span data-ttu-id="d86ae-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="d86ae-113">Example 2</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $rgname -VMScaleSetName $vmssName
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -VirtualMachineScaleSet $vmss -PlatformUpdateDomain 1
```

<span data-ttu-id="d86ae-114">Ez a parancs kényszeríti a szolgáltatáshálózati háló frissítését az UD 1-en a virtuális gép méretarány-beállítási objektuma által megadott virtuális gép méretarányához.</span><span class="sxs-lookup"><span data-stu-id="d86ae-114">This command forces service fabric update walk on UD 1 for the virtual machine scale set specified by VM scale set object.</span></span>

### <span data-ttu-id="d86ae-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="d86ae-115">Example 3</span></span>
```
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -ResourceId $resourceId  -PlatformUpdateDomain 2;
```

<span data-ttu-id="d86ae-116">Ez a parancs kényszeríti a service fabric update walk on UD 2 for the virtual machine scale set by resource id.</span><span class="sxs-lookup"><span data-stu-id="d86ae-116">This command forces service fabric update walk on UD 2 for the virtual machine scale set specified by resource id.</span></span>

## <span data-ttu-id="d86ae-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d86ae-117">PARAMETERS</span></span>

### <span data-ttu-id="d86ae-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d86ae-118">-AsJob</span></span>
<span data-ttu-id="d86ae-119">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="d86ae-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d86ae-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d86ae-120">-DefaultProfile</span></span>
<span data-ttu-id="d86ae-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d86ae-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d86ae-122">-PlatformUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="d86ae-122">-PlatformUpdateDomain</span></span>
<span data-ttu-id="d86ae-123">Az a platformfrissítési tartomány, amelyhez manuális helyreállítási jár.</span><span class="sxs-lookup"><span data-stu-id="d86ae-123">The platform update domain for which a manual recovery walk is requested.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d86ae-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d86ae-124">-ResourceGroupName</span></span>
<span data-ttu-id="d86ae-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d86ae-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d86ae-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d86ae-126">-ResourceId</span></span>
<span data-ttu-id="d86ae-127">A virtuális gép méretaránykészletének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d86ae-127">The resource id for the virtual machine scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d86ae-128">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d86ae-128">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="d86ae-129">Local virtual machine scale set object</span><span class="sxs-lookup"><span data-stu-id="d86ae-129">Local virtual machine scale set object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d86ae-130">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="d86ae-130">-VMScaleSetName</span></span>
<span data-ttu-id="d86ae-131">A virtuális gép méretaránykészletének neve</span><span class="sxs-lookup"><span data-stu-id="d86ae-131">The name of the virtual machine scale set</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d86ae-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d86ae-132">-Confirm</span></span>
<span data-ttu-id="d86ae-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d86ae-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d86ae-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d86ae-134">-WhatIf</span></span>
<span data-ttu-id="d86ae-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d86ae-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d86ae-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d86ae-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d86ae-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d86ae-137">CommonParameters</span></span>
<span data-ttu-id="d86ae-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d86ae-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d86ae-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d86ae-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d86ae-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d86ae-140">INPUTS</span></span>

### <span data-ttu-id="d86ae-141">System.String</span><span class="sxs-lookup"><span data-stu-id="d86ae-141">System.String</span></span>

### <span data-ttu-id="d86ae-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d86ae-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="d86ae-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d86ae-143">OUTPUTS</span></span>

### <span data-ttu-id="d86ae-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSRecoverySzolgáltatásokatResponse</span><span class="sxs-lookup"><span data-stu-id="d86ae-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSRecoveryWalkResponse</span></span>

## <span data-ttu-id="d86ae-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d86ae-145">NOTES</span></span>

## <span data-ttu-id="d86ae-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d86ae-146">RELATED LINKS</span></span>
