---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
ms.openlocfilehash: b3e060680ee5df25708f153b239ec6c13b4e8a35
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667234"
---
# <span data-ttu-id="df7e3-101">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="df7e3-101">Set-AzVM</span></span>

## <span data-ttu-id="df7e3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="df7e3-102">SYNOPSIS</span></span>
<span data-ttu-id="df7e3-103">A virtuális gépet általánosként jelöli meg.</span><span class="sxs-lookup"><span data-stu-id="df7e3-103">Marks a virtual machine as generalized.</span></span>

## <span data-ttu-id="df7e3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="df7e3-104">SYNTAX</span></span>

### <span data-ttu-id="df7e3-105">GeneralizeResourceGroupNameParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="df7e3-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df7e3-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="df7e3-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df7e3-107">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="df7e3-107">GeneralizeIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Generalized] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df7e3-108">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="df7e3-108">RedeployIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Redeploy] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="df7e3-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="df7e3-109">DESCRIPTION</span></span>
<span data-ttu-id="df7e3-110">A **set-AzVM** parancsmag a virtuális gépet általánosként jelöli meg.</span><span class="sxs-lookup"><span data-stu-id="df7e3-110">The **Set-AzVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="df7e3-111">A parancsmag futtatása előtt jelentkezzen be a virtuális gépre, és a Sysprep segítségével készítse elő a merevlemezt.</span><span class="sxs-lookup"><span data-stu-id="df7e3-111">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="df7e3-112">Példák</span><span class="sxs-lookup"><span data-stu-id="df7e3-112">EXAMPLES</span></span>

### <span data-ttu-id="df7e3-113">1. példa: virtuális gép megjelölése általánosként</span><span class="sxs-lookup"><span data-stu-id="df7e3-113">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="df7e3-114">Ez a parancs a VirtualMachine07 nevű virtuális gépet általánosként jelöli meg.</span><span class="sxs-lookup"><span data-stu-id="df7e3-114">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="df7e3-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="df7e3-115">PARAMETERS</span></span>

### <span data-ttu-id="df7e3-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="df7e3-116">-AsJob</span></span>
<span data-ttu-id="df7e3-117">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="df7e3-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="df7e3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df7e3-118">-DefaultProfile</span></span>
<span data-ttu-id="df7e3-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="df7e3-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df7e3-120">-Általános</span><span class="sxs-lookup"><span data-stu-id="df7e3-120">-Generalized</span></span>
<span data-ttu-id="df7e3-121">Jelzi, hogy ez a parancsmag a virtuális gépet általánosként jelöli meg.</span><span class="sxs-lookup"><span data-stu-id="df7e3-121">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

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

### <span data-ttu-id="df7e3-122">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="df7e3-122">-Id</span></span>
<span data-ttu-id="df7e3-123">A virtuális gép erőforrás-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="df7e3-123">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeIdParameterSetName, RedeployIdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df7e3-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="df7e3-124">-Name</span></span>
<span data-ttu-id="df7e3-125">Annak a virtuális gépnek a neve, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="df7e3-125">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df7e3-126">-Várva</span><span class="sxs-lookup"><span data-stu-id="df7e3-126">-NoWait</span></span>
<span data-ttu-id="df7e3-127">Elindítja a műveletet, és a művelet befejezése előtt azonnal visszaküldi a műveletet.</span><span class="sxs-lookup"><span data-stu-id="df7e3-127">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="df7e3-128">Ha meg szeretné állapítani, hogy sikerült-e végrehajtani a műveletet, használjon más mechanizmust.</span><span class="sxs-lookup"><span data-stu-id="df7e3-128">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployResourceGroupNameParameterSetName, RedeployIdParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df7e3-129">-Redeploy</span><span class="sxs-lookup"><span data-stu-id="df7e3-129">-Redeploy</span></span>
<span data-ttu-id="df7e3-130">Jelzi, hogy ez a parancsmag manuálisan telepíti át a virtuális gépet egy másik Azure-állomásra a problémák megoldásához.</span><span class="sxs-lookup"><span data-stu-id="df7e3-130">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>
<span data-ttu-id="df7e3-131">Ha újratelepíti a virtuális gépet, az újraindul, ami az elmúló Drive-adatvesztés elvesztésével jár.</span><span class="sxs-lookup"><span data-stu-id="df7e3-131">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

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

### <span data-ttu-id="df7e3-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df7e3-132">-ResourceGroupName</span></span>
<span data-ttu-id="df7e3-133">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="df7e3-133">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df7e3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df7e3-134">CommonParameters</span></span>
<span data-ttu-id="df7e3-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="df7e3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df7e3-136">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="df7e3-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df7e3-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="df7e3-137">INPUTS</span></span>

### <span data-ttu-id="df7e3-138">System. String</span><span class="sxs-lookup"><span data-stu-id="df7e3-138">System.String</span></span>

## <span data-ttu-id="df7e3-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="df7e3-139">OUTPUTS</span></span>

### <span data-ttu-id="df7e3-140">Microsoft. Azure. commands. kiszámítás. models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="df7e3-140">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="df7e3-141">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="df7e3-141">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="df7e3-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="df7e3-142">NOTES</span></span>

## <span data-ttu-id="df7e3-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="df7e3-143">RELATED LINKS</span></span>

[<span data-ttu-id="df7e3-144">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="df7e3-144">Get-AzVM</span></span>](./Get-AzVM.md)


