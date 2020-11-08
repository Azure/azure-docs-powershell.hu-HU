---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: AF0DDDD0-B664-4AD8-A569-1363FB2EDB40
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmss.md
ms.openlocfilehash: ac961b4e7032d793cecb46008fe62091dca052f0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186770"
---
# <span data-ttu-id="65220-101">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="65220-101">Stop-AzVmss</span></span>

## <span data-ttu-id="65220-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="65220-102">SYNOPSIS</span></span>
<span data-ttu-id="65220-103">Leállítja a VMSS vagy a virtuális gépeket a VMSS belül.</span><span class="sxs-lookup"><span data-stu-id="65220-103">Stops the VMSS or a set of virtual machines within the VMSS.</span></span>

## <span data-ttu-id="65220-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="65220-104">SYNTAX</span></span>

### <span data-ttu-id="65220-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="65220-105">DefaultParameter (Default)</span></span>
```
Stop-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65220-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="65220-106">FriendMethod</span></span>
```
Stop-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-StayProvisioned] [-SkipShutdown] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="65220-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="65220-107">DESCRIPTION</span></span>
<span data-ttu-id="65220-108">A **stop-AzVmss** parancsmag a Virtual Machine Scale set (VMSS) vagy a virtuális gépek egy halmazán belül minden virtuális gépet leállítja.</span><span class="sxs-lookup"><span data-stu-id="65220-108">The **Stop-AzVmss** cmdlet stops all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="65220-109">A *InstanceId* paraméterrel kiválaszthatja a virtuális gépek halmazát.</span><span class="sxs-lookup"><span data-stu-id="65220-109">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="65220-110">Példák</span><span class="sxs-lookup"><span data-stu-id="65220-110">EXAMPLES</span></span>

### <span data-ttu-id="65220-111">1. példa: az összes virtuális gép leállítása a VMSS belül</span><span class="sxs-lookup"><span data-stu-id="65220-111">Example 1: Stop all the virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="65220-112">Ez a parancs a ContosoVMSS nevű VMSS tartozó összes virtuális gépet leállítja.</span><span class="sxs-lookup"><span data-stu-id="65220-112">This command stops all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="65220-113">2. példa: a virtuális gépek meghatározott halmazának leállítása a VMSS belül</span><span class="sxs-lookup"><span data-stu-id="65220-113">Example 2: Stop a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS" -InstanceId "3","5"
```

<span data-ttu-id="65220-114">Ez a parancs a ContosoVMSS nevű VMSS tartozó példánynév-karakterlánc tömbben meghatározott virtuális gépek meghatározott halmazát leállítja.</span><span class="sxs-lookup"><span data-stu-id="65220-114">This command stops a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="65220-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="65220-115">PARAMETERS</span></span>

### <span data-ttu-id="65220-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="65220-116">-AsJob</span></span>
<span data-ttu-id="65220-117">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="65220-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="65220-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65220-118">-DefaultProfile</span></span>
<span data-ttu-id="65220-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="65220-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65220-120">-Force</span><span class="sxs-lookup"><span data-stu-id="65220-120">-Force</span></span>
<span data-ttu-id="65220-121">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="65220-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="65220-122">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="65220-122">-InstanceId</span></span>
<span data-ttu-id="65220-123">Karakterláncként adja meg azt a virtuális gép-példányok AZONOSÍTÓját vagy azonosítóit, amelyekre a parancsmag leáll.</span><span class="sxs-lookup"><span data-stu-id="65220-123">Specifies, as a string array, the ID or IDs of the virtual machine instances that this cmdlet stops.</span></span>
<span data-ttu-id="65220-124">Például: `-InstanceId "0", "3"` .</span><span class="sxs-lookup"><span data-stu-id="65220-124">For instance: `-InstanceId "0", "3"`.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65220-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65220-125">-ResourceGroupName</span></span>
<span data-ttu-id="65220-126">A VMSS erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="65220-126">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="65220-127">-SkipShutdown</span><span class="sxs-lookup"><span data-stu-id="65220-127">-SkipShutdown</span></span>
<span data-ttu-id="65220-128">Nem kecses VM-leállás kérése</span><span class="sxs-lookup"><span data-stu-id="65220-128">To request non-graceful VM shutdown</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65220-129">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="65220-129">-StayProvisioned</span></span>
<span data-ttu-id="65220-130">Ha meg van adva, a virtuális gép bekapcsolja a leállítási állapotot.</span><span class="sxs-lookup"><span data-stu-id="65220-130">If specified, the virtual machine will enter stopped state.</span></span> <span data-ttu-id="65220-131">Ha nem adja meg, a virtuális gép beírja a leállított kihagyott állapotot.</span><span class="sxs-lookup"><span data-stu-id="65220-131">If not specified, the virtual machine will enter stopped-deallocated state.</span></span> <span data-ttu-id="65220-132">A rendszer továbbra is terheli a VMs-et a leállított állapotban, de nem a VMs esetében a leállított állapotban.</span><span class="sxs-lookup"><span data-stu-id="65220-132">The user is still charged for VMs in stopped state but not for VMs in stopped-deallocated state.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65220-133">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="65220-133">-VMScaleSetName</span></span>
<span data-ttu-id="65220-134">Annak a VMSS a nevét adja meg, amelyhez ez a parancsmag leállítja a virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="65220-134">Specifies the name of the VMSS for which this cmdlet stops the virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65220-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="65220-135">-Confirm</span></span>
<span data-ttu-id="65220-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="65220-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65220-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65220-137">-WhatIf</span></span>
<span data-ttu-id="65220-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="65220-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="65220-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="65220-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65220-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65220-140">CommonParameters</span></span>
<span data-ttu-id="65220-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="65220-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65220-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="65220-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65220-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="65220-143">INPUTS</span></span>

### <span data-ttu-id="65220-144">System. String</span><span class="sxs-lookup"><span data-stu-id="65220-144">System.String</span></span>

### <span data-ttu-id="65220-145">System. string []</span><span class="sxs-lookup"><span data-stu-id="65220-145">System.String[]</span></span>

## <span data-ttu-id="65220-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="65220-146">OUTPUTS</span></span>

### <span data-ttu-id="65220-147">Microsoft. Azure. commands. számítási. Automation. models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="65220-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="65220-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="65220-148">NOTES</span></span>

## <span data-ttu-id="65220-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="65220-149">RELATED LINKS</span></span>

[<span data-ttu-id="65220-150">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="65220-150">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="65220-151">Új – AzVmss</span><span class="sxs-lookup"><span data-stu-id="65220-151">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="65220-152">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="65220-152">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="65220-153">Újraindítás – AzVmss</span><span class="sxs-lookup"><span data-stu-id="65220-153">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="65220-154">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="65220-154">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="65220-155">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="65220-155">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="65220-156">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="65220-156">Update-AzVmss</span></span>](./Update-AzVmss.md)


