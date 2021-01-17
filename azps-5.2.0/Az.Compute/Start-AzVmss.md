---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmss.md
ms.openlocfilehash: 1845e7f1e76f4b05624c9c79500389b2839d25dd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362318"
---
# <span data-ttu-id="50e88-101">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="50e88-101">Start-AzVmss</span></span>

## <span data-ttu-id="50e88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50e88-102">SYNOPSIS</span></span>
<span data-ttu-id="50e88-103">Elindítja a VMSS-t vagy virtuális gépeket a VMSS-en belül.</span><span class="sxs-lookup"><span data-stu-id="50e88-103">Starts the VMSS or a set of virtual machines within the VMSS.</span></span>

## <span data-ttu-id="50e88-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="50e88-104">SYNTAX</span></span>

```
Start-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50e88-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="50e88-105">DESCRIPTION</span></span>
<span data-ttu-id="50e88-106">A **Start-AzVmss** parancsmag elindítja az összes virtuális gépet a virtuálisgép-mérethalmazon (VMSS) vagy virtuális gépek készletén belül.</span><span class="sxs-lookup"><span data-stu-id="50e88-106">The **Start-AzVmss** cmdlet starts all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="50e88-107">A *InstanceId paraméterrel* kiválaszthatja a virtuális gépek készletét.</span><span class="sxs-lookup"><span data-stu-id="50e88-107">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="50e88-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="50e88-108">EXAMPLES</span></span>

### <span data-ttu-id="50e88-109">1. példa: Virtuális gépek adott készletének kezdése a VMSS-en belül</span><span class="sxs-lookup"><span data-stu-id="50e88-109">Example 1: Start a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

<span data-ttu-id="50e88-110">Ez a parancs elindítja a ContosoVMSS nevű VMSS-hez tartozó példányazonosító karakterlánctömbben megadott virtuális gépek meghatározott készletét.</span><span class="sxs-lookup"><span data-stu-id="50e88-110">This command starts a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="50e88-111">2. példa: Az összes virtuális gép kezdése a VMSS-en belül</span><span class="sxs-lookup"><span data-stu-id="50e88-111">Example 2: Start all virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="50e88-112">Ez a parancs elindítja a ContosoVMSS nevű VMSS-hez tartozó összes virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="50e88-112">This command starts all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="50e88-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50e88-113">PARAMETERS</span></span>

### <span data-ttu-id="50e88-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="50e88-114">-AsJob</span></span>
<span data-ttu-id="50e88-115">Futtasa a parancsmagot a háttérben, és adja vissza a feladatot az előrehaladás nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="50e88-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="50e88-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50e88-116">-DefaultProfile</span></span>
<span data-ttu-id="50e88-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="50e88-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50e88-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="50e88-118">-InstanceId</span></span>
<span data-ttu-id="50e88-119">Karakterlánc-tömbként megadja a parancsmag által elindított példányok azonosítóját vagy azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="50e88-119">Specifies, as a string array, the ID or IDs of the instances that cmdlet starts.</span></span>
<span data-ttu-id="50e88-120">Például: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="50e88-120">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="50e88-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50e88-121">-ResourceGroupName</span></span>
<span data-ttu-id="50e88-122">A VMSS erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="50e88-122">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="50e88-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="50e88-123">-VMScaleSetName</span></span>
<span data-ttu-id="50e88-124">Megadja annak a VMSS-nek a nevét, amelytől a parancsmag elindítja a virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="50e88-124">Specifies the name of the VMSS that this cmdlet starts the virtual machines.</span></span>

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

### <span data-ttu-id="50e88-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="50e88-125">-Confirm</span></span>
<span data-ttu-id="50e88-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="50e88-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50e88-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50e88-127">-WhatIf</span></span>
<span data-ttu-id="50e88-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="50e88-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="50e88-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="50e88-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50e88-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50e88-130">CommonParameters</span></span>
<span data-ttu-id="50e88-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50e88-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50e88-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="50e88-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50e88-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="50e88-133">INPUTS</span></span>

### <span data-ttu-id="50e88-134">System.String</span><span class="sxs-lookup"><span data-stu-id="50e88-134">System.String</span></span>

### <span data-ttu-id="50e88-135">System.String[]</span><span class="sxs-lookup"><span data-stu-id="50e88-135">System.String[]</span></span>

## <span data-ttu-id="50e88-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="50e88-136">OUTPUTS</span></span>

### <span data-ttu-id="50e88-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="50e88-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="50e88-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="50e88-138">NOTES</span></span>

## <span data-ttu-id="50e88-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="50e88-139">RELATED LINKS</span></span>

[<span data-ttu-id="50e88-140">Get-AzVms</span><span class="sxs-lookup"><span data-stu-id="50e88-140">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="50e88-141">Új-AzVms</span><span class="sxs-lookup"><span data-stu-id="50e88-141">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="50e88-142">Remove-AzVms</span><span class="sxs-lookup"><span data-stu-id="50e88-142">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="50e88-143">Restart-AzVms</span><span class="sxs-lookup"><span data-stu-id="50e88-143">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="50e88-144">Set-AzVms</span><span class="sxs-lookup"><span data-stu-id="50e88-144">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="50e88-145">Stop-AzVms</span><span class="sxs-lookup"><span data-stu-id="50e88-145">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="50e88-146">Update-AzVms</span><span class="sxs-lookup"><span data-stu-id="50e88-146">Update-AzVmss</span></span>](./Update-AzVmss.md)


