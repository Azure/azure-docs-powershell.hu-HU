---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAlertRule.md
ms.openlocfilehash: 65c5bc7a2767fd00497b487783c4e6f0ce6d6723
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504932"
---
# <span data-ttu-id="24f5c-101">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="24f5c-101">Get-AzureRmAlertRule</span></span>

## <span data-ttu-id="24f5c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="24f5c-102">SYNOPSIS</span></span>
<span data-ttu-id="24f5c-103">Figyelmeztetési szabályokat kap.</span><span class="sxs-lookup"><span data-stu-id="24f5c-103">Gets alert rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24f5c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="24f5c-104">SYNTAX</span></span>

### <span data-ttu-id="24f5c-105">Get-AzureRmAlertRule parancsmag paraméterei</span><span class="sxs-lookup"><span data-stu-id="24f5c-105">Parameters for Get-AzureRmAlertRule cmdlet</span></span>
```
Get-AzureRmAlertRule -ResourceGroup <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="24f5c-106">Get-AzureRmAlertRule parancsmag paraméterei név használatával</span><span class="sxs-lookup"><span data-stu-id="24f5c-106">Parameters for Get-AzureRmAlertRule cmdlet using name</span></span>
```
Get-AzureRmAlertRule -ResourceGroup <String> -Name <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24f5c-107">Get-AzureRmAlertRule parancsmag paraméterei a cél erőforrás URI azonosítóval</span><span class="sxs-lookup"><span data-stu-id="24f5c-107">Parameters for Get-AzureRmAlertRule cmdlet using target resource uri</span></span>
```
Get-AzureRmAlertRule -ResourceGroup <String> -TargetResourceId <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24f5c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="24f5c-108">DESCRIPTION</span></span>
<span data-ttu-id="24f5c-109">A **Get-AzureRmAlertRule** parancsmag az adott erőforráscsoport nevével vagy URI-ja, vagy az összes figyelmeztetési szabály alapján értesítést kap.</span><span class="sxs-lookup"><span data-stu-id="24f5c-109">The **Get-AzureRmAlertRule** cmdlet gets an alert rule by its name or URI, or all alert rules from a specified resource group.</span></span>

## <span data-ttu-id="24f5c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="24f5c-110">EXAMPLES</span></span>

### <span data-ttu-id="24f5c-111">1. példa: az erőforrás-csoportokra vonatkozó figyelmeztetési szabályok beszerzése</span><span class="sxs-lookup"><span data-stu-id="24f5c-111">Example 1: Get alert rules for a resource group</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS"
```

<span data-ttu-id="24f5c-112">Ez a parancs a Default-Web-CentralUS nevű erőforráscsoport figyelmeztetési szabályait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="24f5c-112">This command gets all of the alert rules for the resource group named Default-Web-CentralUS.</span></span>
<span data-ttu-id="24f5c-113">A kimenet nem tartalmaz részleteket a szabályokról, mert a *DetailedOutput* paraméter nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="24f5c-113">The output does not contain details about the rules because the *DetailedOutput* parameter is not specified.</span></span>

### <span data-ttu-id="24f5c-114">2. példa: figyelmeztetési szabály kérése név alapján</span><span class="sxs-lookup"><span data-stu-id="24f5c-114">Example 2: Get an alert rule by name</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourcGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

<span data-ttu-id="24f5c-115">Ez a parancs a myalert-7da64548-214d-42CA-b12b-b245bb8f0ac8 nevű riasztási szabályt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="24f5c-115">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="24f5c-116">Mivel a *DetailedOutput* paraméter nincs megadva, a kimenet csak az értesítési szabályról tartalmaz alapvető információkat.</span><span class="sxs-lookup"><span data-stu-id="24f5c-116">Because the *DetailedOutput* parameter is not specified, the output contains only basic information about the alert rule.</span></span>

### <span data-ttu-id="24f5c-117">3. példa: figyelmeztetési szabály beszerzése név szerint részletes kimenettel</span><span class="sxs-lookup"><span data-stu-id="24f5c-117">Example 3: Get an alert rule by name with detailed output</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

<span data-ttu-id="24f5c-118">Ez a parancs a myalert-7da64548-214d-42CA-b12b-b245bb8f0ac8 nevű riasztási szabályt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="24f5c-118">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="24f5c-119">A *DetailedOutput* paraméter meg van adva, így a kimenet részletezve van.</span><span class="sxs-lookup"><span data-stu-id="24f5c-119">The *DetailedOutput* parameter is specified, so the output is detailed.</span></span>

## <span data-ttu-id="24f5c-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="24f5c-120">PARAMETERS</span></span>

### <span data-ttu-id="24f5c-121">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="24f5c-121">-DetailedOutput</span></span>
<span data-ttu-id="24f5c-122">A kimenet minden részletét megjeleníti.</span><span class="sxs-lookup"><span data-stu-id="24f5c-122">Displays full details in the output.</span></span>

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

### <span data-ttu-id="24f5c-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="24f5c-123">-Name</span></span>
<span data-ttu-id="24f5c-124">A beolvasott figyelmeztetési szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="24f5c-124">Specifies the name of the alert rule to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for Get-AzureRmAlertRule cmdlet using name
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24f5c-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="24f5c-125">-ResourceGroup</span></span>
<span data-ttu-id="24f5c-126">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="24f5c-126">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24f5c-127">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="24f5c-127">-TargetResourceId</span></span>
<span data-ttu-id="24f5c-128">A cél erőforrás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="24f5c-128">Specifies the ID of the target resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for Get-AzureRmAlertRule cmdlet using target resource uri
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24f5c-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24f5c-129">-DefaultProfile</span></span>
<span data-ttu-id="24f5c-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="24f5c-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24f5c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24f5c-131">CommonParameters</span></span>
<span data-ttu-id="24f5c-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="24f5c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24f5c-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24f5c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24f5c-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="24f5c-134">INPUTS</span></span>

## <span data-ttu-id="24f5c-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="24f5c-135">OUTPUTS</span></span>

### <span data-ttu-id="24f5c-136">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. detekintés. OutputClasses. PSManagementItemDescriptor]</span><span class="sxs-lookup"><span data-stu-id="24f5c-136">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSManagementItemDescriptor]</span></span>

## <span data-ttu-id="24f5c-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="24f5c-137">NOTES</span></span>

## <span data-ttu-id="24f5c-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="24f5c-138">RELATED LINKS</span></span>

[<span data-ttu-id="24f5c-139">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="24f5c-139">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="24f5c-140">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="24f5c-140">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="24f5c-141">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="24f5c-141">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="24f5c-142">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="24f5c-142">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="24f5c-143">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="24f5c-143">Remove-AzureRmAlertRule</span></span>](./Remove-AzureRmAlertRule.md)


