---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: b6bfe8b7064324dea353543e0e9debe77e4b2edd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014788"
---
# <span data-ttu-id="91202-101">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="91202-101">New-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="91202-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="91202-102">SYNOPSIS</span></span>
<span data-ttu-id="91202-103">Átirányítási konfigurációt hoz létre az alkalmazás-átjárók számára.</span><span class="sxs-lookup"><span data-stu-id="91202-103">Creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="91202-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="91202-104">SYNTAX</span></span>

### <span data-ttu-id="91202-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="91202-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91202-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="91202-106">SetByResource</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91202-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="91202-107">SetByURL</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String> [-TargetUrl <String>]
 [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="91202-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="91202-108">DESCRIPTION</span></span>
<span data-ttu-id="91202-109">**A New-AzApplicationGatewayRedirectConfiguration** parancsmag átirányítási konfigurációt hoz létre az alkalmazás-átjárók számára.</span><span class="sxs-lookup"><span data-stu-id="91202-109">**The New-AzApplicationGatewayRedirectConfiguration** cmdlet creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="91202-110">Példák</span><span class="sxs-lookup"><span data-stu-id="91202-110">EXAMPLES</span></span>

### <span data-ttu-id="91202-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="91202-111">Example 1</span></span>
```
PS C:\>$RedirectConfig = New-AzApplicationGatewayRedirectConfiguration -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="91202-112">Ez a parancs létrehoz egy Redirect01 nevű átirányítási konfigurációt, és az eredményt az $RedirectConfig nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="91202-112">This command creates a redirect configuration named Redirect01 and stores the result in the variable named $RedirectConfig.</span></span>

## <span data-ttu-id="91202-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="91202-113">PARAMETERS</span></span>

### <span data-ttu-id="91202-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91202-114">-DefaultProfile</span></span>
<span data-ttu-id="91202-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="91202-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91202-116">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="91202-116">-IncludePath</span></span>
<span data-ttu-id="91202-117">Az átirányított URL-címben az elérési út belefoglalása</span><span class="sxs-lookup"><span data-stu-id="91202-117">Include path in the redirected url.</span></span>
<span data-ttu-id="91202-118">Az alapértelmezett érték az igaz.</span><span class="sxs-lookup"><span data-stu-id="91202-118">Default is true.</span></span>

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

### <span data-ttu-id="91202-119">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="91202-119">-IncludeQueryString</span></span>
<span data-ttu-id="91202-120">Lekérdezési karakterlánc szerepeltetése az átirányított URL-címben.</span><span class="sxs-lookup"><span data-stu-id="91202-120">Include query string in the redirected url.</span></span>
<span data-ttu-id="91202-121">Az alapértelmezett érték az igaz.</span><span class="sxs-lookup"><span data-stu-id="91202-121">Default is true.</span></span>

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

### <span data-ttu-id="91202-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="91202-122">-Name</span></span>
<span data-ttu-id="91202-123">Az átirányítási konfiguráció neve</span><span class="sxs-lookup"><span data-stu-id="91202-123">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="91202-124">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="91202-124">-RedirectType</span></span>
<span data-ttu-id="91202-125">Az átirányítás típusa</span><span class="sxs-lookup"><span data-stu-id="91202-125">The type of redirect</span></span>

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

### <span data-ttu-id="91202-126">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="91202-126">-TargetListener</span></span>
<span data-ttu-id="91202-127">A HTTP-figyelő a kérés átirányításához</span><span class="sxs-lookup"><span data-stu-id="91202-127">HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="91202-128">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="91202-128">-TargetListenerID</span></span>
<span data-ttu-id="91202-129">A HTTP-figyelő azonosítója a kérés átirányításához</span><span class="sxs-lookup"><span data-stu-id="91202-129">ID of HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="91202-130">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="91202-130">-TargetUrl</span></span>
<span data-ttu-id="91202-131">Cél URL-címe</span><span class="sxs-lookup"><span data-stu-id="91202-131">Target URL fo redirection</span></span>

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

### <span data-ttu-id="91202-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91202-132">CommonParameters</span></span>
<span data-ttu-id="91202-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="91202-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91202-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91202-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91202-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="91202-135">INPUTS</span></span>

### <span data-ttu-id="91202-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="91202-136">None</span></span>

## <span data-ttu-id="91202-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="91202-137">OUTPUTS</span></span>

### <span data-ttu-id="91202-138">Microsoft. Azure. commands. Network. models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="91202-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="91202-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="91202-139">NOTES</span></span>

## <span data-ttu-id="91202-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="91202-140">RELATED LINKS</span></span>

[<span data-ttu-id="91202-141">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="91202-141">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="91202-142">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="91202-142">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="91202-143">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="91202-143">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="91202-144">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="91202-144">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
