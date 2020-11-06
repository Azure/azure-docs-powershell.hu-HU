---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 0d2d9d9390f60c7d7eb74061a52b9b437acdf772
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493743"
---
# <span data-ttu-id="5d46c-101">New-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="5d46c-101">New-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="5d46c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5d46c-102">SYNOPSIS</span></span>
<span data-ttu-id="5d46c-103">Átirányítási konfigurációt hoz létre az alkalmazás-átjárók számára.</span><span class="sxs-lookup"><span data-stu-id="5d46c-103">Creates a redirect configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d46c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5d46c-104">SYNTAX</span></span>

### <span data-ttu-id="5d46c-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5d46c-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d46c-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="5d46c-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d46c-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="5d46c-107">SetByURL</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String> [-TargetUrl <String>]
 [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5d46c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="5d46c-108">DESCRIPTION</span></span>
<span data-ttu-id="5d46c-109">**A New-AzureRmApplicationGatewayRedirectConfiguration** parancsmag átirányítási konfigurációt hoz létre az alkalmazás-átjárók számára.</span><span class="sxs-lookup"><span data-stu-id="5d46c-109">**The New-AzureRmApplicationGatewayRedirectConfiguration** cmdlet creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="5d46c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="5d46c-110">EXAMPLES</span></span>

### <span data-ttu-id="5d46c-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5d46c-111">Example 1</span></span>
```
PS C:\>$RedirectConfig = New-AzureRmApplicationGatewayRedirectConfiguration -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="5d46c-112">Ez a parancs létrehoz egy Redirect01 nevű átirányítási konfigurációt, és az eredményt az $RedirectConfig nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="5d46c-112">This command creates a redirect configuration named Redirect01 and stores the result in the variable named $RedirectConfig.</span></span>

## <span data-ttu-id="5d46c-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5d46c-113">PARAMETERS</span></span>

### <span data-ttu-id="5d46c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d46c-114">-DefaultProfile</span></span>
<span data-ttu-id="5d46c-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5d46c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d46c-116">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="5d46c-116">-IncludePath</span></span>
<span data-ttu-id="5d46c-117">Az átirányított URL-címben az elérési út belefoglalása</span><span class="sxs-lookup"><span data-stu-id="5d46c-117">Include path in the redirected url.</span></span>
<span data-ttu-id="5d46c-118">Az alapértelmezett érték az igaz.</span><span class="sxs-lookup"><span data-stu-id="5d46c-118">Default is true.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d46c-119">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="5d46c-119">-IncludeQueryString</span></span>
<span data-ttu-id="5d46c-120">Lekérdezési karakterlánc szerepeltetése az átirányított URL-címben.</span><span class="sxs-lookup"><span data-stu-id="5d46c-120">Include query string in the redirected url.</span></span>
<span data-ttu-id="5d46c-121">Az alapértelmezett érték az igaz.</span><span class="sxs-lookup"><span data-stu-id="5d46c-121">Default is true.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d46c-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5d46c-122">-Name</span></span>
<span data-ttu-id="5d46c-123">Az átirányítási konfiguráció neve</span><span class="sxs-lookup"><span data-stu-id="5d46c-123">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="5d46c-124">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="5d46c-124">-RedirectType</span></span>
<span data-ttu-id="5d46c-125">Az átirányítás típusa</span><span class="sxs-lookup"><span data-stu-id="5d46c-125">The type of redirect</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Permanent, Found, SeeOther, Temporary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d46c-126">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="5d46c-126">-TargetListener</span></span>
<span data-ttu-id="5d46c-127">HTTPListener a kérés átirányításához</span><span class="sxs-lookup"><span data-stu-id="5d46c-127">HTTPListener to redirect the request to</span></span>

```yaml
Type: PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d46c-128">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="5d46c-128">-TargetListenerID</span></span>
<span data-ttu-id="5d46c-129">A figyelő azonosítója a kérés átirányításához</span><span class="sxs-lookup"><span data-stu-id="5d46c-129">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="5d46c-130">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="5d46c-130">-TargetUrl</span></span>
<span data-ttu-id="5d46c-131">Cél URL-címe</span><span class="sxs-lookup"><span data-stu-id="5d46c-131">Target URL fo redirection</span></span>

```yaml
Type: String
Parameter Sets: SetByURL
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d46c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d46c-132">CommonParameters</span></span>
<span data-ttu-id="5d46c-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5d46c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d46c-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d46c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d46c-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d46c-135">INPUTS</span></span>

### <span data-ttu-id="5d46c-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="5d46c-136">None</span></span>

## <span data-ttu-id="5d46c-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d46c-137">OUTPUTS</span></span>

### <span data-ttu-id="5d46c-138">Microsoft. Azure. commands. Network. models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="5d46c-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="5d46c-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5d46c-139">NOTES</span></span>

## <span data-ttu-id="5d46c-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5d46c-140">RELATED LINKS</span></span>

