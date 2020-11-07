---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 75A4826A-7A5F-4742-9DC4-DC728CED63D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: c2c212d3cf80044ce7c81d9d4ebd318f6a1e93ad
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843677"
---
# <span data-ttu-id="3e9d4-101">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="3e9d4-101">Set-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="3e9d4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3e9d4-102">SYNOPSIS</span></span>
<span data-ttu-id="3e9d4-103">Módosítja a kérések útválasztási szabályát egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="3e9d4-103">Modifies a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="3e9d4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3e9d4-104">SYNTAX</span></span>

### <span data-ttu-id="3e9d4-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3e9d4-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e9d4-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="3e9d4-106">SetByResource</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e9d4-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3e9d4-107">DESCRIPTION</span></span>
<span data-ttu-id="3e9d4-108">A **set-AzApplicationGatewayRequestRoutingRule** parancsmag módosítja a kérések útválasztási szabályát.</span><span class="sxs-lookup"><span data-stu-id="3e9d4-108">The **Set-AzApplicationGatewayRequestRoutingRule** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="3e9d4-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3e9d4-109">EXAMPLES</span></span>

### <span data-ttu-id="3e9d4-110">Példa 1: a Request útválasztási szabály frissítése</span><span class="sxs-lookup"><span data-stu-id="3e9d4-110">Example 1: Update a request routing rule</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="3e9d4-111">Az első parancs a ApplicationGateway01 nevű alkalmazás-átjárót kapja meg, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="3e9d4-111">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="3e9d4-112">A második parancs módosítja az alkalmazás átjárójának Request (útválasztási) szabályát a $Setting változóban megadott, a $Listener változóban megadott HTTP-figyelők, valamint a $Pool változóban megadott, a végpontokat tartalmazó címkészlet használatára.</span><span class="sxs-lookup"><span data-stu-id="3e9d4-112">The second command modifies the request routing rule for the application gateway to use back-end HTTP settings specified in the $Setting variable, an HTTP listener specified in the $Listener variable, and a back-end address pool specified in the $Pool variable.</span></span>

## <span data-ttu-id="3e9d4-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3e9d4-113">PARAMETERS</span></span>

### <span data-ttu-id="3e9d4-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3e9d4-114">-ApplicationGateway</span></span>
<span data-ttu-id="3e9d4-115">Azt az alkalmazásobjektum-objektumot adja meg, amelyhez ez a parancsmag a kérések útválasztási szabályát társítja.</span><span class="sxs-lookup"><span data-stu-id="3e9d4-115">Specifies the application gateway object with which this cmdlet associates a request routing rule.</span></span>

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

### <span data-ttu-id="3e9d4-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3e9d4-116">-BackendAddressPool</span></span>
<span data-ttu-id="3e9d4-117">Az Application Gateway back-end címkészletet adja meg.</span><span class="sxs-lookup"><span data-stu-id="3e9d4-117">Specifies the application gateway back-end address pool.</span></span>

```yaml
Type: PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e9d4-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="3e9d4-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="3e9d4-119">Az Application Gateway back-end Address Pool AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="3e9d4-119">Specifies the application gateway back-end address pool ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e9d4-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="3e9d4-120">-BackendHttpSettings</span></span>
<span data-ttu-id="3e9d4-121">Az Application Gateway backend HTTP-beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="3e9d4-121">Specifies the application gateway backend HTTP settings.</span></span>

```yaml
Type: PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e9d4-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="3e9d4-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="3e9d4-123">Az Application Gateway back-end HTTP-beállításai AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="3e9d4-123">Specifies the application gateway back-end HTTP settings ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e9d4-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e9d4-124">-DefaultProfile</span></span>
<span data-ttu-id="3e9d4-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3e9d4-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e9d4-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="3e9d4-126">-HttpListener</span></span>
<span data-ttu-id="3e9d4-127">Az Application Gateway HTTP-figyelőt adja meg.</span><span class="sxs-lookup"><span data-stu-id="3e9d4-127">Specifies the application gateway HTTP listener.</span></span>

```yaml
Type: PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e9d4-128">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="3e9d4-128">-HttpListenerId</span></span>
<span data-ttu-id="3e9d4-129">Az alkalmazás-átjáró HTTP-figyelő AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="3e9d4-129">Specifies the application gateway HTTP listener ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e9d4-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3e9d4-130">-Name</span></span>
<span data-ttu-id="3e9d4-131">Annak a kérési művelettervi szabálynak a neve, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="3e9d4-131">Specifies the name of the request routing rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="3e9d4-132">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="3e9d4-132">-RedirectConfiguration</span></span>
<span data-ttu-id="3e9d4-133">Az Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="3e9d4-133">Application gateway RedirectConfiguration</span></span>

```yaml
Type: PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e9d4-134">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="3e9d4-134">-RedirectConfigurationId</span></span>
<span data-ttu-id="3e9d4-135">Az alkalmazás-átjáró RedirectConfiguration azonosítója</span><span class="sxs-lookup"><span data-stu-id="3e9d4-135">ID of the application gateway RedirectConfiguration</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e9d4-136">-RuleType</span><span class="sxs-lookup"><span data-stu-id="3e9d4-136">-RuleType</span></span>
<span data-ttu-id="3e9d4-137">A Request útválasztási szabály típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3e9d4-137">Specifies the type of request routing rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, PathBasedRouting

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e9d4-138">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="3e9d4-138">-UrlPathMap</span></span>
```yaml
Type: PSApplicationGatewayUrlPathMap
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e9d4-139">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="3e9d4-139">-UrlPathMapId</span></span>
```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e9d4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e9d4-140">CommonParameters</span></span>
<span data-ttu-id="3e9d4-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3e9d4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e9d4-142">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e9d4-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e9d4-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e9d4-143">INPUTS</span></span>

### <span data-ttu-id="3e9d4-144">System. String</span><span class="sxs-lookup"><span data-stu-id="3e9d4-144">System.String</span></span>

## <span data-ttu-id="3e9d4-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e9d4-145">OUTPUTS</span></span>

### <span data-ttu-id="3e9d4-146">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3e9d4-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3e9d4-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3e9d4-147">NOTES</span></span>

## <span data-ttu-id="3e9d4-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3e9d4-148">RELATED LINKS</span></span>

[<span data-ttu-id="3e9d4-149">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="3e9d4-149">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="3e9d4-150">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="3e9d4-150">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="3e9d4-151">Új – AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="3e9d4-151">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="3e9d4-152">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="3e9d4-152">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)


