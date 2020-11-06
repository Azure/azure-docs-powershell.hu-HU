---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C9609E8-0D8B-471B-9F0E-672BF55C3A0E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/stop-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmApplicationGateway.md
ms.openlocfilehash: cf8a639b6ebbe2b5ea7c0e07f212de3c742e7556
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496383"
---
# <span data-ttu-id="3233c-101">Stop-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3233c-101">Stop-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="3233c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3233c-102">SYNOPSIS</span></span>
<span data-ttu-id="3233c-103">Az alkalmazás-átjáró leállítása</span><span class="sxs-lookup"><span data-stu-id="3233c-103">Stops an application gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3233c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3233c-104">SYNTAX</span></span>

```
Stop-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3233c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3233c-105">DESCRIPTION</span></span>
<span data-ttu-id="3233c-106">A **stop-AzureRmApplicationGateway** parancsmag leállítja az alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="3233c-106">The **Stop-AzureRmApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="3233c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3233c-107">EXAMPLES</span></span>

### <span data-ttu-id="3233c-108">1. példa: az alkalmazás-átjáró leállítása</span><span class="sxs-lookup"><span data-stu-id="3233c-108">Example 1: Stop an application gateway</span></span>
```
PS C:\>Stop-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="3233c-109">Ez a parancs leállítja a $AppGw változóban tárolt alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="3233c-109">This command stops the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="3233c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3233c-110">PARAMETERS</span></span>

### <span data-ttu-id="3233c-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3233c-111">-ApplicationGateway</span></span>
<span data-ttu-id="3233c-112">Annak az alkalmazásnak az átjáróját adja meg, amely a parancsmag leáll.</span><span class="sxs-lookup"><span data-stu-id="3233c-112">Specifies the application gateway that this cmdlet stops.</span></span>

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

### <span data-ttu-id="3233c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3233c-113">-AsJob</span></span>
<span data-ttu-id="3233c-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="3233c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3233c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3233c-115">-DefaultProfile</span></span>
<span data-ttu-id="3233c-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3233c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3233c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3233c-117">CommonParameters</span></span>
<span data-ttu-id="3233c-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3233c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3233c-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3233c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3233c-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3233c-120">INPUTS</span></span>

### <span data-ttu-id="3233c-121">System. String</span><span class="sxs-lookup"><span data-stu-id="3233c-121">System.String</span></span>

## <span data-ttu-id="3233c-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3233c-122">OUTPUTS</span></span>

### <span data-ttu-id="3233c-123">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3233c-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3233c-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3233c-124">NOTES</span></span>

## <span data-ttu-id="3233c-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3233c-125">RELATED LINKS</span></span>

[<span data-ttu-id="3233c-126">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3233c-126">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="3233c-127">Új – AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3233c-127">New-AzureRmApplicationGateway</span></span>](./New-AzureRmApplicationGateway.md)

[<span data-ttu-id="3233c-128">Remove-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3233c-128">Remove-AzureRmApplicationGateway</span></span>](./Remove-AzureRmApplicationGateway.md)

[<span data-ttu-id="3233c-129">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3233c-129">Set-AzureRmApplicationGateway</span></span>](./Set-AzureRmApplicationGateway.md)

[<span data-ttu-id="3233c-130">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3233c-130">Start-AzureRmApplicationGateway</span></span>](./Start-AzureRmApplicationGateway.md)


