---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 23b27fc0b8b2a8d55a2af91d808b846e4de324a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672700"
---
# <span data-ttu-id="63ec8-101">Set-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="63ec8-101">Set-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="63ec8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="63ec8-102">SYNOPSIS</span></span>
<span data-ttu-id="63ec8-103">A meglévő alkalmazás-átjárók átirányítási konfigurációjának beállítása.</span><span class="sxs-lookup"><span data-stu-id="63ec8-103">Sets the redirect configuration on an existing Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63ec8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="63ec8-104">SYNTAX</span></span>

### <span data-ttu-id="63ec8-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="63ec8-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63ec8-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="63ec8-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63ec8-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="63ec8-107">SetByURL</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63ec8-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="63ec8-108">DESCRIPTION</span></span>
<span data-ttu-id="63ec8-109">**A set-AzureRmApplicationGatewayRequestRoutingRule** parancsmag módosította az átirányítási konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="63ec8-109">**The Set-AzureRmApplicationGatewayRequestRoutingRule** cmdlet modifies a redirect configuration.</span></span>

## <span data-ttu-id="63ec8-110">Példák</span><span class="sxs-lookup"><span data-stu-id="63ec8-110">EXAMPLES</span></span>

### <span data-ttu-id="63ec8-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="63ec8-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw =  Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $appgw -Name "RedirectConfig01" -RedirectType Permanent -TargetUrl "https://www.contoso.com"
```

<span data-ttu-id="63ec8-112">Az első parancs a ApplicationGateway01 nevű alkalmazás-átjárót kapja meg, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="63ec8-112">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="63ec8-113">A második parancs módosítja az alkalmazás átjárójának átirányítási konfigurációját az állandó típus átirányításához, és a cél URL-címet használja.</span><span class="sxs-lookup"><span data-stu-id="63ec8-113">The second command modifies the redirect configuration for the application gateway to redirect type Permanent and use a target url.</span></span>

## <span data-ttu-id="63ec8-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="63ec8-114">PARAMETERS</span></span>

### <span data-ttu-id="63ec8-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="63ec8-115">-ApplicationGateway</span></span>
<span data-ttu-id="63ec8-116">A applicationGateway</span><span class="sxs-lookup"><span data-stu-id="63ec8-116">The applicationGateway</span></span>

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

### <span data-ttu-id="63ec8-117">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="63ec8-117">-IncludePath</span></span>
<span data-ttu-id="63ec8-118">Az átirányított URL-címben az elérési út belefoglalása</span><span class="sxs-lookup"><span data-stu-id="63ec8-118">Include path in the redirected url.</span></span>
<span data-ttu-id="63ec8-119">Az alapértelmezett érték az igaz.</span><span class="sxs-lookup"><span data-stu-id="63ec8-119">Default is true.</span></span>

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

### <span data-ttu-id="63ec8-120">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="63ec8-120">-IncludeQueryString</span></span>
<span data-ttu-id="63ec8-121">Lekérdezési karakterlánc szerepeltetése az átirányított URL-címben.</span><span class="sxs-lookup"><span data-stu-id="63ec8-121">Include query string in the redirected url.</span></span>
<span data-ttu-id="63ec8-122">Az alapértelmezett érték az igaz.</span><span class="sxs-lookup"><span data-stu-id="63ec8-122">Default is true.</span></span>

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

### <span data-ttu-id="63ec8-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="63ec8-123">-Name</span></span>
<span data-ttu-id="63ec8-124">Az átirányítási konfiguráció neve</span><span class="sxs-lookup"><span data-stu-id="63ec8-124">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="63ec8-125">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="63ec8-125">-RedirectType</span></span>
<span data-ttu-id="63ec8-126">Az átirányítás típusa</span><span class="sxs-lookup"><span data-stu-id="63ec8-126">The type of redirect</span></span>

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

### <span data-ttu-id="63ec8-127">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="63ec8-127">-TargetListener</span></span>
<span data-ttu-id="63ec8-128">HTTPListener a kérés átirányításához</span><span class="sxs-lookup"><span data-stu-id="63ec8-128">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="63ec8-129">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="63ec8-129">-TargetListenerID</span></span>
<span data-ttu-id="63ec8-130">A figyelő azonosítója a kérés átirányításához</span><span class="sxs-lookup"><span data-stu-id="63ec8-130">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="63ec8-131">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="63ec8-131">-TargetUrl</span></span>
<span data-ttu-id="63ec8-132">Cél URL-címe</span><span class="sxs-lookup"><span data-stu-id="63ec8-132">Target URL fo redirection</span></span>

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

### <span data-ttu-id="63ec8-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63ec8-133">-DefaultProfile</span></span>
<span data-ttu-id="63ec8-134">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="63ec8-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63ec8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63ec8-135">CommonParameters</span></span>
<span data-ttu-id="63ec8-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="63ec8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63ec8-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63ec8-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63ec8-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="63ec8-138">INPUTS</span></span>

### <span data-ttu-id="63ec8-139">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="63ec8-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="63ec8-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="63ec8-140">OUTPUTS</span></span>

### <span data-ttu-id="63ec8-141">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="63ec8-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="63ec8-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="63ec8-142">NOTES</span></span>

## <span data-ttu-id="63ec8-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="63ec8-143">RELATED LINKS</span></span>

