---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/update-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelBookmark.md
ms.openlocfilehash: ebc0ffd78f653276e66b85d263db41803a48c356
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165946"
---
# <span data-ttu-id="a01ed-101">Update-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="a01ed-101">Update-AzSentinelBookmark</span></span>

## <span data-ttu-id="a01ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a01ed-102">SYNOPSIS</span></span>
<span data-ttu-id="a01ed-103">Könyvjelző frissítése</span><span class="sxs-lookup"><span data-stu-id="a01ed-103">Update a Bookmark.</span></span>

## <span data-ttu-id="a01ed-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a01ed-104">SYNTAX</span></span>

### <span data-ttu-id="a01ed-105">BookmarkId.</span><span class="sxs-lookup"><span data-stu-id="a01ed-105">BookmarkId.</span></span> <span data-ttu-id="a01ed-106">(Alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a01ed-106">(Default)</span></span>
```
Update-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> -BookmarkId <String>
 [-DisplayName <String>] [-IncidentInfo <PSSentinelBookmarkIncidentInfo>]
 [-Label <System.Collections.Generic.IList`1[System.String]>] [-Notes <String>] [-Query <String>]
 [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a01ed-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="a01ed-107">InputObject</span></span>
```
Update-AzSentinelBookmark -InputObject <PSSentinelBookmark> [-DisplayName <String>]
 [-IncidentInfo <PSSentinelBookmarkIncidentInfo>] [-Label <System.Collections.Generic.IList`1[System.String]>]
 [-Notes <String>] [-Query <String>] [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a01ed-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a01ed-108">ResourceId</span></span>
```
Update-AzSentinelBookmark -ResourceId <String> [-DisplayName <String>]
 [-IncidentInfo <PSSentinelBookmarkIncidentInfo>] [-Label <System.Collections.Generic.IList`1[System.String]>]
 [-Notes <String>] [-Query <String>] [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a01ed-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a01ed-109">DESCRIPTION</span></span>
<span data-ttu-id="a01ed-110">Az **Update-AzSentinelBookmark** parancsmag frissíti a könyvjelzőt a megadott munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="a01ed-110">The **Update-AzSentinelBookmark** cmdlet updates the bookmark in the specified workspace.</span></span>
<span data-ttu-id="a01ed-111">A Bookmark  objektum paraméterként vagy a folyamat műveleti jelének használatával adható át, vagy megadhatja a *szükséges BookmarkId* paramétereket.</span><span class="sxs-lookup"><span data-stu-id="a01ed-111">You can pass an **Bookmark** object as a parameter or by using the pipeline operator, or alternatively you can specify the required *BookmarkId* parameters.</span></span>
<span data-ttu-id="a01ed-112">A Confirm *paraméter* és a Windows PowerShell$ConfirmPreference változó segítségével szabályozhatja, hogy a parancsmag megerősítést kér-e.</span><span class="sxs-lookup"><span data-stu-id="a01ed-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="a01ed-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a01ed-113">EXAMPLES</span></span>

### <span data-ttu-id="a01ed-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="a01ed-114">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceNAme" -BookmarkId "MyBookmarkId" -Notes "Found something interesting"
```

<span data-ttu-id="a01ed-115">A parancs frissíti a Könyvjelzőt a *Jegyzetek tulajdonság beállításával.*</span><span class="sxs-lookup"><span data-stu-id="a01ed-115">The command updates the Bookmark by setting the *Notes* property.</span></span>  <span data-ttu-id="a01ed-116">Minden más kellék azonos marad.</span><span class="sxs-lookup"><span data-stu-id="a01ed-116">All other propreties stay the same.</span></span>

### <span data-ttu-id="a01ed-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="a01ed-117">Example 2</span></span>
```powershell
PS C:\> $Bookmark = Get-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceNAme" -BookmarkId "MyBookmarkId"
PS C:\> $Bookmark | Set-AzSentinelBookmark -Notes "Found something interesting"
```

<span data-ttu-id="a01ed-118">Az első parancs a Bookmark by *BookmarkId* parancsot a megadott munkaterületről, majd a könyvjelzőt a $Bookmark tárolja.</span><span class="sxs-lookup"><span data-stu-id="a01ed-118">The first command gets the Bookmark by *BookmarkId* from the specified workspace, and then stores it in the $Bookmark variable.</span></span>
<span data-ttu-id="a01ed-119">A második parancs frissíti a Jegyzetek tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="a01ed-119">The second command updates the Notes property.</span></span>   <span data-ttu-id="a01ed-120">Minden más kellék azonos marad.</span><span class="sxs-lookup"><span data-stu-id="a01ed-120">All other propreties stay the same.</span></span>

## <span data-ttu-id="a01ed-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a01ed-121">PARAMETERS</span></span>

### <span data-ttu-id="a01ed-122">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="a01ed-122">-BookmarkId</span></span>
<span data-ttu-id="a01ed-123">Könyvjelző azonosítója</span><span class="sxs-lookup"><span data-stu-id="a01ed-123">Bookmark Id,</span></span>

```yaml
Type: String
Parameter Sets: BookmarkId., ParentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a01ed-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a01ed-124">-DefaultProfile</span></span>
<span data-ttu-id="a01ed-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a01ed-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a01ed-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a01ed-126">-DisplayName</span></span>
<span data-ttu-id="a01ed-127">Könyvjelző szabály megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="a01ed-127">Bookmark Rule Display Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a01ed-128">-IncidentInfo</span><span class="sxs-lookup"><span data-stu-id="a01ed-128">-IncidentInfo</span></span>
<span data-ttu-id="a01ed-129">Az esetinformációk könyvjelzővel való megjelenítése.</span><span class="sxs-lookup"><span data-stu-id="a01ed-129">Bookmark Incident Info.</span></span>

```yaml
Type: PSSentinelBookmarkIncidentInfo
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a01ed-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a01ed-130">-InputObject</span></span>
<span data-ttu-id="a01ed-131">InputObject.</span><span class="sxs-lookup"><span data-stu-id="a01ed-131">InputObject.</span></span>

```yaml
Type: PSSentinelBookmark
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a01ed-132">-Label</span><span class="sxs-lookup"><span data-stu-id="a01ed-132">-Label</span></span>
<span data-ttu-id="a01ed-133">Incidenscímkék.</span><span class="sxs-lookup"><span data-stu-id="a01ed-133">Incident Labels.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a01ed-134">-Notes</span><span class="sxs-lookup"><span data-stu-id="a01ed-134">-Notes</span></span>
<span data-ttu-id="a01ed-135">Könyvjelzőt a jegyzetekhez.</span><span class="sxs-lookup"><span data-stu-id="a01ed-135">Bookmark Notes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a01ed-136">-Query</span><span class="sxs-lookup"><span data-stu-id="a01ed-136">-Query</span></span>
<span data-ttu-id="a01ed-137">Könyvjelző lekérdezése elemet.</span><span class="sxs-lookup"><span data-stu-id="a01ed-137">Bookmark Query.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a01ed-138">-QueryResult</span><span class="sxs-lookup"><span data-stu-id="a01ed-138">-QueryResult</span></span>
<span data-ttu-id="a01ed-139">Könyvjelző lekérdezés eredménye.</span><span class="sxs-lookup"><span data-stu-id="a01ed-139">Bookmark Query Result.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a01ed-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a01ed-140">-ResourceGroupName</span></span>
<span data-ttu-id="a01ed-141">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a01ed-141">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a01ed-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a01ed-142">-ResourceId</span></span>
<span data-ttu-id="a01ed-143">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="a01ed-143">Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a01ed-144">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a01ed-144">-WorkspaceName</span></span>
<span data-ttu-id="a01ed-145">Munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="a01ed-145">Workspace Name.</span></span>

```yaml
Type: String
Parameter Sets: BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a01ed-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a01ed-146">-Confirm</span></span>
<span data-ttu-id="a01ed-147">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a01ed-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a01ed-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a01ed-148">-WhatIf</span></span>
<span data-ttu-id="a01ed-149">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a01ed-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a01ed-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a01ed-150">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a01ed-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a01ed-151">CommonParameters</span></span>
<span data-ttu-id="a01ed-152">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a01ed-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a01ed-153">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a01ed-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a01ed-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a01ed-154">INPUTS</span></span>

### <span data-ttu-id="a01ed-155">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="a01ed-155">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>

### <span data-ttu-id="a01ed-156">System.String</span><span class="sxs-lookup"><span data-stu-id="a01ed-156">System.String</span></span>

### <span data-ttu-id="a01ed-157">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span><span class="sxs-lookup"><span data-stu-id="a01ed-157">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span></span>

## <span data-ttu-id="a01ed-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a01ed-158">OUTPUTS</span></span>

### <span data-ttu-id="a01ed-159">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="a01ed-159">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>

## <span data-ttu-id="a01ed-160">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a01ed-160">NOTES</span></span>

## <span data-ttu-id="a01ed-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a01ed-161">RELATED LINKS</span></span>
