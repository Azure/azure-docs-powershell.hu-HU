---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmss.md
ms.openlocfilehash: 623ebc278b2903fb0563c7ea196bd6123f495388
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014621"
---
# <span data-ttu-id="023d5-101">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="023d5-101">Set-AzVmss</span></span>

## <span data-ttu-id="023d5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="023d5-102">SYNOPSIS</span></span>
<span data-ttu-id="023d5-103">Meghatározott műveleteket határoz meg a megadott VMSS.</span><span class="sxs-lookup"><span data-stu-id="023d5-103">Sets specific actions on a specified VMSS.</span></span>

## <span data-ttu-id="023d5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="023d5-104">SYNTAX</span></span>

### <span data-ttu-id="023d5-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="023d5-105">DefaultParameter (Default)</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-TempDisk]
 [-Reimage] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="023d5-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="023d5-106">FriendMethod</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-ReimageAll]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="023d5-107">RedeployMethodParameter</span><span class="sxs-lookup"><span data-stu-id="023d5-107">RedeployMethodParameter</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Redeploy]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="023d5-108">PerformMaintenanceMethodParameter</span><span class="sxs-lookup"><span data-stu-id="023d5-108">PerformMaintenanceMethodParameter</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-PerformMaintenance] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="023d5-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="023d5-109">DESCRIPTION</span></span>
<span data-ttu-id="023d5-110">A **set-AzVmss** parancsmag meghatározott műveleteket állít be a virtuálisgép-készlet (VMSS) beállításnál.</span><span class="sxs-lookup"><span data-stu-id="023d5-110">The **Set-AzVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="023d5-111">A csak a parancsmag által támogatott műveletek a Reimage.</span><span class="sxs-lookup"><span data-stu-id="023d5-111">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="023d5-112">Példák</span><span class="sxs-lookup"><span data-stu-id="023d5-112">EXAMPLES</span></span>

### <span data-ttu-id="023d5-113">Példa 1: VMSS</span><span class="sxs-lookup"><span data-stu-id="023d5-113">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="023d5-114">Ez a parancs a ContosoGroup nevű erőforráscsoporthoz tartozó ContosoVMSS VMSS.</span><span class="sxs-lookup"><span data-stu-id="023d5-114">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="023d5-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="023d5-115">PARAMETERS</span></span>

### <span data-ttu-id="023d5-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="023d5-116">-AsJob</span></span>
<span data-ttu-id="023d5-117">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="023d5-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="023d5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="023d5-118">-DefaultProfile</span></span>
<span data-ttu-id="023d5-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="023d5-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="023d5-120">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="023d5-120">-InstanceId</span></span>
<span data-ttu-id="023d5-121">A virtuális gép példányának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="023d5-121">The instance ID of the virtual machine.</span></span>

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

### <span data-ttu-id="023d5-122">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="023d5-122">-PerformMaintenance</span></span>
<span data-ttu-id="023d5-123">Azt jelzi, hogy ez a parancsmag egy vagy több virtuális gépet végez karbantartással a VMSS.</span><span class="sxs-lookup"><span data-stu-id="023d5-123">Indicates that this cmdlet performs maintenance one or more virtual machines in the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PerformMaintenanceMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="023d5-124">-Redeploy</span><span class="sxs-lookup"><span data-stu-id="023d5-124">-Redeploy</span></span>
<span data-ttu-id="023d5-125">Azt jelzi, hogy a parancsmag áttelepíti egy vagy több virtuális gépet a VMSS.</span><span class="sxs-lookup"><span data-stu-id="023d5-125">Indicates that the cmdlet redeploys one or more virtual machines in the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="023d5-126">-Reimage</span><span class="sxs-lookup"><span data-stu-id="023d5-126">-Reimage</span></span>
<span data-ttu-id="023d5-127">Jelzi, hogy a parancsmag átadja a VMSS.</span><span class="sxs-lookup"><span data-stu-id="023d5-127">Indicates that the cmdlet reimages the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="023d5-128">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="023d5-128">-ReimageAll</span></span>
<span data-ttu-id="023d5-129">Jelzi, hogy a parancsmag a VMSS összes lemezét átadja.</span><span class="sxs-lookup"><span data-stu-id="023d5-129">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

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

### <span data-ttu-id="023d5-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="023d5-130">-ResourceGroupName</span></span>
<span data-ttu-id="023d5-131">A VMSS erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="023d5-131">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="023d5-132">-TempDisk</span><span class="sxs-lookup"><span data-stu-id="023d5-132">-TempDisk</span></span>
<span data-ttu-id="023d5-133">Itt adhatja meg, hogy a temp Disk-e.</span><span class="sxs-lookup"><span data-stu-id="023d5-133">Specifies whether to reimage temp disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="023d5-134">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="023d5-134">-VMScaleSetName</span></span>
<span data-ttu-id="023d5-135">Faj: annak a VMSS a neve, amelyhez a parancsmag a műveleteket állítja be.</span><span class="sxs-lookup"><span data-stu-id="023d5-135">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

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

### <span data-ttu-id="023d5-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="023d5-136">-Confirm</span></span>
<span data-ttu-id="023d5-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="023d5-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="023d5-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="023d5-138">-WhatIf</span></span>
<span data-ttu-id="023d5-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="023d5-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="023d5-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="023d5-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="023d5-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="023d5-141">CommonParameters</span></span>
<span data-ttu-id="023d5-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="023d5-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="023d5-143">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="023d5-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="023d5-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="023d5-144">INPUTS</span></span>

### <span data-ttu-id="023d5-145">System. String</span><span class="sxs-lookup"><span data-stu-id="023d5-145">System.String</span></span>

### <span data-ttu-id="023d5-146">System. string []</span><span class="sxs-lookup"><span data-stu-id="023d5-146">System.String[]</span></span>

## <span data-ttu-id="023d5-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="023d5-147">OUTPUTS</span></span>

### <span data-ttu-id="023d5-148">Microsoft. Azure. commands. számítási. Automation. models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="023d5-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="023d5-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="023d5-149">NOTES</span></span>

## <span data-ttu-id="023d5-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="023d5-150">RELATED LINKS</span></span>

[<span data-ttu-id="023d5-151">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="023d5-151">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="023d5-152">Új – AzVmss</span><span class="sxs-lookup"><span data-stu-id="023d5-152">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="023d5-153">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="023d5-153">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="023d5-154">Újraindítás – AzVmss</span><span class="sxs-lookup"><span data-stu-id="023d5-154">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="023d5-155">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="023d5-155">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="023d5-156">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="023d5-156">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="023d5-157">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="023d5-157">Update-AzVmss</span></span>](./Update-AzVmss.md)


