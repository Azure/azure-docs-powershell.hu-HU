---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
ms.openlocfilehash: c9b7ce0c55ff917839ff8047454dcced42653b3d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010919"
---
# <span data-ttu-id="388d3-101">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="388d3-101">Set-AzVM</span></span>

## <span data-ttu-id="388d3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="388d3-102">SYNOPSIS</span></span>
<span data-ttu-id="388d3-103">A virtuális gépet általánosként jelöli meg.</span><span class="sxs-lookup"><span data-stu-id="388d3-103">Marks a virtual machine as generalized.</span></span>

## <span data-ttu-id="388d3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="388d3-104">SYNTAX</span></span>

### <span data-ttu-id="388d3-105">GeneralizeResourceGroupNameParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="388d3-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="388d3-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="388d3-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="388d3-107">ReapplyResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="388d3-107">ReapplyResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Reapply] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="388d3-108">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="388d3-108">GeneralizeIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Generalized] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="388d3-109">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="388d3-109">RedeployIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Redeploy] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="388d3-110">ReapplyIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="388d3-110">ReapplyIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Reapply] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="388d3-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="388d3-111">DESCRIPTION</span></span>
<span data-ttu-id="388d3-112">A **set-AzVM** parancsmag a virtuális gépet általánosként jelöli meg.</span><span class="sxs-lookup"><span data-stu-id="388d3-112">The **Set-AzVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="388d3-113">A parancsmag futtatása előtt jelentkezzen be a virtuális gépre, és a Sysprep segítségével készítse elő a merevlemezt.</span><span class="sxs-lookup"><span data-stu-id="388d3-113">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="388d3-114">Példák</span><span class="sxs-lookup"><span data-stu-id="388d3-114">EXAMPLES</span></span>

### <span data-ttu-id="388d3-115">1. példa: virtuális gép megjelölése általánosként</span><span class="sxs-lookup"><span data-stu-id="388d3-115">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="388d3-116">Ez a parancs a VirtualMachine07 nevű virtuális gépet általánosként jelöli meg.</span><span class="sxs-lookup"><span data-stu-id="388d3-116">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="388d3-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="388d3-117">PARAMETERS</span></span>

### <span data-ttu-id="388d3-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="388d3-118">-AsJob</span></span>
<span data-ttu-id="388d3-119">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="388d3-119">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="388d3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="388d3-120">-DefaultProfile</span></span>
<span data-ttu-id="388d3-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="388d3-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="388d3-122">-Általános</span><span class="sxs-lookup"><span data-stu-id="388d3-122">-Generalized</span></span>
<span data-ttu-id="388d3-123">Jelzi, hogy ez a parancsmag a virtuális gépet általánosként jelöli meg.</span><span class="sxs-lookup"><span data-stu-id="388d3-123">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

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

### <span data-ttu-id="388d3-124">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="388d3-124">-Id</span></span>
<span data-ttu-id="388d3-125">A virtuális gép erőforrás-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="388d3-125">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeIdParameterSetName, RedeployIdParameterSetName, ReapplyIdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="388d3-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="388d3-126">-Name</span></span>
<span data-ttu-id="388d3-127">Annak a virtuális gépnek a neve, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="388d3-127">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName, ReapplyResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="388d3-128">-Várva</span><span class="sxs-lookup"><span data-stu-id="388d3-128">-NoWait</span></span>
<span data-ttu-id="388d3-129">Elindítja a műveletet, és a művelet befejezése előtt azonnal visszaküldi a műveletet.</span><span class="sxs-lookup"><span data-stu-id="388d3-129">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="388d3-130">Ha meg szeretné állapítani, hogy sikerült-e végrehajtani a műveletet, használjon más mechanizmust.</span><span class="sxs-lookup"><span data-stu-id="388d3-130">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="388d3-131">-Újbóli alkalmazása</span><span class="sxs-lookup"><span data-stu-id="388d3-131">-Reapply</span></span>
<span data-ttu-id="388d3-132">A virtuális gép ismételt alkalmazásához.</span><span class="sxs-lookup"><span data-stu-id="388d3-132">To reapply virtual machine.</span></span>

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

### <span data-ttu-id="388d3-133">-Redeploy</span><span class="sxs-lookup"><span data-stu-id="388d3-133">-Redeploy</span></span>
<span data-ttu-id="388d3-134">Jelzi, hogy ez a parancsmag manuálisan telepíti át a virtuális gépet egy másik Azure-állomásra a problémák megoldásához.</span><span class="sxs-lookup"><span data-stu-id="388d3-134">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>
<span data-ttu-id="388d3-135">Ha újratelepíti a virtuális gépet, az újraindul, ami az elmúló Drive-adatvesztés elvesztésével jár.</span><span class="sxs-lookup"><span data-stu-id="388d3-135">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

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

### <span data-ttu-id="388d3-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="388d3-136">-ResourceGroupName</span></span>
<span data-ttu-id="388d3-137">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="388d3-137">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName, ReapplyResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="388d3-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="388d3-138">CommonParameters</span></span>
<span data-ttu-id="388d3-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="388d3-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="388d3-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="388d3-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="388d3-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="388d3-141">INPUTS</span></span>

### <span data-ttu-id="388d3-142">System. String</span><span class="sxs-lookup"><span data-stu-id="388d3-142">System.String</span></span>

## <span data-ttu-id="388d3-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="388d3-143">OUTPUTS</span></span>

### <span data-ttu-id="388d3-144">Microsoft. Azure. commands. kiszámítás. models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="388d3-144">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="388d3-145">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="388d3-145">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="388d3-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="388d3-146">NOTES</span></span>

## <span data-ttu-id="388d3-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="388d3-147">RELATED LINKS</span></span>

[<span data-ttu-id="388d3-148">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="388d3-148">Get-AzVM</span></span>](./Get-AzVM.md)


