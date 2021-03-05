---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/get-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelBookmark.md
ms.openlocfilehash: 5093f924f87f146550b13e3858f9a93b3f193ca0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005654"
---
# <span data-ttu-id="279d5-101">Get-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="279d5-101">Get-AzSentinelBookmark</span></span>

## <span data-ttu-id="279d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="279d5-102">SYNOPSIS</span></span>
<span data-ttu-id="279d5-103">Könyvjelző elemet.</span><span class="sxs-lookup"><span data-stu-id="279d5-103">Get a Bookmark.</span></span>

## <span data-ttu-id="279d5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="279d5-104">SYNTAX</span></span>

### <span data-ttu-id="279d5-105">WorkspaceScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="279d5-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="279d5-106">BookmarkId.</span><span class="sxs-lookup"><span data-stu-id="279d5-106">BookmarkId.</span></span>
```
Get-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> -BookmarkId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="279d5-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="279d5-107">ResourceId</span></span>
```
Get-AzSentinelBookmark -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="279d5-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="279d5-108">DESCRIPTION</span></span>
<span data-ttu-id="279d5-109">A **Get-AzSentinelBookmark** parancsmag egy könyvjelzőt kap a megadott munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="279d5-109">The **Get-AzSentinelBookmark** cmdlet gets a Bookmark from the specified workspace.</span></span>
<span data-ttu-id="279d5-110">Ha a *BookmarkId* paramétert adja meg, egyetlen **Könyvjelző** objektumot ad vissza.</span><span class="sxs-lookup"><span data-stu-id="279d5-110">If you specify the *BookmarkId* parameter, a single **Bookmark** object is returned.</span></span>
<span data-ttu-id="279d5-111">Ha nem adja meg *a BookmarkId* paramétert, a megadott munkaterület összes Könyvjelzőt tartalmazó tömbje lesz az eredmény.</span><span class="sxs-lookup"><span data-stu-id="279d5-111">If you do not specify the *BookmarkId* parameter, an array containing all of the Bookmarks in the specified workspace are returned.</span></span>
<span data-ttu-id="279d5-112">A Könyvjelző **objektummal** frissítheti a Könyvjelzőt, például felveheti a Könyvjelzőt a Jegyzetek **közé.**</span><span class="sxs-lookup"><span data-stu-id="279d5-112">You can use the **Bookmark** object to update the Bookmark, for example you can add Notes the **Bookmark**.</span></span>

## <span data-ttu-id="279d5-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="279d5-113">EXAMPLES</span></span>

### <span data-ttu-id="279d5-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="279d5-114">Example 1</span></span>
```powershell
PS C:\> $Bookmarks = Get-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="279d5-115">Ebben a példában  a megadott munkaterület összes könyvjelzőt megkapja, majd a $Bookmarks tárolja.</span><span class="sxs-lookup"><span data-stu-id="279d5-115">This example gets all of the **Bookmarks** in the specified workspace, and then stores it in the $Bookmarks variable.</span></span>

### <span data-ttu-id="279d5-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="279d5-116">Example 2</span></span>
```powershell
PS C:\> $Bookmark = Get-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -BookmarkId "MyBookmarkId"
```

<span data-ttu-id="279d5-117">Ebben a példában egy **könyvjelzőt** kap a megadott munkaterületen, majd a könyvjelzőt $Bookmark változóban.</span><span class="sxs-lookup"><span data-stu-id="279d5-117">This example gets an **Bookmark** in the specified workspace, and then stores it in the $Bookmark variable.</span></span>

## <span data-ttu-id="279d5-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="279d5-118">PARAMETERS</span></span>

### <span data-ttu-id="279d5-119">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="279d5-119">-BookmarkId</span></span>
<span data-ttu-id="279d5-120">Könyvjelző azonosítója</span><span class="sxs-lookup"><span data-stu-id="279d5-120">Bookmark Id,</span></span>

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

### <span data-ttu-id="279d5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="279d5-121">-DefaultProfile</span></span>
<span data-ttu-id="279d5-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="279d5-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="279d5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="279d5-123">-ResourceGroupName</span></span>
<span data-ttu-id="279d5-124">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="279d5-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="279d5-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="279d5-125">-ResourceId</span></span>
<span data-ttu-id="279d5-126">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="279d5-126">Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="279d5-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="279d5-127">-WorkspaceName</span></span>
<span data-ttu-id="279d5-128">Munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="279d5-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="279d5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="279d5-129">CommonParameters</span></span>
<span data-ttu-id="279d5-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="279d5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="279d5-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="279d5-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="279d5-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="279d5-132">INPUTS</span></span>

### <span data-ttu-id="279d5-133">System.String</span><span class="sxs-lookup"><span data-stu-id="279d5-133">System.String</span></span>
## <span data-ttu-id="279d5-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="279d5-134">OUTPUTS</span></span>

### <span data-ttu-id="279d5-135">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="279d5-135">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="279d5-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="279d5-136">NOTES</span></span>

## <span data-ttu-id="279d5-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="279d5-137">RELATED LINKS</span></span>
