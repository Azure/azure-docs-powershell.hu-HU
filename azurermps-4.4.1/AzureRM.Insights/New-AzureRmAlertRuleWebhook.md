---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 0137ECA3-37E1-4064-8A65-A582519E9017
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleWebhook.md
ms.openlocfilehash: ed8b8fe18e6320a297635b09089ff95bd52fe1e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504159"
---
# <span data-ttu-id="c5140-101">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="c5140-101">New-AzureRmAlertRuleWebhook</span></span>

## <span data-ttu-id="c5140-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c5140-102">SYNOPSIS</span></span>
<span data-ttu-id="c5140-103">Figyelmeztetési szabályt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c5140-103">Creates an alert rule webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5140-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c5140-104">SYNTAX</span></span>

```
New-AzureRmAlertRuleWebhook [-ServiceUri] <String> [[-Properties] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5140-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c5140-105">DESCRIPTION</span></span>
<span data-ttu-id="c5140-106">A **New-AzureRmAlertRuleWebhook** parancsmag figyelmeztetési szabályt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c5140-106">The **New-AzureRmAlertRuleWebhook** cmdlet creates an alert rule webhook.</span></span>

## <span data-ttu-id="c5140-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c5140-107">EXAMPLES</span></span>

### <span data-ttu-id="c5140-108">Példa 1: figyelmeztetési szabály létrehozása – webhook</span><span class="sxs-lookup"><span data-stu-id="c5140-108">Example 1: Create an alert rule webhook</span></span>
```
PS C:\>New-AzureRmAlertRuleWebhook -ServiceUri "http://contoso.com"
```

<span data-ttu-id="c5140-109">Ez a parancs csak a szolgáltatás URI-azonosítójának megadásával hoz létre figyelmeztetési szabályt webhooktal.</span><span class="sxs-lookup"><span data-stu-id="c5140-109">This command creates an alert rule webhook by specifying only the service URI.</span></span>

### <span data-ttu-id="c5140-110">2. példa: webkampó létrehozása egy tulajdonsággal</span><span class="sxs-lookup"><span data-stu-id="c5140-110">Example 2: Create a webhook with one property</span></span>
```
PS C:\>$Actual = New-AzureRmAlertRuleWebhook -ServiceUri "http://contoso.com" -Properties @{prop1 = 'value1'}
```

<span data-ttu-id="c5140-111">Ez a parancs figyelmeztetési szabályt hoz létre a Contoso.com, amely egy tulajdonsággal rendelkezik, majd a $Actual változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="c5140-111">This command creates an alert rule webhook for Contoso.com that has one property, and then stores it in the $Actual variable.</span></span>

## <span data-ttu-id="c5140-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c5140-112">PARAMETERS</span></span>

### <span data-ttu-id="c5140-113">-Tulajdonságok</span><span class="sxs-lookup"><span data-stu-id="c5140-113">-Properties</span></span>
<span data-ttu-id="c5140-114">A @ formátum @ (property1 = "érték1",....) tulajdonságainak listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c5140-114">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="c5140-115">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="c5140-115">-ServiceUri</span></span>
<span data-ttu-id="c5140-116">A szolgáltatás URI-jét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c5140-116">Specifies the service URI.</span></span>

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

### <span data-ttu-id="c5140-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5140-117">-DefaultProfile</span></span>
<span data-ttu-id="c5140-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c5140-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5140-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5140-119">CommonParameters</span></span>
<span data-ttu-id="c5140-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c5140-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5140-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5140-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5140-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5140-122">INPUTS</span></span>

## <span data-ttu-id="c5140-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5140-123">OUTPUTS</span></span>

### <span data-ttu-id="c5140-124">Microsoft. Azure. Management. monitor. Management. models. RuleWebhookAction</span><span class="sxs-lookup"><span data-stu-id="c5140-124">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span></span>

## <span data-ttu-id="c5140-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c5140-125">NOTES</span></span>

## <span data-ttu-id="c5140-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c5140-126">RELATED LINKS</span></span>

[<span data-ttu-id="c5140-127">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="c5140-127">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="c5140-128">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="c5140-128">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="c5140-129">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="c5140-129">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="c5140-130">Új – AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="c5140-130">New-AzureRmAlertRuleEmail</span></span>](./New-AzureRmAlertRuleEmail.md)

[<span data-ttu-id="c5140-131">Új – AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="c5140-131">New-AzureRmAutoscaleWebhook</span></span>](./New-AzureRmAutoscaleWebhook.md)


