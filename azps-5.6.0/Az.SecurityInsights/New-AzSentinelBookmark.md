---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/new-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelBookmark.md
ms.openlocfilehash: 31c9728a95e5cfc52b283a8dddc0e24ffffe1630
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930793"
---
# <span data-ttu-id="5b5e4-101">New-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="5b5e4-101">New-AzSentinelBookmark</span></span>

## <span data-ttu-id="5b5e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b5e4-102">SYNOPSIS</span></span>
<span data-ttu-id="5b5e4-103">Könyvjelző létrehozása</span><span class="sxs-lookup"><span data-stu-id="5b5e4-103">Create a Bookmark.</span></span>

## <span data-ttu-id="5b5e4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5b5e4-104">SYNTAX</span></span>

```
New-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> [-BookmarkId <String>]
 -DisplayName <String> [-IncidentInfo <PSSentinelBookmarkIncidentInfo>]
 [-Label <System.Collections.Generic.IList`1[System.String]>] [-Notes <String>] -Query <String>
 [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b5e4-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5b5e4-105">DESCRIPTION</span></span>
<span data-ttu-id="5b5e4-106">A **New-AzSentinelBookmark** parancsmag létrehoz egy könyvjelzőt a megadott munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="5b5e4-106">The **New-AzSentinelBookmark** cmdlet creates a Bookmark from the specified workspace.</span></span>
<span data-ttu-id="5b5e4-107">A Confirm *paraméter* és a Windows PowerShell$ConfirmPreference változó segítségével szabályozhatja, hogy a parancsmag megerősítést kér-e.</span><span class="sxs-lookup"><span data-stu-id="5b5e4-107">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="5b5e4-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5b5e4-108">EXAMPLES</span></span>

### <span data-ttu-id="5b5e4-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="5b5e4-109">Example 1</span></span>
```powershell
PS C:\> $Bookmark = New-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DisplayName "MyBookmark" -Query "SecurityAlert | take 1"
```

<span data-ttu-id="5b5e4-110">Ebben a példában egy **könyvjelzőt** hoz létre a megadott munkaterületen, majd azt a $Bookmark tárolja.</span><span class="sxs-lookup"><span data-stu-id="5b5e4-110">This example creates a **Bookmark** in the specified workspace, and then stores it in the $Bookmark variable.</span></span>

## <span data-ttu-id="5b5e4-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b5e4-111">PARAMETERS</span></span>

### <span data-ttu-id="5b5e4-112">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="5b5e4-112">-BookmarkId</span></span>
<span data-ttu-id="5b5e4-113">Könyvjelző azonosítója</span><span class="sxs-lookup"><span data-stu-id="5b5e4-113">Bookmark Id,</span></span>

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

### <span data-ttu-id="5b5e4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b5e4-114">-DefaultProfile</span></span>
<span data-ttu-id="5b5e4-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5b5e4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b5e4-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5b5e4-116">-DisplayName</span></span>
<span data-ttu-id="5b5e4-117">Könyvjelző szabály megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="5b5e4-117">Bookmark Rule Display Name.</span></span>

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

### <span data-ttu-id="5b5e4-118">-IncidentInfo</span><span class="sxs-lookup"><span data-stu-id="5b5e4-118">-IncidentInfo</span></span>
<span data-ttu-id="5b5e4-119">Az esetinformációk könyvjelzővel való megjelenítése</span><span class="sxs-lookup"><span data-stu-id="5b5e4-119">Bookmark Incident Info.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b5e4-120">-Label</span><span class="sxs-lookup"><span data-stu-id="5b5e4-120">-Label</span></span>
<span data-ttu-id="5b5e4-121">Incidenscímkék.</span><span class="sxs-lookup"><span data-stu-id="5b5e4-121">Incident Labels.</span></span>

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

### <span data-ttu-id="5b5e4-122">-Notes</span><span class="sxs-lookup"><span data-stu-id="5b5e4-122">-Notes</span></span>
<span data-ttu-id="5b5e4-123">Könyvjelzőt a jegyzetekhez.</span><span class="sxs-lookup"><span data-stu-id="5b5e4-123">Bookmark Notes.</span></span>

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

### <span data-ttu-id="5b5e4-124">-Query</span><span class="sxs-lookup"><span data-stu-id="5b5e4-124">-Query</span></span>
<span data-ttu-id="5b5e4-125">Könyvjelző lekérdezése</span><span class="sxs-lookup"><span data-stu-id="5b5e4-125">Bookmark Query.</span></span>

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

### <span data-ttu-id="5b5e4-126">-QueryResult</span><span class="sxs-lookup"><span data-stu-id="5b5e4-126">-QueryResult</span></span>
<span data-ttu-id="5b5e4-127">Könyvjelző lekérdezés eredménye.</span><span class="sxs-lookup"><span data-stu-id="5b5e4-127">Bookmark Query Result.</span></span>

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

### <span data-ttu-id="5b5e4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b5e4-128">-ResourceGroupName</span></span>
<span data-ttu-id="5b5e4-129">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5b5e4-129">Resource group name.</span></span>

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

### <span data-ttu-id="5b5e4-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5b5e4-130">-WorkspaceName</span></span>
<span data-ttu-id="5b5e4-131">Munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="5b5e4-131">Workspace Name.</span></span>

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

### <span data-ttu-id="5b5e4-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5b5e4-132">-Confirm</span></span>
<span data-ttu-id="5b5e4-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5b5e4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b5e4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b5e4-134">-WhatIf</span></span>
<span data-ttu-id="5b5e4-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5b5e4-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5b5e4-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5b5e4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b5e4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b5e4-137">CommonParameters</span></span>
<span data-ttu-id="5b5e4-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b5e4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b5e4-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5b5e4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b5e4-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5b5e4-140">INPUTS</span></span>

### <span data-ttu-id="5b5e4-141">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span><span class="sxs-lookup"><span data-stu-id="5b5e4-141">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span></span>
## <span data-ttu-id="5b5e4-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b5e4-142">OUTPUTS</span></span>

### <span data-ttu-id="5b5e4-143">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="5b5e4-143">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="5b5e4-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5b5e4-144">NOTES</span></span>

## <span data-ttu-id="5b5e4-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5b5e4-145">RELATED LINKS</span></span>
