---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9D9D079C-5557-40DC-8CFB-1DCD446D9109
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 821f31ba8f42ff8a7b94839aad344a2f144353d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501760"
---
# <span data-ttu-id="351bc-101">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="351bc-101">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="351bc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="351bc-102">SYNOPSIS</span></span>
<span data-ttu-id="351bc-103">URL-elérésiút-megfeleltetések tömbjét egészíti ki a backend-kiszolgálók készletéből.</span><span class="sxs-lookup"><span data-stu-id="351bc-103">Adds an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="351bc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="351bc-104">SYNTAX</span></span>

### <span data-ttu-id="351bc-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="351bc-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="351bc-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="351bc-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="351bc-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="351bc-107">DESCRIPTION</span></span>
<span data-ttu-id="351bc-108">Az **Add-AzureRmApplicationGatewayUrlPathMapConfig** parancsmag egy URL-elérési út típusú megfeleltetést ad vissza egy back end Server-készlethez.</span><span class="sxs-lookup"><span data-stu-id="351bc-108">The **Add-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet adds an array of URL path mappings to a back end server pool.</span></span>

## <span data-ttu-id="351bc-109">Példák</span><span class="sxs-lookup"><span data-stu-id="351bc-109">EXAMPLES</span></span>

## <span data-ttu-id="351bc-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="351bc-110">PARAMETERS</span></span>

### <span data-ttu-id="351bc-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="351bc-111">-ApplicationGateway</span></span>
<span data-ttu-id="351bc-112">Annak az alkalmazásnak az átjáróját adja meg, amelyre a parancsmag URL-elérésiút-megfeleltetést ad.</span><span class="sxs-lookup"><span data-stu-id="351bc-112">Specifies the application gateway to which this cmdlet adds a URL path map configuration.</span></span>

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

### <span data-ttu-id="351bc-113">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="351bc-113">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="351bc-114">Az alapértelmezett backend-címkészletet adja meg az átirányításhoz, ha a *pathRules* paraméterben megadott szabályok egyike sem egyezik meg.</span><span class="sxs-lookup"><span data-stu-id="351bc-114">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="351bc-115">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="351bc-115">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="351bc-116">Az alapértelmezett backend-címkészlet AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="351bc-116">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="351bc-117">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="351bc-117">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="351bc-118">Az alapértelmezett backend-HTTP-beállításokat adja meg, ha a *pathRules* paraméterben megadott szabályok egyike sem egyezik meg.</span><span class="sxs-lookup"><span data-stu-id="351bc-118">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="351bc-119">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="351bc-119">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="351bc-120">Az alapértelmezett backend-HTTP-beállítások AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="351bc-120">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="351bc-121">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="351bc-121">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="351bc-122">Az alkalmazás-átjáró alapértelmezett RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="351bc-122">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="351bc-123">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="351bc-123">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="351bc-124">Az alkalmazás-átjáró alapértelmezett RedirectConfiguration azonosítója</span><span class="sxs-lookup"><span data-stu-id="351bc-124">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="351bc-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="351bc-125">-Name</span></span>
<span data-ttu-id="351bc-126">Itt adhatja meg az URL-cím elérési útjának nevét, amelyet a parancsmag a backend Server-készlethez ad.</span><span class="sxs-lookup"><span data-stu-id="351bc-126">Specifies the URL path map name that this cmdlet adds to the backend server pool.</span></span>

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

### <span data-ttu-id="351bc-127">-PathRules</span><span class="sxs-lookup"><span data-stu-id="351bc-127">-PathRules</span></span>
<span data-ttu-id="351bc-128">Az elérésiút-szabályok listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="351bc-128">Specifies a list of path rules.</span></span>
<span data-ttu-id="351bc-129">Az elérésiút-szabályok a megkülönböztetett sorrendet használják, ezek a sorrendjük szerint vannak alkalmazva.</span><span class="sxs-lookup"><span data-stu-id="351bc-129">The path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="351bc-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="351bc-130">-DefaultProfile</span></span>
<span data-ttu-id="351bc-131">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="351bc-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="351bc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="351bc-132">CommonParameters</span></span>
<span data-ttu-id="351bc-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="351bc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="351bc-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="351bc-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="351bc-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="351bc-135">INPUTS</span></span>

### <span data-ttu-id="351bc-136">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="351bc-136">PSApplicationGateway</span></span>
<span data-ttu-id="351bc-137">A ' ApplicationGateway ' paraméter az "PSApplicationGateway" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="351bc-137">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="351bc-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="351bc-138">OUTPUTS</span></span>

### <span data-ttu-id="351bc-139">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="351bc-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="351bc-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="351bc-140">NOTES</span></span>

## <span data-ttu-id="351bc-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="351bc-141">RELATED LINKS</span></span>

[<span data-ttu-id="351bc-142">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="351bc-142">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="351bc-143">Új – AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="351bc-143">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="351bc-144">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="351bc-144">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="351bc-145">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="351bc-145">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)

