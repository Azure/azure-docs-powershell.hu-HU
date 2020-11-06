---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 11A521DF-E77C-4D6F-A2D9-1C2CF8972F57
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogAlertRule.md
ms.openlocfilehash: 38644018ac9ae19d1c413123ca071f564d336fa7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504960"
---
# <span data-ttu-id="6539c-101">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="6539c-101">Add-AzureRmLogAlertRule</span></span>

## <span data-ttu-id="6539c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6539c-102">SYNOPSIS</span></span>
<span data-ttu-id="6539c-103">Naplózási riasztási szabály hozzáadása vagy cseréje</span><span class="sxs-lookup"><span data-stu-id="6539c-103">Adds or replaces a log alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6539c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6539c-104">SYNTAX</span></span>

```
Add-AzureRmLogAlertRule [-TargetResourceGroup <String>] [-TargetResourceId <String>] [-Level <String>]
 -OperationName <String> [-TargetResourceProvider <String>] [-Status <String>] [-SubStatus <String>]
 -Location <String> [-Description <String>] [-DisableRule] -ResourceGroup <String> -Name <String>
 [-Actions <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6539c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6539c-105">DESCRIPTION</span></span>
<span data-ttu-id="6539c-106">Az **Add-AzureRmLogAlertRule** parancsmag esemény-figyelmeztetési szabályt ad hozzá vagy cserél.</span><span class="sxs-lookup"><span data-stu-id="6539c-106">The **Add-AzureRmLogAlertRule** cmdlet adds or replaces an event alert rule.</span></span>
<span data-ttu-id="6539c-107">A hozzáadott szabály erőforrás-csoporthoz van társítva, és nevet tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="6539c-107">The added rule is associated with a resource group and has a name.</span></span>

<span data-ttu-id="6539c-108">Ahogy az előző kiadásokban is bejelentettük, a **Add-AzureRMLogAlertRule parancsmagot egy jövőbeli kiadásban nem fogja érvényteleníteni.**</span><span class="sxs-lookup"><span data-stu-id="6539c-108">As announced in previous releases: **Add-AzureRMLogAlertRule cmdlet will be deprecated in a future release.**</span></span> <span data-ttu-id="6539c-109">Miután október 1-től az 2017-ös parancsmagot használja, a továbbiakban nem lesz semmilyen hatással, mert ez a funkció a tevékenység-naplózási riasztásokra áttért.</span><span class="sxs-lookup"><span data-stu-id="6539c-109">After October 1st 2017 using this cmdlet will no longer have any effect as this functionality is being transitioned to Activity Log Alerts.</span></span> <span data-ttu-id="6539c-110">**_https://aka.ms/migratemealerts_** További információt itt talál.</span><span class="sxs-lookup"><span data-stu-id="6539c-110">Please see **_https://aka.ms/migratemealerts_** for more information.</span></span>

## <span data-ttu-id="6539c-111">Példák</span><span class="sxs-lookup"><span data-stu-id="6539c-111">EXAMPLES</span></span>

### <span data-ttu-id="6539c-112">1. példa: a naplózási riasztási szabály hozzáadása</span><span class="sxs-lookup"><span data-stu-id="6539c-112">Example 1: Add a log alert rule</span></span>
```
PS C:\>Add-AzureRmLogAlertRule -Name "logRule" -Location "East US" -ResourceGroup "Default-Web-EastUS" -OperationName "Create" -TargetResourceId "/subscriptions/abbfb07c-6c93-40be-bc9b-4f0deba32f4c/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/misitiooeltuyo" -Description "My log rule"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="6539c-113">Ez a parancs eseményvezérelt figyelmeztetési szabályt ad hozzá vagy frissít.</span><span class="sxs-lookup"><span data-stu-id="6539c-113">This command adds or updates an event-based alert rule.</span></span>

## <span data-ttu-id="6539c-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6539c-114">PARAMETERS</span></span>

