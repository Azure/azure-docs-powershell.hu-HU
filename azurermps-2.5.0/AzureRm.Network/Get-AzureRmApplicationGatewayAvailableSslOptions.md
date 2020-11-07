---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayavailablessloptions
schema: 2.0.0
ms.openlocfilehash: 023b2a43114fe47b50956e7f4626a75706e914f5
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849253"
---
# <span data-ttu-id="5e62b-101">Get-AzureRmApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="5e62b-101">Get-AzureRmApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="5e62b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5e62b-102">SYNOPSIS</span></span>
<span data-ttu-id="5e62b-103">Az összes elérhető SSL-beállítás beolvasása az alkalmazás-átjáró SSL-házirendjében.</span><span class="sxs-lookup"><span data-stu-id="5e62b-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e62b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5e62b-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAvailableSslOptions [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5e62b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5e62b-105">DESCRIPTION</span></span>
<span data-ttu-id="5e62b-106">A **Get-AzureRmApplicationGatewayAvailableSslOptions** parancsmag az SSL-házirend minden elérhető SSL-beállítását megkapja</span><span class="sxs-lookup"><span data-stu-id="5e62b-106">The **Get-AzureRmApplicationGatewayAvailableSslOptions** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="5e62b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5e62b-107">EXAMPLES</span></span>

### <span data-ttu-id="5e62b-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5e62b-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzureRmApplicationGatewayAvailableSslOptions
```

<span data-ttu-id="5e62b-109">Ez a parancs az SSL-házirend minden elérhető SSL-beállítását visszaállítja.</span><span class="sxs-lookup"><span data-stu-id="5e62b-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="5e62b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5e62b-110">PARAMETERS</span></span>

### <span data-ttu-id="5e62b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e62b-111">-DefaultProfile</span></span>
<span data-ttu-id="5e62b-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5e62b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e62b-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e62b-113">CommonParameters</span></span>
<span data-ttu-id="5e62b-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5e62b-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e62b-115">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e62b-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e62b-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5e62b-116">INPUTS</span></span>

### <span data-ttu-id="5e62b-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="5e62b-117">None</span></span>

## <span data-ttu-id="5e62b-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5e62b-118">OUTPUTS</span></span>

### <span data-ttu-id="5e62b-119">Microsoft. Azure. commands. Network. models. PSApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="5e62b-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="5e62b-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5e62b-120">NOTES</span></span>

## <span data-ttu-id="5e62b-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5e62b-121">RELATED LINKS</span></span>

