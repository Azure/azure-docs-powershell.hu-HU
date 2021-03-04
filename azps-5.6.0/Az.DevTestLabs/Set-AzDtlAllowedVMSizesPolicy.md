---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: AAABDD1D-71BF-409C-B50B-9BE861D84229
online version: https://docs.microsoft.com/powershell/module/az.devtestlabs/set-azdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: 04538710a078c72c7b91725823601a55c21ef846
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940505"
---
# <span data-ttu-id="cda0f-101">Set-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="cda0f-101">Set-AzDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="cda0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cda0f-102">SYNOPSIS</span></span>
<span data-ttu-id="cda0f-103">Beállítja a DevTest Labs által engedélyezett virtuális gépméretekre vonatkozó házirendet.</span><span class="sxs-lookup"><span data-stu-id="cda0f-103">Sets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="cda0f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cda0f-104">SYNTAX</span></span>

### <span data-ttu-id="cda0f-105">Engedélyezés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cda0f-105">Enable (Default)</span></span>
```
Set-AzDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cda0f-106">Letiltás</span><span class="sxs-lookup"><span data-stu-id="cda0f-106">Disable</span></span>
```
Set-AzDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cda0f-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cda0f-107">DESCRIPTION</span></span>
<span data-ttu-id="cda0f-108">A **Set-AzDtlAllowedVMSizesPolicy** parancsmag beállítja az engedélyezett virtuális gépméretekre vonatkozó házirendet, amely megadja a laboratóriumokban engedélyezett virtuális gépméretek listáját.</span><span class="sxs-lookup"><span data-stu-id="cda0f-108">The **Set-AzDtlAllowedVMSizesPolicy** cmdlet sets the allowed virtual machine sizes policy, which specifies a list of virtual machine sizes allowed in a lab.</span></span>
<span data-ttu-id="cda0f-109">A parancsmag a megadott erőforráscsoportot és a laboratórium nevét használja a házirend beállításhoz.</span><span class="sxs-lookup"><span data-stu-id="cda0f-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="cda0f-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cda0f-110">EXAMPLES</span></span>

## <span data-ttu-id="cda0f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cda0f-111">PARAMETERS</span></span>

### <span data-ttu-id="cda0f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cda0f-112">-DefaultProfile</span></span>
<span data-ttu-id="cda0f-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="cda0f-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cda0f-114">-Disable</span><span class="sxs-lookup"><span data-stu-id="cda0f-114">-Disable</span></span>
<span data-ttu-id="cda0f-115">Azt jelzi, hogy ez a parancsmag letiltja a házirendet.</span><span class="sxs-lookup"><span data-stu-id="cda0f-115">Indicates that this cmdlet disables the policy.</span></span>

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

### <span data-ttu-id="cda0f-116">-Enable</span><span class="sxs-lookup"><span data-stu-id="cda0f-116">-Enable</span></span>
<span data-ttu-id="cda0f-117">Azt jelzi, hogy ez a parancsmag engedélyezi a házirendet.</span><span class="sxs-lookup"><span data-stu-id="cda0f-117">Indicates that this cmdlet enables the policy.</span></span>

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

### <span data-ttu-id="cda0f-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="cda0f-118">-LabName</span></span>
<span data-ttu-id="cda0f-119">Annak a laboratóriumnak a nevét adja meg, amelyhez ez a parancsmag beállítja a virtuális gépméretekre vonatkozó házirendet.</span><span class="sxs-lookup"><span data-stu-id="cda0f-119">Specifies the name of the lab for which this cmdlet sets the virtual machine sizes policy.</span></span>

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

### <span data-ttu-id="cda0f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cda0f-120">-ResourceGroupName</span></span>
<span data-ttu-id="cda0f-121">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a laboratórium tartozik.</span><span class="sxs-lookup"><span data-stu-id="cda0f-121">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="cda0f-122">-VmSizes</span><span class="sxs-lookup"><span data-stu-id="cda0f-122">-VmSizes</span></span>
<span data-ttu-id="cda0f-123">Karakterlánc-tömbként megadja a laboratóriumban engedélyezett virtuális gépméretek listáját.</span><span class="sxs-lookup"><span data-stu-id="cda0f-123">Specifies, as a string array, the list of virtual machine sizes allowed in the lab.</span></span>

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

### <span data-ttu-id="cda0f-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cda0f-124">-Confirm</span></span>
<span data-ttu-id="cda0f-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="cda0f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cda0f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cda0f-126">-WhatIf</span></span>
<span data-ttu-id="cda0f-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="cda0f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cda0f-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cda0f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cda0f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cda0f-129">CommonParameters</span></span>
<span data-ttu-id="cda0f-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cda0f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cda0f-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cda0f-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cda0f-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cda0f-132">INPUTS</span></span>

### <span data-ttu-id="cda0f-133">System.String</span><span class="sxs-lookup"><span data-stu-id="cda0f-133">System.String</span></span>

## <span data-ttu-id="cda0f-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cda0f-134">OUTPUTS</span></span>

### <span data-ttu-id="cda0f-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="cda0f-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="cda0f-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cda0f-136">NOTES</span></span>

## <span data-ttu-id="cda0f-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cda0f-137">RELATED LINKS</span></span>

[<span data-ttu-id="cda0f-138">Get-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="cda0f-138">Get-AzDtlAllowedVMSizesPolicy</span></span>](./Get-AzDtlAllowedVMSizesPolicy.md)


