---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 0137ECA3-37E1-4064-8A65-A582519E9017
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertrulewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
ms.openlocfilehash: 4d6e6fef4ff51038c0939f11571b582628ab0740
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835045"
---
# <span data-ttu-id="e897f-101">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="e897f-101">New-AzAlertRuleWebhook</span></span>

## <span data-ttu-id="e897f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e897f-102">SYNOPSIS</span></span>
<span data-ttu-id="e897f-103">Figyelmeztetési szabályt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e897f-103">Creates an alert rule webhook.</span></span>

## <span data-ttu-id="e897f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e897f-104">SYNTAX</span></span>

```
New-AzAlertRuleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e897f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e897f-105">DESCRIPTION</span></span>
<span data-ttu-id="e897f-106">A **New-AzAlertRuleWebhook** parancsmag figyelmeztetési szabályt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e897f-106">The **New-AzAlertRuleWebhook** cmdlet creates an alert rule webhook.</span></span>

## <span data-ttu-id="e897f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e897f-107">EXAMPLES</span></span>

### <span data-ttu-id="e897f-108">Példa 1: figyelmeztetési szabály létrehozása – webhook</span><span class="sxs-lookup"><span data-stu-id="e897f-108">Example 1: Create an alert rule webhook</span></span>
```
PS C:\>New-AzAlertRuleWebhook -ServiceUri "http://contoso.com"
```

<span data-ttu-id="e897f-109">Ez a parancs csak a szolgáltatás URI-azonosítójának megadásával hoz létre figyelmeztetési szabályt webhooktal.</span><span class="sxs-lookup"><span data-stu-id="e897f-109">This command creates an alert rule webhook by specifying only the service URI.</span></span>

### <span data-ttu-id="e897f-110">2. példa: webkampó létrehozása egy tulajdonsággal</span><span class="sxs-lookup"><span data-stu-id="e897f-110">Example 2: Create a webhook with one property</span></span>
```
PS C:\>$Actual = New-AzAlertRuleWebhook -ServiceUri "http://contoso.com" -Properties @{prop1 = 'value1'}
```

<span data-ttu-id="e897f-111">Ez a parancs figyelmeztetési szabályt hoz létre a Contoso.com, amely egy tulajdonsággal rendelkezik, majd a $Actual változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e897f-111">This command creates an alert rule webhook for Contoso.com that has one property, and then stores it in the $Actual variable.</span></span>

## <span data-ttu-id="e897f-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e897f-112">PARAMETERS</span></span>

### <span data-ttu-id="e897f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e897f-113">-DefaultProfile</span></span>
<span data-ttu-id="e897f-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e897f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e897f-115">-Tulajdonság</span><span class="sxs-lookup"><span data-stu-id="e897f-115">-Property</span></span>
<span data-ttu-id="e897f-116">A @ formátum @ (property1 = "érték1",....) tulajdonságainak listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e897f-116">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e897f-117">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="e897f-117">-ServiceUri</span></span>
<span data-ttu-id="e897f-118">A szolgáltatás URI-jét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e897f-118">Specifies the service URI.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e897f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e897f-119">CommonParameters</span></span>
<span data-ttu-id="e897f-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e897f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e897f-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e897f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e897f-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e897f-122">INPUTS</span></span>

### <span data-ttu-id="e897f-123">System. String</span><span class="sxs-lookup"><span data-stu-id="e897f-123">System.String</span></span>

### <span data-ttu-id="e897f-124">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e897f-124">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e897f-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e897f-125">OUTPUTS</span></span>

### <span data-ttu-id="e897f-126">Microsoft. Azure. Management. monitor. Management. models. RuleWebhookAction</span><span class="sxs-lookup"><span data-stu-id="e897f-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span></span>

## <span data-ttu-id="e897f-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e897f-127">NOTES</span></span>

## <span data-ttu-id="e897f-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e897f-128">RELATED LINKS</span></span>

[<span data-ttu-id="e897f-129">Add-AzLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="e897f-129">Add-AzLogAlertRule</span></span>](./Add-AzLogAlertRule.md)

[<span data-ttu-id="e897f-130">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="e897f-130">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="e897f-131">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="e897f-131">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="e897f-132">Új – AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="e897f-132">New-AzAlertRuleEmail</span></span>](./New-AzAlertRuleEmail.md)

[<span data-ttu-id="e897f-133">Új – AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="e897f-133">New-AzAutoscaleWebhook</span></span>](./New-AzAutoscaleWebhook.md)


