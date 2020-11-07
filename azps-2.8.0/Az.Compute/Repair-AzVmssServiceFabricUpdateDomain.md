---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/repair-azvmssservicefabricupdatedomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Repair-AzVmssServiceFabricUpdateDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Repair-AzVmssServiceFabricUpdateDomain.md
ms.openlocfilehash: d593f7444d6a14c6dbff72ac3922265938d7816a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667270"
---
# <span data-ttu-id="5980a-101">Repair-AzVmssServiceFabricUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="5980a-101">Repair-AzVmssServiceFabricUpdateDomain</span></span>

## <span data-ttu-id="5980a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5980a-102">SYNOPSIS</span></span>
<span data-ttu-id="5980a-103">Kézi platform Update domain Walk to Update Virtual Machines a Service Fabric Virtual Machine Scale set.</span><span class="sxs-lookup"><span data-stu-id="5980a-103">Manual platform update domain walk to update virtual machines in a service fabric virtual machine scale set.</span></span>

## <span data-ttu-id="5980a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5980a-104">SYNTAX</span></span>

### <span data-ttu-id="5980a-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5980a-105">DefaultParameter (Default)</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-PlatformUpdateDomain] <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5980a-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="5980a-106">ResourceIdParameter</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-PlatformUpdateDomain] <Int32> [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5980a-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="5980a-107">ObjectParameter</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-PlatformUpdateDomain] <Int32>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5980a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="5980a-108">DESCRIPTION</span></span>
<span data-ttu-id="5980a-109">Kényszerítse a kézi platform frissítési tartományának a virtuális gépek frissítését a virtuális gép méretarányi készletében.</span><span class="sxs-lookup"><span data-stu-id="5980a-109">Force manual platform update domain walk to update virtual machines in a service fabric virtual machine scale set.</span></span>

## <span data-ttu-id="5980a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="5980a-110">EXAMPLES</span></span>

### <span data-ttu-id="5980a-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5980a-111">Example 1</span></span>
```
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -ResourceGroupName $rgname -VMScaleSetName $vmssName -PlatformUpdateDomain 0
```

<span data-ttu-id="5980a-112">Ez a parancs kényszeríti a Service Fabric Update Walk at UD 0 értékre a virtuális gép méretarányát, amelyet az erőforráscsoport neve és a méretarány neve határoz meg.</span><span class="sxs-lookup"><span data-stu-id="5980a-112">This command forces service fabric update walk on UD 0 for the virtual machine scale set specified by resource group name and scale set name.</span></span>

### <span data-ttu-id="5980a-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="5980a-113">Example 2</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $rgname -VMScaleSetName $vmssName
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -VirtualMachineScaleSet $vmss -PlatformUpdateDomain 1
```

<span data-ttu-id="5980a-114">Ez a parancs kényszeríti a Service Fabric Update Walk at UD 1 értékre a VM Scale set objektum által meghatározott virtuális gép méretarányát.</span><span class="sxs-lookup"><span data-stu-id="5980a-114">This command forces service fabric update walk on UD 1 for the virtual machine scale set specified by VM scale set object.</span></span>

### <span data-ttu-id="5980a-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="5980a-115">Example 3</span></span>
```
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -ResourceId $resourceId  -PlatformUpdateDomain 2;
```

<span data-ttu-id="5980a-116">Ez a parancs kényszeríti a Service Fabric Update Walk for UD 2 az erőforrás-azonosító által meghatározott virtuális gép méretarányát.</span><span class="sxs-lookup"><span data-stu-id="5980a-116">This command forces service fabric update walk on UD 2 for the virtual machine scale set specified by resource id.</span></span>

## <span data-ttu-id="5980a-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5980a-117">PARAMETERS</span></span>

### <span data-ttu-id="5980a-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5980a-118">-AsJob</span></span>
<span data-ttu-id="5980a-119">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="5980a-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5980a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5980a-120">-DefaultProfile</span></span>
<span data-ttu-id="5980a-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5980a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5980a-122">-PlatformUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="5980a-122">-PlatformUpdateDomain</span></span>
<span data-ttu-id="5980a-123">A platform frissítési tartománya, amelyhez kézi helyreállítási séta szükséges.</span><span class="sxs-lookup"><span data-stu-id="5980a-123">The platform update domain for which a manual recovery walk is requested.</span></span>

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

### <span data-ttu-id="5980a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5980a-124">-ResourceGroupName</span></span>
<span data-ttu-id="5980a-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5980a-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="5980a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5980a-126">-ResourceId</span></span>
<span data-ttu-id="5980a-127">A virtuálisgép-készlet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5980a-127">The resource id for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="5980a-128">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="5980a-128">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="5980a-129">Helyi virtuális gép méretarány beállítása objektum</span><span class="sxs-lookup"><span data-stu-id="5980a-129">Local virtual machine scale set object</span></span>

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

### <span data-ttu-id="5980a-130">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="5980a-130">-VMScaleSetName</span></span>
<span data-ttu-id="5980a-131">A virtuális gép méretarányának beállítása</span><span class="sxs-lookup"><span data-stu-id="5980a-131">The name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="5980a-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5980a-132">-Confirm</span></span>
<span data-ttu-id="5980a-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5980a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5980a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5980a-134">-WhatIf</span></span>
<span data-ttu-id="5980a-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5980a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5980a-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5980a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5980a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5980a-137">CommonParameters</span></span>
<span data-ttu-id="5980a-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5980a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5980a-139">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5980a-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5980a-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5980a-140">INPUTS</span></span>

### <span data-ttu-id="5980a-141">System. String</span><span class="sxs-lookup"><span data-stu-id="5980a-141">System.String</span></span>

### <span data-ttu-id="5980a-142">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="5980a-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="5980a-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5980a-143">OUTPUTS</span></span>

### <span data-ttu-id="5980a-144">Microsoft. Azure. commands. számítási. Automation. models. PSRecoveryWalkResponse</span><span class="sxs-lookup"><span data-stu-id="5980a-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSRecoveryWalkResponse</span></span>

## <span data-ttu-id="5980a-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5980a-145">NOTES</span></span>

## <span data-ttu-id="5980a-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5980a-146">RELATED LINKS</span></span>
