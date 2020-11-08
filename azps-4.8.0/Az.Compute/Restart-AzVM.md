---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/restart-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
ms.openlocfilehash: 358b24c403c4b08b221f97ad99271112ee0852be
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183089"
---
# <span data-ttu-id="ee503-101">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="ee503-101">Restart-AzVM</span></span>

## <span data-ttu-id="ee503-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ee503-102">SYNOPSIS</span></span>
<span data-ttu-id="ee503-103">Azure virtuális gép újraindítása.</span><span class="sxs-lookup"><span data-stu-id="ee503-103">Restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="ee503-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ee503-104">SYNTAX</span></span>

### <span data-ttu-id="ee503-105">RestartResourceGroupNameParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ee503-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee503-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="ee503-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee503-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="ee503-107">RestartIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ee503-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="ee503-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-PerformMaintenance] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee503-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="ee503-109">DESCRIPTION</span></span>
<span data-ttu-id="ee503-110">Az **Újraindítás – AzVM** parancsmag újraindítja az Azure Virtual machinet.</span><span class="sxs-lookup"><span data-stu-id="ee503-110">The **Restart-AzVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="ee503-111">Példák</span><span class="sxs-lookup"><span data-stu-id="ee503-111">EXAMPLES</span></span>

### <span data-ttu-id="ee503-112">1. példa: virtuális gép újraindítása</span><span class="sxs-lookup"><span data-stu-id="ee503-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="ee503-113">Ez a parancs elindítja a VirtualMachine07 nevű virtuális gépet a ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="ee503-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="ee503-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ee503-114">PARAMETERS</span></span>

### <span data-ttu-id="ee503-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ee503-115">-AsJob</span></span>
<span data-ttu-id="ee503-116">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="ee503-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="ee503-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee503-117">-DefaultProfile</span></span>
<span data-ttu-id="ee503-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ee503-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee503-119">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="ee503-119">-Id</span></span>
<span data-ttu-id="ee503-120">A virtuális gép azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ee503-120">The ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartIdParameterSetName, PerformMaintenanceIdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee503-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ee503-121">-Name</span></span>
<span data-ttu-id="ee503-122">A virtuális gép neve.</span><span class="sxs-lookup"><span data-stu-id="ee503-122">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartResourceGroupNameParameterSetName, PerformMaintenanceResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee503-123">-Várva</span><span class="sxs-lookup"><span data-stu-id="ee503-123">-NoWait</span></span>
<span data-ttu-id="ee503-124">Elindítja a műveletet, és a művelet befejezése előtt azonnal visszaküldi a műveletet.</span><span class="sxs-lookup"><span data-stu-id="ee503-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="ee503-125">Ha meg szeretné állapítani, hogy sikerült-e végrehajtani a műveletet, használjon más mechanizmust.</span><span class="sxs-lookup"><span data-stu-id="ee503-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="ee503-126">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="ee503-126">-PerformMaintenance</span></span>
<span data-ttu-id="ee503-127">A virtuális gép karbantartásának elvégzéséhez.</span><span class="sxs-lookup"><span data-stu-id="ee503-127">To perform the maintenance of virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PerformMaintenanceResourceGroupNameParameterSetName, PerformMaintenanceIdParameterSetName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee503-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee503-128">-ResourceGroupName</span></span>
<span data-ttu-id="ee503-129">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee503-129">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartResourceGroupNameParameterSetName, PerformMaintenanceResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee503-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ee503-130">-Confirm</span></span>
<span data-ttu-id="ee503-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ee503-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee503-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee503-132">-WhatIf</span></span>
<span data-ttu-id="ee503-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ee503-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ee503-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ee503-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee503-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee503-135">CommonParameters</span></span>
<span data-ttu-id="ee503-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ee503-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee503-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ee503-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee503-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee503-138">INPUTS</span></span>

### <span data-ttu-id="ee503-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ee503-139">System.String</span></span>

### <span data-ttu-id="ee503-140">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ee503-140">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ee503-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee503-141">OUTPUTS</span></span>

### <span data-ttu-id="ee503-142">Microsoft. Azure. commands. kiszámítás. models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="ee503-142">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="ee503-143">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ee503-143">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="ee503-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ee503-144">NOTES</span></span>

## <span data-ttu-id="ee503-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ee503-145">RELATED LINKS</span></span>

[<span data-ttu-id="ee503-146">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="ee503-146">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="ee503-147">Új – AzVM</span><span class="sxs-lookup"><span data-stu-id="ee503-147">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="ee503-148">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="ee503-148">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="ee503-149">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="ee503-149">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="ee503-150">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="ee503-150">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="ee503-151">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="ee503-151">Update-AzVM</span></span>](./Update-AzVM.md)


