---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLocalNetworkGateway.md
ms.openlocfilehash: 04cec0db46eef985819ea44355b9bbedf792dbf2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670544"
---
# <span data-ttu-id="467a7-101">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="467a7-101">Get-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="467a7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="467a7-102">SYNOPSIS</span></span>
<span data-ttu-id="467a7-103">Helyi hálózati átjárót kap</span><span class="sxs-lookup"><span data-stu-id="467a7-103">Gets a Local Network Gateway</span></span>

## <span data-ttu-id="467a7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="467a7-104">SYNTAX</span></span>

```
Get-AzLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="467a7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="467a7-105">DESCRIPTION</span></span>
<span data-ttu-id="467a7-106">A helyi hálózat átjárója a helyszíni VPN-eszközt jelképező objektum.</span><span class="sxs-lookup"><span data-stu-id="467a7-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="467a7-107">A **Get-AzLocalNetworkGateway** parancsmag a helyszíni átjáró nevét és az erőforráscsoport neve alapján adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="467a7-107">The **Get-AzLocalNetworkGateway** cmdlet returns the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="467a7-108">Példák</span><span class="sxs-lookup"><span data-stu-id="467a7-108">EXAMPLES</span></span>

### <span data-ttu-id="467a7-109">1: helyi hálózati átjáró beszerzése</span><span class="sxs-lookup"><span data-stu-id="467a7-109">1: Get a Local Network Gateway</span></span>
```
Get-AzLocalNetworkGateway -Name myLocalGW1 -ResourceGroupName myRG

Name                     : myLocalGW1
ResourceGroupName        : myRG
Location                 : eastus
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                           icrosoft.Network/localNetworkGateways/myLocalGW1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
GatewayIpAddress         : x.x.x.x
LocalNetworkAddressSpace : {
                             "AddressPrefixes": []
                           }
BgpSettings              : null
```

<span data-ttu-id="467a7-110">A helyi hálózati átjáró objektumát adja eredményül, az "myRG" erőforráscsoporthoz tartozó "myLocalGW1" névvel</span><span class="sxs-lookup"><span data-stu-id="467a7-110">Returns the object of the Local Network Gateway with the name "myLocalGW1" within the resource group "myRG"</span></span>

### <span data-ttu-id="467a7-111">2: a helyi hálózati átjárók beszerzése szűréssel</span><span class="sxs-lookup"><span data-stu-id="467a7-111">2: Get Local Network Gateways using filtering</span></span>
```
Get-AzLocalNetworkGateway -Name myLocalGW* -ResourceGroupName myRG

Name                     : myLocalGW1
ResourceGroupName        : myRG
Location                 : eastus
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                           icrosoft.Network/localNetworkGateways/myLocalGW1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
GatewayIpAddress         : x.x.x.x
LocalNetworkAddressSpace : {
                             "AddressPrefixes": []
                           }
BgpSettings              : null

Name                     : myLocalGW2
ResourceGroupName        : myRG
Location                 : eastus
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                           icrosoft.Network/localNetworkGateways/myLocalGW2
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
GatewayIpAddress         : x.x.x.x
LocalNetworkAddressSpace : {
                             "AddressPrefixes": []
                           }
BgpSettings              : null
```

<span data-ttu-id="467a7-112">A helyi hálózati átjáró objektumát adja eredményül, az "myRG" erőforráscsoporthoz tartozó "myLocalGW" névvel kezdve</span><span class="sxs-lookup"><span data-stu-id="467a7-112">Returns the object of the Local Network Gateway with name starting with "myLocalGW" within the resource group "myRG"</span></span>

## <span data-ttu-id="467a7-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="467a7-113">PARAMETERS</span></span>

### <span data-ttu-id="467a7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="467a7-114">-DefaultProfile</span></span>
<span data-ttu-id="467a7-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="467a7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="467a7-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="467a7-116">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="467a7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="467a7-117">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="467a7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="467a7-118">CommonParameters</span></span>
<span data-ttu-id="467a7-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="467a7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="467a7-120">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="467a7-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="467a7-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="467a7-121">INPUTS</span></span>

### <span data-ttu-id="467a7-122">System. String</span><span class="sxs-lookup"><span data-stu-id="467a7-122">System.String</span></span>

## <span data-ttu-id="467a7-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="467a7-123">OUTPUTS</span></span>

### <span data-ttu-id="467a7-124">Microsoft. Azure. commands. Network. models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="467a7-124">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="467a7-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="467a7-125">NOTES</span></span>

## <span data-ttu-id="467a7-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="467a7-126">RELATED LINKS</span></span>

[<span data-ttu-id="467a7-127">Új – AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="467a7-127">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="467a7-128">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="467a7-128">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)

[<span data-ttu-id="467a7-129">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="467a7-129">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
