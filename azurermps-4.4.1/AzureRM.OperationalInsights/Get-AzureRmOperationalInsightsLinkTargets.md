---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 35C6E85B-E5E1-44E8-86E8-F18E197F69DC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsLinkTargets.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsLinkTargets.md
ms.openlocfilehash: 3f0418a06b11af933cfc7ad09a2c0fc492db4f24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501696"
---
# <span data-ttu-id="a14ce-101">Get-AzureRmOperationalInsightsLinkTargets</span><span class="sxs-lookup"><span data-stu-id="a14ce-101">Get-AzureRmOperationalInsightsLinkTargets</span></span>

## <span data-ttu-id="a14ce-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a14ce-102">SYNOPSIS</span></span>
<span data-ttu-id="a14ce-103">Olyan fiókokat kap, amelyek nincs előfizetéshez társítva.</span><span class="sxs-lookup"><span data-stu-id="a14ce-103">Gets accounts that are not associated with a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a14ce-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a14ce-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsLinkTargets [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a14ce-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a14ce-105">DESCRIPTION</span></span>
<span data-ttu-id="a14ce-106">A **Get-AzureRmOperationalInsightsLinkTargets** parancsmag felsorolja azokat a meglévő fiókokat, amelyek nincsenek Azure-előfizetéshez társítva.</span><span class="sxs-lookup"><span data-stu-id="a14ce-106">The **Get-AzureRmOperationalInsightsLinkTargets** cmdlet lists existing accounts that are not associated with an Azure subscription.</span></span>
<span data-ttu-id="a14ce-107">Ha új munkaterületet szeretne egy meglévő fiókhoz csatolni, használja a művelet által visszaadott ügyfél-azonosítót egy új munkaterület ügyfél-azonosító tulajdonságában.</span><span class="sxs-lookup"><span data-stu-id="a14ce-107">To link a new workspace to an existing account, use a customer ID returned by this operation in the customer ID property of a new workspace.</span></span>

## <span data-ttu-id="a14ce-108">Példák</span><span class="sxs-lookup"><span data-stu-id="a14ce-108">EXAMPLES</span></span>

### <span data-ttu-id="a14ce-109">Példa 1: leválasztott fiókok lekérése</span><span class="sxs-lookup"><span data-stu-id="a14ce-109">Example 1: Get unlinked accounts</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsLinkTargets
```

<span data-ttu-id="a14ce-110">Ez a parancs a hívó azonosítója által birtokolt leválasztott fiókokat kapja.</span><span class="sxs-lookup"><span data-stu-id="a14ce-110">This command gets unlinked accounts that are owned by the caller's ID.</span></span>

## <span data-ttu-id="a14ce-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a14ce-111">PARAMETERS</span></span>

### <span data-ttu-id="a14ce-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a14ce-112">-DefaultProfile</span></span>
<span data-ttu-id="a14ce-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a14ce-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a14ce-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a14ce-114">CommonParameters</span></span>
<span data-ttu-id="a14ce-115">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a14ce-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a14ce-116">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a14ce-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a14ce-117">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a14ce-117">INPUTS</span></span>

## <span data-ttu-id="a14ce-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a14ce-118">OUTPUTS</span></span>

### <span data-ttu-id="a14ce-119">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. OperationalInsights. models. PSAccount]</span><span class="sxs-lookup"><span data-stu-id="a14ce-119">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSAccount]</span></span>

## <span data-ttu-id="a14ce-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a14ce-120">NOTES</span></span>

## <span data-ttu-id="a14ce-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a14ce-121">RELATED LINKS</span></span>

[<span data-ttu-id="a14ce-122">Azure hadműveleti parancsmagok</span><span class="sxs-lookup"><span data-stu-id="a14ce-122">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


