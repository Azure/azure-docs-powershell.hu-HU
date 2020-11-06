---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 674A11E4-36B9-4075-9F4E-952BD9FF07A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleWebhook.md
ms.openlocfilehash: 2fc67e4f50d3c0a045ed6f0e6d82d5bf46d10c25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500844"
---
# <span data-ttu-id="c8c9b-101">New-AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="c8c9b-101">New-AzureRmAutoscaleWebhook</span></span>

## <span data-ttu-id="c8c9b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c8c9b-102">SYNOPSIS</span></span>
<span data-ttu-id="c8c9b-103">Automatikusan létrehoz egy automéretarányos webkampót.</span><span class="sxs-lookup"><span data-stu-id="c8c9b-103">Creates an Autoscale webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8c9b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c8c9b-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleWebhook [-ServiceUri] <String> [[-Properties] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8c9b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c8c9b-105">DESCRIPTION</span></span>
<span data-ttu-id="c8c9b-106">A **New-AzureRmAutoscaleWebhook** parancsmag automéretarányos webkampót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c8c9b-106">The **New-AzureRmAutoscaleWebhook** cmdlet creates an Autoscale webhook.</span></span>

## <span data-ttu-id="c8c9b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c8c9b-107">EXAMPLES</span></span>

## <span data-ttu-id="c8c9b-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c8c9b-108">PARAMETERS</span></span>

### <span data-ttu-id="c8c9b-109">-Tulajdonságok</span><span class="sxs-lookup"><span data-stu-id="c8c9b-109">-Properties</span></span>
<span data-ttu-id="c8c9b-110">A @ formátum @ (property1 = "érték1",....) tulajdonságainak listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c8c9b-110">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="c8c9b-111">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="c8c9b-111">-ServiceUri</span></span>
<span data-ttu-id="c8c9b-112">A szolgáltatás URI-jét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c8c9b-112">Specifies the service URI.</span></span>

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

### <span data-ttu-id="c8c9b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8c9b-113">-DefaultProfile</span></span>
<span data-ttu-id="c8c9b-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c8c9b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8c9b-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8c9b-115">CommonParameters</span></span>
<span data-ttu-id="c8c9b-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c8c9b-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8c9b-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8c9b-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8c9b-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8c9b-118">INPUTS</span></span>

## <span data-ttu-id="c8c9b-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8c9b-119">OUTPUTS</span></span>

### <span data-ttu-id="c8c9b-120">Microsoft. Azure. Management. monitor. Management. models. WebhookNotification</span><span class="sxs-lookup"><span data-stu-id="c8c9b-120">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification</span></span>

## <span data-ttu-id="c8c9b-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c8c9b-121">NOTES</span></span>

## <span data-ttu-id="c8c9b-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c8c9b-122">RELATED LINKS</span></span>

[<span data-ttu-id="c8c9b-123">Új – AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="c8c9b-123">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


