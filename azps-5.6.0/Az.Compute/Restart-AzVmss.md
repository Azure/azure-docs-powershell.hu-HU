---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 47F0EE55-78C0-4C71-BD32-C7CB7B200DC3
online version: https://docs.microsoft.com/powershell/module/az.compute/restart-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVmss.md
ms.openlocfilehash: a29e21bba3d04ca301d5f2bf3d2b5f9050fe9765
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940577"
---
# <span data-ttu-id="5f931-101">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="5f931-101">Restart-AzVmss</span></span>

## <span data-ttu-id="5f931-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f931-102">SYNOPSIS</span></span>
<span data-ttu-id="5f931-103">Újraindítja a VMSS-t vagy egy virtuális gépet a VMSS-en belül.</span><span class="sxs-lookup"><span data-stu-id="5f931-103">Restarts the VMSS or a virtual machine within the VMSS.</span></span>

## <span data-ttu-id="5f931-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5f931-104">SYNTAX</span></span>

```
Restart-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f931-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5f931-105">DESCRIPTION</span></span>
<span data-ttu-id="5f931-106">Az **Restart-AzVmss** parancsmag újraindítja a virtuális gép méretezési készletét (VMSS).</span><span class="sxs-lookup"><span data-stu-id="5f931-106">The **Restart-AzVmss** cmdlet restarts the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="5f931-107">Ez a parancsmag egy adott virtuális gépnek a VMSS-en belüli újraindításához is használható *a InstanceId paraméter* használatával.</span><span class="sxs-lookup"><span data-stu-id="5f931-107">This cmdlet can also be used to restart a specific virtual machine inside the VMSS by using the *InstanceId* parameter.</span></span>

## <span data-ttu-id="5f931-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5f931-108">EXAMPLES</span></span>

### <span data-ttu-id="5f931-109">1. példa: A VMSS újraindítása</span><span class="sxs-lookup"><span data-stu-id="5f931-109">Example 1: Restart the VMSS</span></span>
```
PS C:\> Restart-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001";
```

<span data-ttu-id="5f931-110">Ez a parancs újraindítja a VMSS001 nevű VMSSS-t, amely a Group0001 nevű erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="5f931-110">This command restarts the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="5f931-111">2. példa: Egy adott virtuális gép újraindítása a VMSS-en belül</span><span class="sxs-lookup"><span data-stu-id="5f931-111">Example 2: Restart a specific virtual machine within the VMSS</span></span>
```
PS C:\> Restart-AzVmss -ResourceGroupName "Group004" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="5f931-112">Ez a parancs újraindít egy virtuális gépet, amely 1-es példányazonosítóval rendelkezik a VMSS001 nevű VMSS-ben, amely a Group0001 nevű erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="5f931-112">This command restarts a virtual machine that has the instance ID of 1 in the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="5f931-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5f931-113">PARAMETERS</span></span>

### <span data-ttu-id="5f931-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5f931-114">-AsJob</span></span>
<span data-ttu-id="5f931-115">Futtasa a parancsmagot a háttérben, és adja vissza a feladatot az előrehaladás nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="5f931-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="5f931-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f931-116">-DefaultProfile</span></span>
<span data-ttu-id="5f931-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5f931-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f931-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="5f931-118">-InstanceId</span></span>
<span data-ttu-id="5f931-119">Karakterlánc-tömbként megadja az újraindítandó példányok azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="5f931-119">Specifies, as a string array, the ID of the instances that need restarted.</span></span>

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

### <span data-ttu-id="5f931-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f931-120">-ResourceGroupName</span></span>
<span data-ttu-id="5f931-121">A VMSS erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5f931-121">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="5f931-122">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="5f931-122">-VMScaleSetName</span></span>
<span data-ttu-id="5f931-123">A parancsmag által újraindított VMSS nevének fakása.</span><span class="sxs-lookup"><span data-stu-id="5f931-123">Species the name of the VMSS that this cmdlet restarts.</span></span>

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

### <span data-ttu-id="5f931-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5f931-124">-Confirm</span></span>
<span data-ttu-id="5f931-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5f931-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f931-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f931-126">-WhatIf</span></span>
<span data-ttu-id="5f931-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5f931-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5f931-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5f931-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f931-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f931-129">CommonParameters</span></span>
<span data-ttu-id="5f931-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f931-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f931-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5f931-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f931-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5f931-132">INPUTS</span></span>

### <span data-ttu-id="5f931-133">System.String</span><span class="sxs-lookup"><span data-stu-id="5f931-133">System.String</span></span>

### <span data-ttu-id="5f931-134">System.String[]</span><span class="sxs-lookup"><span data-stu-id="5f931-134">System.String[]</span></span>

## <span data-ttu-id="5f931-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5f931-135">OUTPUTS</span></span>

### <span data-ttu-id="5f931-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="5f931-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="5f931-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5f931-137">NOTES</span></span>

## <span data-ttu-id="5f931-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5f931-138">RELATED LINKS</span></span>

[<span data-ttu-id="5f931-139">Get-AzVms</span><span class="sxs-lookup"><span data-stu-id="5f931-139">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="5f931-140">Új-AzVms</span><span class="sxs-lookup"><span data-stu-id="5f931-140">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="5f931-141">Remove-AzVms</span><span class="sxs-lookup"><span data-stu-id="5f931-141">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="5f931-142">Set-AzVms</span><span class="sxs-lookup"><span data-stu-id="5f931-142">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="5f931-143">Start-AzVms</span><span class="sxs-lookup"><span data-stu-id="5f931-143">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="5f931-144">Stop-AzVms</span><span class="sxs-lookup"><span data-stu-id="5f931-144">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="5f931-145">Update-AzVms</span><span class="sxs-lookup"><span data-stu-id="5f931-145">Update-AzVmss</span></span>](./Update-AzVmss.md)


