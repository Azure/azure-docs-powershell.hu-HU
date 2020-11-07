---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: e768c8f5e557954dd6e932726f38b9844699de9d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670394"
---
# <span data-ttu-id="30946-101">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="30946-101">New-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="30946-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="30946-102">SYNOPSIS</span></span>
<span data-ttu-id="30946-103">Átirányítási konfigurációt hoz létre az alkalmazás-átjárók számára.</span><span class="sxs-lookup"><span data-stu-id="30946-103">Creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="30946-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="30946-104">SYNTAX</span></span>

### <span data-ttu-id="30946-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="30946-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30946-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="30946-106">SetByResource</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30946-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="30946-107">SetByURL</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String> [-TargetUrl <String>]
 [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="30946-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="30946-108">DESCRIPTION</span></span>
<span data-ttu-id="30946-109">**A New-AzApplicationGatewayRedirectConfiguration** parancsmag átirányítási konfigurációt hoz létre az alkalmazás-átjárók számára.</span><span class="sxs-lookup"><span data-stu-id="30946-109">**The New-AzApplicationGatewayRedirectConfiguration** cmdlet creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="30946-110">Példák</span><span class="sxs-lookup"><span data-stu-id="30946-110">EXAMPLES</span></span>

### <span data-ttu-id="30946-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="30946-111">Example 1</span></span>
```
PS C:\>$RedirectConfig = New-AzApplicationGatewayRedirectConfiguration -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="30946-112">Ez a parancs létrehoz egy Redirect01 nevű átirányítási konfigurációt, és az eredményt az $RedirectConfig nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="30946-112">This command creates a redirect configuration named Redirect01 and stores the result in the variable named $RedirectConfig.</span></span>

## <span data-ttu-id="30946-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="30946-113">PARAMETERS</span></span>

### <span data-ttu-id="30946-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30946-114">-DefaultProfile</span></span>
<span data-ttu-id="30946-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="30946-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30946-116">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="30946-116">-IncludePath</span></span>
<span data-ttu-id="30946-117">Az átirányított URL-címben az elérési út belefoglalása</span><span class="sxs-lookup"><span data-stu-id="30946-117">Include path in the redirected url.</span></span>
<span data-ttu-id="30946-118">Az alapértelmezett érték az igaz.</span><span class="sxs-lookup"><span data-stu-id="30946-118">Default is true.</span></span>

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

### <span data-ttu-id="30946-119">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="30946-119">-IncludeQueryString</span></span>
<span data-ttu-id="30946-120">Lekérdezési karakterlánc szerepeltetése az átirányított URL-címben.</span><span class="sxs-lookup"><span data-stu-id="30946-120">Include query string in the redirected url.</span></span>
<span data-ttu-id="30946-121">Az alapértelmezett érték az igaz.</span><span class="sxs-lookup"><span data-stu-id="30946-121">Default is true.</span></span>

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

### <span data-ttu-id="30946-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="30946-122">-Name</span></span>
<span data-ttu-id="30946-123">Az átirányítási konfiguráció neve</span><span class="sxs-lookup"><span data-stu-id="30946-123">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="30946-124">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="30946-124">-RedirectType</span></span>
<span data-ttu-id="30946-125">Az átirányítás típusa</span><span class="sxs-lookup"><span data-stu-id="30946-125">The type of redirect</span></span>

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

### <span data-ttu-id="30946-126">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="30946-126">-TargetListener</span></span>
<span data-ttu-id="30946-127">A HTTP-figyelő a kérés átirányításához</span><span class="sxs-lookup"><span data-stu-id="30946-127">HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="30946-128">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="30946-128">-TargetListenerID</span></span>
<span data-ttu-id="30946-129">A HTTP-figyelő azonosítója a kérés átirányításához</span><span class="sxs-lookup"><span data-stu-id="30946-129">ID of HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="30946-130">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="30946-130">-TargetUrl</span></span>
<span data-ttu-id="30946-131">Cél URL-címe</span><span class="sxs-lookup"><span data-stu-id="30946-131">Target URL fo redirection</span></span>

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

### <span data-ttu-id="30946-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30946-132">CommonParameters</span></span>
<span data-ttu-id="30946-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="30946-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30946-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30946-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30946-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="30946-135">INPUTS</span></span>

### <span data-ttu-id="30946-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="30946-136">None</span></span>

## <span data-ttu-id="30946-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="30946-137">OUTPUTS</span></span>

### <span data-ttu-id="30946-138">Microsoft. Azure. commands. Network. models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="30946-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="30946-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="30946-139">NOTES</span></span>

## <span data-ttu-id="30946-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="30946-140">RELATED LINKS</span></span>

[<span data-ttu-id="30946-141">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="30946-141">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="30946-142">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="30946-142">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="30946-143">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="30946-143">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="30946-144">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="30946-144">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
