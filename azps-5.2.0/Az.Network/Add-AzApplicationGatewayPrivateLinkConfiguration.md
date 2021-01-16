---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 2083dd00c5163a67492ff9973fdf7399d67d7cb6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342017"
---
# <span data-ttu-id="a80e5-101">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="a80e5-101">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="a80e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a80e5-102">SYNOPSIS</span></span>
<span data-ttu-id="a80e5-103">Személyes hivatkozáskonfigurációt ad hozzá egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="a80e5-103">Adds a private link configuration to an application gateway.</span></span>

## <span data-ttu-id="a80e5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a80e5-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a80e5-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a80e5-105">DESCRIPTION</span></span>
<span data-ttu-id="a80e5-106">Az **Add-AzApplicationGatewayPrivateLinkConfiguration** parancsmag hozzáad egy privát csatolási konfigurációt egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="a80e5-106">The **Add-AzApplicationGatewayPrivateLinkConfiguration** cmdlet adds a private link configuration to an application gateway.</span></span>

## <span data-ttu-id="a80e5-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a80e5-107">EXAMPLES</span></span>

### <span data-ttu-id="a80e5-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="a80e5-108">Example 1</span></span>
```powershell
PS C:\> $PrivateLinkIpConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "ipConfig01" -Subnet $subnet -Primary
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01" -IpConfiguration $PrivateLinkIpConfiguration
```

<span data-ttu-id="a80e5-109">Az első parancs létrehoz egy privateLinkIpConfigurationt, és a $PrivateLinkIpConfiguration tárolja.</span><span class="sxs-lookup"><span data-stu-id="a80e5-109">The first command creates a privateLinkIpConfiguration and stores it in the $PrivateLinkIpConfiguration variable.</span></span>
<span data-ttu-id="a80e5-110">A második parancs lekérte az ApplicationGateway01 nevű alkalmazás-átjárót, amely az ResourceGroup01 nevű erőforráscsoporthoz tartozik, és a helyi $AppGw tárolja.</span><span class="sxs-lookup"><span data-stu-id="a80e5-110">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="a80e5-111">A harmadik parancs hozzáadja a privateLinkConfig01 nevű privát hivatkozáskonfigurációt a $AppGw</span><span class="sxs-lookup"><span data-stu-id="a80e5-111">The third command adds the private link configuration named privateLinkConfig01, for the gateway in $AppGw</span></span>

## <span data-ttu-id="a80e5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a80e5-112">PARAMETERS</span></span>

### <span data-ttu-id="a80e5-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a80e5-113">-ApplicationGateway</span></span>
<span data-ttu-id="a80e5-114">Az applicationGateway</span><span class="sxs-lookup"><span data-stu-id="a80e5-114">The applicationGateway</span></span>

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

### <span data-ttu-id="a80e5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a80e5-115">-DefaultProfile</span></span>
<span data-ttu-id="a80e5-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a80e5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a80e5-117">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="a80e5-117">-IpConfiguration</span></span>
<span data-ttu-id="a80e5-118">Az ipConfiguration listája</span><span class="sxs-lookup"><span data-stu-id="a80e5-118">The list of ipConfiguration</span></span>

```yaml
Type: PSApplicationGatewayPrivateLinkIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a80e5-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a80e5-119">-Name</span></span>
<span data-ttu-id="a80e5-120">A privateLink-konfiguráció neve</span><span class="sxs-lookup"><span data-stu-id="a80e5-120">The name of the privateLink configuration</span></span>

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

### <span data-ttu-id="a80e5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a80e5-121">CommonParameters</span></span>
<span data-ttu-id="a80e5-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a80e5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a80e5-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a80e5-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a80e5-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a80e5-124">INPUTS</span></span>

### <span data-ttu-id="a80e5-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a80e5-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="a80e5-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="a80e5-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="a80e5-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a80e5-127">OUTPUTS</span></span>

### <span data-ttu-id="a80e5-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a80e5-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a80e5-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a80e5-129">NOTES</span></span>

## <span data-ttu-id="a80e5-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a80e5-130">RELATED LINKS</span></span>

[<span data-ttu-id="a80e5-131">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="a80e5-131">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="a80e5-132">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="a80e5-132">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="a80e5-133">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="a80e5-133">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="a80e5-134">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="a80e5-134">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)