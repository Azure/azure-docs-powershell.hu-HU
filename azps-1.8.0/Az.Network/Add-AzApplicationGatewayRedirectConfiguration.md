---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 6db510e79d2c1796cf62a1fd00e55e7860164af9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670737"
---
# <span data-ttu-id="15c9c-101">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="15c9c-101">Add-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="15c9c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="15c9c-102">SYNOPSIS</span></span>
<span data-ttu-id="15c9c-103">Átirányítási konfigurációt ad hozzá egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="15c9c-103">Adds a redirect configuration to an Application Gateway.</span></span>

## <span data-ttu-id="15c9c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="15c9c-104">SYNTAX</span></span>

### <span data-ttu-id="15c9c-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="15c9c-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15c9c-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="15c9c-106">SetByResource</span></span>
```
Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15c9c-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="15c9c-107">SetByURL</span></span>
```
Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15c9c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="15c9c-108">DESCRIPTION</span></span>
<span data-ttu-id="15c9c-109">Az **Add-AzApplicationGatewayRedirectConfiguration** parancsmag átirányítási konfigurációt ad az alkalmazás-átjárónak.</span><span class="sxs-lookup"><span data-stu-id="15c9c-109">The **Add-AzApplicationGatewayRedirectConfiguration** cmdlet adds a redirect configuration to an Application Gateway.</span></span>

## <span data-ttu-id="15c9c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="15c9c-110">EXAMPLES</span></span>

### <span data-ttu-id="15c9c-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="15c9c-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$Appgw = Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="15c9c-112">Az első parancs beolvassa az Application Gatewayt, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="15c9c-112">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="15c9c-113">A második parancs hozzáadja az átirányítási konfigurációt az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="15c9c-113">The second command adds the redirect configuration to the application gateway.</span></span>

## <span data-ttu-id="15c9c-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="15c9c-114">PARAMETERS</span></span>

### <span data-ttu-id="15c9c-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="15c9c-115">-ApplicationGateway</span></span>
<span data-ttu-id="15c9c-116">A applicationGateway</span><span class="sxs-lookup"><span data-stu-id="15c9c-116">The applicationGateway</span></span>

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

### <span data-ttu-id="15c9c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15c9c-117">-DefaultProfile</span></span>
<span data-ttu-id="15c9c-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="15c9c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15c9c-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="15c9c-119">-IncludePath</span></span>
<span data-ttu-id="15c9c-120">Az átirányított URL-címben az elérési út belefoglalása</span><span class="sxs-lookup"><span data-stu-id="15c9c-120">Include path in the redirected url.</span></span>
<span data-ttu-id="15c9c-121">Az alapértelmezett érték az igaz.</span><span class="sxs-lookup"><span data-stu-id="15c9c-121">Default is true.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15c9c-122">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="15c9c-122">-IncludeQueryString</span></span>
<span data-ttu-id="15c9c-123">Lekérdezési karakterlánc szerepeltetése az átirányított URL-címben.</span><span class="sxs-lookup"><span data-stu-id="15c9c-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="15c9c-124">Az alapértelmezett érték az igaz.</span><span class="sxs-lookup"><span data-stu-id="15c9c-124">Default is true.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15c9c-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="15c9c-125">-Name</span></span>
<span data-ttu-id="15c9c-126">Az átirányítási konfiguráció neve</span><span class="sxs-lookup"><span data-stu-id="15c9c-126">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="15c9c-127">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="15c9c-127">-RedirectType</span></span>
<span data-ttu-id="15c9c-128">Az átirányítás típusa</span><span class="sxs-lookup"><span data-stu-id="15c9c-128">The type of redirect</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Permanent, Found, SeeOther, Temporary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15c9c-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="15c9c-129">-TargetListener</span></span>
<span data-ttu-id="15c9c-130">A HTTP-figyelő a kérés átirányításához</span><span class="sxs-lookup"><span data-stu-id="15c9c-130">HTTP listener to redirect the request to</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15c9c-131">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="15c9c-131">-TargetListenerID</span></span>
<span data-ttu-id="15c9c-132">A HTTP-figyelő azonosítója a kérés átirányításához</span><span class="sxs-lookup"><span data-stu-id="15c9c-132">ID of HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="15c9c-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="15c9c-133">-TargetUrl</span></span>
<span data-ttu-id="15c9c-134">Cél URL-címe</span><span class="sxs-lookup"><span data-stu-id="15c9c-134">Target URL fo redirection</span></span>

```yaml
Type: System.String
Parameter Sets: SetByURL
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15c9c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15c9c-135">CommonParameters</span></span>
<span data-ttu-id="15c9c-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="15c9c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15c9c-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15c9c-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15c9c-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="15c9c-138">INPUTS</span></span>

### <span data-ttu-id="15c9c-139">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="15c9c-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="15c9c-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="15c9c-140">OUTPUTS</span></span>

### <span data-ttu-id="15c9c-141">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="15c9c-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="15c9c-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="15c9c-142">NOTES</span></span>

## <span data-ttu-id="15c9c-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="15c9c-143">RELATED LINKS</span></span>

[<span data-ttu-id="15c9c-144">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="15c9c-144">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="15c9c-145">Új – AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="15c9c-145">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="15c9c-146">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="15c9c-146">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="15c9c-147">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="15c9c-147">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
