---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayavailablewafrulesets
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAvailableWafRuleSets.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAvailableWafRuleSets.md
ms.openlocfilehash: d5e65b90c818102f2cb61997f0e5ff08640d6395
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493650"
---
# <span data-ttu-id="37510-101">Get-AzureRmApplicationGatewayAvailableWafRuleSets</span><span class="sxs-lookup"><span data-stu-id="37510-101">Get-AzureRmApplicationGatewayAvailableWafRuleSets</span></span>

## <span data-ttu-id="37510-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="37510-102">SYNOPSIS</span></span>
<span data-ttu-id="37510-103">Bekapcsolja az összes elérhető webalkalmazási tűzfalszabály-készletet.</span><span class="sxs-lookup"><span data-stu-id="37510-103">Gets all available web application firewall rule sets.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37510-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="37510-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAvailableWafRuleSets [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="37510-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="37510-105">DESCRIPTION</span></span>
<span data-ttu-id="37510-106">A **Get-AzureRmApplicationGatewayAvailableWafRuleSets** parancsmag minden elérhető webalkalmazási tűzfalszabály-készletet kap.</span><span class="sxs-lookup"><span data-stu-id="37510-106">The **Get-AzureRmApplicationGatewayAvailableWafRuleSets** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="37510-107">Példák</span><span class="sxs-lookup"><span data-stu-id="37510-107">EXAMPLES</span></span>

### <span data-ttu-id="37510-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="37510-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzureRmApplicationGatewayAvailableWafRuleSets
```

<span data-ttu-id="37510-109">Ez a parancs az összes elérhető webalkalmazási tűzfalszabály-készletet visszaállítja.</span><span class="sxs-lookup"><span data-stu-id="37510-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="37510-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="37510-110">PARAMETERS</span></span>

### <span data-ttu-id="37510-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37510-111">-DefaultProfile</span></span>
<span data-ttu-id="37510-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="37510-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37510-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37510-113">CommonParameters</span></span>
<span data-ttu-id="37510-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="37510-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37510-115">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37510-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37510-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="37510-116">INPUTS</span></span>

### <span data-ttu-id="37510-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="37510-117">None</span></span>

## <span data-ttu-id="37510-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="37510-118">OUTPUTS</span></span>

### <span data-ttu-id="37510-119">Microsoft. Azure. commands. Network. models. PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="37510-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="37510-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="37510-120">NOTES</span></span>
<span data-ttu-id="37510-121">**Lista – a AzureRmApplicationGatewayAvailableWafRuleSets** a **Get-AzureRmApplicationGatewayAvailableWafRuleSets** parancsmag aliasa.</span><span class="sxs-lookup"><span data-stu-id="37510-121">**List-AzureRmApplicationGatewayAvailableWafRuleSets** is an alias for the **Get-AzureRmApplicationGatewayAvailableWafRuleSets** cmdlet.</span></span>

## <span data-ttu-id="37510-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="37510-122">RELATED LINKS</span></span>