### <span data-ttu-id="6539c-115">-Műveletek</span><span class="sxs-lookup"><span data-stu-id="6539c-115">-Actions</span></span>
<span data-ttu-id="6539c-116">A műveletek vesszővel elválasztott listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6539c-116">Specifies a comma-separated list of actions.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6539c-117">-Leírás</span><span class="sxs-lookup"><span data-stu-id="6539c-117">-Description</span></span>
<span data-ttu-id="6539c-118">A szabály leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="6539c-118">Specifies a description of the rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6539c-119">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="6539c-119">-DisableRule</span></span>
<span data-ttu-id="6539c-120">Letiltja a szabályt.</span><span class="sxs-lookup"><span data-stu-id="6539c-120">Disables a rule.</span></span>
<span data-ttu-id="6539c-121">Ha nem adja meg ezt a paramétert, a szabály engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="6539c-121">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="6539c-122">-Szint</span><span class="sxs-lookup"><span data-stu-id="6539c-122">-Level</span></span>
<span data-ttu-id="6539c-123">A szabály által figyelt esemény szintjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6539c-123">Specifies the level of the event the rule is monitoring.</span></span>
<span data-ttu-id="6539c-124">Ezt a paramétert csak eseményvezérelt szabályok esetén adja meg.</span><span class="sxs-lookup"><span data-stu-id="6539c-124">Specify this parameter only for event-based rules.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6539c-125">-Hely</span><span class="sxs-lookup"><span data-stu-id="6539c-125">-Location</span></span>
<span data-ttu-id="6539c-126">A szabály helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6539c-126">Specifies the location for the rule.</span></span>

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

### <span data-ttu-id="6539c-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6539c-127">-Name</span></span>
<span data-ttu-id="6539c-128">A szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6539c-128">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="6539c-129">-OperationName</span><span class="sxs-lookup"><span data-stu-id="6539c-129">-OperationName</span></span>
<span data-ttu-id="6539c-130">A művelet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6539c-130">Specifies the name of the operation.</span></span>

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

### <span data-ttu-id="6539c-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6539c-131">-ResourceGroup</span></span>
<span data-ttu-id="6539c-132">A szabály erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6539c-132">Specifies the name of the resource group for the rule.</span></span>

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

### <span data-ttu-id="6539c-133">-Állapot</span><span class="sxs-lookup"><span data-stu-id="6539c-133">-Status</span></span>
<span data-ttu-id="6539c-134">Az állapotot adja meg.</span><span class="sxs-lookup"><span data-stu-id="6539c-134">Specifies the status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6539c-135">-Részállapot</span><span class="sxs-lookup"><span data-stu-id="6539c-135">-SubStatus</span></span>
<span data-ttu-id="6539c-136">A részállapot meghatározása.</span><span class="sxs-lookup"><span data-stu-id="6539c-136">Specifies the substatus.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6539c-137">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6539c-137">-TargetResourceGroup</span></span>
<span data-ttu-id="6539c-138">Annak az erőforrásnak a csoportját adja meg, amelyre a szabály figyeli a szabályt.</span><span class="sxs-lookup"><span data-stu-id="6539c-138">Specifies the resource group of the resource the rule is monitoring.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6539c-139">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="6539c-139">-TargetResourceId</span></span>
<span data-ttu-id="6539c-140">A szabály által figyelt erőforrás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6539c-140">Specifies the ID of the resource the rule is monitoring.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6539c-141">-TargetResourceProvider</span><span class="sxs-lookup"><span data-stu-id="6539c-141">-TargetResourceProvider</span></span>
<span data-ttu-id="6539c-142">Annak az erőforrásnak az erőforrás-szolgáltatója, amelyet a szabály figyel.</span><span class="sxs-lookup"><span data-stu-id="6539c-142">Specifies the resource provider of the resource the rule is monitoring.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6539c-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6539c-143">-DefaultProfile</span></span>
<span data-ttu-id="6539c-144">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6539c-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6539c-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6539c-145">CommonParameters</span></span>
<span data-ttu-id="6539c-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6539c-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6539c-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6539c-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6539c-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6539c-148">INPUTS</span></span>

## <span data-ttu-id="6539c-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6539c-149">OUTPUTS</span></span>

### <span data-ttu-id="6539c-150">Microsoft. Azure. commands. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="6539c-150">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="6539c-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6539c-151">NOTES</span></span>

## <span data-ttu-id="6539c-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6539c-152">RELATED LINKS</span></span>

[<span data-ttu-id="6539c-153">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="6539c-153">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="6539c-154">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="6539c-154">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="6539c-155">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="6539c-155">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="6539c-156">Új – AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="6539c-156">New-AzureRmAlertRuleEmail</span></span>](./New-AzureRmAlertRuleEmail.md)

[<span data-ttu-id="6539c-157">Új – AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="6539c-157">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


