---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F312FD6E-AF0F-4901-B763-741E1B46A654
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 590793e8a2caeb360b88a7d41d91dcea07baacfd
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841373"
---
# <span data-ttu-id="5a01f-101">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5a01f-101">New-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="5a01f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5a01f-102">SYNOPSIS</span></span>
<span data-ttu-id="5a01f-103">URL-elérésiút-megfeleltetések tömbjét hozza létre a backend-kiszolgálók készletéből.</span><span class="sxs-lookup"><span data-stu-id="5a01f-103">Creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="5a01f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5a01f-104">SYNTAX</span></span>

### <span data-ttu-id="5a01f-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5a01f-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a01f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="5a01f-106">SetByResource</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a01f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5a01f-107">DESCRIPTION</span></span>
<span data-ttu-id="5a01f-108">A **New-AzApplicationGatewayUrlPathMapConfig** parancsmag az URL-címek tömbjét hozza létre a backend-kiszolgálók készletéből.</span><span class="sxs-lookup"><span data-stu-id="5a01f-108">The **New-AzApplicationGatewayUrlPathMapConfig** cmdlet creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="5a01f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="5a01f-109">EXAMPLES</span></span>

### <span data-ttu-id="5a01f-110">Példa 1: URL-elérésiút-megfeleltetések tömbje létrehozása egy backend-kiszolgáló készletéből</span><span class="sxs-lookup"><span data-stu-id="5a01f-110">Example 1: Create an array of URL path mappings to a backend server pool</span></span>
```
PS C:\>New-AzApplicationGatewayUrlPathMapConfig -Name $UrlPathMapName -PathRules $VideoPathRule, $ImagePathRule -DefaultBackendAddressPool $Pool -DefaultBackendHttpSettings $PoolSetting02
```

<span data-ttu-id="5a01f-111">Ez a parancs URL-elérésiút-megfeleltetések tömbjét hozza létre a backend-kiszolgálók készletéből.</span><span class="sxs-lookup"><span data-stu-id="5a01f-111">This command creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="5a01f-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5a01f-112">PARAMETERS</span></span>

### <span data-ttu-id="5a01f-113">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="5a01f-113">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="5a01f-114">Az alapértelmezett backend-címkészletet adja meg az átirányításhoz, ha a *pathRules* paraméterben megadott szabályok egyike sem egyezik meg.</span><span class="sxs-lookup"><span data-stu-id="5a01f-114">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="5a01f-115">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="5a01f-115">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="5a01f-116">Az alapértelmezett backend-címkészlet AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5a01f-116">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="5a01f-117">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="5a01f-117">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="5a01f-118">Az alapértelmezett backend-HTTP-beállításokat adja meg, ha a *pathRules* paraméterben megadott szabályok egyike sem egyezik meg.</span><span class="sxs-lookup"><span data-stu-id="5a01f-118">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="5a01f-119">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="5a01f-119">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="5a01f-120">Az alapértelmezett backend-HTTP-beállítások AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5a01f-120">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="5a01f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a01f-121">-DefaultProfile</span></span>
<span data-ttu-id="5a01f-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5a01f-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a01f-123">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="5a01f-123">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="5a01f-124">Az alkalmazás-átjáró alapértelmezett RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="5a01f-124">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="5a01f-125">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="5a01f-125">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="5a01f-126">Az alkalmazás-átjáró alapértelmezett RedirectConfiguration azonosítója</span><span class="sxs-lookup"><span data-stu-id="5a01f-126">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="5a01f-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5a01f-127">-Name</span></span>
<span data-ttu-id="5a01f-128">Itt adhatja meg a parancsmag által létrehozott URL-elérési út megfeleltetésének nevét.</span><span class="sxs-lookup"><span data-stu-id="5a01f-128">Specifies the URL path map name that this cmdlet creates.</span></span>

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

### <span data-ttu-id="5a01f-129">-PathRules</span><span class="sxs-lookup"><span data-stu-id="5a01f-129">-PathRules</span></span>
<span data-ttu-id="5a01f-130">Az elérésiút-szabályok listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5a01f-130">Specifies a list of path rules.</span></span>
<span data-ttu-id="5a01f-131">Ügyeljen arra, hogy az elérésiút-szabályok a megrendelésük során bizalmasak legyenek, ezeket a program a megadott sorrendben alkalmazza.</span><span class="sxs-lookup"><span data-stu-id="5a01f-131">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="5a01f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a01f-132">CommonParameters</span></span>
<span data-ttu-id="5a01f-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5a01f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a01f-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a01f-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a01f-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a01f-135">INPUTS</span></span>

## <span data-ttu-id="5a01f-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a01f-136">OUTPUTS</span></span>

### <span data-ttu-id="5a01f-137">Microsoft. Azure. commands. Network. models. PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="5a01f-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="5a01f-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5a01f-138">NOTES</span></span>

## <span data-ttu-id="5a01f-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5a01f-139">RELATED LINKS</span></span>

[<span data-ttu-id="5a01f-140">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5a01f-140">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="5a01f-141">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5a01f-141">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="5a01f-142">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5a01f-142">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="5a01f-143">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5a01f-143">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


