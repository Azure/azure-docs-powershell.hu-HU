---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
ms.openlocfilehash: 2cb7455d5a902882fdd98dd5fea47ae5a28e1dc9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848134"
---
# <span data-ttu-id="54d6f-101">New-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="54d6f-101">New-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="54d6f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="54d6f-102">SYNOPSIS</span></span>
<span data-ttu-id="54d6f-103">Átirányítási konfigurációt hoz létre az alkalmazás-átjárók számára.</span><span class="sxs-lookup"><span data-stu-id="54d6f-103">Creates a redirect configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54d6f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="54d6f-104">SYNTAX</span></span>

### <span data-ttu-id="54d6f-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="54d6f-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54d6f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="54d6f-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54d6f-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="54d6f-107">SetByURL</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String> [-TargetUrl <String>]
 [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="54d6f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="54d6f-108">DESCRIPTION</span></span>
<span data-ttu-id="54d6f-109">**A New-AzureRmApplicationGatewayRedirectConfiguration** parancsmag átirányítási konfigurációt hoz létre az alkalmazás-átjárók számára.</span><span class="sxs-lookup"><span data-stu-id="54d6f-109">**The New-AzureRmApplicationGatewayRedirectConfiguration** cmdlet creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="54d6f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="54d6f-110">EXAMPLES</span></span>

### <span data-ttu-id="54d6f-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="54d6f-111">Example 1</span></span>
```
PS C:\>$RedirectConfig = New-AzureRmApplicationGatewayRedirectConfiguration -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="54d6f-112">Ez a parancs létrehoz egy Redirect01 nevű átirányítási konfigurációt, és az eredményt az $RedirectConfig nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="54d6f-112">This command creates a redirect configuration named Redirect01 and stores the result in the variable named $RedirectConfig.</span></span>

## <span data-ttu-id="54d6f-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="54d6f-113">PARAMETERS</span></span>

### <span data-ttu-id="54d6f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54d6f-114">-DefaultProfile</span></span>
<span data-ttu-id="54d6f-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="54d6f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54d6f-116">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="54d6f-116">-IncludePath</span></span>
<span data-ttu-id="54d6f-117">Az átirányított URL-címben az elérési út belefoglalása</span><span class="sxs-lookup"><span data-stu-id="54d6f-117">Include path in the redirected url.</span></span>
<span data-ttu-id="54d6f-118">Az alapértelmezett érték az igaz.</span><span class="sxs-lookup"><span data-stu-id="54d6f-118">Default is true.</span></span>

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

### <span data-ttu-id="54d6f-119">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="54d6f-119">-IncludeQueryString</span></span>
<span data-ttu-id="54d6f-120">Lekérdezési karakterlánc szerepeltetése az átirányított URL-címben.</span><span class="sxs-lookup"><span data-stu-id="54d6f-120">Include query string in the redirected url.</span></span>
<span data-ttu-id="54d6f-121">Az alapértelmezett érték az igaz.</span><span class="sxs-lookup"><span data-stu-id="54d6f-121">Default is true.</span></span>

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

### <span data-ttu-id="54d6f-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="54d6f-122">-Name</span></span>
<span data-ttu-id="54d6f-123">Az átirányítási konfiguráció neve</span><span class="sxs-lookup"><span data-stu-id="54d6f-123">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="54d6f-124">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="54d6f-124">-RedirectType</span></span>
<span data-ttu-id="54d6f-125">Az átirányítás típusa</span><span class="sxs-lookup"><span data-stu-id="54d6f-125">The type of redirect</span></span>

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

### <span data-ttu-id="54d6f-126">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="54d6f-126">-TargetListener</span></span>
<span data-ttu-id="54d6f-127">HTTPListener a kérés átirányításához</span><span class="sxs-lookup"><span data-stu-id="54d6f-127">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="54d6f-128">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="54d6f-128">-TargetListenerID</span></span>
<span data-ttu-id="54d6f-129">A figyelő azonosítója a kérés átirányításához</span><span class="sxs-lookup"><span data-stu-id="54d6f-129">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="54d6f-130">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="54d6f-130">-TargetUrl</span></span>
<span data-ttu-id="54d6f-131">Cél URL-címe</span><span class="sxs-lookup"><span data-stu-id="54d6f-131">Target URL fo redirection</span></span>

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

### <span data-ttu-id="54d6f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54d6f-132">CommonParameters</span></span>
<span data-ttu-id="54d6f-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="54d6f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54d6f-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54d6f-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54d6f-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="54d6f-135">INPUTS</span></span>

### <span data-ttu-id="54d6f-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="54d6f-136">None</span></span>

## <span data-ttu-id="54d6f-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="54d6f-137">OUTPUTS</span></span>

### <span data-ttu-id="54d6f-138">Microsoft. Azure. commands. Network. models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="54d6f-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="54d6f-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="54d6f-139">NOTES</span></span>

## <span data-ttu-id="54d6f-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="54d6f-140">RELATED LINKS</span></span>

