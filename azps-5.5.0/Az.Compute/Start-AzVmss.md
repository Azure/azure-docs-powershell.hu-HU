---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmss.md
ms.openlocfilehash: 1845e7f1e76f4b05624c9c79500389b2839d25dd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167882"
---
# <span data-ttu-id="cddef-101">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cddef-101">Start-AzVmss</span></span>

## <span data-ttu-id="cddef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cddef-102">SYNOPSIS</span></span>
<span data-ttu-id="cddef-103">Elindítja a VMSS-t vagy virtuális gépeket a VMSS-en belül.</span><span class="sxs-lookup"><span data-stu-id="cddef-103">Starts the VMSS or a set of virtual machines within the VMSS.</span></span>

## <span data-ttu-id="cddef-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cddef-104">SYNTAX</span></span>

```
Start-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cddef-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cddef-105">DESCRIPTION</span></span>
<span data-ttu-id="cddef-106">A **Start-AzVmss** parancsmag elindítja az összes virtuális gépet a virtuálisgép-mérethalmazon (VMSS) vagy virtuális gépek készletén belül.</span><span class="sxs-lookup"><span data-stu-id="cddef-106">The **Start-AzVmss** cmdlet starts all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="cddef-107">A *InstanceId paraméterrel* kiválaszthatja a virtuális gépek készletét.</span><span class="sxs-lookup"><span data-stu-id="cddef-107">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="cddef-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cddef-108">EXAMPLES</span></span>

### <span data-ttu-id="cddef-109">1. példa: Virtuális gépek adott készletének kezdése a VMSS-en belül</span><span class="sxs-lookup"><span data-stu-id="cddef-109">Example 1: Start a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

<span data-ttu-id="cddef-110">Ez a parancs elindítja a ContosoVMSS nevű VMSS-hez tartozó példányazonosító karakterlánctömbben megadott virtuális gépek meghatározott készletét.</span><span class="sxs-lookup"><span data-stu-id="cddef-110">This command starts a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="cddef-111">2. példa: Az összes virtuális gép kezdése a VMSS-en belül</span><span class="sxs-lookup"><span data-stu-id="cddef-111">Example 2: Start all virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="cddef-112">Ez a parancs elindítja az összes virtuális gépet, amely a ContosoVMSS nevű VMSS-hez tartozik.</span><span class="sxs-lookup"><span data-stu-id="cddef-112">This command starts all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="cddef-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cddef-113">PARAMETERS</span></span>

### <span data-ttu-id="cddef-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cddef-114">-AsJob</span></span>
<span data-ttu-id="cddef-115">Futtasa a parancsmagot a háttérben, és adja vissza a feladatot az előrehaladás nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="cddef-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="cddef-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cddef-116">-DefaultProfile</span></span>
<span data-ttu-id="cddef-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cddef-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cddef-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="cddef-118">-InstanceId</span></span>
<span data-ttu-id="cddef-119">Karakterlánc-tömbként megadja a parancsmag által elindított példányok azonosítóját vagy azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="cddef-119">Specifies, as a string array, the ID or IDs of the instances that cmdlet starts.</span></span>
<span data-ttu-id="cddef-120">Például: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="cddef-120">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="cddef-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cddef-121">-ResourceGroupName</span></span>
<span data-ttu-id="cddef-122">A VMSS erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cddef-122">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="cddef-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="cddef-123">-VMScaleSetName</span></span>
<span data-ttu-id="cddef-124">Annak a VMSS-nek a nevét adja meg, amely elindítja a virtuális gépeket a parancsmagban.</span><span class="sxs-lookup"><span data-stu-id="cddef-124">Specifies the name of the VMSS that this cmdlet starts the virtual machines.</span></span>

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

### <span data-ttu-id="cddef-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cddef-125">-Confirm</span></span>
<span data-ttu-id="cddef-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="cddef-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cddef-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cddef-127">-WhatIf</span></span>
<span data-ttu-id="cddef-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="cddef-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cddef-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cddef-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cddef-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cddef-130">CommonParameters</span></span>
<span data-ttu-id="cddef-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cddef-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cddef-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cddef-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cddef-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cddef-133">INPUTS</span></span>

### <span data-ttu-id="cddef-134">System.String</span><span class="sxs-lookup"><span data-stu-id="cddef-134">System.String</span></span>

### <span data-ttu-id="cddef-135">System.String[]</span><span class="sxs-lookup"><span data-stu-id="cddef-135">System.String[]</span></span>

## <span data-ttu-id="cddef-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cddef-136">OUTPUTS</span></span>

### <span data-ttu-id="cddef-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="cddef-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="cddef-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cddef-138">NOTES</span></span>

## <span data-ttu-id="cddef-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cddef-139">RELATED LINKS</span></span>

[<span data-ttu-id="cddef-140">Get-AzVms</span><span class="sxs-lookup"><span data-stu-id="cddef-140">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="cddef-141">Új-AzVms</span><span class="sxs-lookup"><span data-stu-id="cddef-141">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="cddef-142">Remove-AzVms</span><span class="sxs-lookup"><span data-stu-id="cddef-142">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="cddef-143">Restart-AzVms</span><span class="sxs-lookup"><span data-stu-id="cddef-143">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="cddef-144">Set-AzVms</span><span class="sxs-lookup"><span data-stu-id="cddef-144">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="cddef-145">Stop-AzVms</span><span class="sxs-lookup"><span data-stu-id="cddef-145">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="cddef-146">Update-AzVms</span><span class="sxs-lookup"><span data-stu-id="cddef-146">Update-AzVmss</span></span>](./Update-AzVmss.md)


