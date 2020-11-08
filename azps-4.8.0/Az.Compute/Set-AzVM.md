---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
ms.openlocfilehash: 34c49bdd798e23e9c5d151ed3de577136fad5b03
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183088"
---
# <span data-ttu-id="abb08-101">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="abb08-101">Set-AzVM</span></span>

## <span data-ttu-id="abb08-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="abb08-102">SYNOPSIS</span></span>
<span data-ttu-id="abb08-103">A virtuális gépet általánosként jelöli meg.</span><span class="sxs-lookup"><span data-stu-id="abb08-103">Marks a virtual machine as generalized.</span></span>

## <span data-ttu-id="abb08-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="abb08-104">SYNTAX</span></span>

### <span data-ttu-id="abb08-105">GeneralizeResourceGroupNameParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="abb08-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="abb08-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="abb08-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="abb08-107">ReapplyResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="abb08-107">ReapplyResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Reapply] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="abb08-108">SimulateEvictionResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="abb08-108">SimulateEvictionResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-SimulateEviction] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="abb08-109">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="abb08-109">GeneralizeIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Generalized] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="abb08-110">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="abb08-110">RedeployIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Redeploy] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="abb08-111">ReapplyIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="abb08-111">ReapplyIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Reapply] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="abb08-112">SimulateEvictionIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="abb08-112">SimulateEvictionIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-SimulateEviction] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="abb08-113">Leírás</span><span class="sxs-lookup"><span data-stu-id="abb08-113">DESCRIPTION</span></span>
<span data-ttu-id="abb08-114">A **set-AzVM** parancsmag a virtuális gépet általánosként jelöli meg.</span><span class="sxs-lookup"><span data-stu-id="abb08-114">The **Set-AzVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="abb08-115">A parancsmag futtatása előtt jelentkezzen be a virtuális gépre, és a Sysprep segítségével készítse elő a merevlemezt.</span><span class="sxs-lookup"><span data-stu-id="abb08-115">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="abb08-116">Példák</span><span class="sxs-lookup"><span data-stu-id="abb08-116">EXAMPLES</span></span>

### <span data-ttu-id="abb08-117">1. példa: virtuális gép megjelölése általánosként</span><span class="sxs-lookup"><span data-stu-id="abb08-117">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="abb08-118">Ez a parancs a VirtualMachine07 nevű virtuális gépet általánosként jelöli meg.</span><span class="sxs-lookup"><span data-stu-id="abb08-118">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="abb08-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="abb08-119">PARAMETERS</span></span>

### <span data-ttu-id="abb08-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="abb08-120">-AsJob</span></span>
<span data-ttu-id="abb08-121">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="abb08-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="abb08-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abb08-122">-DefaultProfile</span></span>
<span data-ttu-id="abb08-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="abb08-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="abb08-124">-Általános</span><span class="sxs-lookup"><span data-stu-id="abb08-124">-Generalized</span></span>
<span data-ttu-id="abb08-125">Jelzi, hogy ez a parancsmag a virtuális gépet általánosként jelöli meg.</span><span class="sxs-lookup"><span data-stu-id="abb08-125">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

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

### <span data-ttu-id="abb08-126">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="abb08-126">-Id</span></span>
<span data-ttu-id="abb08-127">A virtuális gép erőforrás-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="abb08-127">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="abb08-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="abb08-128">-Name</span></span>
<span data-ttu-id="abb08-129">Annak a virtuális gépnek a neve, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="abb08-129">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="abb08-130">-Várva</span><span class="sxs-lookup"><span data-stu-id="abb08-130">-NoWait</span></span>
<span data-ttu-id="abb08-131">Elindítja a műveletet, és a művelet befejezése előtt azonnal visszaküldi a műveletet.</span><span class="sxs-lookup"><span data-stu-id="abb08-131">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="abb08-132">Ha meg szeretné állapítani, hogy sikerült-e végrehajtani a műveletet, használjon más mechanizmust.</span><span class="sxs-lookup"><span data-stu-id="abb08-132">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="abb08-133">-Újbóli alkalmazása</span><span class="sxs-lookup"><span data-stu-id="abb08-133">-Reapply</span></span>
<span data-ttu-id="abb08-134">A virtuális gép ismételt alkalmazásához.</span><span class="sxs-lookup"><span data-stu-id="abb08-134">To reapply virtual machine.</span></span>

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

### <span data-ttu-id="abb08-135">-Redeploy</span><span class="sxs-lookup"><span data-stu-id="abb08-135">-Redeploy</span></span>
<span data-ttu-id="abb08-136">Jelzi, hogy ez a parancsmag manuálisan telepíti át a virtuális gépet egy másik Azure-állomásra a problémák megoldásához.</span><span class="sxs-lookup"><span data-stu-id="abb08-136">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>
<span data-ttu-id="abb08-137">Ha újratelepíti a virtuális gépet, az újraindul, ami az elmúló Drive-adatvesztés elvesztésével jár.</span><span class="sxs-lookup"><span data-stu-id="abb08-137">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

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

### <span data-ttu-id="abb08-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abb08-138">-ResourceGroupName</span></span>
<span data-ttu-id="abb08-139">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="abb08-139">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="abb08-140">-SimulateEviction</span><span class="sxs-lookup"><span data-stu-id="abb08-140">-SimulateEviction</span></span>
<span data-ttu-id="abb08-141">Jelzi, hogy ez a parancsmag szimulálja a direkt virtuális gép kilakoltatását.</span><span class="sxs-lookup"><span data-stu-id="abb08-141">Indicates that this cmdlet simulates the eviction of spot virtual machine.</span></span>
<span data-ttu-id="abb08-142">A kilakoltatás az API hívása után 30 percen belül fog történni.</span><span class="sxs-lookup"><span data-stu-id="abb08-142">The eviction will occur within 30 minutes of calling the API.</span></span>

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

### <span data-ttu-id="abb08-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abb08-143">CommonParameters</span></span>
<span data-ttu-id="abb08-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="abb08-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abb08-145">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="abb08-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abb08-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="abb08-146">INPUTS</span></span>

### <span data-ttu-id="abb08-147">System. String</span><span class="sxs-lookup"><span data-stu-id="abb08-147">System.String</span></span>

## <span data-ttu-id="abb08-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="abb08-148">OUTPUTS</span></span>

### <span data-ttu-id="abb08-149">Microsoft. Azure. commands. kiszámítás. models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="abb08-149">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="abb08-150">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="abb08-150">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="abb08-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="abb08-151">NOTES</span></span>

## <span data-ttu-id="abb08-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="abb08-152">RELATED LINKS</span></span>

[<span data-ttu-id="abb08-153">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="abb08-153">Get-AzVM</span></span>](./Get-AzVM.md)


