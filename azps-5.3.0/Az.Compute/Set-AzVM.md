---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
ms.openlocfilehash: 34c49bdd798e23e9c5d151ed3de577136fad5b03
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480714"
---
# <span data-ttu-id="143a3-101">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="143a3-101">Set-AzVM</span></span>

## <span data-ttu-id="143a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="143a3-102">SYNOPSIS</span></span>
<span data-ttu-id="143a3-103">Egy virtuális gépet általánosítottként megjelöl.</span><span class="sxs-lookup"><span data-stu-id="143a3-103">Marks a virtual machine as generalized.</span></span>

## <span data-ttu-id="143a3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="143a3-104">SYNTAX</span></span>

### <span data-ttu-id="143a3-105">GeneralizeResourceGroupNameParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="143a3-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="143a3-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="143a3-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="143a3-107">ReapplyResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="143a3-107">ReapplyResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Reapply] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="143a3-108">SimulateEvictionResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="143a3-108">SimulateEvictionResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-SimulateEviction] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="143a3-109">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="143a3-109">GeneralizeIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Generalized] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="143a3-110">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="143a3-110">RedeployIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Redeploy] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="143a3-111">ReapplyIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="143a3-111">ReapplyIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Reapply] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="143a3-112">SimulateEvictionIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="143a3-112">SimulateEvictionIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-SimulateEviction] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="143a3-113">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="143a3-113">DESCRIPTION</span></span>
<span data-ttu-id="143a3-114">A **Set-AzVM parancsmag** általánosítottként jelöli meg a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="143a3-114">The **Set-AzVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="143a3-115">A parancsmag futtatása előtt jelentkezzen be a virtuális gépre, és a Sysprep segítségével készítse elő a merevlemezt.</span><span class="sxs-lookup"><span data-stu-id="143a3-115">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="143a3-116">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="143a3-116">EXAMPLES</span></span>

### <span data-ttu-id="143a3-117">1. példa: Virtuális gép megjelölése általánosítottként</span><span class="sxs-lookup"><span data-stu-id="143a3-117">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="143a3-118">Ez a parancs általánosítottként jelöli meg a VirtualMachine07 nevű virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="143a3-118">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="143a3-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="143a3-119">PARAMETERS</span></span>

### <span data-ttu-id="143a3-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="143a3-120">-AsJob</span></span>
<span data-ttu-id="143a3-121">Futtasa a parancsmagot a háttérben, és adja vissza a feladatot az előrehaladás nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="143a3-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="143a3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="143a3-122">-DefaultProfile</span></span>
<span data-ttu-id="143a3-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="143a3-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="143a3-124">-Generalized</span><span class="sxs-lookup"><span data-stu-id="143a3-124">-Generalized</span></span>
<span data-ttu-id="143a3-125">Azt jelzi, hogy ez a parancsmag általánosítottként jelöli meg a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="143a3-125">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, GeneralizeIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="143a3-126">-Id</span><span class="sxs-lookup"><span data-stu-id="143a3-126">-Id</span></span>
<span data-ttu-id="143a3-127">A virtuális gép erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="143a3-127">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeIdParameterSetName, RedeployIdParameterSetName, ReapplyIdParameterSetName, SimulateEvictionIdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="143a3-128">-Name</span><span class="sxs-lookup"><span data-stu-id="143a3-128">-Name</span></span>
<span data-ttu-id="143a3-129">Annak a virtuális gépnek a nevét adja meg, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="143a3-129">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName, ReapplyResourceGroupNameParameterSetName, SimulateEvictionResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="143a3-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="143a3-130">-NoWait</span></span>
<span data-ttu-id="143a3-131">Elindítja a műveletet, és azonnal, a művelet befejezése előtt visszatér.</span><span class="sxs-lookup"><span data-stu-id="143a3-131">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="143a3-132">Ha meg szeretné állapítani, hogy a művelet sikeresen befejeződött-e, használjon más mechanizmust.</span><span class="sxs-lookup"><span data-stu-id="143a3-132">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployResourceGroupNameParameterSetName, ReapplyResourceGroupNameParameterSetName, RedeployIdParameterSetName, ReapplyIdParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="143a3-133">-Reapply</span><span class="sxs-lookup"><span data-stu-id="143a3-133">-Reapply</span></span>
<span data-ttu-id="143a3-134">Virtuális gép újraalkalmazása.</span><span class="sxs-lookup"><span data-stu-id="143a3-134">To reapply virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ReapplyResourceGroupNameParameterSetName, ReapplyIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="143a3-135">-Redeploy</span><span class="sxs-lookup"><span data-stu-id="143a3-135">-Redeploy</span></span>
<span data-ttu-id="143a3-136">Azt jelzi, hogy ez a parancsmag manuálisan átcsoportosíti a virtuális gépet egy másik Azure-állomásra az esetleges problémák megoldása érdekében.</span><span class="sxs-lookup"><span data-stu-id="143a3-136">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>
<span data-ttu-id="143a3-137">Ha újra üzembe hoz egy virtuális gépet, az újraindul, ami a meghajtó adatainak elvesztéséhez vezet.</span><span class="sxs-lookup"><span data-stu-id="143a3-137">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployResourceGroupNameParameterSetName, RedeployIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="143a3-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="143a3-138">-ResourceGroupName</span></span>
<span data-ttu-id="143a3-139">A virtuális gép erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="143a3-139">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName, ReapplyResourceGroupNameParameterSetName, SimulateEvictionResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="143a3-140">-SimulateEviction</span><span class="sxs-lookup"><span data-stu-id="143a3-140">-SimulateEviction</span></span>
<span data-ttu-id="143a3-141">Azt jelzi, hogy ez a parancsmag szimulálja a direkt virtuális gép kilakoltatását.</span><span class="sxs-lookup"><span data-stu-id="143a3-141">Indicates that this cmdlet simulates the eviction of spot virtual machine.</span></span>
<span data-ttu-id="143a3-142">A kilakoltatás az API hívását követő 30 percen belül meg fog történik.</span><span class="sxs-lookup"><span data-stu-id="143a3-142">The eviction will occur within 30 minutes of calling the API.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimulateEvictionResourceGroupNameParameterSetName, SimulateEvictionIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="143a3-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="143a3-143">CommonParameters</span></span>
<span data-ttu-id="143a3-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="143a3-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="143a3-145">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="143a3-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="143a3-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="143a3-146">INPUTS</span></span>

### <span data-ttu-id="143a3-147">System.String</span><span class="sxs-lookup"><span data-stu-id="143a3-147">System.String</span></span>

## <span data-ttu-id="143a3-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="143a3-148">OUTPUTS</span></span>

### <span data-ttu-id="143a3-149">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="143a3-149">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="143a3-150">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="143a3-150">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="143a3-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="143a3-151">NOTES</span></span>

## <span data-ttu-id="143a3-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="143a3-152">RELATED LINKS</span></span>

[<span data-ttu-id="143a3-153">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="143a3-153">Get-AzVM</span></span>](./Get-AzVM.md)


