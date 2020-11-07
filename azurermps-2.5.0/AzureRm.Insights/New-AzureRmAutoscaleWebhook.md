---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 674A11E4-36B9-4075-9F4E-952BD9FF07A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscalewebhook
schema: 2.0.0
ms.openlocfilehash: fe6170842bcacf4d7fb0c8e442dc988c03c67e35
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849326"
---
# <span data-ttu-id="13671-101">New-AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="13671-101">New-AzureRmAutoscaleWebhook</span></span>

## <span data-ttu-id="13671-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="13671-102">SYNOPSIS</span></span>
<span data-ttu-id="13671-103">Automatikusan létrehoz egy automéretarányos webkampót.</span><span class="sxs-lookup"><span data-stu-id="13671-103">Creates an Autoscale webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13671-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="13671-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13671-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="13671-105">DESCRIPTION</span></span>
<span data-ttu-id="13671-106">A **New-AzureRmAutoscaleWebhook** parancsmag automéretarányos webkampót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="13671-106">The **New-AzureRmAutoscaleWebhook** cmdlet creates an Autoscale webhook.</span></span>

## <span data-ttu-id="13671-107">Példák</span><span class="sxs-lookup"><span data-stu-id="13671-107">EXAMPLES</span></span>

## <span data-ttu-id="13671-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="13671-108">PARAMETERS</span></span>

### <span data-ttu-id="13671-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13671-109">-DefaultProfile</span></span>
<span data-ttu-id="13671-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="13671-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="13671-111">-Tulajdonság</span><span class="sxs-lookup"><span data-stu-id="13671-111">-Property</span></span>
<span data-ttu-id="13671-112">A @ formátum @ (property1 = "érték1",....) tulajdonságainak listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="13671-112">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="13671-113">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="13671-113">-ServiceUri</span></span>
<span data-ttu-id="13671-114">A szolgáltatás URI-jét adja meg.</span><span class="sxs-lookup"><span data-stu-id="13671-114">Specifies the service URI.</span></span>

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

### <span data-ttu-id="13671-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13671-115">CommonParameters</span></span>
<span data-ttu-id="13671-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="13671-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13671-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13671-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13671-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="13671-118">INPUTS</span></span>

### <span data-ttu-id="13671-119">System. String</span><span class="sxs-lookup"><span data-stu-id="13671-119">System.String</span></span>

### <span data-ttu-id="13671-120">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="13671-120">System.Collections.Hashtable</span></span>

## <span data-ttu-id="13671-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="13671-121">OUTPUTS</span></span>

### <span data-ttu-id="13671-122">Microsoft. Azure. Management. monitor. Management. models. WebhookNotification</span><span class="sxs-lookup"><span data-stu-id="13671-122">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification</span></span>

## <span data-ttu-id="13671-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="13671-123">NOTES</span></span>

## <span data-ttu-id="13671-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="13671-124">RELATED LINKS</span></span>

[<span data-ttu-id="13671-125">Új – AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="13671-125">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


