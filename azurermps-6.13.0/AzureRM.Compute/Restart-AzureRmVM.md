---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/restart-azurermvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Restart-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Restart-AzureRmVM.md
ms.openlocfilehash: f8451f4164b58c2d6599778ab86dfca4e5ff79dd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494107"
---
# <span data-ttu-id="ba650-101">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ba650-101">Restart-AzureRmVM</span></span>

## <span data-ttu-id="ba650-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ba650-102">SYNOPSIS</span></span>
<span data-ttu-id="ba650-103">Azure virtuális gép újraindítása.</span><span class="sxs-lookup"><span data-stu-id="ba650-103">Restarts an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba650-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ba650-104">SYNTAX</span></span>

### <span data-ttu-id="ba650-105">RestartResourceGroupNameParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ba650-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba650-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="ba650-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba650-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="ba650-107">RestartIdParameterSetName</span></span>
```
Restart-AzureRmVM [-Id] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba650-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="ba650-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzureRmVM [-Id] <String> [-Name] <String> [-PerformMaintenance] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba650-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="ba650-109">DESCRIPTION</span></span>
<span data-ttu-id="ba650-110">Az **Újraindítás – AzureRmVM** parancsmag újraindítja az Azure Virtual machinet.</span><span class="sxs-lookup"><span data-stu-id="ba650-110">The **Restart-AzureRmVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="ba650-111">Példák</span><span class="sxs-lookup"><span data-stu-id="ba650-111">EXAMPLES</span></span>

### <span data-ttu-id="ba650-112">1. példa: virtuális gép újraindítása</span><span class="sxs-lookup"><span data-stu-id="ba650-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="ba650-113">Ez a parancs elindítja a VirtualMachine07 nevű virtuális gépet a ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="ba650-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="ba650-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ba650-114">PARAMETERS</span></span>

### <span data-ttu-id="ba650-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ba650-115">-AsJob</span></span>
<span data-ttu-id="ba650-116">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="ba650-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="ba650-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba650-117">-DefaultProfile</span></span>
<span data-ttu-id="ba650-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ba650-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba650-119">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="ba650-119">-Id</span></span>
<span data-ttu-id="ba650-120">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="ba650-120">The resource group name.</span></span>

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

### <span data-ttu-id="ba650-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ba650-121">-Name</span></span>
<span data-ttu-id="ba650-122">A virtuális gép neve.</span><span class="sxs-lookup"><span data-stu-id="ba650-122">The virtual machine name.</span></span>

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

### <span data-ttu-id="ba650-123">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="ba650-123">-PerformMaintenance</span></span>
<span data-ttu-id="ba650-124">A virtuális gép karbantartásának elvégzéséhez.</span><span class="sxs-lookup"><span data-stu-id="ba650-124">To perform the maintenance of virtual machine.</span></span>

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

### <span data-ttu-id="ba650-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba650-125">-ResourceGroupName</span></span>
<span data-ttu-id="ba650-126">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ba650-126">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="ba650-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ba650-127">-Confirm</span></span>
<span data-ttu-id="ba650-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ba650-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba650-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba650-129">-WhatIf</span></span>
<span data-ttu-id="ba650-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ba650-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ba650-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ba650-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba650-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba650-132">CommonParameters</span></span>
<span data-ttu-id="ba650-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ba650-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba650-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba650-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba650-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba650-135">INPUTS</span></span>

### <span data-ttu-id="ba650-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ba650-136">System.String</span></span>

### <span data-ttu-id="ba650-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ba650-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ba650-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba650-138">OUTPUTS</span></span>

### <span data-ttu-id="ba650-139">Microsoft. Azure. commands. kiszámítás. models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="ba650-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="ba650-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ba650-140">NOTES</span></span>

## <span data-ttu-id="ba650-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ba650-141">RELATED LINKS</span></span>

[<span data-ttu-id="ba650-142">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ba650-142">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="ba650-143">Új – AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ba650-143">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="ba650-144">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ba650-144">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="ba650-145">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ba650-145">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="ba650-146">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ba650-146">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="ba650-147">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ba650-147">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


