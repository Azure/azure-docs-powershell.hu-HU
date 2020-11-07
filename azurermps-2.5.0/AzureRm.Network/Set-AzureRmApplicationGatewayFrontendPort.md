---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 85C0A1C3-FC6D-496A-B6B5-8DC2A73B8032
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayfrontendport
schema: 2.0.0
ms.openlocfilehash: 83c29e3c059664d7848fe66bd8ad7bcc005a8d47
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850573"
---
# <span data-ttu-id="a5c1f-101">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="a5c1f-101">Set-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="a5c1f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a5c1f-102">SYNOPSIS</span></span>
<span data-ttu-id="a5c1f-103">Az alkalmazás-átjáró előtér-portjának módosítása.</span><span class="sxs-lookup"><span data-stu-id="a5c1f-103">Modifies a front-end port for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5c1f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a5c1f-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5c1f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a5c1f-105">DESCRIPTION</span></span>
<span data-ttu-id="a5c1f-106">A **set-AzureRmApplicationGatewayFrontendPort** parancsmag az alkalmazás-átjárók előtér-portját módosítja.</span><span class="sxs-lookup"><span data-stu-id="a5c1f-106">The **Set-AzureRmApplicationGatewayFrontendPort** cmdlet modifies a front-end port for an application gateway.</span></span>

## <span data-ttu-id="a5c1f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a5c1f-107">EXAMPLES</span></span>

### <span data-ttu-id="a5c1f-108">1. példa: az alkalmazás-átjáró előtér-Port beállítása az 80-hoz</span><span class="sxs-lookup"><span data-stu-id="a5c1f-108">Example 1: Set an application gateway front-end port to 80</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="a5c1f-109">Az első parancs megkapja a ApplicationGateway01 nevű alkalmazás-átjárót, amely a ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a5c1f-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="a5c1f-110">A második parancs módosítja az átjárót a $AppGw-ban, hogy a 80-ös portot használja a FrontEndPort01 nevű előtér-porthoz.</span><span class="sxs-lookup"><span data-stu-id="a5c1f-110">The second command modifies the gateway in $AppGw to use port 80 for the front-end port named FrontEndPort01.</span></span>

## <span data-ttu-id="a5c1f-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a5c1f-111">PARAMETERS</span></span>

### <span data-ttu-id="a5c1f-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a5c1f-112">-ApplicationGateway</span></span>
<span data-ttu-id="a5c1f-113">Azt az Application Gateway-objektumot adja meg, amelyhez a parancsmag az előtér-portot társítja.</span><span class="sxs-lookup"><span data-stu-id="a5c1f-113">Specifies the application gateway object with which this cmdlet associates the front-end port.</span></span>

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

### <span data-ttu-id="a5c1f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5c1f-114">-DefaultProfile</span></span>
<span data-ttu-id="a5c1f-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a5c1f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5c1f-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a5c1f-116">-Name</span></span>
<span data-ttu-id="a5c1f-117">A módosítani kívánt előtér-végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a5c1f-117">Specifies the name of the front-end port to modify.</span></span>

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

### <span data-ttu-id="a5c1f-118">-Port</span><span class="sxs-lookup"><span data-stu-id="a5c1f-118">-Port</span></span>
<span data-ttu-id="a5c1f-119">Az előtér-porthoz használni kívánt portszámot adja meg.</span><span class="sxs-lookup"><span data-stu-id="a5c1f-119">Specifies the port number to use for the front-end port.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5c1f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5c1f-120">CommonParameters</span></span>
<span data-ttu-id="a5c1f-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a5c1f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5c1f-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5c1f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5c1f-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5c1f-123">INPUTS</span></span>

### <span data-ttu-id="a5c1f-124">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a5c1f-124">PSApplicationGateway</span></span>
<span data-ttu-id="a5c1f-125">A ' ApplicationGateway ' paraméter az "PSApplicationGateway" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="a5c1f-125">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="a5c1f-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5c1f-126">OUTPUTS</span></span>

### <span data-ttu-id="a5c1f-127">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a5c1f-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a5c1f-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a5c1f-128">NOTES</span></span>

## <span data-ttu-id="a5c1f-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a5c1f-129">RELATED LINKS</span></span>

[<span data-ttu-id="a5c1f-130">Add-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="a5c1f-130">Add-AzureRmApplicationGatewayFrontendPort</span></span>](./Add-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="a5c1f-131">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="a5c1f-131">Get-AzureRmApplicationGatewayFrontendPort</span></span>](./Get-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="a5c1f-132">Új – AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="a5c1f-132">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="a5c1f-133">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="a5c1f-133">Remove-AzureRmApplicationGatewayFrontendPort</span></span>](./Remove-AzureRmApplicationGatewayFrontendPort.md)
