---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/remove-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateProject.md
ms.openlocfilehash: d9edb00bf7944400fa681f857dd7005d9eaf69b5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003750"
---
# <span data-ttu-id="e3f28-101">Remove-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="e3f28-101">Remove-AzMigrateProject</span></span>

## <span data-ttu-id="e3f28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3f28-102">SYNOPSIS</span></span>
<span data-ttu-id="e3f28-103">Törölje a projekt áttelepítését.</span><span class="sxs-lookup"><span data-stu-id="e3f28-103">Delete the migrate project.</span></span>
<span data-ttu-id="e3f28-104">A nem létező projekt törlése nem művelet.</span><span class="sxs-lookup"><span data-stu-id="e3f28-104">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="e3f28-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e3f28-105">SYNTAX</span></span>

```
Remove-AzMigrateProject -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e3f28-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e3f28-106">DESCRIPTION</span></span>
<span data-ttu-id="e3f28-107">Törölje a projekt áttelepítését.</span><span class="sxs-lookup"><span data-stu-id="e3f28-107">Delete the migrate project.</span></span>
<span data-ttu-id="e3f28-108">A nem létező projekt törlése nem művelet.</span><span class="sxs-lookup"><span data-stu-id="e3f28-108">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="e3f28-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e3f28-109">EXAMPLES</span></span>

### <span data-ttu-id="e3f28-110">1. példa: Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e3f28-110">Example 1: Delete (Default)</span></span>
```powershell
PS C:\> Remove-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -Name BugBashAVSVMware

--No output--
```

<span data-ttu-id="e3f28-111">Törölje a projekt áttelepítését.</span><span class="sxs-lookup"><span data-stu-id="e3f28-111">Delete the migrate project.</span></span>
<span data-ttu-id="e3f28-112">A nem létező projekt törlése nem művelet.</span><span class="sxs-lookup"><span data-stu-id="e3f28-112">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="e3f28-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3f28-113">PARAMETERS</span></span>

### <span data-ttu-id="e3f28-114">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="e3f28-114">-AcceptLanguage</span></span>
<span data-ttu-id="e3f28-115">Szokásos kérésfejléc.</span><span class="sxs-lookup"><span data-stu-id="e3f28-115">Standard request header.</span></span>
<span data-ttu-id="e3f28-116">A szolgáltatás arra használja, hogy a megfelelő nyelven válaszoljon az ügyfélre.</span><span class="sxs-lookup"><span data-stu-id="e3f28-116">Used by service to respond to client in appropriate language.</span></span>

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

### <span data-ttu-id="e3f28-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3f28-117">-DefaultProfile</span></span>
<span data-ttu-id="e3f28-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e3f28-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3f28-119">-Name</span><span class="sxs-lookup"><span data-stu-id="e3f28-119">-Name</span></span>
<span data-ttu-id="e3f28-120">Az Azure-áttelepítési projekt neve.</span><span class="sxs-lookup"><span data-stu-id="e3f28-120">Name of the Azure Migrate project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MigrateProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3f28-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e3f28-121">-PassThru</span></span>
<span data-ttu-id="e3f28-122">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="e3f28-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e3f28-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3f28-123">-ResourceGroupName</span></span>
<span data-ttu-id="e3f28-124">Annak az Azure-erőforráscsoportnak a neve, amelybe a projektet át kell átcsoportosálni, annak a csoportnak a neve is része.</span><span class="sxs-lookup"><span data-stu-id="e3f28-124">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="e3f28-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e3f28-125">-SubscriptionId</span></span>
<span data-ttu-id="e3f28-126">Azure-előfizetés azonosítója, amelyben a projekt létrejött.</span><span class="sxs-lookup"><span data-stu-id="e3f28-126">Azure Subscription Id in which migrate project was created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3f28-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e3f28-127">-Confirm</span></span>
<span data-ttu-id="e3f28-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e3f28-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3f28-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3f28-129">-WhatIf</span></span>
<span data-ttu-id="e3f28-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e3f28-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3f28-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e3f28-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3f28-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3f28-132">CommonParameters</span></span>
<span data-ttu-id="e3f28-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3f28-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3f28-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e3f28-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3f28-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e3f28-135">INPUTS</span></span>

## <span data-ttu-id="e3f28-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3f28-136">OUTPUTS</span></span>

### <span data-ttu-id="e3f28-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e3f28-137">System.Boolean</span></span>

## <span data-ttu-id="e3f28-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e3f28-138">NOTES</span></span>

<span data-ttu-id="e3f28-139">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="e3f28-139">ALIASES</span></span>

## <span data-ttu-id="e3f28-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e3f28-140">RELATED LINKS</span></span>

