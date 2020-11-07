---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayavailablewafrulesets
schema: 2.0.0
ms.openlocfilehash: 83ee8e673271079690c24691f22badfe5193ba50
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849250"
---
# <span data-ttu-id="06357-101">Get-AzureRmApplicationGatewayAvailableWafRuleSets</span><span class="sxs-lookup"><span data-stu-id="06357-101">Get-AzureRmApplicationGatewayAvailableWafRuleSets</span></span>

## <span data-ttu-id="06357-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="06357-102">SYNOPSIS</span></span>
<span data-ttu-id="06357-103">Bekapcsolja az összes elérhető webalkalmazási tűzfalszabály-készletet.</span><span class="sxs-lookup"><span data-stu-id="06357-103">Gets all available web application firewall rule sets.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06357-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="06357-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAvailableWafRuleSets [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="06357-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="06357-105">DESCRIPTION</span></span>
<span data-ttu-id="06357-106">A **Get-AzureRmApplicationGatewayAvailableWafRuleSets** parancsmag minden elérhető webalkalmazási tűzfalszabály-készletet kap.</span><span class="sxs-lookup"><span data-stu-id="06357-106">The **Get-AzureRmApplicationGatewayAvailableWafRuleSets** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="06357-107">Példák</span><span class="sxs-lookup"><span data-stu-id="06357-107">EXAMPLES</span></span>

### <span data-ttu-id="06357-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="06357-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzureRmApplicationGatewayAvailableWafRuleSets
```

<span data-ttu-id="06357-109">Ez a parancs az összes elérhető webalkalmazási tűzfalszabály-készletet visszaállítja.</span><span class="sxs-lookup"><span data-stu-id="06357-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="06357-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="06357-110">PARAMETERS</span></span>

### <span data-ttu-id="06357-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06357-111">-DefaultProfile</span></span>
<span data-ttu-id="06357-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="06357-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06357-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06357-113">CommonParameters</span></span>
<span data-ttu-id="06357-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="06357-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06357-115">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06357-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06357-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="06357-116">INPUTS</span></span>

### <span data-ttu-id="06357-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="06357-117">None</span></span>

## <span data-ttu-id="06357-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="06357-118">OUTPUTS</span></span>

### <span data-ttu-id="06357-119">Microsoft. Azure. commands. Network. models. PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="06357-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="06357-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="06357-120">NOTES</span></span>
<span data-ttu-id="06357-121">**Lista – a AzureRmApplicationGatewayAvailableWafRuleSets** a **Get-AzureRmApplicationGatewayAvailableWafRuleSets** parancsmag aliasa.</span><span class="sxs-lookup"><span data-stu-id="06357-121">**List-AzureRmApplicationGatewayAvailableWafRuleSets** is an alias for the **Get-AzureRmApplicationGatewayAvailableWafRuleSets** cmdlet.</span></span>

## <span data-ttu-id="06357-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="06357-122">RELATED LINKS</span></span>

