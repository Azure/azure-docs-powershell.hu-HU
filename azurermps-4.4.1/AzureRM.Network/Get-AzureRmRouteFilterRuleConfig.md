---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: cb8c6fcca5fb64427efc17123320d1e2a8156aa3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497804"
---
# <span data-ttu-id="8cdc6-101">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8cdc6-101">Get-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="8cdc6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8cdc6-102">SYNOPSIS</span></span>
<span data-ttu-id="8cdc6-103">{{Töltse ki a szinopszist}}</span><span class="sxs-lookup"><span data-stu-id="8cdc6-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8cdc6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8cdc6-104">SYNTAX</span></span>

```
Get-AzureRmRouteFilterRuleConfig [-Name <String>] -RouteFilter <PSRouteFilter>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8cdc6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8cdc6-105">DESCRIPTION</span></span>
<span data-ttu-id="8cdc6-106">{{Kitöltendő a Leírás}}</span><span class="sxs-lookup"><span data-stu-id="8cdc6-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="8cdc6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8cdc6-107">EXAMPLES</span></span>

### <span data-ttu-id="8cdc6-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8cdc6-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="8cdc6-109">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="8cdc6-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="8cdc6-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8cdc6-110">PARAMETERS</span></span>

### <span data-ttu-id="8cdc6-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8cdc6-111">-Name</span></span>
<span data-ttu-id="8cdc6-112">Az útvonal-szűrő szabály neve</span><span class="sxs-lookup"><span data-stu-id="8cdc6-112">The name of the route filter rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cdc6-113">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="8cdc6-113">-RouteFilter</span></span>
<span data-ttu-id="8cdc6-114">A RouteFilter</span><span class="sxs-lookup"><span data-stu-id="8cdc6-114">The RouteFilter</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilter
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8cdc6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cdc6-115">-DefaultProfile</span></span>
<span data-ttu-id="8cdc6-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8cdc6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8cdc6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cdc6-117">CommonParameters</span></span>
<span data-ttu-id="8cdc6-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8cdc6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cdc6-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cdc6-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cdc6-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8cdc6-120">INPUTS</span></span>

### <span data-ttu-id="8cdc6-121">Microsoft. Azure. commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8cdc6-121">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="8cdc6-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8cdc6-122">OUTPUTS</span></span>

### <span data-ttu-id="8cdc6-123">Microsoft. Azure. commands. Network. models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="8cdc6-123">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="8cdc6-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8cdc6-124">NOTES</span></span>

## <span data-ttu-id="8cdc6-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8cdc6-125">RELATED LINKS</span></span>

