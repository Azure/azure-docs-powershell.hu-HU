---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
ms.openlocfilehash: 32e633d1f9fea877ef81b6c6e7ef5e8bb09da81a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477638"
---
# <span data-ttu-id="935b9-101">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="935b9-101">Start-AzVM</span></span>

## <span data-ttu-id="935b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="935b9-102">SYNOPSIS</span></span>
<span data-ttu-id="935b9-103">Elindít egy Azure virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="935b9-103">Starts an Azure virtual machine.</span></span>

## <span data-ttu-id="935b9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="935b9-104">SYNTAX</span></span>

### <span data-ttu-id="935b9-105">ResourceGroupNameParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="935b9-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzVM [-Name] <String> [-NoWait] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="935b9-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="935b9-106">IdParameterSetName</span></span>
```
Start-AzVM [-NoWait] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="935b9-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="935b9-107">DESCRIPTION</span></span>
<span data-ttu-id="935b9-108">A **Start-AzVM parancsmag** elindít egy Azure virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="935b9-108">The **Start-AzVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="935b9-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="935b9-109">EXAMPLES</span></span>

### <span data-ttu-id="935b9-110">1. példa: Virtuális gép létrehozása</span><span class="sxs-lookup"><span data-stu-id="935b9-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="935b9-111">Ez a parancs elindítja a VirtualMachine07 nevű virtuális gépet az ResourceGroup11-ben.</span><span class="sxs-lookup"><span data-stu-id="935b9-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="935b9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="935b9-112">PARAMETERS</span></span>

### <span data-ttu-id="935b9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="935b9-113">-AsJob</span></span>
<span data-ttu-id="935b9-114">Futtasa a parancsmagot a háttérben, és adja vissza a feladatot az előrehaladás nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="935b9-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="935b9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="935b9-115">-DefaultProfile</span></span>
<span data-ttu-id="935b9-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="935b9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="935b9-117">-Id</span><span class="sxs-lookup"><span data-stu-id="935b9-117">-Id</span></span>
<span data-ttu-id="935b9-118">A virtuális gép azonosítója.</span><span class="sxs-lookup"><span data-stu-id="935b9-118">The ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="935b9-119">-Name</span><span class="sxs-lookup"><span data-stu-id="935b9-119">-Name</span></span>
<span data-ttu-id="935b9-120">A virtuális gép neve.</span><span class="sxs-lookup"><span data-stu-id="935b9-120">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="935b9-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="935b9-121">-NoWait</span></span>
<span data-ttu-id="935b9-122">Elindítja a műveletet, és azonnal, a művelet befejezése előtt visszatér.</span><span class="sxs-lookup"><span data-stu-id="935b9-122">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="935b9-123">Ha meg szeretné állapítani, hogy a művelet sikeresen befejeződött-e, használjon más mechanizmust.</span><span class="sxs-lookup"><span data-stu-id="935b9-123">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="935b9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="935b9-124">-ResourceGroupName</span></span>
<span data-ttu-id="935b9-125">A virtuális gép erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="935b9-125">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="935b9-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="935b9-126">-Confirm</span></span>
<span data-ttu-id="935b9-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="935b9-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="935b9-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="935b9-128">-WhatIf</span></span>
<span data-ttu-id="935b9-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="935b9-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="935b9-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="935b9-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="935b9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="935b9-131">CommonParameters</span></span>
<span data-ttu-id="935b9-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="935b9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="935b9-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="935b9-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="935b9-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="935b9-134">INPUTS</span></span>

### <span data-ttu-id="935b9-135">System.String</span><span class="sxs-lookup"><span data-stu-id="935b9-135">System.String</span></span>

## <span data-ttu-id="935b9-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="935b9-136">OUTPUTS</span></span>

### <span data-ttu-id="935b9-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="935b9-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="935b9-138">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="935b9-138">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="935b9-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="935b9-139">NOTES</span></span>

## <span data-ttu-id="935b9-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="935b9-140">RELATED LINKS</span></span>

[<span data-ttu-id="935b9-141">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="935b9-141">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="935b9-142">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="935b9-142">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="935b9-143">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="935b9-143">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="935b9-144">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="935b9-144">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="935b9-145">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="935b9-145">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="935b9-146">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="935b9-146">Update-AzVM</span></span>](./Update-AzVM.md)


