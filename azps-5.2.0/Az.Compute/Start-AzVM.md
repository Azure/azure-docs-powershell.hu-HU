---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
ms.openlocfilehash: 32e633d1f9fea877ef81b6c6e7ef5e8bb09da81a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346325"
---
# <span data-ttu-id="86776-101">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="86776-101">Start-AzVM</span></span>

## <span data-ttu-id="86776-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86776-102">SYNOPSIS</span></span>
<span data-ttu-id="86776-103">Elindít egy Azure virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="86776-103">Starts an Azure virtual machine.</span></span>

## <span data-ttu-id="86776-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="86776-104">SYNTAX</span></span>

### <span data-ttu-id="86776-105">ResourceGroupNameParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="86776-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzVM [-Name] <String> [-NoWait] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86776-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="86776-106">IdParameterSetName</span></span>
```
Start-AzVM [-NoWait] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="86776-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="86776-107">DESCRIPTION</span></span>
<span data-ttu-id="86776-108">A **Start-AzVM parancsmag** elindít egy Azure virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="86776-108">The **Start-AzVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="86776-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="86776-109">EXAMPLES</span></span>

### <span data-ttu-id="86776-110">1. példa: Virtuális gép létrehozása</span><span class="sxs-lookup"><span data-stu-id="86776-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="86776-111">Ez a parancs elindítja a VirtualMachine07 nevű virtuális gépet az ResourceGroup11-ben.</span><span class="sxs-lookup"><span data-stu-id="86776-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="86776-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="86776-112">PARAMETERS</span></span>

### <span data-ttu-id="86776-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="86776-113">-AsJob</span></span>
<span data-ttu-id="86776-114">Futtasa a parancsmagot a háttérben, és adja vissza a feladatot az előrehaladás nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="86776-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="86776-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86776-115">-DefaultProfile</span></span>
<span data-ttu-id="86776-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="86776-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86776-117">-Id</span><span class="sxs-lookup"><span data-stu-id="86776-117">-Id</span></span>
<span data-ttu-id="86776-118">A virtuális gép azonosítója.</span><span class="sxs-lookup"><span data-stu-id="86776-118">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="86776-119">-Name</span><span class="sxs-lookup"><span data-stu-id="86776-119">-Name</span></span>
<span data-ttu-id="86776-120">A virtuális gép neve.</span><span class="sxs-lookup"><span data-stu-id="86776-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="86776-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="86776-121">-NoWait</span></span>
<span data-ttu-id="86776-122">Elindítja a műveletet, és azonnal, a művelet befejezése előtt visszatér.</span><span class="sxs-lookup"><span data-stu-id="86776-122">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="86776-123">Ha meg szeretné állapítani, hogy a művelet sikeresen befejeződött-e, használjon más mechanizmust.</span><span class="sxs-lookup"><span data-stu-id="86776-123">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="86776-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86776-124">-ResourceGroupName</span></span>
<span data-ttu-id="86776-125">A virtuális gép erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="86776-125">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="86776-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="86776-126">-Confirm</span></span>
<span data-ttu-id="86776-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="86776-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86776-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86776-128">-WhatIf</span></span>
<span data-ttu-id="86776-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="86776-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="86776-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="86776-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86776-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86776-131">CommonParameters</span></span>
<span data-ttu-id="86776-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86776-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86776-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="86776-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86776-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="86776-134">INPUTS</span></span>

### <span data-ttu-id="86776-135">System.String</span><span class="sxs-lookup"><span data-stu-id="86776-135">System.String</span></span>

## <span data-ttu-id="86776-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="86776-136">OUTPUTS</span></span>

### <span data-ttu-id="86776-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="86776-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="86776-138">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="86776-138">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="86776-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="86776-139">NOTES</span></span>

## <span data-ttu-id="86776-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="86776-140">RELATED LINKS</span></span>

[<span data-ttu-id="86776-141">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="86776-141">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="86776-142">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="86776-142">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="86776-143">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="86776-143">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="86776-144">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="86776-144">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="86776-145">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="86776-145">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="86776-146">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="86776-146">Update-AzVM</span></span>](./Update-AzVM.md)


