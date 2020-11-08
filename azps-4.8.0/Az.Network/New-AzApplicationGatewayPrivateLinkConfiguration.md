---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: df616c0b8e6d2fdb7de3567c921714251093fd60
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184874"
---
# <span data-ttu-id="88df6-101">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="88df6-101">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="88df6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="88df6-102">SYNOPSIS</span></span>
<span data-ttu-id="88df6-103">Privát hivatkozás-konfiguráció létrehozása az alkalmazás-átjárók számára</span><span class="sxs-lookup"><span data-stu-id="88df6-103">Creates a private link configuration for an application gateway</span></span>

## <span data-ttu-id="88df6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="88df6-104">SYNTAX</span></span>

```
New-AzApplicationGatewayPrivateLinkConfiguration -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88df6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="88df6-105">DESCRIPTION</span></span>
<span data-ttu-id="88df6-106">A **New-AzApplicationGatewayPrivateLinkConfiguration** parancsmag létrehoz egy PrivateLink-konfigurációt az Azure Application Gateway számára.</span><span class="sxs-lookup"><span data-stu-id="88df6-106">The **New-AzApplicationGatewayPrivateLinkConfiguration** cmdlet creates an PrivateLink Configuration for an Azure application gateway.</span></span>
<span data-ttu-id="88df6-107">A privát hivatkozás-konfigurációt egy olyan felület IP-konfigurációjához kell társítani, amely lehetővé teszi a magánjellegű hivatkozás működését.</span><span class="sxs-lookup"><span data-stu-id="88df6-107">The private link configuration must be associated to a frontend ip configuration to enable the private link functionality.</span></span>
<span data-ttu-id="88df6-108">Egy privát hivatkozás-konfiguráció csak egy atmost társítható az Application Gateway IP-beállításaihoz.</span><span class="sxs-lookup"><span data-stu-id="88df6-108">One private link configuration can atmost be associated to only one frontend ip configuration on application gateway.</span></span>

## <span data-ttu-id="88df6-109">Példák</span><span class="sxs-lookup"><span data-stu-id="88df6-109">EXAMPLES</span></span>

### <span data-ttu-id="88df6-110">Példa 1: privát hivatkozás-konfiguráció létrehozása egyetlen IP-konfigurációval</span><span class="sxs-lookup"><span data-stu-id="88df6-110">Example 1: Create an Private Link Configuration with single Ip Configuration</span></span>
```powershell
PS C:\> $PrivateLinkConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration1
```

<span data-ttu-id="88df6-111">Ez a parancs létrehoz egy "privateLinkConfig01" nevű PrivateLink-konfigurációt, és az eredményt az $PrivateLinkConfiguration nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="88df6-111">This command creates an PrivateLink configuration named 'privateLinkConfig01' and stores the result in the variable named $PrivateLinkConfiguration.</span></span>

### <span data-ttu-id="88df6-112">2. példa: privát hivatkozás-konfiguráció létrehozása több IP-konfigurációval</span><span class="sxs-lookup"><span data-stu-id="88df6-112">Example 2: Create an Private Link Configuration with multiple Ip Configurations</span></span>
```powershell
PS C:\> $PrivateLinkConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration1, $privateLinkIpConfiguration2
```

<span data-ttu-id="88df6-113">Ez a parancs létrehoz egy "privateLinkConfig01" nevű PrivateLink-konfigurációt két ipConfigurations, és az eredményt az $PrivateLinkConfiguration nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="88df6-113">This command creates an PrivateLink configuration named 'privateLinkConfig01' with two ipConfigurations and stores the result in the variable named $PrivateLinkConfiguration.</span></span> 

## <span data-ttu-id="88df6-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="88df6-114">PARAMETERS</span></span>

### <span data-ttu-id="88df6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88df6-115">-DefaultProfile</span></span>
<span data-ttu-id="88df6-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="88df6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88df6-117">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="88df6-117">-IpConfiguration</span></span>
<span data-ttu-id="88df6-118">A ipConfiguration listája</span><span class="sxs-lookup"><span data-stu-id="88df6-118">The list of ipConfiguration</span></span>

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

### <span data-ttu-id="88df6-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="88df6-119">-Name</span></span>
<span data-ttu-id="88df6-120">A privateLink konfigurációjának neve</span><span class="sxs-lookup"><span data-stu-id="88df6-120">The name of the privateLink configuration</span></span>

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

### <span data-ttu-id="88df6-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="88df6-121">-Confirm</span></span>
<span data-ttu-id="88df6-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="88df6-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88df6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88df6-123">-WhatIf</span></span>
<span data-ttu-id="88df6-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="88df6-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88df6-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="88df6-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88df6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88df6-126">CommonParameters</span></span>
<span data-ttu-id="88df6-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="88df6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88df6-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="88df6-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88df6-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="88df6-129">INPUTS</span></span>

### <span data-ttu-id="88df6-130">Microsoft. Azure. commands. Network. models. PSApplicationGatewayPrivateLinkIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="88df6-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="88df6-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="88df6-131">OUTPUTS</span></span>

### <span data-ttu-id="88df6-132">Microsoft. Azure. commands. Network. models. PSApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="88df6-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="88df6-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="88df6-133">NOTES</span></span>

## <span data-ttu-id="88df6-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="88df6-134">RELATED LINKS</span></span>

[<span data-ttu-id="88df6-135">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="88df6-135">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="88df6-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="88df6-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="88df6-137">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="88df6-137">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="88df6-138">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="88df6-138">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)
