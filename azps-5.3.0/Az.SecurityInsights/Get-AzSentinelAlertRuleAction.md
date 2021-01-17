---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 6e60f4ed93dd3963fa748db250cacfcf0aeecce3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479735"
---
# <span data-ttu-id="20561-101">Get-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="20561-101">Get-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="20561-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20561-102">SYNOPSIS</span></span>
<span data-ttu-id="20561-103">Automatikus válasz (értesítési szabály művelet) stb.</span><span class="sxs-lookup"><span data-stu-id="20561-103">Get an Automated Response (Alert Rule Action).</span></span>

## <span data-ttu-id="20561-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="20561-104">SYNTAX</span></span>

### <span data-ttu-id="20561-105">AlertRuleId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="20561-105">AlertRuleId (Default)</span></span>
```
Get-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20561-106">ActionId</span><span class="sxs-lookup"><span data-stu-id="20561-106">ActionId</span></span>
```
Get-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 -ActionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20561-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="20561-107">DESCRIPTION</span></span>
<span data-ttu-id="20561-108">A **Get-AzSentinelAlertRuleAction** parancsmag automatikus választ (riasztási szabály-műveletet) kap a megadott munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="20561-108">The **Get-AzSentinelAlertRuleAction** cmdlet gets an Automated Response (Alert Rule Action) from the specified workspace.</span></span>
<span data-ttu-id="20561-109">Ha megadja az *ActionId* és az *AlertRuleId* paramétert, a művelet egyetlen **AlertRuleAction** objektumot ad vissza.</span><span class="sxs-lookup"><span data-stu-id="20561-109">If you specify the *ActionId* and *AlertRuleId* parameters, a single **AlertRuleAction** object is returned.</span></span>
<span data-ttu-id="20561-110">Ha nem adja meg az *ActionId* paramétert, a megadott munkaterület adott riasztási szabályának összes műveletét tartalmazó tömb jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="20561-110">If you do not specify the *ActionId* parameter, an array containing all of the Actions for the specificed Alert Rule in the specified workspace are returned.</span></span>
<span data-ttu-id="20561-111">A Művelet **objektummal** frissítheti a Műveletet, például módosíthatja egy riasztási szabály műveletét. </span><span class="sxs-lookup"><span data-stu-id="20561-111">You can use the **Action** object to update the Action, for example you can change the the **Action** for an Alert Rule.</span></span>

## <span data-ttu-id="20561-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="20561-112">EXAMPLES</span></span>

### <span data-ttu-id="20561-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="20561-113">Example 1</span></span>
```powershell
PS C:\> $AlertRuleActions = Get-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
```

<span data-ttu-id="20561-114">Ebben a példában  a megadott riasztási szabály összes műveletét lejátsa a megadott munkaterületen, majd tárolja azt a $AlertRuleActions változóban.</span><span class="sxs-lookup"><span data-stu-id="20561-114">This example gets all of the **Actions** for the specified Alert Rule in the specified workspace, and then stores it in the $AlertRuleActions variable.</span></span>

### <span data-ttu-id="20561-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="20561-115">Example 2</span></span>
```powershell
PS C:\> $AlertRuleAction = Get-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId"
```

<span data-ttu-id="20561-116">Ebben a példában egy **AlertRuleAction** függvényt kap a megadott értesítési szabályhoz a megadott munkaterületen, majd azt a $AlertRuleAction tárolja.</span><span class="sxs-lookup"><span data-stu-id="20561-116">This example gets an **AlertRuleAction** for the specified Alert Rule in the specified workspace, and then stores it in the $AlertRuleAction variable.</span></span>

## <span data-ttu-id="20561-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="20561-117">PARAMETERS</span></span>

### <span data-ttu-id="20561-118">-ActionId</span><span class="sxs-lookup"><span data-stu-id="20561-118">-ActionId</span></span>
<span data-ttu-id="20561-119">Műveletazonosító.</span><span class="sxs-lookup"><span data-stu-id="20561-119">Action Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20561-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="20561-120">-AlertRuleId</span></span>
<span data-ttu-id="20561-121">Riasztási szabály azonosítója.</span><span class="sxs-lookup"><span data-stu-id="20561-121">Alert Rule Id.</span></span>

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

### <span data-ttu-id="20561-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20561-122">-DefaultProfile</span></span>
<span data-ttu-id="20561-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="20561-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20561-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20561-124">-ResourceGroupName</span></span>
<span data-ttu-id="20561-125">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="20561-125">Resource group name.</span></span>

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

### <span data-ttu-id="20561-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="20561-126">-WorkspaceName</span></span>
<span data-ttu-id="20561-127">Munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="20561-127">Workspace Name.</span></span>

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

### <span data-ttu-id="20561-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20561-128">CommonParameters</span></span>
<span data-ttu-id="20561-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20561-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20561-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="20561-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20561-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="20561-131">INPUTS</span></span>

### <span data-ttu-id="20561-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="20561-132">None</span></span>
## <span data-ttu-id="20561-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="20561-133">OUTPUTS</span></span>

### <span data-ttu-id="20561-134">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="20561-134">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="20561-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="20561-135">NOTES</span></span>

## <span data-ttu-id="20561-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="20561-136">RELATED LINKS</span></span>
