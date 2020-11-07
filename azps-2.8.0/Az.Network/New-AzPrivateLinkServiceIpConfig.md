---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkserviceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceIpConfig.md
ms.openlocfilehash: c7ea999af626206b741e86457d92627e4db196a7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837174"
---
# <span data-ttu-id="eb23c-101">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="eb23c-101">New-AzPrivateLinkServiceIpConfig</span></span>

## <span data-ttu-id="eb23c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eb23c-102">SYNOPSIS</span></span>
<span data-ttu-id="eb23c-103">Hozzon létre egy privát kapcsolat szolgáltatás IP-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="eb23c-103">Create a private link service ip configuration.</span></span>

## <span data-ttu-id="eb23c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eb23c-104">SYNTAX</span></span>

```
New-AzPrivateLinkServiceIpConfig -Name <String> [-PrivateIpAddressVersion <String>]
 [-PrivateIpAddress <String>] [-PublicIpAddress <PSPublicIpAddress>]
 [-Subnet <PSSubnet>] [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb23c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="eb23c-105">DESCRIPTION</span></span>
<span data-ttu-id="eb23c-106">A **New-AzPrivateLinkServiceIpConfig** parancsmag létrehoz egy privát kapcsolati szolgáltatás IP-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="eb23c-106">The **New-AzPrivateLinkServiceIpConfig** cmdlet creates a private link service ip configuration.</span></span> <span data-ttu-id="eb23c-107">Ezt a konfigurációt a program a privát végpontról származó bejövő forgalom forrás NAT-nek használja.</span><span class="sxs-lookup"><span data-stu-id="eb23c-107">This configuration is used for source NAT-ing the incoming traffic from private endpoint.</span></span> 

## <span data-ttu-id="eb23c-108">Példák</span><span class="sxs-lookup"><span data-stu-id="eb23c-108">EXAMPLES</span></span>

### <span data-ttu-id="eb23c-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="eb23c-109">Example 1</span></span>
```
New-AzPrivateLinkServiceIpConfig -Name $IpConfigurationName -PrivateIpAddress "10.0.0.5" -Primary
```

<span data-ttu-id="eb23c-110">Ez a példa létrehoz egy privát hivatkozás szolgáltatás IP-konfigurációját a memóriában.</span><span class="sxs-lookup"><span data-stu-id="eb23c-110">This example create a private link service ip configuration in memory.</span></span>

## <span data-ttu-id="eb23c-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eb23c-111">PARAMETERS</span></span>

### <span data-ttu-id="eb23c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb23c-112">-DefaultProfile</span></span>
<span data-ttu-id="eb23c-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eb23c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb23c-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="eb23c-114">-Name</span></span>
<span data-ttu-id="eb23c-115">A IpConfiguration neve</span><span class="sxs-lookup"><span data-stu-id="eb23c-115">The name of the IpConfiguration</span></span>

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

### <span data-ttu-id="eb23c-116">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="eb23c-116">-PrivateIpAddress</span></span>
<span data-ttu-id="eb23c-117">A ipConfiguration privát IP-címe, ha a statikus hozzárendelés van megadva.</span><span class="sxs-lookup"><span data-stu-id="eb23c-117">The private ip address of the ipConfiguration if static allocation is specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb23c-118">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="eb23c-118">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="eb23c-119">Az IP-konfiguráció IP-verziója</span><span class="sxs-lookup"><span data-stu-id="eb23c-119">The ip version of the ip configuration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb23c-120">-Elsődleges</span><span class="sxs-lookup"><span data-stu-id="eb23c-120">-Primary</span></span>
<span data-ttu-id="eb23c-121">Jelzi, hogy az aktuális IP-konfiguráció elsődleges vagy nem.</span><span class="sxs-lookup"><span data-stu-id="eb23c-121">Indicate current ip configuration is primary or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb23c-122">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="eb23c-122">-Subnet</span></span>
<span data-ttu-id="eb23c-123">Alhálózati</span><span class="sxs-lookup"><span data-stu-id="eb23c-123">Subnet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb23c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb23c-124">CommonParameters</span></span>
<span data-ttu-id="eb23c-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eb23c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb23c-126">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="eb23c-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb23c-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb23c-127">INPUTS</span></span>

### <span data-ttu-id="eb23c-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="eb23c-128">None</span></span>

## <span data-ttu-id="eb23c-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb23c-129">OUTPUTS</span></span>

### <span data-ttu-id="eb23c-130">Microsoft. Azure. commands. Network. models. PSPrivateLinkServiceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="eb23c-130">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration</span></span>

## <span data-ttu-id="eb23c-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eb23c-131">NOTES</span></span>

## <span data-ttu-id="eb23c-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eb23c-132">RELATED LINKS</span></span>

[<span data-ttu-id="eb23c-133">Új – AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="eb23c-133">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)