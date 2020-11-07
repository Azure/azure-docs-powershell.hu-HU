---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F5EC8E7-12E9-40E5-B98D-AAFD8F9F3C37
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 5eb4fb0f036331fe68755a3a8ebddcd7e1b6e424
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843658"
---
# <span data-ttu-id="d0f59-101">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d0f59-101">Set-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="d0f59-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d0f59-102">SYNOPSIS</span></span>
<span data-ttu-id="d0f59-103">URL-elérésiút-megfeleltetések konfigurációját állítja be a backend-kiszolgálók készletéből.</span><span class="sxs-lookup"><span data-stu-id="d0f59-103">Sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="d0f59-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d0f59-104">SYNTAX</span></span>

### <span data-ttu-id="d0f59-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d0f59-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0f59-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d0f59-106">SetByResource</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0f59-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d0f59-107">DESCRIPTION</span></span>
<span data-ttu-id="d0f59-108">A **set-AzApplicationGatewayUrlPathMapConfig** parancsmag a backend-kiszolgálók készletéből URL-elérési utakhoz való megfeleltetések konfigurációját állítja be.</span><span class="sxs-lookup"><span data-stu-id="d0f59-108">The **Set-AzApplicationGatewayUrlPathMapConfig** cmdlet sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="d0f59-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d0f59-109">EXAMPLES</span></span>

### <span data-ttu-id="d0f59-110">1:</span><span class="sxs-lookup"><span data-stu-id="d0f59-110">1:</span></span>
```

```

## <span data-ttu-id="d0f59-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d0f59-111">PARAMETERS</span></span>

### <span data-ttu-id="d0f59-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d0f59-112">-ApplicationGateway</span></span>
<span data-ttu-id="d0f59-113">Annak az alkalmazásnak az átjáróját adja meg, amelyre a parancsmag az URL-elérési út megfeleltetését állítja be.</span><span class="sxs-lookup"><span data-stu-id="d0f59-113">Specifies the application gateway to which this cmdlet sets a URL path map configuration.</span></span>

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

### <span data-ttu-id="d0f59-114">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d0f59-114">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="d0f59-115">Az alapértelmezett backend-címkészletet adja meg az átirányításhoz, ha a *pathRules* paraméterben megadott szabályok egyike sem egyezik meg.</span><span class="sxs-lookup"><span data-stu-id="d0f59-115">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="d0f59-116">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="d0f59-116">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="d0f59-117">Az alapértelmezett backend-címkészlet AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d0f59-117">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="d0f59-118">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="d0f59-118">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="d0f59-119">Az alapértelmezett backend-HTTP-beállításokat adja meg, ha a *pathRules* paraméterben megadott szabályok egyike sem egyezik meg.</span><span class="sxs-lookup"><span data-stu-id="d0f59-119">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="d0f59-120">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="d0f59-120">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="d0f59-121">Az alapértelmezett backend-HTTP-beállítások AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d0f59-121">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="d0f59-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0f59-122">-DefaultProfile</span></span>
<span data-ttu-id="d0f59-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d0f59-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0f59-124">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="d0f59-124">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="d0f59-125">Az alkalmazás-átjáró alapértelmezett RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="d0f59-125">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="d0f59-126">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="d0f59-126">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="d0f59-127">Az alkalmazás-átjáró alapértelmezett RedirectConfiguration azonosítója</span><span class="sxs-lookup"><span data-stu-id="d0f59-127">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="d0f59-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d0f59-128">-Name</span></span>
<span data-ttu-id="d0f59-129">Annak az URL-elérési útvonalnak a nevét adja meg, amelyben a parancsmag beállítja a konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="d0f59-129">Specifies the URL path map name in which this cmdlet sets configuration for.</span></span>

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

### <span data-ttu-id="d0f59-130">-PathRules</span><span class="sxs-lookup"><span data-stu-id="d0f59-130">-PathRules</span></span>
<span data-ttu-id="d0f59-131">Az elérésiút-szabályok listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d0f59-131">Specifies a list of path rules.</span></span>
<span data-ttu-id="d0f59-132">Ügyeljen arra, hogy az elérésiút-szabályok a megrendelésük során bizalmasak legyenek, ezeket a program a megadott sorrendben alkalmazza.</span><span class="sxs-lookup"><span data-stu-id="d0f59-132">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="d0f59-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0f59-133">CommonParameters</span></span>
<span data-ttu-id="d0f59-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d0f59-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0f59-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0f59-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0f59-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d0f59-136">INPUTS</span></span>

### <span data-ttu-id="d0f59-137">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d0f59-137">PSApplicationGateway</span></span>
<span data-ttu-id="d0f59-138">A ' ApplicationGateway ' paraméter az "PSApplicationGateway" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="d0f59-138">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="d0f59-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d0f59-139">OUTPUTS</span></span>

### <span data-ttu-id="d0f59-140">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d0f59-140">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d0f59-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d0f59-141">NOTES</span></span>

## <span data-ttu-id="d0f59-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d0f59-142">RELATED LINKS</span></span>

[<span data-ttu-id="d0f59-143">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d0f59-143">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="d0f59-144">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d0f59-144">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="d0f59-145">Új – AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d0f59-145">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="d0f59-146">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d0f59-146">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)


