---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9D9D079C-5557-40DC-8CFB-1DCD446D9109
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 321c7272c02b4e5555f731d3a9dbaa7d806c0727
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495964"
---
# <span data-ttu-id="5b4e7-101">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5b4e7-101">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="5b4e7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5b4e7-102">SYNOPSIS</span></span>
<span data-ttu-id="5b4e7-103">URL-elérésiút-megfeleltetések tömbjét egészíti ki a backend-kiszolgálók készletéből.</span><span class="sxs-lookup"><span data-stu-id="5b4e7-103">Adds an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b4e7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5b4e7-104">SYNTAX</span></span>

### <span data-ttu-id="5b4e7-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5b4e7-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b4e7-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="5b4e7-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b4e7-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5b4e7-107">DESCRIPTION</span></span>
<span data-ttu-id="5b4e7-108">Az **Add-AzureRmApplicationGatewayUrlPathMapConfig** parancsmag egy URL-elérési út típusú megfeleltetést ad vissza egy back end Server-készlethez.</span><span class="sxs-lookup"><span data-stu-id="5b4e7-108">The **Add-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet adds an array of URL path mappings to a back end server pool.</span></span>

## <span data-ttu-id="5b4e7-109">Példák</span><span class="sxs-lookup"><span data-stu-id="5b4e7-109">EXAMPLES</span></span>

## <span data-ttu-id="5b4e7-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5b4e7-110">PARAMETERS</span></span>

### <span data-ttu-id="5b4e7-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5b4e7-111">-ApplicationGateway</span></span>
<span data-ttu-id="5b4e7-112">Annak az alkalmazásnak az átjáróját adja meg, amelyre a parancsmag URL-elérésiút-megfeleltetést ad.</span><span class="sxs-lookup"><span data-stu-id="5b4e7-112">Specifies the application gateway to which this cmdlet adds a URL path map configuration.</span></span>

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

### <span data-ttu-id="5b4e7-113">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="5b4e7-113">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="5b4e7-114">Az alapértelmezett backend-címkészletet adja meg az átirányításhoz, ha a *pathRules* paraméterben megadott szabályok egyike sem egyezik meg.</span><span class="sxs-lookup"><span data-stu-id="5b4e7-114">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b4e7-115">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="5b4e7-115">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="5b4e7-116">Az alapértelmezett backend-címkészlet AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5b4e7-116">Specifies the default backend address pool ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b4e7-117">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="5b4e7-117">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="5b4e7-118">Az alapértelmezett backend-HTTP-beállításokat adja meg, ha a *pathRules* paraméterben megadott szabályok egyike sem egyezik meg.</span><span class="sxs-lookup"><span data-stu-id="5b4e7-118">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b4e7-119">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="5b4e7-119">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="5b4e7-120">Az alapértelmezett backend-HTTP-beállítások AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5b4e7-120">Specifies the default backend HTTP settings ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b4e7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b4e7-121">-DefaultProfile</span></span>
<span data-ttu-id="5b4e7-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5b4e7-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b4e7-123">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="5b4e7-123">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="5b4e7-124">Az alkalmazás-átjáró alapértelmezett RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="5b4e7-124">Application gateway default RedirectConfiguration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b4e7-125">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="5b4e7-125">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="5b4e7-126">Az alkalmazás-átjáró alapértelmezett RedirectConfiguration azonosítója</span><span class="sxs-lookup"><span data-stu-id="5b4e7-126">ID of the application gateway default RedirectConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b4e7-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5b4e7-127">-Name</span></span>
<span data-ttu-id="5b4e7-128">Itt adhatja meg az URL-cím elérési útjának nevét, amelyet a parancsmag a backend Server-készlethez ad.</span><span class="sxs-lookup"><span data-stu-id="5b4e7-128">Specifies the URL path map name that this cmdlet adds to the backend server pool.</span></span>

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

### <span data-ttu-id="5b4e7-129">-PathRules</span><span class="sxs-lookup"><span data-stu-id="5b4e7-129">-PathRules</span></span>
<span data-ttu-id="5b4e7-130">Az elérésiút-szabályok listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5b4e7-130">Specifies a list of path rules.</span></span>
<span data-ttu-id="5b4e7-131">Az elérésiút-szabályok a megkülönböztetett sorrendet használják, ezek a sorrendjük szerint vannak alkalmazva.</span><span class="sxs-lookup"><span data-stu-id="5b4e7-131">The path rules are order sensitive, they are applied in order they are specified.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b4e7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b4e7-132">CommonParameters</span></span>
<span data-ttu-id="5b4e7-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5b4e7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b4e7-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b4e7-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b4e7-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b4e7-135">INPUTS</span></span>

### <span data-ttu-id="5b4e7-136">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5b4e7-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="5b4e7-137">Paraméterek: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5b4e7-137">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="5b4e7-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b4e7-138">OUTPUTS</span></span>

### <span data-ttu-id="5b4e7-139">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5b4e7-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5b4e7-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5b4e7-140">NOTES</span></span>

## <span data-ttu-id="5b4e7-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5b4e7-141">RELATED LINKS</span></span>

[<span data-ttu-id="5b4e7-142">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5b4e7-142">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="5b4e7-143">Új – AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5b4e7-143">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="5b4e7-144">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5b4e7-144">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="5b4e7-145">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5b4e7-145">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


