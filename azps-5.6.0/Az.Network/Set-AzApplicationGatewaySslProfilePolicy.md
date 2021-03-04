---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewaysslprofilepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslProfilePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslProfilePolicy.md
ms.openlocfilehash: 6dff1e78f83c48a103266c39bd9f3462a20b50a3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941057"
---
# <span data-ttu-id="7cce6-101">Set-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="7cce6-101">Set-AzApplicationGatewaySslProfilePolicy</span></span>

## <span data-ttu-id="7cce6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7cce6-102">SYNOPSIS</span></span>
<span data-ttu-id="7cce6-103">Módosítja egy alkalmazásátjáró SSL-profiljának SSL-házirendét.</span><span class="sxs-lookup"><span data-stu-id="7cce6-103">Modifies the SSL policy of an application gateway SSL profile.</span></span>

## <span data-ttu-id="7cce6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7cce6-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslProfilePolicy -SslProfile <PSApplicationGatewaySslProfile>
 [-DisabledSslProtocols <String[]>] [-PolicyType <String>] [-PolicyName <String>] [-CipherSuite <String[]>]
 [-MinProtocolVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7cce6-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7cce6-105">DESCRIPTION</span></span>
<span data-ttu-id="7cce6-106">A **Set-AzApplicationGatewaySslProfilePolicy** parancsmag módosítja egy alkalmazásátjáró SSL-profiljának SSL-házirendét.</span><span class="sxs-lookup"><span data-stu-id="7cce6-106">The **Set-AzApplicationGatewaySslProfilePolicy** cmdlet modifies the SSL policy of an application gateway SSL profile.</span></span>

## <span data-ttu-id="7cce6-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7cce6-107">EXAMPLES</span></span>

### <span data-ttu-id="7cce6-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="7cce6-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> $profile = Set-AzApplicationGatewaySslProfilePolicy -SslProfile $profile -PolicyType Predefined -PolicyName AppGwSslPolicy20170401
```

<span data-ttu-id="7cce6-109">Az első parancs az ApplicationGateway01 nevű alkalmazás-átjárót az ResourceGroup01 nevű erőforráscsoportban tárolja a $AppGw változóban.</span><span class="sxs-lookup"><span data-stu-id="7cce6-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="7cce6-110">A második parancs az SslProfile01 nevű ssl-profilt kapja $AppGw a beállításokat a $profile változóban.</span><span class="sxs-lookup"><span data-stu-id="7cce6-110">The second command gets the ssl profile named SslProfile01 for $AppGw and stores the settings in the $profile variable.</span></span> <span data-ttu-id="7cce6-111">Az utolsó parancs módosítja a böngészőben tárolt ssl-profilobjektum ssl-házirend $profile.</span><span class="sxs-lookup"><span data-stu-id="7cce6-111">The last command modifies the ssl policy of the ssl profile object stored in $profile.</span></span>

## <span data-ttu-id="7cce6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7cce6-112">PARAMETERS</span></span>

### <span data-ttu-id="7cce6-113">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="7cce6-113">-CipherSuite</span></span>
<span data-ttu-id="7cce6-114">Ssl cipher suites to be enabled in the specified order to application gateway</span><span class="sxs-lookup"><span data-stu-id="7cce6-114">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cce6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cce6-115">-DefaultProfile</span></span>
<span data-ttu-id="7cce6-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7cce6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cce6-117">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="7cce6-117">-DisabledSslProtocols</span></span>
<span data-ttu-id="7cce6-118">A letiltani szükséges SSL-protokollok listája</span><span class="sxs-lookup"><span data-stu-id="7cce6-118">List of SSL protocols to be disabled</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cce6-119">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="7cce6-119">-MinProtocolVersion</span></span>
<span data-ttu-id="7cce6-120">Az Ssl-protokoll minimális verziója, amelyet az alkalmazás-átjáró támogat</span><span class="sxs-lookup"><span data-stu-id="7cce6-120">Minimum version of Ssl protocol to be supported on application gateway</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cce6-121">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="7cce6-121">-PolicyName</span></span>
<span data-ttu-id="7cce6-122">Az Ssl előre definiált házirend neve</span><span class="sxs-lookup"><span data-stu-id="7cce6-122">Name of Ssl predefined policy</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cce6-123">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="7cce6-123">-PolicyType</span></span>
<span data-ttu-id="7cce6-124">Az Ssl-házirend típusa</span><span class="sxs-lookup"><span data-stu-id="7cce6-124">Type of Ssl Policy</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Predefined, Custom

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cce6-125">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="7cce6-125">-SslProfile</span></span>
<span data-ttu-id="7cce6-126">Az alkalmazás átjárója SSL-profilja</span><span class="sxs-lookup"><span data-stu-id="7cce6-126">The application gateway SSL profile</span></span>

```yaml
Type: PSApplicationGatewaySslProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7cce6-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7cce6-127">-Confirm</span></span>
<span data-ttu-id="7cce6-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7cce6-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cce6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cce6-129">-WhatIf</span></span>
<span data-ttu-id="7cce6-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7cce6-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cce6-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7cce6-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cce6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cce6-132">CommonParameters</span></span>
<span data-ttu-id="7cce6-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cce6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cce6-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7cce6-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cce6-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7cce6-135">INPUTS</span></span>

### <span data-ttu-id="7cce6-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="7cce6-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="7cce6-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7cce6-137">OUTPUTS</span></span>

### <span data-ttu-id="7cce6-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="7cce6-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="7cce6-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7cce6-139">NOTES</span></span>

## <span data-ttu-id="7cce6-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7cce6-140">RELATED LINKS</span></span>

[<span data-ttu-id="7cce6-141">Add-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="7cce6-141">Add-AzApplicationGatewaySslProfilePolicy</span></span>](./Add-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="7cce6-142">New-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="7cce6-142">New-AzApplicationGatewaySslProfilePolicy</span></span>](./New-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="7cce6-143">Get-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="7cce6-143">Get-AzApplicationGatewaySslProfilePolicy</span></span>](./Get-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="7cce6-144">Remove-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="7cce6-144">Remove-AzApplicationGatewaySslProfilePolicy</span></span>](./Remove-AzApplicationGatewaySslProfilePolicy.md)