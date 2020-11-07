---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/restart-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
ms.openlocfilehash: 5f2c7d4c3a047a4893158e7f1a12b375106d640b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671264"
---
# <span data-ttu-id="e56e4-101">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="e56e4-101">Restart-AzVM</span></span>

## <span data-ttu-id="e56e4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e56e4-102">SYNOPSIS</span></span>
<span data-ttu-id="e56e4-103">Azure virtuális gép újraindítása.</span><span class="sxs-lookup"><span data-stu-id="e56e4-103">Restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="e56e4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e56e4-104">SYNTAX</span></span>

### <span data-ttu-id="e56e4-105">RestartResourceGroupNameParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e56e4-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e56e4-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="e56e4-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e56e4-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="e56e4-107">RestartIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [[-Name] <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e56e4-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="e56e4-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [[-Name] <String>] [-PerformMaintenance] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e56e4-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="e56e4-109">DESCRIPTION</span></span>
<span data-ttu-id="e56e4-110">Az **Újraindítás – AzVM** parancsmag újraindítja az Azure Virtual machinet.</span><span class="sxs-lookup"><span data-stu-id="e56e4-110">The **Restart-AzVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="e56e4-111">Példák</span><span class="sxs-lookup"><span data-stu-id="e56e4-111">EXAMPLES</span></span>

### <span data-ttu-id="e56e4-112">1. példa: virtuális gép újraindítása</span><span class="sxs-lookup"><span data-stu-id="e56e4-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="e56e4-113">Ez a parancs elindítja a VirtualMachine07 nevű virtuális gépet a ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="e56e4-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="e56e4-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e56e4-114">PARAMETERS</span></span>

### <span data-ttu-id="e56e4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e56e4-115">-AsJob</span></span>
<span data-ttu-id="e56e4-116">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="e56e4-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="e56e4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e56e4-117">-DefaultProfile</span></span>
<span data-ttu-id="e56e4-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e56e4-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e56e4-119">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="e56e4-119">-Id</span></span>
<span data-ttu-id="e56e4-120">A virtuális gép azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e56e4-120">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="e56e4-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e56e4-121">-Name</span></span>
<span data-ttu-id="e56e4-122">A virtuális gép neve.</span><span class="sxs-lookup"><span data-stu-id="e56e4-122">The virtual machine name.</span></span>

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

```yaml
Type: System.String
Parameter Sets: RestartIdParameterSetName, PerformMaintenanceIdParameterSetName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e56e4-123">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="e56e4-123">-PerformMaintenance</span></span>
<span data-ttu-id="e56e4-124">A virtuális gép karbantartásának elvégzéséhez.</span><span class="sxs-lookup"><span data-stu-id="e56e4-124">To perform the maintenance of virtual machine.</span></span>

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

### <span data-ttu-id="e56e4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e56e4-125">-ResourceGroupName</span></span>
<span data-ttu-id="e56e4-126">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e56e4-126">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="e56e4-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e56e4-127">-Confirm</span></span>
<span data-ttu-id="e56e4-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e56e4-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e56e4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e56e4-129">-WhatIf</span></span>
<span data-ttu-id="e56e4-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e56e4-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e56e4-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e56e4-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e56e4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e56e4-132">CommonParameters</span></span>
<span data-ttu-id="e56e4-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e56e4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e56e4-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e56e4-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e56e4-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e56e4-135">INPUTS</span></span>

### <span data-ttu-id="e56e4-136">System. String</span><span class="sxs-lookup"><span data-stu-id="e56e4-136">System.String</span></span>

### <span data-ttu-id="e56e4-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e56e4-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e56e4-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e56e4-138">OUTPUTS</span></span>

### <span data-ttu-id="e56e4-139">Microsoft. Azure. commands. kiszámítás. models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="e56e4-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="e56e4-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e56e4-140">NOTES</span></span>

## <span data-ttu-id="e56e4-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e56e4-141">RELATED LINKS</span></span>

[<span data-ttu-id="e56e4-142">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="e56e4-142">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="e56e4-143">Új – AzVM</span><span class="sxs-lookup"><span data-stu-id="e56e4-143">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="e56e4-144">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="e56e4-144">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="e56e4-145">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="e56e4-145">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="e56e4-146">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="e56e4-146">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="e56e4-147">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="e56e4-147">Update-AzVM</span></span>](./Update-AzVM.md)


