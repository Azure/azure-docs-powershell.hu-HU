---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAlertRule.md
ms.openlocfilehash: 9e1a0035a9736ac01963d150f06db9e510e51e17
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93665859"
---
# <span data-ttu-id="e23b1-101">Get-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="e23b1-101">Get-AzAlertRule</span></span>

## <span data-ttu-id="e23b1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e23b1-102">SYNOPSIS</span></span>
<span data-ttu-id="e23b1-103">Figyelmeztetési szabályokat kap.</span><span class="sxs-lookup"><span data-stu-id="e23b1-103">Gets alert rules.</span></span>

## <span data-ttu-id="e23b1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e23b1-104">SYNTAX</span></span>

### <span data-ttu-id="e23b1-105">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e23b1-105">GetByResourceGroup</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e23b1-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="e23b1-106">GetByName</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> -Name <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e23b1-107">GetByResourceUri</span><span class="sxs-lookup"><span data-stu-id="e23b1-107">GetByResourceUri</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> -TargetResourceId <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e23b1-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e23b1-108">DESCRIPTION</span></span>
<span data-ttu-id="e23b1-109">A **Get-AzAlertRule** parancsmag az adott erőforráscsoport nevével vagy URI-ja, vagy az összes figyelmeztetési szabály alapján értesítést kap.</span><span class="sxs-lookup"><span data-stu-id="e23b1-109">The **Get-AzAlertRule** cmdlet gets an alert rule by its name or URI, or all alert rules from a specified resource group.</span></span>

## <span data-ttu-id="e23b1-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e23b1-110">EXAMPLES</span></span>

### <span data-ttu-id="e23b1-111">1. példa: az erőforrás-csoportokra vonatkozó figyelmeztetési szabályok beszerzése</span><span class="sxs-lookup"><span data-stu-id="e23b1-111">Example 1: Get alert rules for a resource group</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS"
```

<span data-ttu-id="e23b1-112">Ez a parancs a Default-Web-CentralUS nevű erőforráscsoport figyelmeztetési szabályait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e23b1-112">This command gets all of the alert rules for the resource group named Default-Web-CentralUS.</span></span>
<span data-ttu-id="e23b1-113">A kimenet nem tartalmaz részleteket a szabályokról, mert a *DetailedOutput* paraméter nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="e23b1-113">The output does not contain details about the rules because the *DetailedOutput* parameter is not specified.</span></span>

### <span data-ttu-id="e23b1-114">2. példa: figyelmeztetési szabály kérése név alapján</span><span class="sxs-lookup"><span data-stu-id="e23b1-114">Example 2: Get an alert rule by name</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

<span data-ttu-id="e23b1-115">Ez a parancs a myalert-7da64548-214d-42CA-b12b-b245bb8f0ac8 nevű riasztási szabályt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e23b1-115">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="e23b1-116">Mivel a *DetailedOutput* paraméter nincs megadva, a kimenet csak az értesítési szabályról tartalmaz alapvető információkat.</span><span class="sxs-lookup"><span data-stu-id="e23b1-116">Because the *DetailedOutput* parameter is not specified, the output contains only basic information about the alert rule.</span></span>

### <span data-ttu-id="e23b1-117">3. példa: figyelmeztetési szabály beszerzése név szerint részletes kimenettel</span><span class="sxs-lookup"><span data-stu-id="e23b1-117">Example 3: Get an alert rule by name with detailed output</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

<span data-ttu-id="e23b1-118">Ez a parancs a myalert-7da64548-214d-42CA-b12b-b245bb8f0ac8 nevű riasztási szabályt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e23b1-118">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="e23b1-119">A *DetailedOutput* paraméter meg van adva, így a kimenet részletezve van.</span><span class="sxs-lookup"><span data-stu-id="e23b1-119">The *DetailedOutput* parameter is specified, so the output is detailed.</span></span>

## <span data-ttu-id="e23b1-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e23b1-120">PARAMETERS</span></span>

### <span data-ttu-id="e23b1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e23b1-121">-DefaultProfile</span></span>
<span data-ttu-id="e23b1-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e23b1-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e23b1-123">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="e23b1-123">-DetailedOutput</span></span>
<span data-ttu-id="e23b1-124">A kimenet minden részletét megjeleníti.</span><span class="sxs-lookup"><span data-stu-id="e23b1-124">Displays full details in the output.</span></span>

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

### <span data-ttu-id="e23b1-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e23b1-125">-Name</span></span>
<span data-ttu-id="e23b1-126">A beolvasott figyelmeztetési szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e23b1-126">Specifies the name of the alert rule to get.</span></span>

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

### <span data-ttu-id="e23b1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e23b1-127">-ResourceGroupName</span></span>
<span data-ttu-id="e23b1-128">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e23b1-128">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e23b1-129">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="e23b1-129">-TargetResourceId</span></span>
<span data-ttu-id="e23b1-130">A cél erőforrás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e23b1-130">Specifies the ID of the target resource.</span></span>

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

### <span data-ttu-id="e23b1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e23b1-131">CommonParameters</span></span>
<span data-ttu-id="e23b1-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e23b1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e23b1-133">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e23b1-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e23b1-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e23b1-134">INPUTS</span></span>

### <span data-ttu-id="e23b1-135">System. String</span><span class="sxs-lookup"><span data-stu-id="e23b1-135">System.String</span></span>

### <span data-ttu-id="e23b1-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e23b1-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e23b1-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e23b1-137">OUTPUTS</span></span>

### <span data-ttu-id="e23b1-138">Microsoft. Azure. commands. OutputClasses. PSAlertRule</span><span class="sxs-lookup"><span data-stu-id="e23b1-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSAlertRule</span></span>

## <span data-ttu-id="e23b1-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e23b1-139">NOTES</span></span>

## <span data-ttu-id="e23b1-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e23b1-140">RELATED LINKS</span></span>

[<span data-ttu-id="e23b1-141">Add-AzLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="e23b1-141">Add-AzLogAlertRule</span></span>](./Add-AzLogAlertRule.md)

[<span data-ttu-id="e23b1-142">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="e23b1-142">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="e23b1-143">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="e23b1-143">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="e23b1-144">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="e23b1-144">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="e23b1-145">Remove-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="e23b1-145">Remove-AzAlertRule</span></span>](./Remove-AzAlertRule.md)


