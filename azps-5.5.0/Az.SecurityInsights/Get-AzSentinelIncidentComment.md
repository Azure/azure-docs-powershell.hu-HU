---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelincidentcomment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncidentComment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncidentComment.md
ms.openlocfilehash: d33c126da2a77736871a9ec1f950382168f52bee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145827"
---
# <span data-ttu-id="87005-101">Get-AzSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="87005-101">Get-AzSentinelIncidentComment</span></span>

## <span data-ttu-id="87005-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87005-102">SYNOPSIS</span></span>
<span data-ttu-id="87005-103">Incidens megjegyzésének bekérte.</span><span class="sxs-lookup"><span data-stu-id="87005-103">Get an Incident Comment.</span></span>

## <span data-ttu-id="87005-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="87005-104">SYNTAX</span></span>

### <span data-ttu-id="87005-105">IncidentId (default)</span><span class="sxs-lookup"><span data-stu-id="87005-105">IncidentId (Default)</span></span>
```
Get-AzSentinelIncidentComment -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87005-106">IncidentCommentId</span><span class="sxs-lookup"><span data-stu-id="87005-106">IncidentCommentId</span></span>
```
Get-AzSentinelIncidentComment -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String>
 -IncidentCommentId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87005-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="87005-107">ResourceId</span></span>
```
Get-AzSentinelIncidentComment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="87005-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="87005-108">DESCRIPTION</span></span>
<span data-ttu-id="87005-109">A **Get-AzSentinelIncidentComment parancsmag** incidensmegsértő megjegyzést kap a megadott munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="87005-109">The **Get-AzSentinelIncidentComment** cmdlet gets a Incident Comment from the specified workspace.</span></span>
<span data-ttu-id="87005-110">Ha megadja az *IncidentCommentId* és *az IncidentId* paramétert, egyetlen **IncidentComment** objektumot ad vissza.</span><span class="sxs-lookup"><span data-stu-id="87005-110">If you specify the *IncidentCommentId* and *IncidentId* parameters, a single **IncidentComment** object is returned.</span></span>
<span data-ttu-id="87005-111">Ha nem adja meg az *IncidentCommentId* paramétert, a megadott munkaterületen visszaadja a megadott Incidens megjegyzéseit tartalmazó tömböt.</span><span class="sxs-lookup"><span data-stu-id="87005-111">If you do not specify the *IncidentCommentId* parameter, an array containing all of the Incident Comments for the specified Incident in the specified workspace are returned.</span></span>

## <span data-ttu-id="87005-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="87005-112">EXAMPLES</span></span>

### <span data-ttu-id="87005-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="87005-113">Example 1</span></span>
```powershell
PS C:\> $IncidentComments = Get-AzSentinelIncidentComment -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
```

<span data-ttu-id="87005-114">Ebben a példában a megadott incidensre vonatkozó összes **Incidenscomments** adatokat megkapja a megadott munkaterületen, majd a $IncidentComments tárolja.</span><span class="sxs-lookup"><span data-stu-id="87005-114">This example gets all of the **IncidentComments** for the specified Incident in the specified workspace, and then stores it in the $IncidentComments variable.</span></span>

### <span data-ttu-id="87005-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="87005-115">Example 2</span></span>
```powershell
PS C:\> $IncidentComment = Get-AzSentinelIncidentComment -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId" -IncidentCommentId "MyIncidentCommentId"
```

<span data-ttu-id="87005-116">Ez a példa egy **Incidenscommentet kap** a megadott incidenshez a megadott munkaterületen, majd tárolja azt a $IncidentComment változóban.</span><span class="sxs-lookup"><span data-stu-id="87005-116">This example gets an **IncidentComment** for the specified Incident in the specified workspace, and then stores it in the $IncidentComment variable.</span></span>

## <span data-ttu-id="87005-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87005-117">PARAMETERS</span></span>

### <span data-ttu-id="87005-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87005-118">-DefaultProfile</span></span>
<span data-ttu-id="87005-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="87005-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87005-120">-IncidentCommentId</span><span class="sxs-lookup"><span data-stu-id="87005-120">-IncidentCommentId</span></span>
<span data-ttu-id="87005-121">Incidens megjegyzésazonosítója.</span><span class="sxs-lookup"><span data-stu-id="87005-121">Incident Comment Id.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentCommentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87005-122">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="87005-122">-IncidentId</span></span>
<span data-ttu-id="87005-123">Incidens azonosítója.</span><span class="sxs-lookup"><span data-stu-id="87005-123">Incident Id.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId, IncidentCommentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87005-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87005-124">-ResourceGroupName</span></span>
<span data-ttu-id="87005-125">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="87005-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId, IncidentCommentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87005-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="87005-126">-ResourceId</span></span>
<span data-ttu-id="87005-127">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="87005-127">Resource Id.</span></span>

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

### <span data-ttu-id="87005-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="87005-128">-WorkspaceName</span></span>
<span data-ttu-id="87005-129">Munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="87005-129">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId, IncidentCommentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87005-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87005-130">CommonParameters</span></span>
<span data-ttu-id="87005-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87005-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87005-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="87005-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87005-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="87005-133">INPUTS</span></span>

### <span data-ttu-id="87005-134">System.String</span><span class="sxs-lookup"><span data-stu-id="87005-134">System.String</span></span>
## <span data-ttu-id="87005-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="87005-135">OUTPUTS</span></span>

### <span data-ttu-id="87005-136">Microsoft.Azure.Commands.SecurityInsights.Models.IncidentComments.PSSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="87005-136">Microsoft.Azure.Commands.SecurityInsights.Models.IncidentComments.PSSentinelIncidentComment</span></span>
## <span data-ttu-id="87005-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="87005-137">NOTES</span></span>

## <span data-ttu-id="87005-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="87005-138">RELATED LINKS</span></span>
