---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/powershell/module/az.customproviders/new-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProviderAssociation.md
ms.openlocfilehash: af502cd4115ba9ef7467c15aa09b78e5e33c2337
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943033"
---
# <span data-ttu-id="d37bc-101">New-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="d37bc-101">New-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="d37bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d37bc-102">SYNOPSIS</span></span>
<span data-ttu-id="d37bc-103">Társítás létrehozása vagy frissítése.</span><span class="sxs-lookup"><span data-stu-id="d37bc-103">Create or update an association.</span></span>

## <span data-ttu-id="d37bc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d37bc-104">SYNTAX</span></span>

```
New-AzCustomProviderAssociation -Name <String> -Scope <String> [-TargetResourceId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d37bc-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d37bc-105">DESCRIPTION</span></span>
<span data-ttu-id="d37bc-106">Társítás létrehozása vagy frissítése.</span><span class="sxs-lookup"><span data-stu-id="d37bc-106">Create or update an association.</span></span>

## <span data-ttu-id="d37bc-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d37bc-107">EXAMPLES</span></span>

### <span data-ttu-id="d37bc-108">1. példa: Egyéni szolgáltató társítás létrehozása</span><span class="sxs-lookup"><span data-stu-id="d37bc-108">Example 1: Create a custom provider association</span></span>
```powershell
PS C:\> $provider = Get-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type
PS C:\> New-AzCustomProviderAssociation -Scope $resourceId -Name MyAssoc -TargetResourceId $provider.Id

Location  Name     Type
--------  ----     ----
East US 2 MyAssoc  Microsoft.CustomProviders/associations
```

<span data-ttu-id="d37bc-109">Egyéni szolgáltató-társítás létrehozása: a társított cél proviodert megfelelően kell konfigurálni a társítások útvonalával.</span><span class="sxs-lookup"><span data-stu-id="d37bc-109">Create a custom provider association, the associated target provioder must be properly configured with a route for "associations"</span></span>

## <span data-ttu-id="d37bc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d37bc-110">PARAMETERS</span></span>

### <span data-ttu-id="d37bc-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d37bc-111">-AsJob</span></span>
<span data-ttu-id="d37bc-112">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="d37bc-112">Run the command as a job</span></span>

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

### <span data-ttu-id="d37bc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d37bc-113">-DefaultProfile</span></span>
<span data-ttu-id="d37bc-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d37bc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d37bc-115">-Name</span><span class="sxs-lookup"><span data-stu-id="d37bc-115">-Name</span></span>
<span data-ttu-id="d37bc-116">A társítás neve.</span><span class="sxs-lookup"><span data-stu-id="d37bc-116">The name of the association.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AssociationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d37bc-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d37bc-117">-NoWait</span></span>
<span data-ttu-id="d37bc-118">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="d37bc-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d37bc-119">-Scope</span><span class="sxs-lookup"><span data-stu-id="d37bc-119">-Scope</span></span>
<span data-ttu-id="d37bc-120">A társítás hatóköre.</span><span class="sxs-lookup"><span data-stu-id="d37bc-120">The scope of the association.</span></span>
<span data-ttu-id="d37bc-121">A hatókör bármilyen érvényes REST-erőforráspéldány lehet.</span><span class="sxs-lookup"><span data-stu-id="d37bc-121">The scope can be any valid REST resource instance.</span></span>
<span data-ttu-id="d37bc-122">Virtuális gép típusú erőforrás esetén például használja a következőt: '/subscriptions/{subscription-id}/resourceGroups/{resource-group-name}/providers/Microsoft.Compute/virtualMachines/{vm-name}'.</span><span class="sxs-lookup"><span data-stu-id="d37bc-122">For example, use '/subscriptions/{subscription-id}/resourceGroups/{resource-group-name}/providers/Microsoft.Compute/virtualMachines/{vm-name}' for a virtual machine resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d37bc-123">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="d37bc-123">-TargetResourceId</span></span>
<span data-ttu-id="d37bc-124">A társítás célerőforrásának REST-erőforráspéldánya.</span><span class="sxs-lookup"><span data-stu-id="d37bc-124">The REST resource instance of the target resource for this association.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d37bc-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d37bc-125">-Confirm</span></span>
<span data-ttu-id="d37bc-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d37bc-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d37bc-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d37bc-127">-WhatIf</span></span>
<span data-ttu-id="d37bc-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d37bc-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d37bc-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d37bc-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d37bc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d37bc-130">CommonParameters</span></span>
<span data-ttu-id="d37bc-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d37bc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d37bc-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d37bc-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d37bc-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d37bc-133">INPUTS</span></span>

## <span data-ttu-id="d37bc-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d37bc-134">OUTPUTS</span></span>

### <span data-ttu-id="d37bc-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span><span class="sxs-lookup"><span data-stu-id="d37bc-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span></span>

## <span data-ttu-id="d37bc-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d37bc-136">NOTES</span></span>

<span data-ttu-id="d37bc-137">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="d37bc-137">ALIASES</span></span>

## <span data-ttu-id="d37bc-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d37bc-138">RELATED LINKS</span></span>

