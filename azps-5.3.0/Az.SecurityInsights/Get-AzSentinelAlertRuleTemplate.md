---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelalertruletemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleTemplate.md
ms.openlocfilehash: aa5dabced1439d8a754e220d56f7309c7b2df3e0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479728"
---
# <span data-ttu-id="67f40-101">Get-AzSentinelAlertRuleTemplate</span><span class="sxs-lookup"><span data-stu-id="67f40-101">Get-AzSentinelAlertRuleTemplate</span></span>

## <span data-ttu-id="67f40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67f40-102">SYNOPSIS</span></span>
<span data-ttu-id="67f40-103">Analitikus szabálysablon létrehozása</span><span class="sxs-lookup"><span data-stu-id="67f40-103">Get Analytic Rule Template.</span></span>

## <span data-ttu-id="67f40-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="67f40-104">SYNTAX</span></span>

### <span data-ttu-id="67f40-105">WorkspaceScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="67f40-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelAlertRuleTemplate -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67f40-106">AlertRuleTemplateId</span><span class="sxs-lookup"><span data-stu-id="67f40-106">AlertRuleTemplateId</span></span>
```
Get-AzSentinelAlertRuleTemplate -ResourceGroupName <String> -WorkspaceName <String>
 -AlertRuleTemplateId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67f40-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="67f40-107">ResourceId</span></span>
```
Get-AzSentinelAlertRuleTemplate -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="67f40-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="67f40-108">DESCRIPTION</span></span>
<span data-ttu-id="67f40-109">A **Get-AzSentinelAlertRuleTemplate** parancsmag egy riasztási szabálysablont kap a megadott munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="67f40-109">The **Get-AzSentinelAlertRuleTemplate** cmdlet gets an Alert Rule Template from the specified workspace.</span></span>
<span data-ttu-id="67f40-110">Ha a *AlertRuleTemplateId* paramétert adja meg, egyetlen **AlertRuleTemplate** objektumot ad vissza.</span><span class="sxs-lookup"><span data-stu-id="67f40-110">If you specify the *AlertRuleTemplateId* parameter, a single **AlertRuleTemplate** object is returned.</span></span>
<span data-ttu-id="67f40-111">Ha nem adja meg a *AlertRuleTemplateId* paramétert, a megadott munkaterületen az összes riasztási szabálysablont tartalmazó tömb jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="67f40-111">If you do not specify the *AlertRuleTemplateId* parameter, an array containing all of the Alert Rule Templates in the specified workspace are returned.</span></span>
<span data-ttu-id="67f40-112">A **AlertRuleTemplate** objektummal új riasztási szabályt hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="67f40-112">You can use the **AlertRuleTemplate** object to create a new Alert Rule.</span></span>

## <span data-ttu-id="67f40-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="67f40-113">EXAMPLES</span></span>

### <span data-ttu-id="67f40-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="67f40-114">Example 1</span></span>
```powershell
PS C:\> $AlertRuleTemplates = Get-AzSentinelAlertRuleTemplate -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="67f40-115">Ebben a példában az összes **AlertRuleTemplates** a megadott munkaterületen, majd tárolja azt a $AlertRuleTemplates változóban.</span><span class="sxs-lookup"><span data-stu-id="67f40-115">This example gets all of the **AlertRuleTemplates** in the specified workspace, and then stores it in the $AlertRuleTemplates variable.</span></span>

### <span data-ttu-id="67f40-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="67f40-116">Example 2</span></span>
```powershell
PS C:\> $AlertRuleTemplate = Get-AzSentinelAlertRuleTemplate -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleTemplateId "MyAlertRuleTemplateId"
```

<span data-ttu-id="67f40-117">Ez a példa egy **AlertRuleTemplate értéket** kap a megadott munkaterületen, majd tárolja azt a $AlertRuleTemplate változóban.</span><span class="sxs-lookup"><span data-stu-id="67f40-117">This example gets an **AlertRuleTemplate** in the specified workspace, and then stores it in the $AlertRuleTemplate variable.</span></span>

## <span data-ttu-id="67f40-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67f40-118">PARAMETERS</span></span>

### <span data-ttu-id="67f40-119">-AlertRuleTemplateId</span><span class="sxs-lookup"><span data-stu-id="67f40-119">-AlertRuleTemplateId</span></span>
<span data-ttu-id="67f40-120">Sablonriasztás szabályazonosítója.</span><span class="sxs-lookup"><span data-stu-id="67f40-120">Template Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertRuleTemplateId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67f40-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67f40-121">-DefaultProfile</span></span>
<span data-ttu-id="67f40-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="67f40-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67f40-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67f40-123">-ResourceGroupName</span></span>
<span data-ttu-id="67f40-124">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="67f40-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, AlertRuleTemplateId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67f40-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="67f40-125">-ResourceId</span></span>
<span data-ttu-id="67f40-126">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="67f40-126">Resource Id.</span></span>

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

### <span data-ttu-id="67f40-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="67f40-127">-WorkspaceName</span></span>
<span data-ttu-id="67f40-128">Munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="67f40-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, AlertRuleTemplateId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67f40-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67f40-129">CommonParameters</span></span>
<span data-ttu-id="67f40-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67f40-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67f40-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="67f40-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67f40-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="67f40-132">INPUTS</span></span>

### <span data-ttu-id="67f40-133">System.String</span><span class="sxs-lookup"><span data-stu-id="67f40-133">System.String</span></span>
## <span data-ttu-id="67f40-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="67f40-134">OUTPUTS</span></span>

### <span data-ttu-id="67f40-135">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRuleTemplates.PSSentinelAlertRuleTemplate</span><span class="sxs-lookup"><span data-stu-id="67f40-135">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRuleTemplates.PSSentinelAlertRuleTemplate</span></span>
## <span data-ttu-id="67f40-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="67f40-136">NOTES</span></span>

## <span data-ttu-id="67f40-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="67f40-137">RELATED LINKS</span></span>
