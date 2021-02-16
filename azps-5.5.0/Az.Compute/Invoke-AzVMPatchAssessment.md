---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMPatchAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMPatchAssessment.md
ms.openlocfilehash: 52e7a7372372bfcb0dfc93a9a89715e91c484b73
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162266"
---
# <span data-ttu-id="358fd-101">Invoke-AzVMPatchAssessment</span><span class="sxs-lookup"><span data-stu-id="358fd-101">Invoke-AzVMPatchAssessment</span></span>

## <span data-ttu-id="358fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="358fd-102">SYNOPSIS</span></span>
<span data-ttu-id="358fd-103">Mérje fel egy virtuális gép javításállapotát.</span><span class="sxs-lookup"><span data-stu-id="358fd-103">Assess patch state of a virtual machine.</span></span>

## <span data-ttu-id="358fd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="358fd-104">SYNTAX</span></span>

### <span data-ttu-id="358fd-105">DefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="358fd-105">DefaultParameterSet (Default)</span></span>
```
Invoke-AzVMPatchAssessment [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="358fd-106">ResourceIDParameterSet</span><span class="sxs-lookup"><span data-stu-id="358fd-106">ResourceIDParameterSet</span></span>
```
Invoke-AzVMPatchAssessment [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="358fd-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="358fd-107">InputObjectParameterSet</span></span>
```
Invoke-AzVMPatchAssessment [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="358fd-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="358fd-108">DESCRIPTION</span></span>
<span data-ttu-id="358fd-109">Felméri egy vm javításának állapotát, és bejelentéseket készít a telepítéshez elérhető összes észlelt javításról.</span><span class="sxs-lookup"><span data-stu-id="358fd-109">Assesses the patch status of a VM and reports all detected patches that are available for installation.</span></span>

## <span data-ttu-id="358fd-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="358fd-110">EXAMPLES</span></span>

### <span data-ttu-id="358fd-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="358fd-111">Example 1</span></span>
```
PS C:\> Invoke-AzVmPatchAssessment -ResourceGroupName "myRG" -VMName "myVM"
```

## <span data-ttu-id="358fd-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="358fd-112">PARAMETERS</span></span>

### <span data-ttu-id="358fd-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="358fd-113">-AsJob</span></span>
<span data-ttu-id="358fd-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="358fd-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="358fd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="358fd-115">-DefaultProfile</span></span>
<span data-ttu-id="358fd-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="358fd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="358fd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="358fd-117">-ResourceGroupName</span></span>
<span data-ttu-id="358fd-118">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="358fd-118">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="358fd-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="358fd-119">-ResourceId</span></span>
<span data-ttu-id="358fd-120">A virtuális gép erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="358fd-120">Resource ID for your virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIDParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="358fd-121">-VM</span><span class="sxs-lookup"><span data-stu-id="358fd-121">-VM</span></span>
<span data-ttu-id="358fd-122">PowerShell Virtuális gép objektum</span><span class="sxs-lookup"><span data-stu-id="358fd-122">PowerShell Virtual Machine Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: InputObjectParameterSet
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="358fd-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="358fd-123">-VMName</span></span>
<span data-ttu-id="358fd-124">Virtuális gép neve</span><span class="sxs-lookup"><span data-stu-id="358fd-124">Virtual Machine name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="358fd-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="358fd-125">-Confirm</span></span>
<span data-ttu-id="358fd-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="358fd-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="358fd-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="358fd-127">-WhatIf</span></span>
<span data-ttu-id="358fd-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="358fd-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="358fd-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="358fd-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="358fd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="358fd-130">CommonParameters</span></span>
<span data-ttu-id="358fd-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="358fd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="358fd-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="358fd-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="358fd-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="358fd-133">INPUTS</span></span>

### <span data-ttu-id="358fd-134">System.String</span><span class="sxs-lookup"><span data-stu-id="358fd-134">System.String</span></span>

## <span data-ttu-id="358fd-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="358fd-135">OUTPUTS</span></span>

### <span data-ttu-id="358fd-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachinePatchAssessmentResult</span><span class="sxs-lookup"><span data-stu-id="358fd-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachinePatchAssessmentResult</span></span>

## <span data-ttu-id="358fd-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="358fd-137">NOTES</span></span>

## <span data-ttu-id="358fd-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="358fd-138">RELATED LINKS</span></span>
