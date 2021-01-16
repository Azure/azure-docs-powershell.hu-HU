---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAlertRule.md
ms.openlocfilehash: f515d7db58e75cc916478e07edb4e34233201a4d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476805"
---
# <span data-ttu-id="8db09-101">Get-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="8db09-101">Get-AzAlertRule</span></span>

## <span data-ttu-id="8db09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8db09-102">SYNOPSIS</span></span>
<span data-ttu-id="8db09-103">Értesítési szabályokat kap.</span><span class="sxs-lookup"><span data-stu-id="8db09-103">Gets alert rules.</span></span>

## <span data-ttu-id="8db09-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8db09-104">SYNTAX</span></span>

### <span data-ttu-id="8db09-105">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8db09-105">GetByResourceGroup</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8db09-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="8db09-106">GetByName</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> -Name <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8db09-107">GetByResourceUri</span><span class="sxs-lookup"><span data-stu-id="8db09-107">GetByResourceUri</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> -TargetResourceId <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8db09-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8db09-108">DESCRIPTION</span></span>
<span data-ttu-id="8db09-109">A **Get-AzAlertRule** parancsmag egy riasztási szabályt kap név vagy URI alapján, illetve egy adott erőforráscsoport összes riasztási szabályát.</span><span class="sxs-lookup"><span data-stu-id="8db09-109">The **Get-AzAlertRule** cmdlet gets an alert rule by its name or URI, or all alert rules from a specified resource group.</span></span>

## <span data-ttu-id="8db09-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8db09-110">EXAMPLES</span></span>

### <span data-ttu-id="8db09-111">1. példa: Értesítési szabályok lekérte egy erőforráscsoportra</span><span class="sxs-lookup"><span data-stu-id="8db09-111">Example 1: Get alert rules for a resource group</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS"
```

<span data-ttu-id="8db09-112">Ez a parancs a Default-Web-CentralUS nevű erőforráscsoport összes riasztási szabályát beveszi.</span><span class="sxs-lookup"><span data-stu-id="8db09-112">This command gets all of the alert rules for the resource group named Default-Web-CentralUS.</span></span>
<span data-ttu-id="8db09-113">A kimenet nem tartalmaz részleteket a szabályokról, mert a *DetailedOutput* paraméter nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="8db09-113">The output does not contain details about the rules because the *DetailedOutput* parameter is not specified.</span></span>

### <span data-ttu-id="8db09-114">2. példa: Értesítési szabály lekérte név szerint</span><span class="sxs-lookup"><span data-stu-id="8db09-114">Example 2: Get an alert rule by name</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

<span data-ttu-id="8db09-115">Ez a parancs a myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 riasztási szabályt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8db09-115">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="8db09-116">Mivel a *DetailedOutput* paraméter nincs megadva, a kimenet csak alapvető információkat tartalmaz a riasztási szabályról.</span><span class="sxs-lookup"><span data-stu-id="8db09-116">Because the *DetailedOutput* parameter is not specified, the output contains only basic information about the alert rule.</span></span>

### <span data-ttu-id="8db09-117">3. példa: Riasztási szabály lekérte név szerint részletes kimenettel</span><span class="sxs-lookup"><span data-stu-id="8db09-117">Example 3: Get an alert rule by name with detailed output</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

<span data-ttu-id="8db09-118">Ez a parancs a myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 riasztási szabályt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8db09-118">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="8db09-119">A *DetailedOutput* paraméter meg van adva, így a kimenet részletes.</span><span class="sxs-lookup"><span data-stu-id="8db09-119">The *DetailedOutput* parameter is specified, so the output is detailed.</span></span>

## <span data-ttu-id="8db09-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8db09-120">PARAMETERS</span></span>

### <span data-ttu-id="8db09-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8db09-121">-DefaultProfile</span></span>
<span data-ttu-id="8db09-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8db09-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8db09-123">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="8db09-123">-DetailedOutput</span></span>
<span data-ttu-id="8db09-124">A kimenet minden részletét megjeleníti.</span><span class="sxs-lookup"><span data-stu-id="8db09-124">Displays full details in the output.</span></span>

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

### <span data-ttu-id="8db09-125">-Name</span><span class="sxs-lookup"><span data-stu-id="8db09-125">-Name</span></span>
<span data-ttu-id="8db09-126">A lekért értesítési szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8db09-126">Specifies the name of the alert rule to get.</span></span>

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

### <span data-ttu-id="8db09-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8db09-127">-ResourceGroupName</span></span>
<span data-ttu-id="8db09-128">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8db09-128">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="8db09-129">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="8db09-129">-TargetResourceId</span></span>
<span data-ttu-id="8db09-130">A célerőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8db09-130">Specifies the ID of the target resource.</span></span>

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

### <span data-ttu-id="8db09-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8db09-131">CommonParameters</span></span>
<span data-ttu-id="8db09-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8db09-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8db09-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8db09-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8db09-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8db09-134">INPUTS</span></span>

### <span data-ttu-id="8db09-135">System.String</span><span class="sxs-lookup"><span data-stu-id="8db09-135">System.String</span></span>

### <span data-ttu-id="8db09-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8db09-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8db09-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8db09-137">OUTPUTS</span></span>

### <span data-ttu-id="8db09-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSAlertRule</span><span class="sxs-lookup"><span data-stu-id="8db09-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSAlertRule</span></span>

## <span data-ttu-id="8db09-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8db09-139">NOTES</span></span>

## <span data-ttu-id="8db09-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8db09-140">RELATED LINKS</span></span>

[<span data-ttu-id="8db09-141">Add-AzLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="8db09-141">Add-AzLogAlertRule</span></span>](./Add-AzLogAlertRule.md)

[<span data-ttu-id="8db09-142">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="8db09-142">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="8db09-143">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="8db09-143">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="8db09-144">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="8db09-144">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="8db09-145">Remove-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="8db09-145">Remove-AzAlertRule</span></span>](./Remove-AzAlertRule.md)


