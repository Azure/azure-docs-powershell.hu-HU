---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 674A11E4-36B9-4075-9F4E-952BD9FF07A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscalewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleWebhook.md
ms.openlocfilehash: 8b94ad5728e7852bb3cd834e7479a29cc11c1698
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500592"
---
# <span data-ttu-id="5fff4-101">New-AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="5fff4-101">New-AzureRmAutoscaleWebhook</span></span>

## <span data-ttu-id="5fff4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5fff4-102">SYNOPSIS</span></span>
<span data-ttu-id="5fff4-103">Automatikusan létrehoz egy automéretarányos webkampót.</span><span class="sxs-lookup"><span data-stu-id="5fff4-103">Creates an Autoscale webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5fff4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5fff4-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5fff4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5fff4-105">DESCRIPTION</span></span>
<span data-ttu-id="5fff4-106">A **New-AzureRmAutoscaleWebhook** parancsmag automéretarányos webkampót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="5fff4-106">The **New-AzureRmAutoscaleWebhook** cmdlet creates an Autoscale webhook.</span></span>

## <span data-ttu-id="5fff4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5fff4-107">EXAMPLES</span></span>

## <span data-ttu-id="5fff4-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5fff4-108">PARAMETERS</span></span>

### <span data-ttu-id="5fff4-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fff4-109">-DefaultProfile</span></span>
<span data-ttu-id="5fff4-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5fff4-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fff4-111">-Tulajdonság</span><span class="sxs-lookup"><span data-stu-id="5fff4-111">-Property</span></span>
<span data-ttu-id="5fff4-112">A @ formátum @ (property1 = "érték1",....) tulajdonságainak listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5fff4-112">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Properties

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fff4-113">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="5fff4-113">-ServiceUri</span></span>
<span data-ttu-id="5fff4-114">A szolgáltatás URI-jét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5fff4-114">Specifies the service URI.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fff4-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fff4-115">CommonParameters</span></span>
<span data-ttu-id="5fff4-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5fff4-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fff4-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fff4-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fff4-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5fff4-118">INPUTS</span></span>

### <span data-ttu-id="5fff4-119">Nincs</span><span class="sxs-lookup"><span data-stu-id="5fff4-119">None</span></span>
<span data-ttu-id="5fff4-120">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="5fff4-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5fff4-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5fff4-121">OUTPUTS</span></span>

### <span data-ttu-id="5fff4-122">Microsoft. Azure. Management. monitor. Management. models. WebhookNotification</span><span class="sxs-lookup"><span data-stu-id="5fff4-122">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification</span></span>

## <span data-ttu-id="5fff4-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5fff4-123">NOTES</span></span>

## <span data-ttu-id="5fff4-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5fff4-124">RELATED LINKS</span></span>

[<span data-ttu-id="5fff4-125">Új – AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="5fff4-125">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


