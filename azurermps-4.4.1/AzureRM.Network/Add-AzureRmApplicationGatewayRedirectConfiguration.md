---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 449c3999a3041be819b9f5f665054969223c1557
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679761"
---
# <span data-ttu-id="51700-101">Add-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="51700-101">Add-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="51700-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="51700-102">SYNOPSIS</span></span>
<span data-ttu-id="51700-103">Átirányítási konfigurációt ad hozzá egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="51700-103">Adds a redirect configuration to an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51700-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="51700-104">SYNTAX</span></span>

### <span data-ttu-id="51700-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="51700-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51700-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="51700-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51700-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="51700-107">SetByURL</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51700-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="51700-108">DESCRIPTION</span></span>
<span data-ttu-id="51700-109">Az **Add-AzureRmApplicationGatewayRedirectConfiguration** parancsmag átirányítási konfigurációt ad az alkalmazás-átjárónak.</span><span class="sxs-lookup"><span data-stu-id="51700-109">The **Add-AzureRmApplicationGatewayRedirectConfiguration** cmdlet adds a redirect configuration to an Application Gateway.</span></span>

## <span data-ttu-id="51700-110">Példák</span><span class="sxs-lookup"><span data-stu-id="51700-110">EXAMPLES</span></span>

### <span data-ttu-id="51700-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="51700-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$Appgw = Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="51700-112">Az első parancs beolvassa az Application Gatewayt, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="51700-112">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="51700-113">A második parancs hozzáadja az átirányítási konfigurációt az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="51700-113">The second command adds the redirect configuration to the application gateway.</span></span>

## <span data-ttu-id="51700-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="51700-114">PARAMETERS</span></span>

### <span data-ttu-id="51700-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="51700-115">-ApplicationGateway</span></span>
<span data-ttu-id="51700-116">A applicationGateway</span><span class="sxs-lookup"><span data-stu-id="51700-116">The applicationGateway</span></span>

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

### <span data-ttu-id="51700-117">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="51700-117">-IncludePath</span></span>
<span data-ttu-id="51700-118">Az átirányított URL-címben az elérési út belefoglalása</span><span class="sxs-lookup"><span data-stu-id="51700-118">Include path in the redirected url.</span></span>
<span data-ttu-id="51700-119">Az alapértelmezett érték az igaz.</span><span class="sxs-lookup"><span data-stu-id="51700-119">Default is true.</span></span>

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

### <span data-ttu-id="51700-120">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="51700-120">-IncludeQueryString</span></span>
<span data-ttu-id="51700-121">Lekérdezési karakterlánc szerepeltetése az átirányított URL-címben.</span><span class="sxs-lookup"><span data-stu-id="51700-121">Include query string in the redirected url.</span></span>
<span data-ttu-id="51700-122">Az alapértelmezett érték az igaz.</span><span class="sxs-lookup"><span data-stu-id="51700-122">Default is true.</span></span>

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

### <span data-ttu-id="51700-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="51700-123">-Name</span></span>
<span data-ttu-id="51700-124">Az átirányítási konfiguráció neve</span><span class="sxs-lookup"><span data-stu-id="51700-124">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="51700-125">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="51700-125">-RedirectType</span></span>
<span data-ttu-id="51700-126">Az átirányítás típusa</span><span class="sxs-lookup"><span data-stu-id="51700-126">The type of redirect</span></span>

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

### <span data-ttu-id="51700-127">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="51700-127">-TargetListener</span></span>
<span data-ttu-id="51700-128">HTTPListener a kérés átirányításához</span><span class="sxs-lookup"><span data-stu-id="51700-128">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="51700-129">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="51700-129">-TargetListenerID</span></span>
<span data-ttu-id="51700-130">A figyelő azonosítója a kérés átirányításához</span><span class="sxs-lookup"><span data-stu-id="51700-130">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="51700-131">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="51700-131">-TargetUrl</span></span>
<span data-ttu-id="51700-132">Cél URL-címe</span><span class="sxs-lookup"><span data-stu-id="51700-132">Target URL fo redirection</span></span>

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

### <span data-ttu-id="51700-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51700-133">-DefaultProfile</span></span>
<span data-ttu-id="51700-134">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="51700-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51700-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51700-135">CommonParameters</span></span>
<span data-ttu-id="51700-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="51700-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51700-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51700-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51700-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="51700-138">INPUTS</span></span>

### <span data-ttu-id="51700-139">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="51700-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="51700-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="51700-140">OUTPUTS</span></span>

### <span data-ttu-id="51700-141">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="51700-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="51700-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="51700-142">NOTES</span></span>

## <span data-ttu-id="51700-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="51700-143">RELATED LINKS</span></span>

