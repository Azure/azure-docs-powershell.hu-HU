---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelincidentcomment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentComment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentComment.md
ms.openlocfilehash: 8824832b1b3d09a24998891ad4636e3a3e0f1e19
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479709"
---
# <span data-ttu-id="b5c52-101">New-AzSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="b5c52-101">New-AzSentinelIncidentComment</span></span>

## <span data-ttu-id="b5c52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5c52-102">SYNOPSIS</span></span>
<span data-ttu-id="b5c52-103">Incidens megjegyzésének hozzáadása incidenshez.</span><span class="sxs-lookup"><span data-stu-id="b5c52-103">Add an Incident Comment to an Incident.</span></span>

## <span data-ttu-id="b5c52-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b5c52-104">SYNTAX</span></span>

```
New-AzSentinelIncidentComment -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String>
 [-IncidentCommentId <String>] -Message <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5c52-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b5c52-105">DESCRIPTION</span></span>
<span data-ttu-id="b5c52-106">A **New-AzSentinelIncidentComment parancsmag** létrehoz egy incidensmegsértő megjegyzést a megadott munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="b5c52-106">The **New-AzSentinelIncidentComment** cmdlet creates a Incident Comment from the specified workspace.</span></span>
<span data-ttu-id="b5c52-107">A Confirm *paraméter* és a Windows PowerShell$ConfirmPreference változó segítségével szabályozhatja, hogy a parancsmag megerősítést kér-e.</span><span class="sxs-lookup"><span data-stu-id="b5c52-107">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="b5c52-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b5c52-108">EXAMPLES</span></span>

### <span data-ttu-id="b5c52-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="b5c52-109">Example 1</span></span>
```powershell
PS C:\> $Incident = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
PS C:\> $IncidentComment = New-AzSentinelIncidentComment -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId ($Incident.Name) -Message "Still needs investigation"
```

<span data-ttu-id="b5c52-110">Ez a példa létrehoz egy **Incidenscommentet** a megadott munkaterületen, majd a $IncidentComment tárolja.</span><span class="sxs-lookup"><span data-stu-id="b5c52-110">This example creates an **IncidentComment** in the specified workspace, and then stores it in the $IncidentComment variable.</span></span>

## <span data-ttu-id="b5c52-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5c52-111">PARAMETERS</span></span>

### <span data-ttu-id="b5c52-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5c52-112">-DefaultProfile</span></span>
<span data-ttu-id="b5c52-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b5c52-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5c52-114">-IncidentCommentId</span><span class="sxs-lookup"><span data-stu-id="b5c52-114">-IncidentCommentId</span></span>
<span data-ttu-id="b5c52-115">Incidens megjegyzésazonosítója.</span><span class="sxs-lookup"><span data-stu-id="b5c52-115">Incident Comment Id.</span></span>

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

### <span data-ttu-id="b5c52-116">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="b5c52-116">-IncidentId</span></span>
<span data-ttu-id="b5c52-117">Incidens azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b5c52-117">Incident Id.</span></span>

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

### <span data-ttu-id="b5c52-118">-Message</span><span class="sxs-lookup"><span data-stu-id="b5c52-118">-Message</span></span>
<span data-ttu-id="b5c52-119">Incidens üzenete.</span><span class="sxs-lookup"><span data-stu-id="b5c52-119">Incident Message.</span></span>

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

### <span data-ttu-id="b5c52-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5c52-120">-ResourceGroupName</span></span>
<span data-ttu-id="b5c52-121">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b5c52-121">Resource group name.</span></span>

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

### <span data-ttu-id="b5c52-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b5c52-122">-WorkspaceName</span></span>
<span data-ttu-id="b5c52-123">Munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="b5c52-123">Workspace Name.</span></span>

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

### <span data-ttu-id="b5c52-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b5c52-124">-Confirm</span></span>
<span data-ttu-id="b5c52-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b5c52-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5c52-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5c52-126">-WhatIf</span></span>
<span data-ttu-id="b5c52-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b5c52-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b5c52-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b5c52-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5c52-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5c52-129">CommonParameters</span></span>
<span data-ttu-id="b5c52-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5c52-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5c52-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b5c52-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5c52-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b5c52-132">INPUTS</span></span>

### <span data-ttu-id="b5c52-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="b5c52-133">None</span></span>
## <span data-ttu-id="b5c52-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5c52-134">OUTPUTS</span></span>

### <span data-ttu-id="b5c52-135">Microsoft.Azure.Commands.SecurityInsights.Models.IncidentComments.PSSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="b5c52-135">Microsoft.Azure.Commands.SecurityInsights.Models.IncidentComments.PSSentinelIncidentComment</span></span>
## <span data-ttu-id="b5c52-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b5c52-136">NOTES</span></span>

## <span data-ttu-id="b5c52-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b5c52-137">RELATED LINKS</span></span>
