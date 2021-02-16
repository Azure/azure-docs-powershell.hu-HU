---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprivatelinkipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkIpConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkIpConfiguration.md
ms.openlocfilehash: 01da3615a43a5923d6017e759c1b04f039332c9f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202904"
---
# <span data-ttu-id="bd8e1-101">New-AzApplicationGatewayPrivateLinkIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="bd8e1-101">New-AzApplicationGatewayPrivateLinkIpConfiguration</span></span>

## <span data-ttu-id="bd8e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd8e1-102">SYNOPSIS</span></span>
<span data-ttu-id="bd8e1-103">Ip-konfigurációt hoz létre a PrivateLink-konfigurációhoz társítva</span><span class="sxs-lookup"><span data-stu-id="bd8e1-103">Creates an Ip Configuration to be associated with PrivateLink Configuration</span></span>

## <span data-ttu-id="bd8e1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bd8e1-104">SYNTAX</span></span>

```
New-AzApplicationGatewayPrivateLinkIpConfiguration -Name <String> -Subnet <PSSubnet>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd8e1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bd8e1-105">DESCRIPTION</span></span>
<span data-ttu-id="bd8e1-106">A **New-AzApplicationGatewayPrivateLinkIpConfiguration** parancsmag létrehoz egy Ip-konfigurációt, amely egy Azure-alkalmazás átjáróHoz tartozó PrivateLink-konfigurációval társítható.</span><span class="sxs-lookup"><span data-stu-id="bd8e1-106">The **New-AzApplicationGatewayPrivateLinkIpConfiguration** cmdlet creates an Ip Configuration to be associated with PrivateLink Configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="bd8e1-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bd8e1-107">EXAMPLES</span></span>

### <span data-ttu-id="bd8e1-108">1. példa: PrivateLink IP-konfiguráció</span><span class="sxs-lookup"><span data-stu-id="bd8e1-108">Example 1: PrivateLink Ip Configuration</span></span>
```powershell
PS C:\> $PrivateLinkIpConfiguration = New-AzApplicationGatewayPrivateLinkIpConfiguration -Name "ipConfig01" -Subnet $subnet -Primary
```

<span data-ttu-id="bd8e1-109">Ez a parancs létrehoz egy "ipConfig01" nevű PrivateLink IP-konfigurációt, amely az eredményt a $PrivateLinkIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="bd8e1-109">This command creates an PrivateLink IP Configuration named 'ipConfig01' stores the result in the variable named $PrivateLinkIpConfiguration.</span></span> 

## <span data-ttu-id="bd8e1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd8e1-110">PARAMETERS</span></span>

### <span data-ttu-id="bd8e1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd8e1-111">-DefaultProfile</span></span>
<span data-ttu-id="bd8e1-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bd8e1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd8e1-113">-Name</span><span class="sxs-lookup"><span data-stu-id="bd8e1-113">-Name</span></span>
<span data-ttu-id="bd8e1-114">Az IpConfiguration neve</span><span class="sxs-lookup"><span data-stu-id="bd8e1-114">The name of the IpConfiguration</span></span>

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

### <span data-ttu-id="bd8e1-115">-Primary</span><span class="sxs-lookup"><span data-stu-id="bd8e1-115">-Primary</span></span>
<span data-ttu-id="bd8e1-116">Az ip-konfiguráció elsődleges beállítása.</span><span class="sxs-lookup"><span data-stu-id="bd8e1-116">Indicate the ip configuration is primary.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd8e1-117">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="bd8e1-117">-PrivateIpAddress</span></span>
<span data-ttu-id="bd8e1-118">Az ipConfiguration privát IP-címe, ha statikus terhelést kíván.</span><span class="sxs-lookup"><span data-stu-id="bd8e1-118">The private ip address of the ipConfiguration if static allocation is desired.</span></span>

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

### <span data-ttu-id="bd8e1-119">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="bd8e1-119">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="bd8e1-120">Az IP-konfiguráció IP-verziója</span><span class="sxs-lookup"><span data-stu-id="bd8e1-120">The ip version of the ip configuration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd8e1-121">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="bd8e1-121">-Subnet</span></span>
<span data-ttu-id="bd8e1-122">Alhálózat</span><span class="sxs-lookup"><span data-stu-id="bd8e1-122">Subnet</span></span>

```yaml
Type: PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd8e1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd8e1-123">CommonParameters</span></span>
<span data-ttu-id="bd8e1-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd8e1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd8e1-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bd8e1-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd8e1-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bd8e1-126">INPUTS</span></span>

### <span data-ttu-id="bd8e1-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="bd8e1-127">None</span></span>

## <span data-ttu-id="bd8e1-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd8e1-128">OUTPUTS</span></span>

### <span data-ttu-id="bd8e1-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="bd8e1-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration</span></span>

## <span data-ttu-id="bd8e1-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bd8e1-130">NOTES</span></span>

## <span data-ttu-id="bd8e1-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bd8e1-131">RELATED LINKS</span></span>

[<span data-ttu-id="bd8e1-132">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="bd8e1-132">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)
