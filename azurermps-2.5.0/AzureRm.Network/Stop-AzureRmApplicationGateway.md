---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C9609E8-0D8B-471B-9F0E-672BF55C3A0E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/stop-azurermapplicationgateway
schema: 2.0.0
ms.openlocfilehash: 74b8664a9b57089fd116620779354515ea984c79
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848686"
---
# <span data-ttu-id="a183b-101">Stop-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a183b-101">Stop-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="a183b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a183b-102">SYNOPSIS</span></span>
<span data-ttu-id="a183b-103">Az alkalmazás-átjáró leállítása</span><span class="sxs-lookup"><span data-stu-id="a183b-103">Stops an application gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a183b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a183b-104">SYNTAX</span></span>

```
Stop-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a183b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a183b-105">DESCRIPTION</span></span>
<span data-ttu-id="a183b-106">A **stop-AzureRmApplicationGateway** parancsmag leállítja az alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="a183b-106">The **Stop-AzureRmApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="a183b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a183b-107">EXAMPLES</span></span>

### <span data-ttu-id="a183b-108">1. példa: az alkalmazás-átjáró leállítása</span><span class="sxs-lookup"><span data-stu-id="a183b-108">Example 1: Stop an application gateway</span></span>
```
PS C:\>Stop-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="a183b-109">Ez a parancs leállítja a $AppGw változóban tárolt alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="a183b-109">This command stops the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="a183b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a183b-110">PARAMETERS</span></span>

### <span data-ttu-id="a183b-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a183b-111">-ApplicationGateway</span></span>
<span data-ttu-id="a183b-112">Annak az alkalmazásnak az átjáróját adja meg, amely a parancsmag leáll.</span><span class="sxs-lookup"><span data-stu-id="a183b-112">Specifies the application gateway that this cmdlet stops.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a183b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a183b-113">-AsJob</span></span>
<span data-ttu-id="a183b-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a183b-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a183b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a183b-115">-DefaultProfile</span></span>
<span data-ttu-id="a183b-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a183b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a183b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a183b-117">CommonParameters</span></span>
<span data-ttu-id="a183b-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a183b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a183b-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a183b-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a183b-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a183b-120">INPUTS</span></span>

### <span data-ttu-id="a183b-121">System. String</span><span class="sxs-lookup"><span data-stu-id="a183b-121">System.String</span></span>

## <span data-ttu-id="a183b-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a183b-122">OUTPUTS</span></span>

### <span data-ttu-id="a183b-123">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a183b-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a183b-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a183b-124">NOTES</span></span>

## <span data-ttu-id="a183b-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a183b-125">RELATED LINKS</span></span>

[<span data-ttu-id="a183b-126">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a183b-126">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="a183b-127">Új – AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a183b-127">New-AzureRmApplicationGateway</span></span>](./New-AzureRmApplicationGateway.md)

[<span data-ttu-id="a183b-128">Remove-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a183b-128">Remove-AzureRmApplicationGateway</span></span>](./Remove-AzureRmApplicationGateway.md)

[<span data-ttu-id="a183b-129">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a183b-129">Set-AzureRmApplicationGateway</span></span>](./Set-AzureRmApplicationGateway.md)

[<span data-ttu-id="a183b-130">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a183b-130">Start-AzureRmApplicationGateway</span></span>](./Start-AzureRmApplicationGateway.md)


