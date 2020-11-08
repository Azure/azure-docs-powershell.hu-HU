---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 87013db1f8bdff42fd34f28d45d5998d056aab40
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194226"
---
# <span data-ttu-id="574a1-101">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="574a1-101">Set-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="574a1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="574a1-102">SYNOPSIS</span></span>
<span data-ttu-id="574a1-103">A meglévő alkalmazás-átjárók átirányítási konfigurációjának beállítása.</span><span class="sxs-lookup"><span data-stu-id="574a1-103">Sets the redirect configuration on an existing Application Gateway.</span></span>

## <span data-ttu-id="574a1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="574a1-104">SYNTAX</span></span>

### <span data-ttu-id="574a1-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="574a1-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="574a1-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="574a1-106">SetByResource</span></span>
```
Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="574a1-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="574a1-107">SetByURL</span></span>
```
Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="574a1-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="574a1-108">DESCRIPTION</span></span>
<span data-ttu-id="574a1-109">**A set-AzApplicationGatewayRequestRoutingRule** parancsmag módosította az átirányítási konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="574a1-109">**The Set-AzApplicationGatewayRequestRoutingRule** cmdlet modifies a redirect configuration.</span></span>

## <span data-ttu-id="574a1-110">Példák</span><span class="sxs-lookup"><span data-stu-id="574a1-110">EXAMPLES</span></span>

### <span data-ttu-id="574a1-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="574a1-111">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw =  Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $appgw -Name "RedirectConfig01" -RedirectType Permanent -TargetUrl "https://www.contoso.com"
```

<span data-ttu-id="574a1-112">Az első parancs a ApplicationGateway01 nevű alkalmazás-átjárót kapja meg, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="574a1-112">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="574a1-113">A második parancs módosítja az alkalmazás átjárójának átirányítási konfigurációját az állandó típus átirányításához, és a cél URL-címet használja.</span><span class="sxs-lookup"><span data-stu-id="574a1-113">The second command modifies the redirect configuration for the application gateway to redirect type Permanent and use a target url.</span></span>

### <span data-ttu-id="574a1-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="574a1-114">Example 2</span></span>

<span data-ttu-id="574a1-115">A meglévő alkalmazás-átjárók átirányítási konfigurációjának beállítása.</span><span class="sxs-lookup"><span data-stu-id="574a1-115">Sets the redirect configuration on an existing Application Gateway.</span></span> <span data-ttu-id="574a1-116">autogenerated</span><span class="sxs-lookup"><span data-stu-id="574a1-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -IncludePath $false -IncludeQueryString $false -Name 'RedirectConfig01' -RedirectType Permanent -TargetListener <PSApplicationGatewayHttpListener>
```

## <span data-ttu-id="574a1-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="574a1-117">PARAMETERS</span></span>

### <span data-ttu-id="574a1-118">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="574a1-118">-ApplicationGateway</span></span>
<span data-ttu-id="574a1-119">A applicationGateway</span><span class="sxs-lookup"><span data-stu-id="574a1-119">The applicationGateway</span></span>

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

### <span data-ttu-id="574a1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="574a1-120">-DefaultProfile</span></span>
<span data-ttu-id="574a1-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="574a1-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="574a1-122">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="574a1-122">-IncludePath</span></span>
<span data-ttu-id="574a1-123">Az átirányított URL-címben az elérési út belefoglalása</span><span class="sxs-lookup"><span data-stu-id="574a1-123">Include path in the redirected url.</span></span>
<span data-ttu-id="574a1-124">Az alapértelmezett érték az igaz.</span><span class="sxs-lookup"><span data-stu-id="574a1-124">Default is true.</span></span>

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

### <span data-ttu-id="574a1-125">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="574a1-125">-IncludeQueryString</span></span>
<span data-ttu-id="574a1-126">Lekérdezési karakterlánc szerepeltetése az átirányított URL-címben.</span><span class="sxs-lookup"><span data-stu-id="574a1-126">Include query string in the redirected url.</span></span>
<span data-ttu-id="574a1-127">Az alapértelmezett érték az igaz.</span><span class="sxs-lookup"><span data-stu-id="574a1-127">Default is true.</span></span>

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

### <span data-ttu-id="574a1-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="574a1-128">-Name</span></span>
<span data-ttu-id="574a1-129">Az átirányítási konfiguráció neve</span><span class="sxs-lookup"><span data-stu-id="574a1-129">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="574a1-130">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="574a1-130">-RedirectType</span></span>
<span data-ttu-id="574a1-131">Az átirányítás típusa</span><span class="sxs-lookup"><span data-stu-id="574a1-131">The type of redirect</span></span>

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

### <span data-ttu-id="574a1-132">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="574a1-132">-TargetListener</span></span>
<span data-ttu-id="574a1-133">A HTTP-figyelő a kérés átirányításához</span><span class="sxs-lookup"><span data-stu-id="574a1-133">HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="574a1-134">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="574a1-134">-TargetListenerID</span></span>
<span data-ttu-id="574a1-135">A HTTP-figyelő azonosítója a kérés átirányításához</span><span class="sxs-lookup"><span data-stu-id="574a1-135">ID of HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="574a1-136">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="574a1-136">-TargetUrl</span></span>
<span data-ttu-id="574a1-137">Cél URL-címe</span><span class="sxs-lookup"><span data-stu-id="574a1-137">Target URL fo redirection</span></span>

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

### <span data-ttu-id="574a1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="574a1-138">CommonParameters</span></span>
<span data-ttu-id="574a1-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="574a1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="574a1-140">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="574a1-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="574a1-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="574a1-141">INPUTS</span></span>

### <span data-ttu-id="574a1-142">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="574a1-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="574a1-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="574a1-143">OUTPUTS</span></span>

### <span data-ttu-id="574a1-144">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="574a1-144">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="574a1-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="574a1-145">NOTES</span></span>

## <span data-ttu-id="574a1-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="574a1-146">RELATED LINKS</span></span>

[<span data-ttu-id="574a1-147">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="574a1-147">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="574a1-148">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="574a1-148">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="574a1-149">Új – AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="574a1-149">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="574a1-150">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="574a1-150">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)