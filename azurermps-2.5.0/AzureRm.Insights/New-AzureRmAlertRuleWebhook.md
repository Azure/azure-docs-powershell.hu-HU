---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 0137ECA3-37E1-4064-8A65-A582519E9017
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermalertrulewebhook
schema: 2.0.0
ms.openlocfilehash: d45624da172ecafba48354968d5a3ac5531be693
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850822"
---
# <span data-ttu-id="c3095-101">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="c3095-101">New-AzureRmAlertRuleWebhook</span></span>

## <span data-ttu-id="c3095-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c3095-102">SYNOPSIS</span></span>
<span data-ttu-id="c3095-103">Figyelmeztetési szabályt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c3095-103">Creates an alert rule webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3095-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c3095-104">SYNTAX</span></span>

```
New-AzureRmAlertRuleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3095-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c3095-105">DESCRIPTION</span></span>
<span data-ttu-id="c3095-106">A **New-AzureRmAlertRuleWebhook** parancsmag figyelmeztetési szabályt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c3095-106">The **New-AzureRmAlertRuleWebhook** cmdlet creates an alert rule webhook.</span></span>

## <span data-ttu-id="c3095-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c3095-107">EXAMPLES</span></span>

### <span data-ttu-id="c3095-108">Példa 1: figyelmeztetési szabály létrehozása – webhook</span><span class="sxs-lookup"><span data-stu-id="c3095-108">Example 1: Create an alert rule webhook</span></span>
```
PS C:\>New-AzureRmAlertRuleWebhook -ServiceUri "http://contoso.com"
```

<span data-ttu-id="c3095-109">Ez a parancs csak a szolgáltatás URI-azonosítójának megadásával hoz létre figyelmeztetési szabályt webhooktal.</span><span class="sxs-lookup"><span data-stu-id="c3095-109">This command creates an alert rule webhook by specifying only the service URI.</span></span>

### <span data-ttu-id="c3095-110">2. példa: webkampó létrehozása egy tulajdonsággal</span><span class="sxs-lookup"><span data-stu-id="c3095-110">Example 2: Create a webhook with one property</span></span>
```
PS C:\>$Actual = New-AzureRmAlertRuleWebhook -ServiceUri "http://contoso.com" -Properties @{prop1 = 'value1'}
```

<span data-ttu-id="c3095-111">Ez a parancs figyelmeztetési szabályt hoz létre a Contoso.com, amely egy tulajdonsággal rendelkezik, majd a $Actual változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="c3095-111">This command creates an alert rule webhook for Contoso.com that has one property, and then stores it in the $Actual variable.</span></span>

## <span data-ttu-id="c3095-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c3095-112">PARAMETERS</span></span>

### <span data-ttu-id="c3095-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3095-113">-DefaultProfile</span></span>
<span data-ttu-id="c3095-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c3095-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c3095-115">-Tulajdonság</span><span class="sxs-lookup"><span data-stu-id="c3095-115">-Property</span></span>
<span data-ttu-id="c3095-116">A @ formátum @ (property1 = "érték1",....) tulajdonságainak listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c3095-116">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="c3095-117">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="c3095-117">-ServiceUri</span></span>
<span data-ttu-id="c3095-118">A szolgáltatás URI-jét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c3095-118">Specifies the service URI.</span></span>

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

### <span data-ttu-id="c3095-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3095-119">CommonParameters</span></span>
<span data-ttu-id="c3095-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c3095-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3095-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3095-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3095-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3095-122">INPUTS</span></span>

### <span data-ttu-id="c3095-123">System. String</span><span class="sxs-lookup"><span data-stu-id="c3095-123">System.String</span></span>

### <span data-ttu-id="c3095-124">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c3095-124">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c3095-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3095-125">OUTPUTS</span></span>

### <span data-ttu-id="c3095-126">Microsoft. Azure. Management. monitor. Management. models. RuleWebhookAction</span><span class="sxs-lookup"><span data-stu-id="c3095-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span></span>

## <span data-ttu-id="c3095-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c3095-127">NOTES</span></span>

## <span data-ttu-id="c3095-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c3095-128">RELATED LINKS</span></span>



[<span data-ttu-id="c3095-129">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="c3095-129">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="c3095-130">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="c3095-130">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="c3095-131">Új – AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="c3095-131">New-AzureRmAlertRuleEmail</span></span>](./New-AzureRmAlertRuleEmail.md)

[<span data-ttu-id="c3095-132">Új – AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="c3095-132">New-AzureRmAutoscaleWebhook</span></span>](./New-AzureRmAutoscaleWebhook.md)


