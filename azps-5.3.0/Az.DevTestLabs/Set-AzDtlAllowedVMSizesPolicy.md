---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: AAABDD1D-71BF-409C-B50B-9BE861D84229
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: d5e8b16fec390c4b4d900760d3efb60abfb7da0e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467846"
---
# <span data-ttu-id="5ce82-101">Set-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="5ce82-101">Set-AzDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="5ce82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ce82-102">SYNOPSIS</span></span>
<span data-ttu-id="5ce82-103">Beállítja a DevTest Labs által engedélyezett virtuális gépméretekre vonatkozó házirendet.</span><span class="sxs-lookup"><span data-stu-id="5ce82-103">Sets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="5ce82-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5ce82-104">SYNTAX</span></span>

### <span data-ttu-id="5ce82-105">Engedélyezés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5ce82-105">Enable (Default)</span></span>
```
Set-AzDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ce82-106">Letiltás</span><span class="sxs-lookup"><span data-stu-id="5ce82-106">Disable</span></span>
```
Set-AzDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5ce82-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5ce82-107">DESCRIPTION</span></span>
<span data-ttu-id="5ce82-108">A **Set-AzDtlAllowedVMSizesPolicy** parancsmag beállítja az engedélyezett virtuális gépméretekre vonatkozó házirendet, amely megadja a laboratóriumokban engedélyezett virtuális gépméretek listáját.</span><span class="sxs-lookup"><span data-stu-id="5ce82-108">The **Set-AzDtlAllowedVMSizesPolicy** cmdlet sets the allowed virtual machine sizes policy, which specifies a list of virtual machine sizes allowed in a lab.</span></span>
<span data-ttu-id="5ce82-109">A parancsmag a megadott erőforráscsoportot és a laboratórium nevét használja a házirend beállításhoz.</span><span class="sxs-lookup"><span data-stu-id="5ce82-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="5ce82-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5ce82-110">EXAMPLES</span></span>

## <span data-ttu-id="5ce82-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ce82-111">PARAMETERS</span></span>

### <span data-ttu-id="5ce82-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ce82-112">-DefaultProfile</span></span>
<span data-ttu-id="5ce82-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5ce82-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ce82-114">-Disable</span><span class="sxs-lookup"><span data-stu-id="5ce82-114">-Disable</span></span>
<span data-ttu-id="5ce82-115">Azt jelzi, hogy ez a parancsmag letiltja a házirendet.</span><span class="sxs-lookup"><span data-stu-id="5ce82-115">Indicates that this cmdlet disables the policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ce82-116">-Enable</span><span class="sxs-lookup"><span data-stu-id="5ce82-116">-Enable</span></span>
<span data-ttu-id="5ce82-117">Azt jelzi, hogy ez a parancsmag engedélyezi a házirendet.</span><span class="sxs-lookup"><span data-stu-id="5ce82-117">Indicates that this cmdlet enables the policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Enable
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ce82-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="5ce82-118">-LabName</span></span>
<span data-ttu-id="5ce82-119">Annak a laboratóriumnak a nevét adja meg, amelyhez ez a parancsmag beállítja a virtuális gépméretekre vonatkozó házirendet.</span><span class="sxs-lookup"><span data-stu-id="5ce82-119">Specifies the name of the lab for which this cmdlet sets the virtual machine sizes policy.</span></span>

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

### <span data-ttu-id="5ce82-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ce82-120">-ResourceGroupName</span></span>
<span data-ttu-id="5ce82-121">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a laboratórium tartozik.</span><span class="sxs-lookup"><span data-stu-id="5ce82-121">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="5ce82-122">-VmSizes</span><span class="sxs-lookup"><span data-stu-id="5ce82-122">-VmSizes</span></span>
<span data-ttu-id="5ce82-123">Karakterlánc-tömbként megadja a laboratóriumban engedélyezett virtuális gépméretek listáját.</span><span class="sxs-lookup"><span data-stu-id="5ce82-123">Specifies, as a string array, the list of virtual machine sizes allowed in the lab.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ce82-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5ce82-124">-Confirm</span></span>
<span data-ttu-id="5ce82-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5ce82-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ce82-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ce82-126">-WhatIf</span></span>
<span data-ttu-id="5ce82-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5ce82-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ce82-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5ce82-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ce82-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ce82-129">CommonParameters</span></span>
<span data-ttu-id="5ce82-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ce82-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ce82-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ce82-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ce82-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5ce82-132">INPUTS</span></span>

### <span data-ttu-id="5ce82-133">System.String</span><span class="sxs-lookup"><span data-stu-id="5ce82-133">System.String</span></span>

## <span data-ttu-id="5ce82-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ce82-134">OUTPUTS</span></span>

### <span data-ttu-id="5ce82-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="5ce82-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="5ce82-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5ce82-136">NOTES</span></span>

## <span data-ttu-id="5ce82-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5ce82-137">RELATED LINKS</span></span>

[<span data-ttu-id="5ce82-138">Get-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="5ce82-138">Get-AzDtlAllowedVMSizesPolicy</span></span>](./Get-AzDtlAllowedVMSizesPolicy.md)


