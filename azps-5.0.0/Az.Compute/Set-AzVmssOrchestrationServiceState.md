---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssorchestrationservicestate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOrchestrationServiceState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOrchestrationServiceState.md
ms.openlocfilehash: c1fbc45a9d82733f73a13b13985bdd6746f4c075
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296468"
---
# <span data-ttu-id="d6dbc-101">Set-AzVmssOrchestrationServiceState</span><span class="sxs-lookup"><span data-stu-id="d6dbc-101">Set-AzVmssOrchestrationServiceState</span></span>

## <span data-ttu-id="d6dbc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d6dbc-102">SYNOPSIS</span></span>
<span data-ttu-id="d6dbc-103">Beállítja a VMSS a hangszerelési szolgáltatás állapotát.</span><span class="sxs-lookup"><span data-stu-id="d6dbc-103">Sets the orchestration service state for the VMSS.</span></span>

## <span data-ttu-id="d6dbc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d6dbc-104">SYNTAX</span></span>

### <span data-ttu-id="d6dbc-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d6dbc-105">DefaultParameter (Default)</span></span>
```
Set-AzVmssOrchestrationServiceState [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-ServiceName] <String> [-Action] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6dbc-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="d6dbc-106">ResourceIdParameter</span></span>
```
Set-AzVmssOrchestrationServiceState [-ServiceName] <String> [-Action] <String> [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6dbc-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="d6dbc-107">ObjectParameter</span></span>
```
Set-AzVmssOrchestrationServiceState [-ServiceName] <String> [-Action] <String>
 [-InputObject] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6dbc-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d6dbc-108">DESCRIPTION</span></span>
<span data-ttu-id="d6dbc-109">Beállítja a VMSS a hangszerelési szolgáltatás állapotát.</span><span class="sxs-lookup"><span data-stu-id="d6dbc-109">Sets the orchestration service state for the VMSS.</span></span>

## <span data-ttu-id="d6dbc-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d6dbc-110">EXAMPLES</span></span>

### <span data-ttu-id="d6dbc-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d6dbc-111">Example 1</span></span>
```
PS C:\> Set-AzVmssOrchestrationServiceState -ResourceGroupName "rg" -VMScaleSetName "vmss1" -ServiceName "AutomaticRepairs" -Action "Suspend"
```

<span data-ttu-id="d6dbc-112">Ez a parancs felfüggeszti az automatikus javítási szolgáltatást az "vmss1" VMSS "RG" erőforráscsoport esetén.</span><span class="sxs-lookup"><span data-stu-id="d6dbc-112">This command suspends Automatic Repairs service on the VMSS "vmss1" in the resource group "rg".</span></span>

### <span data-ttu-id="d6dbc-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="d6dbc-113">Example 2</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "rg" -VMScaleSetName "vmss1" | Set-AzVmssOrchestrationServiceState -ServiceName "AutomaticRepairs" -Action "Resume"
```

<span data-ttu-id="d6dbc-114">Ez a parancs a "RG" erőforráscsoport "vmss1" VMSS automatikus javítási szolgáltatást folytat.</span><span class="sxs-lookup"><span data-stu-id="d6dbc-114">This command resumes Automatic Repairs service on the VMSS "vmss1" in the resource group "rg".</span></span>

## <span data-ttu-id="d6dbc-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d6dbc-115">PARAMETERS</span></span>

### <span data-ttu-id="d6dbc-116">-Műveletek</span><span class="sxs-lookup"><span data-stu-id="d6dbc-116">-Action</span></span>
<span data-ttu-id="d6dbc-117">A végrehajtandó művelet.</span><span class="sxs-lookup"><span data-stu-id="d6dbc-117">The action to be performed.</span></span>  <span data-ttu-id="d6dbc-118">Lehetséges értékek: önéletrajz, felfüggesztés.</span><span class="sxs-lookup"><span data-stu-id="d6dbc-118">Possible values are: Resume, Suspend.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6dbc-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d6dbc-119">-AsJob</span></span>
<span data-ttu-id="d6dbc-120">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="d6dbc-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d6dbc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6dbc-121">-DefaultProfile</span></span>
<span data-ttu-id="d6dbc-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d6dbc-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6dbc-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6dbc-123">-InputObject</span></span>
<span data-ttu-id="d6dbc-124">A virtuális gép léptéke beállítás helyi objektuma.</span><span class="sxs-lookup"><span data-stu-id="d6dbc-124">The local object of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="d6dbc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6dbc-125">-ResourceGroupName</span></span>
<span data-ttu-id="d6dbc-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d6dbc-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="d6dbc-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6dbc-127">-ResourceId</span></span>
<span data-ttu-id="d6dbc-128">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d6dbc-128">The ID of the resource.</span></span>

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

### <span data-ttu-id="d6dbc-129">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="d6dbc-129">-ServiceName</span></span>
<span data-ttu-id="d6dbc-130">A szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="d6dbc-130">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6dbc-131">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="d6dbc-131">-VMScaleSetName</span></span>
<span data-ttu-id="d6dbc-132">A virtuális gép méretarányának neve.</span><span class="sxs-lookup"><span data-stu-id="d6dbc-132">The name of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="d6dbc-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d6dbc-133">-Confirm</span></span>
<span data-ttu-id="d6dbc-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d6dbc-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6dbc-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6dbc-135">-WhatIf</span></span>
<span data-ttu-id="d6dbc-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d6dbc-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6dbc-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d6dbc-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6dbc-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6dbc-138">CommonParameters</span></span>
<span data-ttu-id="d6dbc-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d6dbc-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6dbc-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d6dbc-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6dbc-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6dbc-141">INPUTS</span></span>

### <span data-ttu-id="d6dbc-142">System. String</span><span class="sxs-lookup"><span data-stu-id="d6dbc-142">System.String</span></span>

### <span data-ttu-id="d6dbc-143">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d6dbc-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="d6dbc-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6dbc-144">OUTPUTS</span></span>

### <span data-ttu-id="d6dbc-145">Microsoft. Azure. commands. számítási. Automation. models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="d6dbc-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="d6dbc-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d6dbc-146">NOTES</span></span>

## <span data-ttu-id="d6dbc-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d6dbc-147">RELATED LINKS</span></span>
