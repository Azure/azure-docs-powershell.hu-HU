---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermalertrule
schema: 2.0.0
ms.openlocfilehash: fe763bcf6ff4aeeeedb3ff0dcb0c2ebd5c4b45cc
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850830"
---
# <span data-ttu-id="bea21-101">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="bea21-101">Get-AzureRmAlertRule</span></span>

## <span data-ttu-id="bea21-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bea21-102">SYNOPSIS</span></span>
<span data-ttu-id="bea21-103">Figyelmeztetési szabályokat kap.</span><span class="sxs-lookup"><span data-stu-id="bea21-103">Gets alert rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bea21-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bea21-104">SYNTAX</span></span>

### <span data-ttu-id="bea21-105">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bea21-105">GetByResourceGroup</span></span>
```
Get-AzureRmAlertRule -ResourceGroupName <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bea21-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="bea21-106">GetByName</span></span>
```
Get-AzureRmAlertRule -ResourceGroupName <String> -Name <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bea21-107">GetByResourceUri</span><span class="sxs-lookup"><span data-stu-id="bea21-107">GetByResourceUri</span></span>
```
Get-AzureRmAlertRule -ResourceGroupName <String> -TargetResourceId <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bea21-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="bea21-108">DESCRIPTION</span></span>
<span data-ttu-id="bea21-109">A **Get-AzureRmAlertRule** parancsmag az adott erőforráscsoport nevével vagy URI-ja, vagy az összes figyelmeztetési szabály alapján értesítést kap.</span><span class="sxs-lookup"><span data-stu-id="bea21-109">The **Get-AzureRmAlertRule** cmdlet gets an alert rule by its name or URI, or all alert rules from a specified resource group.</span></span>

## <span data-ttu-id="bea21-110">Példák</span><span class="sxs-lookup"><span data-stu-id="bea21-110">EXAMPLES</span></span>

### <span data-ttu-id="bea21-111">1. példa: az erőforrás-csoportokra vonatkozó figyelmeztetési szabályok beszerzése</span><span class="sxs-lookup"><span data-stu-id="bea21-111">Example 1: Get alert rules for a resource group</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS"
```

<span data-ttu-id="bea21-112">Ez a parancs a Default-Web-CentralUS nevű erőforráscsoport figyelmeztetési szabályait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="bea21-112">This command gets all of the alert rules for the resource group named Default-Web-CentralUS.</span></span>
<span data-ttu-id="bea21-113">A kimenet nem tartalmaz részleteket a szabályokról, mert a *DetailedOutput* paraméter nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="bea21-113">The output does not contain details about the rules because the *DetailedOutput* parameter is not specified.</span></span>

### <span data-ttu-id="bea21-114">2. példa: figyelmeztetési szabály kérése név alapján</span><span class="sxs-lookup"><span data-stu-id="bea21-114">Example 2: Get an alert rule by name</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

<span data-ttu-id="bea21-115">Ez a parancs a myalert-7da64548-214d-42CA-b12b-b245bb8f0ac8 nevű riasztási szabályt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="bea21-115">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="bea21-116">Mivel a *DetailedOutput* paraméter nincs megadva, a kimenet csak az értesítési szabályról tartalmaz alapvető információkat.</span><span class="sxs-lookup"><span data-stu-id="bea21-116">Because the *DetailedOutput* parameter is not specified, the output contains only basic information about the alert rule.</span></span>

### <span data-ttu-id="bea21-117">3. példa: figyelmeztetési szabály beszerzése név szerint részletes kimenettel</span><span class="sxs-lookup"><span data-stu-id="bea21-117">Example 3: Get an alert rule by name with detailed output</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

<span data-ttu-id="bea21-118">Ez a parancs a myalert-7da64548-214d-42CA-b12b-b245bb8f0ac8 nevű riasztási szabályt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="bea21-118">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="bea21-119">A *DetailedOutput* paraméter meg van adva, így a kimenet részletezve van.</span><span class="sxs-lookup"><span data-stu-id="bea21-119">The *DetailedOutput* parameter is specified, so the output is detailed.</span></span>

## <span data-ttu-id="bea21-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bea21-120">PARAMETERS</span></span>

### <span data-ttu-id="bea21-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bea21-121">-DefaultProfile</span></span>
<span data-ttu-id="bea21-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="bea21-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bea21-123">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="bea21-123">-DetailedOutput</span></span>
<span data-ttu-id="bea21-124">A kimenet minden részletét megjeleníti.</span><span class="sxs-lookup"><span data-stu-id="bea21-124">Displays full details in the output.</span></span>

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

### <span data-ttu-id="bea21-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bea21-125">-Name</span></span>
<span data-ttu-id="bea21-126">A beolvasott figyelmeztetési szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bea21-126">Specifies the name of the alert rule to get.</span></span>

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

### <span data-ttu-id="bea21-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bea21-127">-ResourceGroupName</span></span>
<span data-ttu-id="bea21-128">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bea21-128">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="bea21-129">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="bea21-129">-TargetResourceId</span></span>
<span data-ttu-id="bea21-130">A cél erőforrás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="bea21-130">Specifies the ID of the target resource.</span></span>

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

### <span data-ttu-id="bea21-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bea21-131">CommonParameters</span></span>
<span data-ttu-id="bea21-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bea21-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bea21-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bea21-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bea21-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bea21-134">INPUTS</span></span>

### <span data-ttu-id="bea21-135">System. String</span><span class="sxs-lookup"><span data-stu-id="bea21-135">System.String</span></span>

### <span data-ttu-id="bea21-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bea21-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bea21-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bea21-137">OUTPUTS</span></span>

### <span data-ttu-id="bea21-138">Microsoft. Azure. commands. OutputClasses. PSAlertRule</span><span class="sxs-lookup"><span data-stu-id="bea21-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSAlertRule</span></span>

## <span data-ttu-id="bea21-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bea21-139">NOTES</span></span>

## <span data-ttu-id="bea21-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bea21-140">RELATED LINKS</span></span>



[<span data-ttu-id="bea21-141">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="bea21-141">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="bea21-142">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="bea21-142">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="bea21-143">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="bea21-143">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="bea21-144">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="bea21-144">Remove-AzureRmAlertRule</span></span>](./Remove-AzureRmAlertRule.md)


