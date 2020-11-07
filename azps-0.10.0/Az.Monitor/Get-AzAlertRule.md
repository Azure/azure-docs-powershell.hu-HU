---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzAlertRule.md
ms.openlocfilehash: 01774d80ce422c1ac0a48df61d44328b6b5b0105
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842053"
---
# <span data-ttu-id="bcf07-101">Get-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="bcf07-101">Get-AzAlertRule</span></span>

## <span data-ttu-id="bcf07-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bcf07-102">SYNOPSIS</span></span>
<span data-ttu-id="bcf07-103">Figyelmeztetési szabályokat kap.</span><span class="sxs-lookup"><span data-stu-id="bcf07-103">Gets alert rules.</span></span>

## <span data-ttu-id="bcf07-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bcf07-104">SYNTAX</span></span>

### <span data-ttu-id="bcf07-105">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bcf07-105">GetByResourceGroup</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bcf07-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="bcf07-106">GetByName</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> -Name <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcf07-107">GetByResourceUri</span><span class="sxs-lookup"><span data-stu-id="bcf07-107">GetByResourceUri</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> -TargetResourceId <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bcf07-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="bcf07-108">DESCRIPTION</span></span>
<span data-ttu-id="bcf07-109">A **Get-AzAlertRule** parancsmag az adott erőforráscsoport nevével vagy URI-ja, vagy az összes figyelmeztetési szabály alapján értesítést kap.</span><span class="sxs-lookup"><span data-stu-id="bcf07-109">The **Get-AzAlertRule** cmdlet gets an alert rule by its name or URI, or all alert rules from a specified resource group.</span></span>

## <span data-ttu-id="bcf07-110">Példák</span><span class="sxs-lookup"><span data-stu-id="bcf07-110">EXAMPLES</span></span>

### <span data-ttu-id="bcf07-111">1. példa: az erőforrás-csoportokra vonatkozó figyelmeztetési szabályok beszerzése</span><span class="sxs-lookup"><span data-stu-id="bcf07-111">Example 1: Get alert rules for a resource group</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS"
```

<span data-ttu-id="bcf07-112">Ez a parancs a Default-Web-CentralUS nevű erőforráscsoport figyelmeztetési szabályait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="bcf07-112">This command gets all of the alert rules for the resource group named Default-Web-CentralUS.</span></span>
<span data-ttu-id="bcf07-113">A kimenet nem tartalmaz részleteket a szabályokról, mert a *DetailedOutput* paraméter nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="bcf07-113">The output does not contain details about the rules because the *DetailedOutput* parameter is not specified.</span></span>

### <span data-ttu-id="bcf07-114">2. példa: figyelmeztetési szabály kérése név alapján</span><span class="sxs-lookup"><span data-stu-id="bcf07-114">Example 2: Get an alert rule by name</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

<span data-ttu-id="bcf07-115">Ez a parancs a myalert-7da64548-214d-42CA-b12b-b245bb8f0ac8 nevű riasztási szabályt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="bcf07-115">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="bcf07-116">Mivel a *DetailedOutput* paraméter nincs megadva, a kimenet csak az értesítési szabályról tartalmaz alapvető információkat.</span><span class="sxs-lookup"><span data-stu-id="bcf07-116">Because the *DetailedOutput* parameter is not specified, the output contains only basic information about the alert rule.</span></span>

### <span data-ttu-id="bcf07-117">3. példa: figyelmeztetési szabály beszerzése név szerint részletes kimenettel</span><span class="sxs-lookup"><span data-stu-id="bcf07-117">Example 3: Get an alert rule by name with detailed output</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

<span data-ttu-id="bcf07-118">Ez a parancs a myalert-7da64548-214d-42CA-b12b-b245bb8f0ac8 nevű riasztási szabályt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="bcf07-118">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="bcf07-119">A *DetailedOutput* paraméter meg van adva, így a kimenet részletezve van.</span><span class="sxs-lookup"><span data-stu-id="bcf07-119">The *DetailedOutput* parameter is specified, so the output is detailed.</span></span>

## <span data-ttu-id="bcf07-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bcf07-120">PARAMETERS</span></span>

### <span data-ttu-id="bcf07-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcf07-121">-DefaultProfile</span></span>
<span data-ttu-id="bcf07-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="bcf07-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bcf07-123">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="bcf07-123">-DetailedOutput</span></span>
<span data-ttu-id="bcf07-124">A kimenet minden részletét megjeleníti.</span><span class="sxs-lookup"><span data-stu-id="bcf07-124">Displays full details in the output.</span></span>

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

### <span data-ttu-id="bcf07-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bcf07-125">-Name</span></span>
<span data-ttu-id="bcf07-126">A beolvasott figyelmeztetési szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bcf07-126">Specifies the name of the alert rule to get.</span></span>

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

### <span data-ttu-id="bcf07-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcf07-127">-ResourceGroupName</span></span>
<span data-ttu-id="bcf07-128">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bcf07-128">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="bcf07-129">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="bcf07-129">-TargetResourceId</span></span>
<span data-ttu-id="bcf07-130">A cél erőforrás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="bcf07-130">Specifies the ID of the target resource.</span></span>

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

### <span data-ttu-id="bcf07-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcf07-131">CommonParameters</span></span>
<span data-ttu-id="bcf07-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bcf07-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcf07-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="bcf07-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcf07-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bcf07-134">INPUTS</span></span>

### <span data-ttu-id="bcf07-135">System. String</span><span class="sxs-lookup"><span data-stu-id="bcf07-135">System.String</span></span>

### <span data-ttu-id="bcf07-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bcf07-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bcf07-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bcf07-137">OUTPUTS</span></span>

### <span data-ttu-id="bcf07-138">Microsoft. Azure. commands. OutputClasses. PSAlertRule</span><span class="sxs-lookup"><span data-stu-id="bcf07-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSAlertRule</span></span>

## <span data-ttu-id="bcf07-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bcf07-139">NOTES</span></span>

## <span data-ttu-id="bcf07-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bcf07-140">RELATED LINKS</span></span>

[<span data-ttu-id="bcf07-141">Add-AzLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="bcf07-141">Add-AzLogAlertRule</span></span>](./Add-AzLogAlertRule.md)

[<span data-ttu-id="bcf07-142">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="bcf07-142">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="bcf07-143">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="bcf07-143">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="bcf07-144">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="bcf07-144">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="bcf07-145">Remove-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="bcf07-145">Remove-AzAlertRule</span></span>](./Remove-AzAlertRule.md)


