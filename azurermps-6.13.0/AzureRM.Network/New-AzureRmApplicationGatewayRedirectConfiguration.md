---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 06f8b64e1f79a4c024c56d834e09d374ce201cfe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93673158"
---
# <span data-ttu-id="dabd7-101">New-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="dabd7-101">New-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="dabd7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dabd7-102">SYNOPSIS</span></span>
<span data-ttu-id="dabd7-103">Átirányítási konfigurációt hoz létre az alkalmazás-átjárók számára.</span><span class="sxs-lookup"><span data-stu-id="dabd7-103">Creates a redirect configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dabd7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dabd7-104">SYNTAX</span></span>

### <span data-ttu-id="dabd7-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="dabd7-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dabd7-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="dabd7-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dabd7-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="dabd7-107">SetByURL</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String> [-TargetUrl <String>]
 [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dabd7-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="dabd7-108">DESCRIPTION</span></span>
<span data-ttu-id="dabd7-109">**A New-AzureRmApplicationGatewayRedirectConfiguration** parancsmag átirányítási konfigurációt hoz létre az alkalmazás-átjárók számára.</span><span class="sxs-lookup"><span data-stu-id="dabd7-109">**The New-AzureRmApplicationGatewayRedirectConfiguration** cmdlet creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="dabd7-110">Példák</span><span class="sxs-lookup"><span data-stu-id="dabd7-110">EXAMPLES</span></span>

### <span data-ttu-id="dabd7-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="dabd7-111">Example 1</span></span>
```
PS C:\>$RedirectConfig = New-AzureRmApplicationGatewayRedirectConfiguration -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="dabd7-112">Ez a parancs létrehoz egy Redirect01 nevű átirányítási konfigurációt, és az eredményt az $RedirectConfig nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="dabd7-112">This command creates a redirect configuration named Redirect01 and stores the result in the variable named $RedirectConfig.</span></span>

## <span data-ttu-id="dabd7-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dabd7-113">PARAMETERS</span></span>

### <span data-ttu-id="dabd7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dabd7-114">-DefaultProfile</span></span>
<span data-ttu-id="dabd7-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dabd7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dabd7-116">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="dabd7-116">-IncludePath</span></span>
<span data-ttu-id="dabd7-117">Az átirányított URL-címben az elérési út belefoglalása</span><span class="sxs-lookup"><span data-stu-id="dabd7-117">Include path in the redirected url.</span></span>
<span data-ttu-id="dabd7-118">Az alapértelmezett érték az igaz.</span><span class="sxs-lookup"><span data-stu-id="dabd7-118">Default is true.</span></span>

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

### <span data-ttu-id="dabd7-119">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="dabd7-119">-IncludeQueryString</span></span>
<span data-ttu-id="dabd7-120">Lekérdezési karakterlánc szerepeltetése az átirányított URL-címben.</span><span class="sxs-lookup"><span data-stu-id="dabd7-120">Include query string in the redirected url.</span></span>
<span data-ttu-id="dabd7-121">Az alapértelmezett érték az igaz.</span><span class="sxs-lookup"><span data-stu-id="dabd7-121">Default is true.</span></span>

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

### <span data-ttu-id="dabd7-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dabd7-122">-Name</span></span>
<span data-ttu-id="dabd7-123">Az átirányítási konfiguráció neve</span><span class="sxs-lookup"><span data-stu-id="dabd7-123">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="dabd7-124">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="dabd7-124">-RedirectType</span></span>
<span data-ttu-id="dabd7-125">Az átirányítás típusa</span><span class="sxs-lookup"><span data-stu-id="dabd7-125">The type of redirect</span></span>

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

### <span data-ttu-id="dabd7-126">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="dabd7-126">-TargetListener</span></span>
<span data-ttu-id="dabd7-127">HTTPListener a kérés átirányításához</span><span class="sxs-lookup"><span data-stu-id="dabd7-127">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="dabd7-128">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="dabd7-128">-TargetListenerID</span></span>
<span data-ttu-id="dabd7-129">A figyelő azonosítója a kérés átirányításához</span><span class="sxs-lookup"><span data-stu-id="dabd7-129">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="dabd7-130">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="dabd7-130">-TargetUrl</span></span>
<span data-ttu-id="dabd7-131">Cél URL-címe</span><span class="sxs-lookup"><span data-stu-id="dabd7-131">Target URL fo redirection</span></span>

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

### <span data-ttu-id="dabd7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dabd7-132">CommonParameters</span></span>
<span data-ttu-id="dabd7-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dabd7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dabd7-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dabd7-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dabd7-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dabd7-135">INPUTS</span></span>

### <span data-ttu-id="dabd7-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="dabd7-136">None</span></span>

## <span data-ttu-id="dabd7-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dabd7-137">OUTPUTS</span></span>

### <span data-ttu-id="dabd7-138">Microsoft. Azure. commands. Network. models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="dabd7-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="dabd7-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dabd7-139">NOTES</span></span>

## <span data-ttu-id="dabd7-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dabd7-140">RELATED LINKS</span></span>
