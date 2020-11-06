---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmss.md
ms.openlocfilehash: 5fcb99a6e909675b47d245755ffd42e3c058a37a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494100"
---
# <span data-ttu-id="cf2d5-101">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="cf2d5-101">Set-AzureRmVmss</span></span>

## <span data-ttu-id="cf2d5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cf2d5-102">SYNOPSIS</span></span>
<span data-ttu-id="cf2d5-103">Meghatározott műveleteket határoz meg a megadott VMSS.</span><span class="sxs-lookup"><span data-stu-id="cf2d5-103">Sets specific actions on a specified VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf2d5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cf2d5-104">SYNTAX</span></span>

### <span data-ttu-id="cf2d5-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cf2d5-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf2d5-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="cf2d5-106">FriendMethod</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-ReimageAll] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf2d5-107">RedeployMethodParameter</span><span class="sxs-lookup"><span data-stu-id="cf2d5-107">RedeployMethodParameter</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Redeploy]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf2d5-108">PerformMaintenanceMethodParameter</span><span class="sxs-lookup"><span data-stu-id="cf2d5-108">PerformMaintenanceMethodParameter</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-PerformMaintenance] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cf2d5-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="cf2d5-109">DESCRIPTION</span></span>
<span data-ttu-id="cf2d5-110">A **set-AzureRmVmss** parancsmag meghatározott műveleteket állít be a virtuálisgép-készlet (VMSS) beállításnál.</span><span class="sxs-lookup"><span data-stu-id="cf2d5-110">The **Set-AzureRmVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="cf2d5-111">A csak a parancsmag által támogatott műveletek a Reimage.</span><span class="sxs-lookup"><span data-stu-id="cf2d5-111">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="cf2d5-112">Példák</span><span class="sxs-lookup"><span data-stu-id="cf2d5-112">EXAMPLES</span></span>

### <span data-ttu-id="cf2d5-113">Példa 1: VMSS</span><span class="sxs-lookup"><span data-stu-id="cf2d5-113">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzureRmVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="cf2d5-114">Ez a parancs a ContosoGroup nevű erőforráscsoporthoz tartozó ContosoVMSS VMSS.</span><span class="sxs-lookup"><span data-stu-id="cf2d5-114">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="cf2d5-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cf2d5-115">PARAMETERS</span></span>

### <span data-ttu-id="cf2d5-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cf2d5-116">-AsJob</span></span>
<span data-ttu-id="cf2d5-117">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="cf2d5-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="cf2d5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf2d5-118">-DefaultProfile</span></span>
<span data-ttu-id="cf2d5-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cf2d5-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf2d5-120">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="cf2d5-120">-InstanceId</span></span>
<span data-ttu-id="cf2d5-121">A virtuális gép példányának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="cf2d5-121">The instance ID of the virtual machine.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf2d5-122">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="cf2d5-122">-PerformMaintenance</span></span>
<span data-ttu-id="cf2d5-123">Azt jelzi, hogy ez a parancsmag egy vagy több virtuális gépet végez karbantartással a VMSS.</span><span class="sxs-lookup"><span data-stu-id="cf2d5-123">Indicates that this cmdlet performs maintenance one or more virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="cf2d5-124">-Redeploy</span><span class="sxs-lookup"><span data-stu-id="cf2d5-124">-Redeploy</span></span>
<span data-ttu-id="cf2d5-125">Azt jelzi, hogy a parancsmag áttelepíti egy vagy több virtuális gépet a VMSS.</span><span class="sxs-lookup"><span data-stu-id="cf2d5-125">Indicates that the cmdlet redeploys one or more virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="cf2d5-126">-Reimage</span><span class="sxs-lookup"><span data-stu-id="cf2d5-126">-Reimage</span></span>
<span data-ttu-id="cf2d5-127">Jelzi, hogy a parancsmag átadja a VMSS.</span><span class="sxs-lookup"><span data-stu-id="cf2d5-127">Indicates that the cmdlet reimages the VMSS.</span></span>

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

### <span data-ttu-id="cf2d5-128">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="cf2d5-128">-ReimageAll</span></span>
<span data-ttu-id="cf2d5-129">Jelzi, hogy a parancsmag a VMSS összes lemezét átadja.</span><span class="sxs-lookup"><span data-stu-id="cf2d5-129">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

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

### <span data-ttu-id="cf2d5-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf2d5-130">-ResourceGroupName</span></span>
<span data-ttu-id="cf2d5-131">A VMSS erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cf2d5-131">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf2d5-132">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="cf2d5-132">-VMScaleSetName</span></span>
<span data-ttu-id="cf2d5-133">Faj: annak a VMSS a neve, amelyhez a parancsmag a műveleteket állítja be.</span><span class="sxs-lookup"><span data-stu-id="cf2d5-133">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf2d5-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cf2d5-134">-Confirm</span></span>
<span data-ttu-id="cf2d5-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cf2d5-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf2d5-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf2d5-136">-WhatIf</span></span>
<span data-ttu-id="cf2d5-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cf2d5-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cf2d5-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cf2d5-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf2d5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf2d5-139">CommonParameters</span></span>
<span data-ttu-id="cf2d5-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cf2d5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf2d5-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf2d5-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf2d5-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf2d5-142">INPUTS</span></span>

### <span data-ttu-id="cf2d5-143">System. String</span><span class="sxs-lookup"><span data-stu-id="cf2d5-143">System.String</span></span>

### <span data-ttu-id="cf2d5-144">System. string []</span><span class="sxs-lookup"><span data-stu-id="cf2d5-144">System.String[]</span></span>

## <span data-ttu-id="cf2d5-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf2d5-145">OUTPUTS</span></span>

### <span data-ttu-id="cf2d5-146">Microsoft. Azure. commands. számítási. Automation. models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="cf2d5-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="cf2d5-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cf2d5-147">NOTES</span></span>

## <span data-ttu-id="cf2d5-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cf2d5-148">RELATED LINKS</span></span>

[<span data-ttu-id="cf2d5-149">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="cf2d5-149">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="cf2d5-150">Új – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="cf2d5-150">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="cf2d5-151">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="cf2d5-151">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="cf2d5-152">Újraindítás – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="cf2d5-152">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="cf2d5-153">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="cf2d5-153">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="cf2d5-154">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="cf2d5-154">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="cf2d5-155">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="cf2d5-155">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


