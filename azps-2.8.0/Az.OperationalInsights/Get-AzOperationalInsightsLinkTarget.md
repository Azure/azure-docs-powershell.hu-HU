---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 35C6E85B-E5E1-44E8-86E8-F18E197F69DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightslinktarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkTarget.md
ms.openlocfilehash: beb4fad10424a94b2623070508ac827ea7b15306
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93847778"
---
# <span data-ttu-id="fe73d-101">Get-AzOperationalInsightsLinkTarget</span><span class="sxs-lookup"><span data-stu-id="fe73d-101">Get-AzOperationalInsightsLinkTarget</span></span>

## <span data-ttu-id="fe73d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fe73d-102">SYNOPSIS</span></span>
<span data-ttu-id="fe73d-103">Olyan fiókokat kap, amelyek nincs előfizetéshez társítva.</span><span class="sxs-lookup"><span data-stu-id="fe73d-103">Gets accounts that are not associated with a subscription.</span></span>

## <span data-ttu-id="fe73d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fe73d-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkTarget [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe73d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fe73d-105">DESCRIPTION</span></span>
<span data-ttu-id="fe73d-106">A **Get-AzOperationalInsightsLinkTarget** parancsmag felsorolja azokat a meglévő fiókokat, amelyek nincsenek Azure-előfizetéshez társítva.</span><span class="sxs-lookup"><span data-stu-id="fe73d-106">The **Get-AzOperationalInsightsLinkTarget** cmdlet lists existing accounts that are not associated with an Azure subscription.</span></span>
<span data-ttu-id="fe73d-107">Ha új munkaterületet szeretne egy meglévő fiókhoz csatolni, használja a művelet által visszaadott ügyfél-azonosítót egy új munkaterület ügyfél-azonosító tulajdonságában.</span><span class="sxs-lookup"><span data-stu-id="fe73d-107">To link a new workspace to an existing account, use a customer ID returned by this operation in the customer ID property of a new workspace.</span></span>

## <span data-ttu-id="fe73d-108">Példák</span><span class="sxs-lookup"><span data-stu-id="fe73d-108">EXAMPLES</span></span>

### <span data-ttu-id="fe73d-109">Példa 1: leválasztott fiókok lekérése</span><span class="sxs-lookup"><span data-stu-id="fe73d-109">Example 1: Get unlinked accounts</span></span>
```
PS C:\>Get-AzOperationalInsightsLinkTarget
```

<span data-ttu-id="fe73d-110">Ez a parancs a hívó azonosítója által birtokolt leválasztott fiókokat kapja.</span><span class="sxs-lookup"><span data-stu-id="fe73d-110">This command gets unlinked accounts that are owned by the caller's ID.</span></span>

## <span data-ttu-id="fe73d-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fe73d-111">PARAMETERS</span></span>

### <span data-ttu-id="fe73d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe73d-112">-DefaultProfile</span></span>
<span data-ttu-id="fe73d-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fe73d-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fe73d-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe73d-114">CommonParameters</span></span>
<span data-ttu-id="fe73d-115">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fe73d-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe73d-116">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe73d-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe73d-117">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe73d-117">INPUTS</span></span>

### <span data-ttu-id="fe73d-118">Nincs</span><span class="sxs-lookup"><span data-stu-id="fe73d-118">None</span></span>

## <span data-ttu-id="fe73d-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe73d-119">OUTPUTS</span></span>

### <span data-ttu-id="fe73d-120">Microsoft. Azure. Command. OperationalInsights. models. PSAccount</span><span class="sxs-lookup"><span data-stu-id="fe73d-120">Microsoft.Azure.Commands.OperationalInsights.Models.PSAccount</span></span>

## <span data-ttu-id="fe73d-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fe73d-121">NOTES</span></span>

## <span data-ttu-id="fe73d-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fe73d-122">RELATED LINKS</span></span>

[<span data-ttu-id="fe73d-123">Azure hadműveleti parancsmagok</span><span class="sxs-lookup"><span data-stu-id="fe73d-123">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

