---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 85C0A1C3-FC6D-496A-B6B5-8DC2A73B8032
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayFrontendPort.md
ms.openlocfilehash: 1c6a5ffee2f4a8b358f483fee2904fe1a7a970da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492457"
---
# <span data-ttu-id="a0253-101">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="a0253-101">Set-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="a0253-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a0253-102">SYNOPSIS</span></span>
<span data-ttu-id="a0253-103">Az alkalmazás-átjáró előtér-portjának módosítása.</span><span class="sxs-lookup"><span data-stu-id="a0253-103">Modifies a front-end port for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0253-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a0253-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0253-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a0253-105">DESCRIPTION</span></span>
<span data-ttu-id="a0253-106">A **set-AzureRmApplicationGatewayFrontendPort** parancsmag az alkalmazás-átjárók előtér-portját módosítja.</span><span class="sxs-lookup"><span data-stu-id="a0253-106">The **Set-AzureRmApplicationGatewayFrontendPort** cmdlet modifies a front-end port for an application gateway.</span></span>

## <span data-ttu-id="a0253-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a0253-107">EXAMPLES</span></span>

### <span data-ttu-id="a0253-108">1. példa: az alkalmazás-átjáró előtér-Port beállítása az 80-hoz</span><span class="sxs-lookup"><span data-stu-id="a0253-108">Example 1: Set an application gateway front-end port to 80</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="a0253-109">Az első parancs megkapja a ApplicationGateway01 nevű alkalmazás-átjárót, amely a ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a0253-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="a0253-110">A második parancs módosítja az átjárót a $AppGw-ban, hogy a 80-ös portot használja a FrontEndPort01 nevű előtér-porthoz.</span><span class="sxs-lookup"><span data-stu-id="a0253-110">The second command modifies the gateway in $AppGw to use port 80 for the front-end port named FrontEndPort01.</span></span>

## <span data-ttu-id="a0253-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a0253-111">PARAMETERS</span></span>

### <span data-ttu-id="a0253-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a0253-112">-ApplicationGateway</span></span>
<span data-ttu-id="a0253-113">Azt az Application Gateway-objektumot adja meg, amelyhez a parancsmag az előtér-portot társítja.</span><span class="sxs-lookup"><span data-stu-id="a0253-113">Specifies the application gateway object with which this cmdlet associates the front-end port.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0253-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a0253-114">-Name</span></span>
<span data-ttu-id="a0253-115">A módosítani kívánt előtér-végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a0253-115">Specifies the name of the front-end port to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0253-116">-Port</span><span class="sxs-lookup"><span data-stu-id="a0253-116">-Port</span></span>
<span data-ttu-id="a0253-117">Az előtér-porthoz használni kívánt portszámot adja meg.</span><span class="sxs-lookup"><span data-stu-id="a0253-117">Specifies the port number to use for the front-end port.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0253-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0253-118">-DefaultProfile</span></span>
<span data-ttu-id="a0253-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a0253-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0253-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0253-120">CommonParameters</span></span>
<span data-ttu-id="a0253-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a0253-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0253-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0253-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0253-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0253-123">INPUTS</span></span>

### <span data-ttu-id="a0253-124">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a0253-124">PSApplicationGateway</span></span>
<span data-ttu-id="a0253-125">A ' ApplicationGateway ' paraméter az "PSApplicationGateway" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="a0253-125">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="a0253-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0253-126">OUTPUTS</span></span>

### <span data-ttu-id="a0253-127">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a0253-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a0253-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a0253-128">NOTES</span></span>

## <span data-ttu-id="a0253-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a0253-129">RELATED LINKS</span></span>

[<span data-ttu-id="a0253-130">Add-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="a0253-130">Add-AzureRmApplicationGatewayFrontendPort</span></span>](./Add-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="a0253-131">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="a0253-131">Get-AzureRmApplicationGatewayFrontendPort</span></span>](./Get-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="a0253-132">Új – AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="a0253-132">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="a0253-133">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="a0253-133">Remove-AzureRmApplicationGatewayFrontendPort</span></span>](./Remove-AzureRmApplicationGatewayFrontendPort.md)
