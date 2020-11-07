---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9D9D079C-5557-40DC-8CFB-1DCD446D9109
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: eedf03e2468be36fadc519fc2e6b931c82433fc0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841846"
---
# <span data-ttu-id="4efcc-101">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4efcc-101">Add-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="4efcc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4efcc-102">SYNOPSIS</span></span>
<span data-ttu-id="4efcc-103">URL-elérésiút-megfeleltetések tömbjét egészíti ki a backend-kiszolgálók készletéből.</span><span class="sxs-lookup"><span data-stu-id="4efcc-103">Adds an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="4efcc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4efcc-104">SYNTAX</span></span>

### <span data-ttu-id="4efcc-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4efcc-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4efcc-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="4efcc-106">SetByResource</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4efcc-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4efcc-107">DESCRIPTION</span></span>
<span data-ttu-id="4efcc-108">Az **Add-AzApplicationGatewayUrlPathMapConfig** parancsmag egy URL-elérési út típusú megfeleltetést ad vissza egy back end Server-készlethez.</span><span class="sxs-lookup"><span data-stu-id="4efcc-108">The **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet adds an array of URL path mappings to a back end server pool.</span></span>

## <span data-ttu-id="4efcc-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4efcc-109">EXAMPLES</span></span>

### <span data-ttu-id="4efcc-110">1:</span><span class="sxs-lookup"><span data-stu-id="4efcc-110">1:</span></span>
```

```

## <span data-ttu-id="4efcc-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4efcc-111">PARAMETERS</span></span>

### <span data-ttu-id="4efcc-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4efcc-112">-ApplicationGateway</span></span>
<span data-ttu-id="4efcc-113">Annak az alkalmazásnak az átjáróját adja meg, amelyre a parancsmag URL-elérésiút-megfeleltetést ad.</span><span class="sxs-lookup"><span data-stu-id="4efcc-113">Specifies the application gateway to which this cmdlet adds a URL path map configuration.</span></span>

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

### <span data-ttu-id="4efcc-114">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4efcc-114">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="4efcc-115">Az alapértelmezett backend-címkészletet adja meg az átirányításhoz, ha a *pathRules* paraméterben megadott szabályok egyike sem egyezik meg.</span><span class="sxs-lookup"><span data-stu-id="4efcc-115">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="4efcc-116">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="4efcc-116">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="4efcc-117">Az alapértelmezett backend-címkészlet AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4efcc-117">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="4efcc-118">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="4efcc-118">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="4efcc-119">Az alapértelmezett backend-HTTP-beállításokat adja meg, ha a *pathRules* paraméterben megadott szabályok egyike sem egyezik meg.</span><span class="sxs-lookup"><span data-stu-id="4efcc-119">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="4efcc-120">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="4efcc-120">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="4efcc-121">Az alapértelmezett backend-HTTP-beállítások AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4efcc-121">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="4efcc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4efcc-122">-DefaultProfile</span></span>
<span data-ttu-id="4efcc-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4efcc-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4efcc-124">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="4efcc-124">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="4efcc-125">Az alkalmazás-átjáró alapértelmezett RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="4efcc-125">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="4efcc-126">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="4efcc-126">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="4efcc-127">Az alkalmazás-átjáró alapértelmezett RedirectConfiguration azonosítója</span><span class="sxs-lookup"><span data-stu-id="4efcc-127">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="4efcc-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4efcc-128">-Name</span></span>
<span data-ttu-id="4efcc-129">Itt adhatja meg az URL-cím elérési útjának nevét, amelyet a parancsmag a backend Server-készlethez ad.</span><span class="sxs-lookup"><span data-stu-id="4efcc-129">Specifies the URL path map name that this cmdlet adds to the backend server pool.</span></span>

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

### <span data-ttu-id="4efcc-130">-PathRules</span><span class="sxs-lookup"><span data-stu-id="4efcc-130">-PathRules</span></span>
<span data-ttu-id="4efcc-131">Az elérésiút-szabályok listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4efcc-131">Specifies a list of path rules.</span></span>
<span data-ttu-id="4efcc-132">Az elérésiút-szabályok a megkülönböztetett sorrendet használják, ezek a sorrendjük szerint vannak alkalmazva.</span><span class="sxs-lookup"><span data-stu-id="4efcc-132">The path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="4efcc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4efcc-133">CommonParameters</span></span>
<span data-ttu-id="4efcc-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4efcc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4efcc-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4efcc-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4efcc-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4efcc-136">INPUTS</span></span>

### <span data-ttu-id="4efcc-137">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4efcc-137">PSApplicationGateway</span></span>
<span data-ttu-id="4efcc-138">A ' ApplicationGateway ' paraméter az "PSApplicationGateway" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="4efcc-138">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="4efcc-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4efcc-139">OUTPUTS</span></span>

### <span data-ttu-id="4efcc-140">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4efcc-140">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4efcc-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4efcc-141">NOTES</span></span>

## <span data-ttu-id="4efcc-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4efcc-142">RELATED LINKS</span></span>

[<span data-ttu-id="4efcc-143">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4efcc-143">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="4efcc-144">Új – AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4efcc-144">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="4efcc-145">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4efcc-145">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="4efcc-146">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4efcc-146">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


