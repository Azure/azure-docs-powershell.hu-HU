---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
ms.openlocfilehash: 46e6e29b9a79fb5a8273fb3872d09e2cd290accd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477629"
---
# <span data-ttu-id="7ab6c-101">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="7ab6c-101">Stop-AzVM</span></span>

## <span data-ttu-id="7ab6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ab6c-102">SYNOPSIS</span></span>
<span data-ttu-id="7ab6c-103">Leállítja az Azure virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="7ab6c-103">Stops an Azure virtual machine.</span></span>

## <span data-ttu-id="7ab6c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7ab6c-104">SYNTAX</span></span>

### <span data-ttu-id="7ab6c-105">ResourceGroupNameParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7ab6c-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzVM [-Name] <String> [-Force] [-StayProvisioned] [-NoWait] [-SkipShutdown] [-ResourceGroupName] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ab6c-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="7ab6c-106">IdParameterSetName</span></span>
```
Stop-AzVM [-Force] [-StayProvisioned] [-NoWait] [-SkipShutdown] [-Id] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ab6c-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7ab6c-107">DESCRIPTION</span></span>
<span data-ttu-id="7ab6c-108">A **Stop-AzVM parancsmag** leállít egy Azure virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="7ab6c-108">The **Stop-AzVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="7ab6c-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7ab6c-109">EXAMPLES</span></span>

### <span data-ttu-id="7ab6c-110">1. példa: Virtuális gép leállítása</span><span class="sxs-lookup"><span data-stu-id="7ab6c-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="7ab6c-111">Ez a parancs leállítja a VirtualMachine07 nevű virtuális gépet az ResourceGroup11-ben.</span><span class="sxs-lookup"><span data-stu-id="7ab6c-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="7ab6c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ab6c-112">PARAMETERS</span></span>

### <span data-ttu-id="7ab6c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7ab6c-113">-AsJob</span></span>
<span data-ttu-id="7ab6c-114">Futtasa a parancsmagot a háttérben, és adja vissza a feladatot az előrehaladás nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="7ab6c-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="7ab6c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ab6c-115">-DefaultProfile</span></span>
<span data-ttu-id="7ab6c-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7ab6c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ab6c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="7ab6c-117">-Force</span></span>
<span data-ttu-id="7ab6c-118">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="7ab6c-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7ab6c-119">-Id</span><span class="sxs-lookup"><span data-stu-id="7ab6c-119">-Id</span></span>
<span data-ttu-id="7ab6c-120">A virtuális gép azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7ab6c-120">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="7ab6c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="7ab6c-121">-Name</span></span>
<span data-ttu-id="7ab6c-122">A virtuális gép neve.</span><span class="sxs-lookup"><span data-stu-id="7ab6c-122">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ab6c-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7ab6c-123">-NoWait</span></span>
<span data-ttu-id="7ab6c-124">Elindítja a műveletet, és azonnal, a művelet befejezése előtt visszatér.</span><span class="sxs-lookup"><span data-stu-id="7ab6c-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="7ab6c-125">Ha meg szeretné állapítani, hogy a művelet sikeresen befejeződött-e, használjon más mechanizmust.</span><span class="sxs-lookup"><span data-stu-id="7ab6c-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="7ab6c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ab6c-126">-ResourceGroupName</span></span>
<span data-ttu-id="7ab6c-127">A virtuális gép erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7ab6c-127">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="7ab6c-128">-SkipShutdown</span><span class="sxs-lookup"><span data-stu-id="7ab6c-128">-SkipShutdown</span></span>
<span data-ttu-id="7ab6c-129">Nem türelmes vm-leállítás kérése a virtuális gép kiépítésekor.</span><span class="sxs-lookup"><span data-stu-id="7ab6c-129">To request non-graceful VM shutdown when keeping the VM provisioned.</span></span>

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

### <span data-ttu-id="7ab6c-130">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="7ab6c-130">-StayProvisioned</span></span>
<span data-ttu-id="7ab6c-131">A parancsmag leállítja az összes virtuális gépet a VMSS-en belül, de nem foglalkozik velük.</span><span class="sxs-lookup"><span data-stu-id="7ab6c-131">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="7ab6c-132">A leállított virtuális gépekért díjat számítunk fel a fiókért.</span><span class="sxs-lookup"><span data-stu-id="7ab6c-132">The account is charged for the stopped virtual machines.</span></span>

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

### <span data-ttu-id="7ab6c-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7ab6c-133">-Confirm</span></span>
<span data-ttu-id="7ab6c-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7ab6c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ab6c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ab6c-135">-WhatIf</span></span>
<span data-ttu-id="7ab6c-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7ab6c-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7ab6c-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7ab6c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ab6c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ab6c-138">CommonParameters</span></span>
<span data-ttu-id="7ab6c-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ab6c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ab6c-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7ab6c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ab6c-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7ab6c-141">INPUTS</span></span>

### <span data-ttu-id="7ab6c-142">System.String</span><span class="sxs-lookup"><span data-stu-id="7ab6c-142">System.String</span></span>

## <span data-ttu-id="7ab6c-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ab6c-143">OUTPUTS</span></span>

### <span data-ttu-id="7ab6c-144">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="7ab6c-144">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="7ab6c-145">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="7ab6c-145">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="7ab6c-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7ab6c-146">NOTES</span></span>

## <span data-ttu-id="7ab6c-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7ab6c-147">RELATED LINKS</span></span>

[<span data-ttu-id="7ab6c-148">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="7ab6c-148">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="7ab6c-149">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="7ab6c-149">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="7ab6c-150">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="7ab6c-150">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="7ab6c-151">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="7ab6c-151">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="7ab6c-152">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="7ab6c-152">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="7ab6c-153">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="7ab6c-153">Update-AzVM</span></span>](./Update-AzVM.md)


