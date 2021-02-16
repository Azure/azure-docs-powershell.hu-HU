---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/remove-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateProject.md
ms.openlocfilehash: e0918573b7fc1190d32aaaaa4bfe73ed9fe05fe6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152298"
---
# <span data-ttu-id="1cc37-101">Remove-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="1cc37-101">Remove-AzMigrateProject</span></span>

## <span data-ttu-id="1cc37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1cc37-102">SYNOPSIS</span></span>
<span data-ttu-id="1cc37-103">Törölje a projekt áttelepítését.</span><span class="sxs-lookup"><span data-stu-id="1cc37-103">Delete the migrate project.</span></span>
<span data-ttu-id="1cc37-104">A nem létező projekt törlése nem művelet.</span><span class="sxs-lookup"><span data-stu-id="1cc37-104">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="1cc37-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1cc37-105">SYNTAX</span></span>

```
Remove-AzMigrateProject -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1cc37-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1cc37-106">DESCRIPTION</span></span>
<span data-ttu-id="1cc37-107">Törölje a projekt áttelepítését.</span><span class="sxs-lookup"><span data-stu-id="1cc37-107">Delete the migrate project.</span></span>
<span data-ttu-id="1cc37-108">A nem létező projekt törlése nem művelet.</span><span class="sxs-lookup"><span data-stu-id="1cc37-108">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="1cc37-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1cc37-109">EXAMPLES</span></span>

### <span data-ttu-id="1cc37-110">1. példa: Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1cc37-110">Example 1: Delete (Default)</span></span>
```powershell
PS C:\> Remove-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -Name BugBashAVSVMware

--No output--
```

<span data-ttu-id="1cc37-111">Törölje a projekt áttelepítését.</span><span class="sxs-lookup"><span data-stu-id="1cc37-111">Delete the migrate project.</span></span>
<span data-ttu-id="1cc37-112">A nem létező projekt törlése nem művelet.</span><span class="sxs-lookup"><span data-stu-id="1cc37-112">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="1cc37-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1cc37-113">PARAMETERS</span></span>

### <span data-ttu-id="1cc37-114">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="1cc37-114">-AcceptLanguage</span></span>
<span data-ttu-id="1cc37-115">Szokásos kérésfejléc.</span><span class="sxs-lookup"><span data-stu-id="1cc37-115">Standard request header.</span></span>
<span data-ttu-id="1cc37-116">A szolgáltatás arra használja, hogy a megfelelő nyelven válaszoljon az ügyfélre.</span><span class="sxs-lookup"><span data-stu-id="1cc37-116">Used by service to respond to client in appropriate language.</span></span>

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

### <span data-ttu-id="1cc37-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cc37-117">-DefaultProfile</span></span>
<span data-ttu-id="1cc37-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1cc37-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1cc37-119">-Name</span><span class="sxs-lookup"><span data-stu-id="1cc37-119">-Name</span></span>
<span data-ttu-id="1cc37-120">Az Azure-áttelepítési projekt neve.</span><span class="sxs-lookup"><span data-stu-id="1cc37-120">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="1cc37-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1cc37-121">-PassThru</span></span>
<span data-ttu-id="1cc37-122">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="1cc37-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="1cc37-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cc37-123">-ResourceGroupName</span></span>
<span data-ttu-id="1cc37-124">Annak az Azure-erőforráscsoportnak a neve, amelybe a projektet át kell átcsoportosálni, annak a csoportnak a neve is része.</span><span class="sxs-lookup"><span data-stu-id="1cc37-124">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="1cc37-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1cc37-125">-SubscriptionId</span></span>
<span data-ttu-id="1cc37-126">Azure-előfizetés azonosítója, amelyben a projekt létrejött.</span><span class="sxs-lookup"><span data-stu-id="1cc37-126">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="1cc37-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1cc37-127">-Confirm</span></span>
<span data-ttu-id="1cc37-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1cc37-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cc37-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cc37-129">-WhatIf</span></span>
<span data-ttu-id="1cc37-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1cc37-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1cc37-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1cc37-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cc37-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cc37-132">CommonParameters</span></span>
<span data-ttu-id="1cc37-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cc37-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cc37-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1cc37-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cc37-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1cc37-135">INPUTS</span></span>

## <span data-ttu-id="1cc37-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1cc37-136">OUTPUTS</span></span>

### <span data-ttu-id="1cc37-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1cc37-137">System.Boolean</span></span>

## <span data-ttu-id="1cc37-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1cc37-138">NOTES</span></span>

<span data-ttu-id="1cc37-139">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="1cc37-139">ALIASES</span></span>

## <span data-ttu-id="1cc37-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1cc37-140">RELATED LINKS</span></span>

