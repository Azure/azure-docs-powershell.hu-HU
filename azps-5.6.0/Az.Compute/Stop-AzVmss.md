---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: AF0DDDD0-B664-4AD8-A569-1363FB2EDB40
online version: https://docs.microsoft.com/powershell/module/az.compute/stop-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmss.md
ms.openlocfilehash: 152be66a2e1582d9f8377e09e250d3cf044c64db
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010789"
---
# <span data-ttu-id="bf035-101">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="bf035-101">Stop-AzVmss</span></span>

## <span data-ttu-id="bf035-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf035-102">SYNOPSIS</span></span>
<span data-ttu-id="bf035-103">Leállítja a VMSS-t vagy a virtuális gépek készletét a VMSS-en belül.</span><span class="sxs-lookup"><span data-stu-id="bf035-103">Stops the VMSS or a set of virtual machines within the VMSS.</span></span>

## <span data-ttu-id="bf035-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bf035-104">SYNTAX</span></span>

### <span data-ttu-id="bf035-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bf035-105">DefaultParameter (Default)</span></span>
```
Stop-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf035-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="bf035-106">FriendMethod</span></span>
```
Stop-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-StayProvisioned] [-SkipShutdown] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bf035-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bf035-107">DESCRIPTION</span></span>
<span data-ttu-id="bf035-108">A **Stop-AzVmss** parancsmag leállítja az összes virtuális gépet a virtuálisgép-mérethalmazban (VMSS) vagy virtuális gépek készletében.</span><span class="sxs-lookup"><span data-stu-id="bf035-108">The **Stop-AzVmss** cmdlet stops all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="bf035-109">A *InstanceId paraméterrel* kiválaszthatja a virtuális gépek készletét.</span><span class="sxs-lookup"><span data-stu-id="bf035-109">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="bf035-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bf035-110">EXAMPLES</span></span>

### <span data-ttu-id="bf035-111">1. példa: Az összes virtuális gép leállítása a VMSS-en belül</span><span class="sxs-lookup"><span data-stu-id="bf035-111">Example 1: Stop all the virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="bf035-112">Ez a parancs leállítja a ContosoVMSS nevű VMSS-hez tartozó összes virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="bf035-112">This command stops all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="bf035-113">2. példa: Virtuális gépek adott készletének leállítása a VMSS-en belül</span><span class="sxs-lookup"><span data-stu-id="bf035-113">Example 2: Stop a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS" -InstanceId "3","5"
```

<span data-ttu-id="bf035-114">Ez a parancs leállítja a ContosoVMSS nevű VMSS-hez tartozó példányazonosító karakterlánctömbben megadott virtuális gépek adott készletét.</span><span class="sxs-lookup"><span data-stu-id="bf035-114">This command stops a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="bf035-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bf035-115">PARAMETERS</span></span>

### <span data-ttu-id="bf035-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bf035-116">-AsJob</span></span>
<span data-ttu-id="bf035-117">Futtasa a parancsmagot a háttérben, és adja vissza a feladatot az előrehaladás nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="bf035-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="bf035-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf035-118">-DefaultProfile</span></span>
<span data-ttu-id="bf035-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bf035-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf035-120">-Force</span><span class="sxs-lookup"><span data-stu-id="bf035-120">-Force</span></span>
<span data-ttu-id="bf035-121">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="bf035-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bf035-122">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="bf035-122">-InstanceId</span></span>
<span data-ttu-id="bf035-123">Karakterlánc-tömbként megadja a parancsmag által leállítandó virtuális gépi példányok azonosítóját vagy azonosítóit.</span><span class="sxs-lookup"><span data-stu-id="bf035-123">Specifies, as a string array, the ID or IDs of the virtual machine instances that this cmdlet stops.</span></span>
<span data-ttu-id="bf035-124">Például: `-InstanceId "0", "3"` .</span><span class="sxs-lookup"><span data-stu-id="bf035-124">For instance: `-InstanceId "0", "3"`.</span></span>

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

### <span data-ttu-id="bf035-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf035-125">-ResourceGroupName</span></span>
<span data-ttu-id="bf035-126">A VMSS erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bf035-126">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="bf035-127">-SkipShutdown</span><span class="sxs-lookup"><span data-stu-id="bf035-127">-SkipShutdown</span></span>
<span data-ttu-id="bf035-128">Nem türelmes VM-leállítás kérése</span><span class="sxs-lookup"><span data-stu-id="bf035-128">To request non-graceful VM shutdown</span></span>

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

### <span data-ttu-id="bf035-129">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="bf035-129">-StayProvisioned</span></span>
<span data-ttu-id="bf035-130">Ha meg van adva, a virtuális gép leállt állapotba lép.</span><span class="sxs-lookup"><span data-stu-id="bf035-130">If specified, the virtual machine will enter stopped state.</span></span> <span data-ttu-id="bf035-131">Ha nincs megadva, a virtuális gép leállítva-deallocated állapotot ad meg.</span><span class="sxs-lookup"><span data-stu-id="bf035-131">If not specified, the virtual machine will enter stopped-deallocated state.</span></span> <span data-ttu-id="bf035-132">A felhasználónak továbbra is le kell fizetnie a leállítva állapotban, de a leállított deallocated állapotban nem.</span><span class="sxs-lookup"><span data-stu-id="bf035-132">The user is still charged for VMs in stopped state but not for VMs in stopped-deallocated state.</span></span>

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

### <span data-ttu-id="bf035-133">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="bf035-133">-VMScaleSetName</span></span>
<span data-ttu-id="bf035-134">Annak a VMSS-nek a neve, amelynek a parancsmagja leállítja a virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="bf035-134">Specifies the name of the VMSS for which this cmdlet stops the virtual machines.</span></span>

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

### <span data-ttu-id="bf035-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bf035-135">-Confirm</span></span>
<span data-ttu-id="bf035-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="bf035-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf035-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf035-137">-WhatIf</span></span>
<span data-ttu-id="bf035-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="bf035-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bf035-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bf035-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf035-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf035-140">CommonParameters</span></span>
<span data-ttu-id="bf035-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf035-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf035-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bf035-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf035-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bf035-143">INPUTS</span></span>

### <span data-ttu-id="bf035-144">System.String</span><span class="sxs-lookup"><span data-stu-id="bf035-144">System.String</span></span>

### <span data-ttu-id="bf035-145">System.String[]</span><span class="sxs-lookup"><span data-stu-id="bf035-145">System.String[]</span></span>

## <span data-ttu-id="bf035-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf035-146">OUTPUTS</span></span>

### <span data-ttu-id="bf035-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="bf035-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="bf035-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bf035-148">NOTES</span></span>

## <span data-ttu-id="bf035-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bf035-149">RELATED LINKS</span></span>

[<span data-ttu-id="bf035-150">Get-AzVms</span><span class="sxs-lookup"><span data-stu-id="bf035-150">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="bf035-151">Új-AzVms</span><span class="sxs-lookup"><span data-stu-id="bf035-151">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="bf035-152">Remove-AzVms</span><span class="sxs-lookup"><span data-stu-id="bf035-152">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="bf035-153">Restart-AzVms</span><span class="sxs-lookup"><span data-stu-id="bf035-153">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="bf035-154">Set-AzVms</span><span class="sxs-lookup"><span data-stu-id="bf035-154">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="bf035-155">Start-AzVms</span><span class="sxs-lookup"><span data-stu-id="bf035-155">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="bf035-156">Update-AzVms</span><span class="sxs-lookup"><span data-stu-id="bf035-156">Update-AzVmss</span></span>](./Update-AzVmss.md)


