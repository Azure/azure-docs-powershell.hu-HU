---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
ms.openlocfilehash: c851e075c4963477d8b8f6b18440780735c74f32
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849942"
---
# <span data-ttu-id="36a31-101">Set-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="36a31-101">Set-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="36a31-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="36a31-102">SYNOPSIS</span></span>
<span data-ttu-id="36a31-103">A meglévő alkalmazás-átjárók átirányítási konfigurációjának beállítása.</span><span class="sxs-lookup"><span data-stu-id="36a31-103">Sets the redirect configuration on an existing Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36a31-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="36a31-104">SYNTAX</span></span>

### <span data-ttu-id="36a31-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="36a31-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36a31-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="36a31-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36a31-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="36a31-107">SetByURL</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36a31-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="36a31-108">DESCRIPTION</span></span>
<span data-ttu-id="36a31-109">**A set-AzureRmApplicationGatewayRequestRoutingRule** parancsmag módosította az átirányítási konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="36a31-109">**The Set-AzureRmApplicationGatewayRequestRoutingRule** cmdlet modifies a redirect configuration.</span></span>

## <span data-ttu-id="36a31-110">Példák</span><span class="sxs-lookup"><span data-stu-id="36a31-110">EXAMPLES</span></span>

### <span data-ttu-id="36a31-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="36a31-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw =  Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $appgw -Name "RedirectConfig01" -RedirectType Permanent -TargetUrl "https://www.contoso.com"
```

<span data-ttu-id="36a31-112">Az első parancs a ApplicationGateway01 nevű alkalmazás-átjárót kapja meg, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="36a31-112">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="36a31-113">A második parancs módosítja az alkalmazás átjárójának átirányítási konfigurációját az állandó típus átirányításához, és a cél URL-címet használja.</span><span class="sxs-lookup"><span data-stu-id="36a31-113">The second command modifies the redirect configuration for the application gateway to redirect type Permanent and use a target url.</span></span>

## <span data-ttu-id="36a31-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="36a31-114">PARAMETERS</span></span>

### <span data-ttu-id="36a31-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="36a31-115">-ApplicationGateway</span></span>
<span data-ttu-id="36a31-116">A applicationGateway</span><span class="sxs-lookup"><span data-stu-id="36a31-116">The applicationGateway</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36a31-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36a31-117">-DefaultProfile</span></span>
<span data-ttu-id="36a31-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="36a31-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36a31-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="36a31-119">-IncludePath</span></span>
<span data-ttu-id="36a31-120">Az átirányított URL-címben az elérési út belefoglalása</span><span class="sxs-lookup"><span data-stu-id="36a31-120">Include path in the redirected url.</span></span>
<span data-ttu-id="36a31-121">Az alapértelmezett érték az igaz.</span><span class="sxs-lookup"><span data-stu-id="36a31-121">Default is true.</span></span>

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

### <span data-ttu-id="36a31-122">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="36a31-122">-IncludeQueryString</span></span>
<span data-ttu-id="36a31-123">Lekérdezési karakterlánc szerepeltetése az átirányított URL-címben.</span><span class="sxs-lookup"><span data-stu-id="36a31-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="36a31-124">Az alapértelmezett érték az igaz.</span><span class="sxs-lookup"><span data-stu-id="36a31-124">Default is true.</span></span>

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

### <span data-ttu-id="36a31-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="36a31-125">-Name</span></span>
<span data-ttu-id="36a31-126">Az átirányítási konfiguráció neve</span><span class="sxs-lookup"><span data-stu-id="36a31-126">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="36a31-127">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="36a31-127">-RedirectType</span></span>
<span data-ttu-id="36a31-128">Az átirányítás típusa</span><span class="sxs-lookup"><span data-stu-id="36a31-128">The type of redirect</span></span>

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

### <span data-ttu-id="36a31-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="36a31-129">-TargetListener</span></span>
<span data-ttu-id="36a31-130">HTTPListener a kérés átirányításához</span><span class="sxs-lookup"><span data-stu-id="36a31-130">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="36a31-131">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="36a31-131">-TargetListenerID</span></span>
<span data-ttu-id="36a31-132">A figyelő azonosítója a kérés átirányításához</span><span class="sxs-lookup"><span data-stu-id="36a31-132">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="36a31-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="36a31-133">-TargetUrl</span></span>
<span data-ttu-id="36a31-134">Cél URL-címe</span><span class="sxs-lookup"><span data-stu-id="36a31-134">Target URL fo redirection</span></span>

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

### <span data-ttu-id="36a31-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36a31-135">CommonParameters</span></span>
<span data-ttu-id="36a31-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="36a31-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36a31-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36a31-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36a31-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="36a31-138">INPUTS</span></span>

### <span data-ttu-id="36a31-139">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="36a31-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="36a31-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="36a31-140">OUTPUTS</span></span>

### <span data-ttu-id="36a31-141">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="36a31-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="36a31-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="36a31-142">NOTES</span></span>

## <span data-ttu-id="36a31-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="36a31-143">RELATED LINKS</span></span>

