---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 674A11E4-36B9-4075-9F4E-952BD9FF07A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscalewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleWebhook.md
ms.openlocfilehash: 607976539e6bf93a0fa947741a4af4d4a7d34b67
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672480"
---
# <span data-ttu-id="bc33d-101">New-AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="bc33d-101">New-AzureRmAutoscaleWebhook</span></span>

## <span data-ttu-id="bc33d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bc33d-102">SYNOPSIS</span></span>
<span data-ttu-id="bc33d-103">Automatikusan létrehoz egy automéretarányos webkampót.</span><span class="sxs-lookup"><span data-stu-id="bc33d-103">Creates an Autoscale webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc33d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bc33d-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc33d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bc33d-105">DESCRIPTION</span></span>
<span data-ttu-id="bc33d-106">A **New-AzureRmAutoscaleWebhook** parancsmag automéretarányos webkampót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="bc33d-106">The **New-AzureRmAutoscaleWebhook** cmdlet creates an Autoscale webhook.</span></span>

## <span data-ttu-id="bc33d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bc33d-107">EXAMPLES</span></span>

## <span data-ttu-id="bc33d-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bc33d-108">PARAMETERS</span></span>

### <span data-ttu-id="bc33d-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc33d-109">-DefaultProfile</span></span>
<span data-ttu-id="bc33d-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="bc33d-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bc33d-111">-Tulajdonság</span><span class="sxs-lookup"><span data-stu-id="bc33d-111">-Property</span></span>
<span data-ttu-id="bc33d-112">A @ formátum @ (property1 = "érték1",....) tulajdonságainak listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="bc33d-112">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="bc33d-113">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="bc33d-113">-ServiceUri</span></span>
<span data-ttu-id="bc33d-114">A szolgáltatás URI-jét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bc33d-114">Specifies the service URI.</span></span>

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

### <span data-ttu-id="bc33d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc33d-115">CommonParameters</span></span>
<span data-ttu-id="bc33d-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bc33d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc33d-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc33d-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc33d-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc33d-118">INPUTS</span></span>

### <span data-ttu-id="bc33d-119">System. String</span><span class="sxs-lookup"><span data-stu-id="bc33d-119">System.String</span></span>

### <span data-ttu-id="bc33d-120">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="bc33d-120">System.Collections.Hashtable</span></span>

## <span data-ttu-id="bc33d-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc33d-121">OUTPUTS</span></span>

### <span data-ttu-id="bc33d-122">Microsoft. Azure. Management. monitor. Management. models. WebhookNotification</span><span class="sxs-lookup"><span data-stu-id="bc33d-122">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification</span></span>

## <span data-ttu-id="bc33d-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bc33d-123">NOTES</span></span>

## <span data-ttu-id="bc33d-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bc33d-124">RELATED LINKS</span></span>

[<span data-ttu-id="bc33d-125">Új – AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="bc33d-125">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


