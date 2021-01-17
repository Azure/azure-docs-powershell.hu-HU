---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncident.md
ms.openlocfilehash: eb0854ee3a71af3bdf19d2258187c435fb0f5860
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479725"
---
# <span data-ttu-id="a2886-101">Get-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="a2886-101">Get-AzSentinelIncident</span></span>

## <span data-ttu-id="a2886-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2886-102">SYNOPSIS</span></span>
<span data-ttu-id="a2886-103">Eset lekérte.</span><span class="sxs-lookup"><span data-stu-id="a2886-103">Get an Incident.</span></span>

## <span data-ttu-id="a2886-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a2886-104">SYNTAX</span></span>

### <span data-ttu-id="a2886-105">WorkspaceScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a2886-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2886-106">IncidentId</span><span class="sxs-lookup"><span data-stu-id="a2886-106">IncidentId</span></span>
```
Get-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> [-IncidentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2886-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2886-107">ResourceId</span></span>
```
Get-AzSentinelIncident -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2886-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a2886-108">DESCRIPTION</span></span>
<span data-ttu-id="a2886-109">A **Get-AzSentinelIncident** parancsmag egy incidenst kap a megadott munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="a2886-109">The **Get-AzSentinelIncident** cmdlet gets an Incident from the specified workspace.</span></span>
<span data-ttu-id="a2886-110">Ha megadja az *IncidentId paramétert,* egyetlen **Incidens** objektumot ad vissza.</span><span class="sxs-lookup"><span data-stu-id="a2886-110">If you specify the *IncidentId* parameter, a single **Incident** object is returned.</span></span>
<span data-ttu-id="a2886-111">Ha nem adja meg az *IncidentId* paramétert, a megadott munkaterület összes incidensét tartalmazó tömb lesz az eredmény.</span><span class="sxs-lookup"><span data-stu-id="a2886-111">If you do not specify the *IncidentId* parameter, an array containing all of the Incidents in the specified workspace are returned.</span></span>
<span data-ttu-id="a2886-112">Az Incidens **objektummal** frissítheti az incidenst, például hozzáadhatja az Incidens **jegyzeteket.**</span><span class="sxs-lookup"><span data-stu-id="a2886-112">You can use the **Incident** object to update the Incident, for example you can add Notes the **Incident**.</span></span>

## <span data-ttu-id="a2886-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a2886-113">EXAMPLES</span></span>

### <span data-ttu-id="a2886-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="a2886-114">Example 1</span></span>
```powershell
PS C:\> $Incidents = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="a2886-115">Ez a példa  a megadott munkaterület összes incidensét beveszi, majd a $Incidents tárolja.</span><span class="sxs-lookup"><span data-stu-id="a2886-115">This example gets all of the **Incidents** in the specified workspace, and then stores it in the $Incidents variable.</span></span>

### <span data-ttu-id="a2886-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="a2886-116">Example 2</span></span>
```powershell
PS C:\> $Incident = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
```

<span data-ttu-id="a2886-117">Ez a példa egy **incidenst** kap a megadott munkaterületen, majd a $Incident tárolja.</span><span class="sxs-lookup"><span data-stu-id="a2886-117">This example gets an **Incident** in the specified workspace, and then stores it in the $Incident variable.</span></span>

## <span data-ttu-id="a2886-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2886-118">PARAMETERS</span></span>

### <span data-ttu-id="a2886-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2886-119">-DefaultProfile</span></span>
<span data-ttu-id="a2886-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a2886-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2886-121">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="a2886-121">-IncidentId</span></span>
<span data-ttu-id="a2886-122">Incidens azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a2886-122">Incident Id.</span></span>

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

### <span data-ttu-id="a2886-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2886-123">-ResourceGroupName</span></span>
<span data-ttu-id="a2886-124">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a2886-124">Resource group name.</span></span>

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

### <span data-ttu-id="a2886-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2886-125">-ResourceId</span></span>
<span data-ttu-id="a2886-126">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="a2886-126">Resource Id.</span></span>

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

### <span data-ttu-id="a2886-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a2886-127">-WorkspaceName</span></span>
<span data-ttu-id="a2886-128">Munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="a2886-128">Workspace Name.</span></span>

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

### <span data-ttu-id="a2886-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2886-129">CommonParameters</span></span>
<span data-ttu-id="a2886-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2886-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2886-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a2886-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2886-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a2886-132">INPUTS</span></span>

### <span data-ttu-id="a2886-133">System.String</span><span class="sxs-lookup"><span data-stu-id="a2886-133">System.String</span></span>
## <span data-ttu-id="a2886-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2886-134">OUTPUTS</span></span>

### <span data-ttu-id="a2886-135">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="a2886-135">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="a2886-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a2886-136">NOTES</span></span>

## <span data-ttu-id="a2886-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a2886-137">RELATED LINKS</span></span>
