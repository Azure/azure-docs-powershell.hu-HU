---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: da6acfddcee30861b73145d7d8e66871de02568d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011348"
---
# <span data-ttu-id="f4276-101">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f4276-101">Set-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="f4276-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f4276-102">SYNOPSIS</span></span>
<span data-ttu-id="f4276-103">A meglévő alkalmazás-átjárók átirányítási konfigurációjának beállítása.</span><span class="sxs-lookup"><span data-stu-id="f4276-103">Sets the redirect configuration on an existing Application Gateway.</span></span>

## <span data-ttu-id="f4276-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f4276-104">SYNTAX</span></span>

### <span data-ttu-id="f4276-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f4276-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4276-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f4276-106">SetByResource</span></span>
```
Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4276-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="f4276-107">SetByURL</span></span>
```
Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4276-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f4276-108">DESCRIPTION</span></span>
<span data-ttu-id="f4276-109">**A set-AzApplicationGatewayRequestRoutingRule** parancsmag módosította az átirányítási konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="f4276-109">**The Set-AzApplicationGatewayRequestRoutingRule** cmdlet modifies a redirect configuration.</span></span>

## <span data-ttu-id="f4276-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f4276-110">EXAMPLES</span></span>

### <span data-ttu-id="f4276-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f4276-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw =  Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $appgw -Name "RedirectConfig01" -RedirectType Permanent -TargetUrl "https://www.contoso.com"
```

<span data-ttu-id="f4276-112">Az első parancs a ApplicationGateway01 nevű alkalmazás-átjárót kapja meg, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="f4276-112">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="f4276-113">A második parancs módosítja az alkalmazás átjárójának átirányítási konfigurációját az állandó típus átirányításához, és a cél URL-címet használja.</span><span class="sxs-lookup"><span data-stu-id="f4276-113">The second command modifies the redirect configuration for the application gateway to redirect type Permanent and use a target url.</span></span>

## <span data-ttu-id="f4276-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f4276-114">PARAMETERS</span></span>

### <span data-ttu-id="f4276-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f4276-115">-ApplicationGateway</span></span>
<span data-ttu-id="f4276-116">A applicationGateway</span><span class="sxs-lookup"><span data-stu-id="f4276-116">The applicationGateway</span></span>

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

### <span data-ttu-id="f4276-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4276-117">-DefaultProfile</span></span>
<span data-ttu-id="f4276-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f4276-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4276-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="f4276-119">-IncludePath</span></span>
<span data-ttu-id="f4276-120">Az átirányított URL-címben az elérési út belefoglalása</span><span class="sxs-lookup"><span data-stu-id="f4276-120">Include path in the redirected url.</span></span>
<span data-ttu-id="f4276-121">Az alapértelmezett érték az igaz.</span><span class="sxs-lookup"><span data-stu-id="f4276-121">Default is true.</span></span>

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

### <span data-ttu-id="f4276-122">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="f4276-122">-IncludeQueryString</span></span>
<span data-ttu-id="f4276-123">Lekérdezési karakterlánc szerepeltetése az átirányított URL-címben.</span><span class="sxs-lookup"><span data-stu-id="f4276-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="f4276-124">Az alapértelmezett érték az igaz.</span><span class="sxs-lookup"><span data-stu-id="f4276-124">Default is true.</span></span>

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

### <span data-ttu-id="f4276-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f4276-125">-Name</span></span>
<span data-ttu-id="f4276-126">Az átirányítási konfiguráció neve</span><span class="sxs-lookup"><span data-stu-id="f4276-126">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="f4276-127">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="f4276-127">-RedirectType</span></span>
<span data-ttu-id="f4276-128">Az átirányítás típusa</span><span class="sxs-lookup"><span data-stu-id="f4276-128">The type of redirect</span></span>

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

### <span data-ttu-id="f4276-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="f4276-129">-TargetListener</span></span>
<span data-ttu-id="f4276-130">A HTTP-figyelő a kérés átirányításához</span><span class="sxs-lookup"><span data-stu-id="f4276-130">HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="f4276-131">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="f4276-131">-TargetListenerID</span></span>
<span data-ttu-id="f4276-132">A HTTP-figyelő azonosítója a kérés átirányításához</span><span class="sxs-lookup"><span data-stu-id="f4276-132">ID of HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="f4276-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="f4276-133">-TargetUrl</span></span>
<span data-ttu-id="f4276-134">Cél URL-címe</span><span class="sxs-lookup"><span data-stu-id="f4276-134">Target URL fo redirection</span></span>

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

### <span data-ttu-id="f4276-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4276-135">CommonParameters</span></span>
<span data-ttu-id="f4276-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f4276-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4276-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4276-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4276-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4276-138">INPUTS</span></span>

### <span data-ttu-id="f4276-139">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f4276-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f4276-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4276-140">OUTPUTS</span></span>

### <span data-ttu-id="f4276-141">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f4276-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f4276-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f4276-142">NOTES</span></span>

## <span data-ttu-id="f4276-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f4276-143">RELATED LINKS</span></span>

[<span data-ttu-id="f4276-144">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f4276-144">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="f4276-145">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f4276-145">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="f4276-146">Új – AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f4276-146">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="f4276-147">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f4276-147">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)
