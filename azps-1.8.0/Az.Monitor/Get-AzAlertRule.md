---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAlertRule.md
ms.openlocfilehash: 7164c1f37c3205e3bc2d71f2b820290217aff432
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100403102"
---
# <span data-ttu-id="ffbb4-101">Get-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="ffbb4-101">Get-AzAlertRule</span></span>

## <span data-ttu-id="ffbb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffbb4-102">SYNOPSIS</span></span>
<span data-ttu-id="ffbb4-103">Értesítési szabályokat kap.</span><span class="sxs-lookup"><span data-stu-id="ffbb4-103">Gets alert rules.</span></span>

## <span data-ttu-id="ffbb4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ffbb4-104">SYNTAX</span></span>

### <span data-ttu-id="ffbb4-105">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ffbb4-105">GetByResourceGroup</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ffbb4-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="ffbb4-106">GetByName</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> -Name <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ffbb4-107">GetByResourceUri</span><span class="sxs-lookup"><span data-stu-id="ffbb4-107">GetByResourceUri</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> -TargetResourceId <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ffbb4-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ffbb4-108">DESCRIPTION</span></span>
<span data-ttu-id="ffbb4-109">A **Get-AzAlertRule** parancsmag egy riasztási szabályt kap név vagy URI alapján, illetve egy adott erőforráscsoport összes riasztási szabályát.</span><span class="sxs-lookup"><span data-stu-id="ffbb4-109">The **Get-AzAlertRule** cmdlet gets an alert rule by its name or URI, or all alert rules from a specified resource group.</span></span>

## <span data-ttu-id="ffbb4-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ffbb4-110">EXAMPLES</span></span>

### <span data-ttu-id="ffbb4-111">1. példa: Értesítési szabályok lekérte egy erőforráscsoportra</span><span class="sxs-lookup"><span data-stu-id="ffbb4-111">Example 1: Get alert rules for a resource group</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS"
```

<span data-ttu-id="ffbb4-112">Ez a parancs a Default-Web-CentralUS nevű erőforráscsoport összes riasztási szabályát beveszi.</span><span class="sxs-lookup"><span data-stu-id="ffbb4-112">This command gets all of the alert rules for the resource group named Default-Web-CentralUS.</span></span>
<span data-ttu-id="ffbb4-113">A kimenet nem tartalmaz részleteket a szabályokról, mert a *DetailedOutput* paraméter nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="ffbb4-113">The output does not contain details about the rules because the *DetailedOutput* parameter is not specified.</span></span>

### <span data-ttu-id="ffbb4-114">2. példa: Értesítési szabály lekérte név szerint</span><span class="sxs-lookup"><span data-stu-id="ffbb4-114">Example 2: Get an alert rule by name</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

<span data-ttu-id="ffbb4-115">Ez a parancs a myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 riasztási szabályt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ffbb4-115">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="ffbb4-116">Mivel a *DetailedOutput* paraméter nincs megadva, a kimenet csak alapvető információkat tartalmaz a riasztási szabályról.</span><span class="sxs-lookup"><span data-stu-id="ffbb4-116">Because the *DetailedOutput* parameter is not specified, the output contains only basic information about the alert rule.</span></span>

### <span data-ttu-id="ffbb4-117">3. példa: Riasztási szabály lekérte név szerint részletes kimenettel</span><span class="sxs-lookup"><span data-stu-id="ffbb4-117">Example 3: Get an alert rule by name with detailed output</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

<span data-ttu-id="ffbb4-118">Ez a parancs a myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 riasztási szabályt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ffbb4-118">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="ffbb4-119">A *DetailedOutput* paraméter meg van adva, így a kimenet részletes.</span><span class="sxs-lookup"><span data-stu-id="ffbb4-119">The *DetailedOutput* parameter is specified, so the output is detailed.</span></span>

## <span data-ttu-id="ffbb4-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ffbb4-120">PARAMETERS</span></span>

### <span data-ttu-id="ffbb4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffbb4-121">-DefaultProfile</span></span>
<span data-ttu-id="ffbb4-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ffbb4-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ffbb4-123">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="ffbb4-123">-DetailedOutput</span></span>
<span data-ttu-id="ffbb4-124">A kimenet minden részletét megjeleníti.</span><span class="sxs-lookup"><span data-stu-id="ffbb4-124">Displays full details in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffbb4-125">-Name</span><span class="sxs-lookup"><span data-stu-id="ffbb4-125">-Name</span></span>
<span data-ttu-id="ffbb4-126">A lekért értesítési szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ffbb4-126">Specifies the name of the alert rule to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffbb4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffbb4-127">-ResourceGroupName</span></span>
<span data-ttu-id="ffbb4-128">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ffbb4-128">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffbb4-129">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="ffbb4-129">-TargetResourceId</span></span>
<span data-ttu-id="ffbb4-130">A célerőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ffbb4-130">Specifies the ID of the target resource.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffbb4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffbb4-131">CommonParameters</span></span>
<span data-ttu-id="ffbb4-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffbb4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffbb4-133">További információt a about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffbb4-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffbb4-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ffbb4-134">INPUTS</span></span>

### <span data-ttu-id="ffbb4-135">System.String</span><span class="sxs-lookup"><span data-stu-id="ffbb4-135">System.String</span></span>

### <span data-ttu-id="ffbb4-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ffbb4-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ffbb4-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ffbb4-137">OUTPUTS</span></span>

### <span data-ttu-id="ffbb4-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSAlertRule</span><span class="sxs-lookup"><span data-stu-id="ffbb4-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSAlertRule</span></span>

## <span data-ttu-id="ffbb4-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ffbb4-139">NOTES</span></span>

## <span data-ttu-id="ffbb4-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ffbb4-140">RELATED LINKS</span></span>


[<span data-ttu-id="ffbb4-141">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="ffbb4-141">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="ffbb4-142">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="ffbb4-142">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="ffbb4-143">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="ffbb4-143">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="ffbb4-144">Remove-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="ffbb4-144">Remove-AzAlertRule</span></span>](./Remove-AzAlertRule.md)


