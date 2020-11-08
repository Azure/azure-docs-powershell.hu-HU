---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmss.md
ms.openlocfilehash: 1845e7f1e76f4b05624c9c79500389b2839d25dd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014606"
---
# <span data-ttu-id="ba301-101">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ba301-101">Start-AzVmss</span></span>

## <span data-ttu-id="ba301-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ba301-102">SYNOPSIS</span></span>
<span data-ttu-id="ba301-103">Elindítja a VMSS vagy a virtuális gépeket a VMSS belül.</span><span class="sxs-lookup"><span data-stu-id="ba301-103">Starts the VMSS or a set of virtual machines within the VMSS.</span></span>

## <span data-ttu-id="ba301-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ba301-104">SYNTAX</span></span>

```
Start-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba301-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ba301-105">DESCRIPTION</span></span>
<span data-ttu-id="ba301-106">A **Start-AzVmss** parancsmag a Virtual Machine Scale set (VMSS) vagy a virtuális gépek egy halmazán belül minden virtuális gépet elindít.</span><span class="sxs-lookup"><span data-stu-id="ba301-106">The **Start-AzVmss** cmdlet starts all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="ba301-107">A *InstanceId* paraméterrel kiválaszthatja a virtuális gépek halmazát.</span><span class="sxs-lookup"><span data-stu-id="ba301-107">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="ba301-108">Példák</span><span class="sxs-lookup"><span data-stu-id="ba301-108">EXAMPLES</span></span>

### <span data-ttu-id="ba301-109">1. példa: a virtuális gépek meghatározott halmazának indítása a VMSS belül</span><span class="sxs-lookup"><span data-stu-id="ba301-109">Example 1: Start a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

<span data-ttu-id="ba301-110">Ez a parancs a ContosoVMSS nevű VMSS tartozó példánynév karakterláncban meghatározott virtuális gépek meghatározott halmazát indítja el.</span><span class="sxs-lookup"><span data-stu-id="ba301-110">This command starts a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="ba301-111">2. példa: az összes virtuális gép elindítása a VMSS belül</span><span class="sxs-lookup"><span data-stu-id="ba301-111">Example 2: Start all virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="ba301-112">Ez a parancs elindítja az összes olyan virtuális gépet, amely a ContosoVMSS nevű VMSS tartozik.</span><span class="sxs-lookup"><span data-stu-id="ba301-112">This command starts all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="ba301-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ba301-113">PARAMETERS</span></span>

### <span data-ttu-id="ba301-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ba301-114">-AsJob</span></span>
<span data-ttu-id="ba301-115">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="ba301-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="ba301-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba301-116">-DefaultProfile</span></span>
<span data-ttu-id="ba301-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ba301-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba301-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="ba301-118">-InstanceId</span></span>
<span data-ttu-id="ba301-119">Karakterláncként adja meg a parancsmag által elinduló példányok AZONOSÍTÓját vagy azonosítóit.</span><span class="sxs-lookup"><span data-stu-id="ba301-119">Specifies, as a string array, the ID or IDs of the instances that cmdlet starts.</span></span>
<span data-ttu-id="ba301-120">Például: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="ba301-120">For instance: `-InstanceId "0", "3"`</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba301-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba301-121">-ResourceGroupName</span></span>
<span data-ttu-id="ba301-122">A VMSS erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ba301-122">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba301-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="ba301-123">-VMScaleSetName</span></span>
<span data-ttu-id="ba301-124">Annak a VMSS a nevét adja meg, amely a parancsmag által a virtuális gépeket indítja el.</span><span class="sxs-lookup"><span data-stu-id="ba301-124">Specifies the name of the VMSS that this cmdlet starts the virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba301-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ba301-125">-Confirm</span></span>
<span data-ttu-id="ba301-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ba301-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba301-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba301-127">-WhatIf</span></span>
<span data-ttu-id="ba301-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ba301-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ba301-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ba301-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba301-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba301-130">CommonParameters</span></span>
<span data-ttu-id="ba301-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ba301-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba301-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ba301-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba301-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba301-133">INPUTS</span></span>

### <span data-ttu-id="ba301-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ba301-134">System.String</span></span>

### <span data-ttu-id="ba301-135">System. string []</span><span class="sxs-lookup"><span data-stu-id="ba301-135">System.String[]</span></span>

## <span data-ttu-id="ba301-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba301-136">OUTPUTS</span></span>

### <span data-ttu-id="ba301-137">Microsoft. Azure. commands. számítási. Automation. models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="ba301-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="ba301-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ba301-138">NOTES</span></span>

## <span data-ttu-id="ba301-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ba301-139">RELATED LINKS</span></span>

[<span data-ttu-id="ba301-140">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ba301-140">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="ba301-141">Új – AzVmss</span><span class="sxs-lookup"><span data-stu-id="ba301-141">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="ba301-142">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ba301-142">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="ba301-143">Újraindítás – AzVmss</span><span class="sxs-lookup"><span data-stu-id="ba301-143">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="ba301-144">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ba301-144">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="ba301-145">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ba301-145">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="ba301-146">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ba301-146">Update-AzVmss</span></span>](./Update-AzVmss.md)


