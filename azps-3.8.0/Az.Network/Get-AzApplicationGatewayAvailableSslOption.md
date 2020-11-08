---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailablessloption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
ms.openlocfilehash: f2175583aaaf3af04120e22e32db79d7b20f1e30
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013583"
---
# <span data-ttu-id="5eaf3-101">Get-AzApplicationGatewayAvailableSslOption</span><span class="sxs-lookup"><span data-stu-id="5eaf3-101">Get-AzApplicationGatewayAvailableSslOption</span></span>

## <span data-ttu-id="5eaf3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5eaf3-102">SYNOPSIS</span></span>
<span data-ttu-id="5eaf3-103">Az összes elérhető SSL-beállítás beolvasása az alkalmazás-átjáró SSL-házirendjében.</span><span class="sxs-lookup"><span data-stu-id="5eaf3-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

## <span data-ttu-id="5eaf3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5eaf3-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableSslOption [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5eaf3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5eaf3-105">DESCRIPTION</span></span>
<span data-ttu-id="5eaf3-106">A **Get-AzApplicationGatewayAvailableSslOption** parancsmag az SSL-házirend minden elérhető SSL-beállítását megkapja</span><span class="sxs-lookup"><span data-stu-id="5eaf3-106">The **Get-AzApplicationGatewayAvailableSslOption** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="5eaf3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5eaf3-107">EXAMPLES</span></span>

### <span data-ttu-id="5eaf3-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5eaf3-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzApplicationGatewayAvailableSslOption
```

<span data-ttu-id="5eaf3-109">Ez a parancs az SSL-házirend minden elérhető SSL-beállítását visszaállítja.</span><span class="sxs-lookup"><span data-stu-id="5eaf3-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="5eaf3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5eaf3-110">PARAMETERS</span></span>

### <span data-ttu-id="5eaf3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5eaf3-111">-DefaultProfile</span></span>
<span data-ttu-id="5eaf3-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5eaf3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5eaf3-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5eaf3-113">CommonParameters</span></span>
<span data-ttu-id="5eaf3-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5eaf3-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5eaf3-115">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5eaf3-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5eaf3-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5eaf3-116">INPUTS</span></span>

### <span data-ttu-id="5eaf3-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="5eaf3-117">None</span></span>

## <span data-ttu-id="5eaf3-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5eaf3-118">OUTPUTS</span></span>

### <span data-ttu-id="5eaf3-119">Microsoft. Azure. commands. Network. models. PSApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="5eaf3-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="5eaf3-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5eaf3-120">NOTES</span></span>

## <span data-ttu-id="5eaf3-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5eaf3-121">RELATED LINKS</span></span>
