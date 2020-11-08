---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprivatelinkipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkIpConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkIpConfiguration.md
ms.openlocfilehash: 01da3615a43a5923d6017e759c1b04f039332c9f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195382"
---
# <span data-ttu-id="bfda0-101">New-AzApplicationGatewayPrivateLinkIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="bfda0-101">New-AzApplicationGatewayPrivateLinkIpConfiguration</span></span>

## <span data-ttu-id="bfda0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bfda0-102">SYNOPSIS</span></span>
<span data-ttu-id="bfda0-103">IP-konfiguráció létrehozása a PrivateLink-konfigurációhoz való társításhoz</span><span class="sxs-lookup"><span data-stu-id="bfda0-103">Creates an Ip Configuration to be associated with PrivateLink Configuration</span></span>

## <span data-ttu-id="bfda0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bfda0-104">SYNTAX</span></span>

```
New-AzApplicationGatewayPrivateLinkIpConfiguration -Name <String> -Subnet <PSSubnet>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bfda0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bfda0-105">DESCRIPTION</span></span>
<span data-ttu-id="bfda0-106">A **New-AzApplicationGatewayPrivateLinkIpConfiguration** parancsmag olyan IP-konfigurációt hoz létre, amelyet az Azure Application Gateway PrivateLink-konfigurációjához társít.</span><span class="sxs-lookup"><span data-stu-id="bfda0-106">The **New-AzApplicationGatewayPrivateLinkIpConfiguration** cmdlet creates an Ip Configuration to be associated with PrivateLink Configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="bfda0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bfda0-107">EXAMPLES</span></span>

### <span data-ttu-id="bfda0-108">1. példa: PrivateLink IP-konfigurációja</span><span class="sxs-lookup"><span data-stu-id="bfda0-108">Example 1: PrivateLink Ip Configuration</span></span>
```powershell
PS C:\> $PrivateLinkIpConfiguration = New-AzApplicationGatewayPrivateLinkIpConfiguration -Name "ipConfig01" -Subnet $subnet -Primary
```

<span data-ttu-id="bfda0-109">Ez a parancs létrehoz egy "ipConfig01" nevű PrivateLink IP-konfigurációt, amelyet az eredmény az $PrivateLinkIpConfiguration nevű változóban tárol.</span><span class="sxs-lookup"><span data-stu-id="bfda0-109">This command creates an PrivateLink IP Configuration named 'ipConfig01' stores the result in the variable named $PrivateLinkIpConfiguration.</span></span> 

## <span data-ttu-id="bfda0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bfda0-110">PARAMETERS</span></span>

### <span data-ttu-id="bfda0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfda0-111">-DefaultProfile</span></span>
<span data-ttu-id="bfda0-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bfda0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfda0-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bfda0-113">-Name</span></span>
<span data-ttu-id="bfda0-114">A IpConfiguration neve</span><span class="sxs-lookup"><span data-stu-id="bfda0-114">The name of the IpConfiguration</span></span>

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

### <span data-ttu-id="bfda0-115">-Elsődleges</span><span class="sxs-lookup"><span data-stu-id="bfda0-115">-Primary</span></span>
<span data-ttu-id="bfda0-116">Jelzi, hogy az IP-konfiguráció elsődleges.</span><span class="sxs-lookup"><span data-stu-id="bfda0-116">Indicate the ip configuration is primary.</span></span>

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

### <span data-ttu-id="bfda0-117">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="bfda0-117">-PrivateIpAddress</span></span>
<span data-ttu-id="bfda0-118">A ipConfiguration privát IP-címe, ha a statikus kiosztást szeretné használni.</span><span class="sxs-lookup"><span data-stu-id="bfda0-118">The private ip address of the ipConfiguration if static allocation is desired.</span></span>

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

### <span data-ttu-id="bfda0-119">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="bfda0-119">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="bfda0-120">Az IP-konfiguráció IP-verziója</span><span class="sxs-lookup"><span data-stu-id="bfda0-120">The ip version of the ip configuration</span></span>

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

### <span data-ttu-id="bfda0-121">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="bfda0-121">-Subnet</span></span>
<span data-ttu-id="bfda0-122">Alhálózati</span><span class="sxs-lookup"><span data-stu-id="bfda0-122">Subnet</span></span>

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

### <span data-ttu-id="bfda0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfda0-123">CommonParameters</span></span>
<span data-ttu-id="bfda0-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bfda0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfda0-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="bfda0-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfda0-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bfda0-126">INPUTS</span></span>

### <span data-ttu-id="bfda0-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="bfda0-127">None</span></span>

## <span data-ttu-id="bfda0-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bfda0-128">OUTPUTS</span></span>

### <span data-ttu-id="bfda0-129">Microsoft. Azure. commands. Network. models. PSApplicationGatewayPrivateLinkIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="bfda0-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration</span></span>

## <span data-ttu-id="bfda0-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bfda0-130">NOTES</span></span>

## <span data-ttu-id="bfda0-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bfda0-131">RELATED LINKS</span></span>

[<span data-ttu-id="bfda0-132">Új – AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="bfda0-132">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)
