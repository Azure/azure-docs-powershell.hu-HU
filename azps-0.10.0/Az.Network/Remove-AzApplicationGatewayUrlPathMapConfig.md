---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 51428d44c2fc5ce29259924f71617317b163ac29
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841177"
---
# <span data-ttu-id="e18e2-101">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e18e2-101">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="e18e2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e18e2-102">SYNOPSIS</span></span>
<span data-ttu-id="e18e2-103">Eltávolítja az URL-címek elérési útját a backend-kiszolgálók készletéből.</span><span class="sxs-lookup"><span data-stu-id="e18e2-103">Removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="e18e2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e18e2-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e18e2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e18e2-105">DESCRIPTION</span></span>
<span data-ttu-id="e18e2-106">A **Remove-AzApplicationGatewayUrlPathMapConfig** parancsmag eltávolítja az URL-elérési utakat a backend-kiszolgálók készletéből.</span><span class="sxs-lookup"><span data-stu-id="e18e2-106">The **Remove-AzApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="e18e2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e18e2-107">EXAMPLES</span></span>

### <span data-ttu-id="e18e2-108">1:</span><span class="sxs-lookup"><span data-stu-id="e18e2-108">1:</span></span>
```

```

## <span data-ttu-id="e18e2-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e18e2-109">PARAMETERS</span></span>

### <span data-ttu-id="e18e2-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e18e2-110">-ApplicationGateway</span></span>
<span data-ttu-id="e18e2-111">Annak az alkalmazásnak az átjáróját adja meg, amelyre a parancsmag eltávolítja az URL Path Map-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="e18e2-111">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

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

### <span data-ttu-id="e18e2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e18e2-112">-DefaultProfile</span></span>
<span data-ttu-id="e18e2-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e18e2-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e18e2-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e18e2-114">-Name</span></span>
<span data-ttu-id="e18e2-115">Itt adhatja meg az URL-cím elérési útjának nevét, amelyet a parancsmag a backend-kiszolgálóról távolít el.</span><span class="sxs-lookup"><span data-stu-id="e18e2-115">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e18e2-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e18e2-116">CommonParameters</span></span>
<span data-ttu-id="e18e2-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e18e2-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e18e2-118">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e18e2-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e18e2-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e18e2-119">INPUTS</span></span>

### <span data-ttu-id="e18e2-120">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e18e2-120">PSApplicationGateway</span></span>
<span data-ttu-id="e18e2-121">A ' ApplicationGateway ' paraméter az "PSApplicationGateway" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="e18e2-121">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="e18e2-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e18e2-122">OUTPUTS</span></span>

### <span data-ttu-id="e18e2-123">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e18e2-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e18e2-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e18e2-124">NOTES</span></span>

## <span data-ttu-id="e18e2-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e18e2-125">RELATED LINKS</span></span>

[<span data-ttu-id="e18e2-126">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e18e2-126">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="e18e2-127">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e18e2-127">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="e18e2-128">Új – AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e18e2-128">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="e18e2-129">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e18e2-129">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


