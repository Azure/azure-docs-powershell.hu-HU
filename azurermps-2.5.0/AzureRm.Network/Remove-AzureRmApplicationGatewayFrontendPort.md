---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A698954A-994E-45AD-BA36-1E03196CFCB0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayfrontendport
schema: 2.0.0
ms.openlocfilehash: ecee205ee831c5ba7a2fa78c00f005af3303a13a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848761"
---
# <span data-ttu-id="e48da-101">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="e48da-101">Remove-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="e48da-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e48da-102">SYNOPSIS</span></span>
<span data-ttu-id="e48da-103">Eltávolítja az előtér-portot egy alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="e48da-103">Removes a front-end port from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e48da-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e48da-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayFrontendPort -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e48da-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e48da-105">DESCRIPTION</span></span>
<span data-ttu-id="e48da-106">A **Remove-AzureRmApplicationGatewayFrontendPort** parancsmag eltávolítja az előtér-portot egy Azure Application Gateway-ből.</span><span class="sxs-lookup"><span data-stu-id="e48da-106">The **Remove-AzureRmApplicationGatewayFrontendPort** cmdlet removes a front-end port from an Azure application gateway.</span></span>

## <span data-ttu-id="e48da-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e48da-107">EXAMPLES</span></span>

### <span data-ttu-id="e48da-108">Példa: az előtér-port eltávolítása egy alkalmazás-átjáróról</span><span class="sxs-lookup"><span data-stu-id="e48da-108">Example: Remove a front-end port from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort02"
```

<span data-ttu-id="e48da-109">Az első parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, amely a ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és az átjárót az $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e48da-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores the gateway in $AppGw variable.</span></span>

<span data-ttu-id="e48da-110">A második parancs eltávolítja a FrontEndPort02 nevű portot az Application Gateway-ből.</span><span class="sxs-lookup"><span data-stu-id="e48da-110">The second command removes the port named FrontEndPort02 from the application gateway.</span></span>

## <span data-ttu-id="e48da-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e48da-111">PARAMETERS</span></span>

### <span data-ttu-id="e48da-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e48da-112">-ApplicationGateway</span></span>
<span data-ttu-id="e48da-113">Annak az alkalmazásnak az átjáróját adja meg, amelyből el szeretné távolítani az előtér-portot.</span><span class="sxs-lookup"><span data-stu-id="e48da-113">Specifies the application gateway from which to remove a front-end port.</span></span>

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

### <span data-ttu-id="e48da-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e48da-114">-DefaultProfile</span></span>
<span data-ttu-id="e48da-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e48da-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e48da-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e48da-116">-Name</span></span>
<span data-ttu-id="e48da-117">Az eltávolítandó frontend-port nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e48da-117">Specifies name of the frontend port to remove.</span></span>

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

### <span data-ttu-id="e48da-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e48da-118">CommonParameters</span></span>
<span data-ttu-id="e48da-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e48da-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e48da-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e48da-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e48da-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e48da-121">INPUTS</span></span>

### <span data-ttu-id="e48da-122">System. String</span><span class="sxs-lookup"><span data-stu-id="e48da-122">System.String</span></span>

## <span data-ttu-id="e48da-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e48da-123">OUTPUTS</span></span>

### <span data-ttu-id="e48da-124">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e48da-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e48da-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e48da-125">NOTES</span></span>

## <span data-ttu-id="e48da-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e48da-126">RELATED LINKS</span></span>

[<span data-ttu-id="e48da-127">Add-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="e48da-127">Add-AzureRmApplicationGatewayFrontendPort</span></span>](./Add-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="e48da-128">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="e48da-128">Get-AzureRmApplicationGatewayFrontendPort</span></span>](./Get-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="e48da-129">Új – AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="e48da-129">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="e48da-130">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="e48da-130">Set-AzureRmApplicationGatewayFrontendPort</span></span>](./Set-AzureRmApplicationGatewayFrontendPort.md)


