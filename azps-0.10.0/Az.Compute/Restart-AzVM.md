---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/restart-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Restart-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Restart-AzVM.md
ms.openlocfilehash: f7965e43c7a294d50d6f0774f76504a90c9d7148
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844333"
---
# <span data-ttu-id="47442-101">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="47442-101">Restart-AzVM</span></span>

## <span data-ttu-id="47442-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="47442-102">SYNOPSIS</span></span>
<span data-ttu-id="47442-103">Azure virtuális gép újraindítása.</span><span class="sxs-lookup"><span data-stu-id="47442-103">Restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="47442-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="47442-104">SYNTAX</span></span>

### <span data-ttu-id="47442-105">RestartResourceGroupNameParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="47442-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47442-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="47442-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47442-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="47442-107">RestartIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47442-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="47442-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-Name] <String> [-PerformMaintenance] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47442-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="47442-109">DESCRIPTION</span></span>
<span data-ttu-id="47442-110">Az **Újraindítás – AzVM** parancsmag újraindítja az Azure Virtual machinet.</span><span class="sxs-lookup"><span data-stu-id="47442-110">The **Restart-AzVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="47442-111">Példák</span><span class="sxs-lookup"><span data-stu-id="47442-111">EXAMPLES</span></span>

### <span data-ttu-id="47442-112">1. példa: virtuális gép újraindítása</span><span class="sxs-lookup"><span data-stu-id="47442-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="47442-113">Ez a parancs elindítja a VirtualMachine07 nevű virtuális gépet a ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="47442-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="47442-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="47442-114">PARAMETERS</span></span>

### <span data-ttu-id="47442-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47442-115">-AsJob</span></span>
<span data-ttu-id="47442-116">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="47442-116">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47442-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47442-117">-DefaultProfile</span></span>
<span data-ttu-id="47442-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="47442-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47442-119">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="47442-119">-Id</span></span>
<span data-ttu-id="47442-120">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="47442-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: RestartIdParameterSetName, PerformMaintenanceIdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47442-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="47442-121">-Name</span></span>
<span data-ttu-id="47442-122">A virtuális gép neve.</span><span class="sxs-lookup"><span data-stu-id="47442-122">The virtual machine name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47442-123">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="47442-123">-PerformMaintenance</span></span>
<span data-ttu-id="47442-124">A virtuális gép karbantartásának elvégzéséhez.</span><span class="sxs-lookup"><span data-stu-id="47442-124">To perform the maintenance of virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PerformMaintenanceResourceGroupNameParameterSetName, PerformMaintenanceIdParameterSetName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47442-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47442-125">-ResourceGroupName</span></span>
<span data-ttu-id="47442-126">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="47442-126">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: RestartResourceGroupNameParameterSetName, PerformMaintenanceResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47442-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="47442-127">-Confirm</span></span>
<span data-ttu-id="47442-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="47442-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47442-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47442-129">-WhatIf</span></span>
<span data-ttu-id="47442-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="47442-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="47442-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="47442-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47442-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47442-132">CommonParameters</span></span>
<span data-ttu-id="47442-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="47442-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47442-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47442-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47442-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="47442-135">INPUTS</span></span>

### <span data-ttu-id="47442-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="47442-136">None</span></span>
<span data-ttu-id="47442-137">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="47442-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="47442-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="47442-138">OUTPUTS</span></span>

### <span data-ttu-id="47442-139">Microsoft. Azure. commands. kiszámítás. models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="47442-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="47442-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="47442-140">NOTES</span></span>

## <span data-ttu-id="47442-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="47442-141">RELATED LINKS</span></span>

[<span data-ttu-id="47442-142">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="47442-142">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="47442-143">Új – AzVM</span><span class="sxs-lookup"><span data-stu-id="47442-143">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="47442-144">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="47442-144">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="47442-145">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="47442-145">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="47442-146">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="47442-146">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="47442-147">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="47442-147">Update-AzVM</span></span>](./Update-AzVM.md)


