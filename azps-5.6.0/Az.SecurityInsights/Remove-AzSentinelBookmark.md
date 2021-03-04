---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/remove-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelBookmark.md
ms.openlocfilehash: ed75d128053a4b08fc7d63a4ef8b02254d868408
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931689"
---
# <span data-ttu-id="801e7-101">Remove-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="801e7-101">Remove-AzSentinelBookmark</span></span>

## <span data-ttu-id="801e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="801e7-102">SYNOPSIS</span></span>
<span data-ttu-id="801e7-103">Könyvjelző törlése</span><span class="sxs-lookup"><span data-stu-id="801e7-103">Delete a Bookmark.</span></span>

## <span data-ttu-id="801e7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="801e7-104">SYNTAX</span></span>

### <span data-ttu-id="801e7-105">BookmarkId.</span><span class="sxs-lookup"><span data-stu-id="801e7-105">BookmarkId.</span></span> <span data-ttu-id="801e7-106">(Alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="801e7-106">(Default)</span></span>
```
Remove-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> -BookmarkId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="801e7-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="801e7-107">InputObject</span></span>
```
Remove-AzSentinelBookmark -InputObject <PSSentinelBookmark> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="801e7-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="801e7-108">DESCRIPTION</span></span>
<span data-ttu-id="801e7-109">A **Remove-AzSentinelBookmark** parancsmag véglegesen törli a könyvjelzőket egy adott munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="801e7-109">The **Remove-AzSentinelBookmark** cmdlet permanently deletes a Bookmark from a specified workspace.</span></span>
<span data-ttu-id="801e7-110">A Könyvjelző **objektumokat** átadhatja a folyamat műveleti jelével, vagy megadhatja a szükséges paramétereket.</span><span class="sxs-lookup"><span data-stu-id="801e7-110">You can pass an **Bookmark** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="801e7-111">A Confirm paraméter és a Windows PowerShell $ConfirmPreference szabályozhatja, hogy a parancsmag megerősítést kér-e.</span><span class="sxs-lookup"><span data-stu-id="801e7-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="801e7-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="801e7-112">EXAMPLES</span></span>

### <span data-ttu-id="801e7-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="801e7-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -BookmarkId "MyBookmarkId"
```

<span data-ttu-id="801e7-114">Ez a parancs eltávolítja a Könyvjelzőt a munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="801e7-114">This command removes the Bookmark from the workspace.</span></span>

## <span data-ttu-id="801e7-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="801e7-115">PARAMETERS</span></span>

### <span data-ttu-id="801e7-116">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="801e7-116">-BookmarkId</span></span>
<span data-ttu-id="801e7-117">Könyvjelző azonosítója</span><span class="sxs-lookup"><span data-stu-id="801e7-117">Bookmark Id,</span></span>

```yaml
Type: System.String
Parameter Sets: BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="801e7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="801e7-118">-DefaultProfile</span></span>
<span data-ttu-id="801e7-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="801e7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="801e7-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="801e7-120">-InputObject</span></span>
<span data-ttu-id="801e7-121">InputObject.</span><span class="sxs-lookup"><span data-stu-id="801e7-121">InputObject.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="801e7-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="801e7-122">-PassThru</span></span>
<span data-ttu-id="801e7-123">PassThru</span><span class="sxs-lookup"><span data-stu-id="801e7-123">PassThru</span></span>

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

### <span data-ttu-id="801e7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="801e7-124">-ResourceGroupName</span></span>
<span data-ttu-id="801e7-125">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="801e7-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="801e7-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="801e7-126">-WorkspaceName</span></span>
<span data-ttu-id="801e7-127">Munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="801e7-127">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="801e7-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="801e7-128">-Confirm</span></span>
<span data-ttu-id="801e7-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="801e7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="801e7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="801e7-130">-WhatIf</span></span>
<span data-ttu-id="801e7-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="801e7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="801e7-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="801e7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="801e7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="801e7-133">CommonParameters</span></span>
<span data-ttu-id="801e7-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="801e7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="801e7-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="801e7-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="801e7-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="801e7-136">INPUTS</span></span>

### <span data-ttu-id="801e7-137">System.String</span><span class="sxs-lookup"><span data-stu-id="801e7-137">System.String</span></span>
### <span data-ttu-id="801e7-138">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="801e7-138">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="801e7-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="801e7-139">OUTPUTS</span></span>

### <span data-ttu-id="801e7-140">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="801e7-140">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="801e7-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="801e7-141">NOTES</span></span>

## <span data-ttu-id="801e7-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="801e7-142">RELATED LINKS</span></span>
