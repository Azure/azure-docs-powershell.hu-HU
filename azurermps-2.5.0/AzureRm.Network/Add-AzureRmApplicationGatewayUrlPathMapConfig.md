---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9D9D079C-5557-40DC-8CFB-1DCD446D9109
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
ms.openlocfilehash: 1b6e5c2c2a28333e51c74d9621a3fd607f6a652d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849265"
---
# <span data-ttu-id="bf8ab-101">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="bf8ab-101">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="bf8ab-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bf8ab-102">SYNOPSIS</span></span>
<span data-ttu-id="bf8ab-103">URL-elérésiút-megfeleltetések tömbjét egészíti ki a backend-kiszolgálók készletéből.</span><span class="sxs-lookup"><span data-stu-id="bf8ab-103">Adds an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf8ab-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bf8ab-104">SYNTAX</span></span>

### <span data-ttu-id="bf8ab-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="bf8ab-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf8ab-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="bf8ab-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf8ab-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="bf8ab-107">DESCRIPTION</span></span>
<span data-ttu-id="bf8ab-108">Az **Add-AzureRmApplicationGatewayUrlPathMapConfig** parancsmag egy URL-elérési út típusú megfeleltetést ad vissza egy back end Server-készlethez.</span><span class="sxs-lookup"><span data-stu-id="bf8ab-108">The **Add-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet adds an array of URL path mappings to a back end server pool.</span></span>

## <span data-ttu-id="bf8ab-109">Példák</span><span class="sxs-lookup"><span data-stu-id="bf8ab-109">EXAMPLES</span></span>

### <span data-ttu-id="bf8ab-110">1:</span><span class="sxs-lookup"><span data-stu-id="bf8ab-110">1:</span></span>
```

```

## <span data-ttu-id="bf8ab-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bf8ab-111">PARAMETERS</span></span>

### <span data-ttu-id="bf8ab-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bf8ab-112">-ApplicationGateway</span></span>
<span data-ttu-id="bf8ab-113">Annak az alkalmazásnak az átjáróját adja meg, amelyre a parancsmag URL-elérésiút-megfeleltetést ad.</span><span class="sxs-lookup"><span data-stu-id="bf8ab-113">Specifies the application gateway to which this cmdlet adds a URL path map configuration.</span></span>

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

### <span data-ttu-id="bf8ab-114">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="bf8ab-114">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="bf8ab-115">Az alapértelmezett backend-címkészletet adja meg az átirányításhoz, ha a *pathRules* paraméterben megadott szabályok egyike sem egyezik meg.</span><span class="sxs-lookup"><span data-stu-id="bf8ab-115">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="bf8ab-116">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="bf8ab-116">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="bf8ab-117">Az alapértelmezett backend-címkészlet AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="bf8ab-117">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="bf8ab-118">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="bf8ab-118">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="bf8ab-119">Az alapértelmezett backend-HTTP-beállításokat adja meg, ha a *pathRules* paraméterben megadott szabályok egyike sem egyezik meg.</span><span class="sxs-lookup"><span data-stu-id="bf8ab-119">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="bf8ab-120">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="bf8ab-120">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="bf8ab-121">Az alapértelmezett backend-HTTP-beállítások AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="bf8ab-121">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="bf8ab-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf8ab-122">-DefaultProfile</span></span>
<span data-ttu-id="bf8ab-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bf8ab-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf8ab-124">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="bf8ab-124">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="bf8ab-125">Az alkalmazás-átjáró alapértelmezett RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="bf8ab-125">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="bf8ab-126">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="bf8ab-126">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="bf8ab-127">Az alkalmazás-átjáró alapértelmezett RedirectConfiguration azonosítója</span><span class="sxs-lookup"><span data-stu-id="bf8ab-127">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="bf8ab-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bf8ab-128">-Name</span></span>
<span data-ttu-id="bf8ab-129">Itt adhatja meg az URL-cím elérési útjának nevét, amelyet a parancsmag a backend Server-készlethez ad.</span><span class="sxs-lookup"><span data-stu-id="bf8ab-129">Specifies the URL path map name that this cmdlet adds to the backend server pool.</span></span>

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

### <span data-ttu-id="bf8ab-130">-PathRules</span><span class="sxs-lookup"><span data-stu-id="bf8ab-130">-PathRules</span></span>
<span data-ttu-id="bf8ab-131">Az elérésiút-szabályok listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="bf8ab-131">Specifies a list of path rules.</span></span>
<span data-ttu-id="bf8ab-132">Az elérésiút-szabályok a megkülönböztetett sorrendet használják, ezek a sorrendjük szerint vannak alkalmazva.</span><span class="sxs-lookup"><span data-stu-id="bf8ab-132">The path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="bf8ab-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf8ab-133">CommonParameters</span></span>
<span data-ttu-id="bf8ab-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bf8ab-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf8ab-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf8ab-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf8ab-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf8ab-136">INPUTS</span></span>

### <span data-ttu-id="bf8ab-137">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bf8ab-137">PSApplicationGateway</span></span>
<span data-ttu-id="bf8ab-138">A ' ApplicationGateway ' paraméter az "PSApplicationGateway" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="bf8ab-138">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="bf8ab-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf8ab-139">OUTPUTS</span></span>

### <span data-ttu-id="bf8ab-140">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bf8ab-140">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bf8ab-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bf8ab-141">NOTES</span></span>

## <span data-ttu-id="bf8ab-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bf8ab-142">RELATED LINKS</span></span>

[<span data-ttu-id="bf8ab-143">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="bf8ab-143">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="bf8ab-144">Új – AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="bf8ab-144">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="bf8ab-145">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="bf8ab-145">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="bf8ab-146">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="bf8ab-146">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


