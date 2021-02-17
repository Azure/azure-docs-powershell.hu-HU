---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRule.md
ms.openlocfilehash: 02dc3b58d9cd4b4be58b83f36cc6e42e11008812
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165122"
---
# <span data-ttu-id="a9ccb-101">Get-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="a9ccb-101">Get-AzSentinelAlertRule</span></span>

## <span data-ttu-id="a9ccb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9ccb-102">SYNOPSIS</span></span>
<span data-ttu-id="a9ccb-103">Analytic (riasztási szabály) kap.</span><span class="sxs-lookup"><span data-stu-id="a9ccb-103">Gets an Analytic (Alert Rule).</span></span>

## <span data-ttu-id="a9ccb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a9ccb-104">SYNTAX</span></span>

### <span data-ttu-id="a9ccb-105">WorkspaceScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a9ccb-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9ccb-106">AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="a9ccb-106">AlertRuleId</span></span>
```
Get-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9ccb-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9ccb-107">ResourceId</span></span>
```
Get-AzSentinelAlertRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9ccb-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a9ccb-108">DESCRIPTION</span></span>
<span data-ttu-id="a9ccb-109">A **Get-AzSentinelAlertRule parancsmag** egy analytic (riasztási szabály) értéket kap a megadott munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="a9ccb-109">The **Get-AzSentinelAlertRule** cmdlet gets an Analytic (Alert Rule) from the specified workspace.</span></span>
<span data-ttu-id="a9ccb-110">Ha a *AlertRuleId* paramétert adja meg, egyetlen **AlertRule-objektumot** ad vissza.</span><span class="sxs-lookup"><span data-stu-id="a9ccb-110">If you specify the *AlertRuleId* parameter, a single **AlertRule** object is returned.</span></span>
<span data-ttu-id="a9ccb-111">Ha nem adja meg az *AlertRuleId* paramétert, a rendszer egy olyan tömböt ad vissza, amely a megadott munkaterület összes riasztási szabályát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="a9ccb-111">If you do not specify the *AlertRuleId* parameter, an array containing all of the Alert Rules in the specified workspace are returned.</span></span>
<span data-ttu-id="a9ccb-112">A **AlertRule** objektummal frissítheti az AlertRule objektumot, például letilthatja az **AlertRule objektumot.**</span><span class="sxs-lookup"><span data-stu-id="a9ccb-112">You can use the **AlertRule** object to update the AlertRule, for example you can disable the **AlertRule**.</span></span>

## <span data-ttu-id="a9ccb-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a9ccb-113">EXAMPLES</span></span>

### <span data-ttu-id="a9ccb-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="a9ccb-114">Example 1</span></span>
```powershell
PS C:\> $AlertRules = Get-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="a9ccb-115">Ebben a példában az összes **AlertRules** adatokat megkapja a megadott munkaterületről, majd a $AlertRules tárolja.</span><span class="sxs-lookup"><span data-stu-id="a9ccb-115">This example gets all of the **AlertRules** in the specified workspace, and then stores it in the $AlertRules variable.</span></span>

### <span data-ttu-id="a9ccb-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="a9ccb-116">Example 2</span></span>
```powershell
PS C:\> $AlertRule = Get-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
```

<span data-ttu-id="a9ccb-117">Ez a példa egy **AlertRule értéket kap** a megadott munkaterületen, majd tárolja azt a $AlertRule változóban.</span><span class="sxs-lookup"><span data-stu-id="a9ccb-117">This example gets an **AlertRule** in the specified workspace, and then stores it in the $AlertRule variable.</span></span>

## <span data-ttu-id="a9ccb-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9ccb-118">PARAMETERS</span></span>

### <span data-ttu-id="a9ccb-119">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="a9ccb-119">-AlertRuleId</span></span>
<span data-ttu-id="a9ccb-120">Riasztási szabály azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a9ccb-120">Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9ccb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9ccb-121">-DefaultProfile</span></span>
<span data-ttu-id="a9ccb-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a9ccb-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9ccb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9ccb-123">-ResourceGroupName</span></span>
<span data-ttu-id="a9ccb-124">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a9ccb-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9ccb-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9ccb-125">-ResourceId</span></span>
<span data-ttu-id="a9ccb-126">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="a9ccb-126">Resource Id.</span></span>

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

### <span data-ttu-id="a9ccb-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a9ccb-127">-WorkspaceName</span></span>
<span data-ttu-id="a9ccb-128">Munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="a9ccb-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9ccb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9ccb-129">CommonParameters</span></span>
<span data-ttu-id="a9ccb-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9ccb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9ccb-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a9ccb-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9ccb-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a9ccb-132">INPUTS</span></span>

### <span data-ttu-id="a9ccb-133">System.String</span><span class="sxs-lookup"><span data-stu-id="a9ccb-133">System.String</span></span>
## <span data-ttu-id="a9ccb-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9ccb-134">OUTPUTS</span></span>

### <span data-ttu-id="a9ccb-135">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="a9ccb-135">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="a9ccb-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a9ccb-136">NOTES</span></span>

## <span data-ttu-id="a9ccb-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a9ccb-137">RELATED LINKS</span></span>
