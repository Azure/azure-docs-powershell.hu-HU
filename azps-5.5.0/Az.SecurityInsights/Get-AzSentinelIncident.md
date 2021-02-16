---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncident.md
ms.openlocfilehash: eb0854ee3a71af3bdf19d2258187c435fb0f5860
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150770"
---
# <span data-ttu-id="989a4-101">Get-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="989a4-101">Get-AzSentinelIncident</span></span>

## <span data-ttu-id="989a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="989a4-102">SYNOPSIS</span></span>
<span data-ttu-id="989a4-103">Eset lekérte.</span><span class="sxs-lookup"><span data-stu-id="989a4-103">Get an Incident.</span></span>

## <span data-ttu-id="989a4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="989a4-104">SYNTAX</span></span>

### <span data-ttu-id="989a4-105">WorkspaceScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="989a4-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="989a4-106">IncidentId</span><span class="sxs-lookup"><span data-stu-id="989a4-106">IncidentId</span></span>
```
Get-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> [-IncidentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="989a4-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="989a4-107">ResourceId</span></span>
```
Get-AzSentinelIncident -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="989a4-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="989a4-108">DESCRIPTION</span></span>
<span data-ttu-id="989a4-109">A **Get-AzSentinelIncident** parancsmag egy incidenst kap a megadott munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="989a4-109">The **Get-AzSentinelIncident** cmdlet gets an Incident from the specified workspace.</span></span>
<span data-ttu-id="989a4-110">Ha megadja az *IncidentId paramétert,* egyetlen **Incidens** objektumot ad vissza.</span><span class="sxs-lookup"><span data-stu-id="989a4-110">If you specify the *IncidentId* parameter, a single **Incident** object is returned.</span></span>
<span data-ttu-id="989a4-111">Ha nem adja meg az *IncidentId* paramétert, a megadott munkaterület összes incidensét tartalmazó tömb lesz az eredmény.</span><span class="sxs-lookup"><span data-stu-id="989a4-111">If you do not specify the *IncidentId* parameter, an array containing all of the Incidents in the specified workspace are returned.</span></span>
<span data-ttu-id="989a4-112">Az Incidens **objektummal** frissítheti az incidenst, például hozzáadhatja az Incidens **jegyzeteket.**</span><span class="sxs-lookup"><span data-stu-id="989a4-112">You can use the **Incident** object to update the Incident, for example you can add Notes the **Incident**.</span></span>

## <span data-ttu-id="989a4-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="989a4-113">EXAMPLES</span></span>

### <span data-ttu-id="989a4-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="989a4-114">Example 1</span></span>
```powershell
PS C:\> $Incidents = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="989a4-115">Ez a példa  a megadott munkaterület összes incidensét beveszi, majd a $Incidents tárolja.</span><span class="sxs-lookup"><span data-stu-id="989a4-115">This example gets all of the **Incidents** in the specified workspace, and then stores it in the $Incidents variable.</span></span>

### <span data-ttu-id="989a4-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="989a4-116">Example 2</span></span>
```powershell
PS C:\> $Incident = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
```

<span data-ttu-id="989a4-117">Ez a példa egy **incidenst** kap a megadott munkaterületen, majd a $Incident tárolja.</span><span class="sxs-lookup"><span data-stu-id="989a4-117">This example gets an **Incident** in the specified workspace, and then stores it in the $Incident variable.</span></span>

## <span data-ttu-id="989a4-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="989a4-118">PARAMETERS</span></span>

### <span data-ttu-id="989a4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="989a4-119">-DefaultProfile</span></span>
<span data-ttu-id="989a4-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="989a4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="989a4-121">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="989a4-121">-IncidentId</span></span>
<span data-ttu-id="989a4-122">Incidens azonosítója.</span><span class="sxs-lookup"><span data-stu-id="989a4-122">Incident Id.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="989a4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="989a4-123">-ResourceGroupName</span></span>
<span data-ttu-id="989a4-124">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="989a4-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="989a4-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="989a4-125">-ResourceId</span></span>
<span data-ttu-id="989a4-126">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="989a4-126">Resource Id.</span></span>

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

### <span data-ttu-id="989a4-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="989a4-127">-WorkspaceName</span></span>
<span data-ttu-id="989a4-128">Munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="989a4-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="989a4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="989a4-129">CommonParameters</span></span>
<span data-ttu-id="989a4-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="989a4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="989a4-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="989a4-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="989a4-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="989a4-132">INPUTS</span></span>

### <span data-ttu-id="989a4-133">System.String</span><span class="sxs-lookup"><span data-stu-id="989a4-133">System.String</span></span>
## <span data-ttu-id="989a4-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="989a4-134">OUTPUTS</span></span>

### <span data-ttu-id="989a4-135">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="989a4-135">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="989a4-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="989a4-136">NOTES</span></span>

## <span data-ttu-id="989a4-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="989a4-137">RELATED LINKS</span></span>
