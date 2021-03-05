---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: D2A7ECF6-E2B1-4BD5-BEA6-C9EC0C7377BA
online version: https://docs.microsoft.com/powershell/module/az.devtestlabs/set-azdtlvmsperlabpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerLabPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerLabPolicy.md
ms.openlocfilehash: 30aad11674cbdef747e444d18bce55ed223e3698
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010581"
---
# <span data-ttu-id="17c29-101">Set-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="17c29-101">Set-AzDtlVMsPerLabPolicy</span></span>

## <span data-ttu-id="17c29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17c29-102">SYNOPSIS</span></span>
<span data-ttu-id="17c29-103">A DevTest Labs tesztelési laboratóriumának laboratóriumi szabályzata szerint beállítja a virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="17c29-103">Sets the virtual machines per lab policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="17c29-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="17c29-104">SYNTAX</span></span>

### <span data-ttu-id="17c29-105">Engedélyezés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="17c29-105">Enable (Default)</span></span>
```
Set-AzDtlVMsPerLabPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17c29-106">Letiltás</span><span class="sxs-lookup"><span data-stu-id="17c29-106">Disable</span></span>
```
Set-AzDtlVMsPerLabPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17c29-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="17c29-107">DESCRIPTION</span></span>
<span data-ttu-id="17c29-108">A **Set-AzDtlVMsPerLabPolicy** parancsmag beállítja a virtuális gépeket egy laboratóriumi házirend alapján, amely meghatározza a laboratóriumokban engedélyezett virtuális gépek teljes számát.</span><span class="sxs-lookup"><span data-stu-id="17c29-108">The **Set-AzDtlVMsPerLabPolicy** cmdlet sets the virtual machines per lab policy of a lab, which sets the total number of virtual machines allowed in a lab.</span></span>
<span data-ttu-id="17c29-109">A parancsmag a megadott erőforráscsoportot és a laboratórium nevét használja a házirend beállításhoz.</span><span class="sxs-lookup"><span data-stu-id="17c29-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="17c29-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="17c29-110">EXAMPLES</span></span>

## <span data-ttu-id="17c29-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17c29-111">PARAMETERS</span></span>

### <span data-ttu-id="17c29-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17c29-112">-DefaultProfile</span></span>
<span data-ttu-id="17c29-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="17c29-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="17c29-114">-Disable</span><span class="sxs-lookup"><span data-stu-id="17c29-114">-Disable</span></span>
<span data-ttu-id="17c29-115">Azt jelzi, hogy ez a parancsmag letiltja a lab házirendet.</span><span class="sxs-lookup"><span data-stu-id="17c29-115">Indicates that this cmdlet disables the policy of the lab.</span></span>

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

### <span data-ttu-id="17c29-116">-Enable</span><span class="sxs-lookup"><span data-stu-id="17c29-116">-Enable</span></span>
<span data-ttu-id="17c29-117">Azt jelzi, hogy ez a parancsmag engedélyezi a laboratóriumi házirendet.</span><span class="sxs-lookup"><span data-stu-id="17c29-117">Indicates that this cmdlet enables the policy of the lab.</span></span>

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

### <span data-ttu-id="17c29-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="17c29-118">-LabName</span></span>
<span data-ttu-id="17c29-119">Annak a laboratóriumnak a neve, amelyhez ez a parancsmag beállítja a virtuális gépeket laboratóriumi házirendenként.</span><span class="sxs-lookup"><span data-stu-id="17c29-119">Specifies the name of the lab for which this cmdlet sets the virtual machines per lab policy.</span></span>

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

### <span data-ttu-id="17c29-120">-MaxVMs</span><span class="sxs-lookup"><span data-stu-id="17c29-120">-MaxVMs</span></span>
<span data-ttu-id="17c29-121">A laboratóriumban létrehozható virtuális gépek maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="17c29-121">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17c29-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17c29-122">-ResourceGroupName</span></span>
<span data-ttu-id="17c29-123">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a laboratórium tartozik.</span><span class="sxs-lookup"><span data-stu-id="17c29-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="17c29-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="17c29-124">-Confirm</span></span>
<span data-ttu-id="17c29-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="17c29-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17c29-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17c29-126">-WhatIf</span></span>
<span data-ttu-id="17c29-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="17c29-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17c29-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="17c29-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17c29-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17c29-129">CommonParameters</span></span>
<span data-ttu-id="17c29-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17c29-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17c29-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17c29-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17c29-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="17c29-132">INPUTS</span></span>

### <span data-ttu-id="17c29-133">System.String</span><span class="sxs-lookup"><span data-stu-id="17c29-133">System.String</span></span>

## <span data-ttu-id="17c29-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="17c29-134">OUTPUTS</span></span>

### <span data-ttu-id="17c29-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="17c29-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="17c29-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="17c29-136">NOTES</span></span>

## <span data-ttu-id="17c29-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="17c29-137">RELATED LINKS</span></span>

[<span data-ttu-id="17c29-138">Get-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="17c29-138">Get-AzDtlVMsPerLabPolicy</span></span>](./Get-AzDtlVMsPerLabPolicy.md)


