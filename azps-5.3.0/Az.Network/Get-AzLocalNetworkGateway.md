---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLocalNetworkGateway.md
ms.openlocfilehash: 14c0ec31f10a6405fb2a3f412f004d53dbdeb9a8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380070"
---
# <span data-ttu-id="1af9e-101">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1af9e-101">Get-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="1af9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1af9e-102">SYNOPSIS</span></span>
<span data-ttu-id="1af9e-103">Helyi hálózati átjárót kap</span><span class="sxs-lookup"><span data-stu-id="1af9e-103">Gets a Local Network Gateway</span></span>

## <span data-ttu-id="1af9e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1af9e-104">SYNTAX</span></span>

```
Get-AzLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1af9e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1af9e-105">DESCRIPTION</span></span>
<span data-ttu-id="1af9e-106">A helyi hálózati átjáró a virtuális magánhálózati eszköz helyszíni objektumának megfelelő objektum.</span><span class="sxs-lookup"><span data-stu-id="1af9e-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="1af9e-107">A **Get-AzLocalNetworkGateway** parancsmag a név és az erőforráscsoport neve alapján visszaadja a helyi átjárónak megfelelő objektumot.</span><span class="sxs-lookup"><span data-stu-id="1af9e-107">The **Get-AzLocalNetworkGateway** cmdlet returns the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="1af9e-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1af9e-108">EXAMPLES</span></span>

### <span data-ttu-id="1af9e-109">1. példa: Helyi hálózati átjáró létrehozása</span><span class="sxs-lookup"><span data-stu-id="1af9e-109">Example 1: Get a Local Network Gateway</span></span>
```powershell
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

<span data-ttu-id="1af9e-110">A helyi hálózati átjáró "myLocalGW1" nevű objektumát adja eredményül a "myRG" erőforráscsoporton belül.</span><span class="sxs-lookup"><span data-stu-id="1af9e-110">Returns the object of the Local Network Gateway with the name "myLocalGW1" within the resource group "myRG"</span></span>

### <span data-ttu-id="1af9e-111">2. példa: Helyi hálózati átjárók behozása szűrés használatával</span><span class="sxs-lookup"><span data-stu-id="1af9e-111">Example 2: Get Local Network Gateways using filtering</span></span>
```powershell
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

<span data-ttu-id="1af9e-112">A helyi hálózati átjárónak a "myRG" erőforráscsoporton belüli "myLocalGW" névvel kezdődő nevű objektumát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="1af9e-112">Returns the object of the Local Network Gateway with name starting with "myLocalGW" within the resource group "myRG"</span></span>

## <span data-ttu-id="1af9e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1af9e-113">PARAMETERS</span></span>

### <span data-ttu-id="1af9e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1af9e-114">-DefaultProfile</span></span>
<span data-ttu-id="1af9e-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1af9e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1af9e-116">-Name</span><span class="sxs-lookup"><span data-stu-id="1af9e-116">-Name</span></span>
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

### <span data-ttu-id="1af9e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1af9e-117">-ResourceGroupName</span></span>
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

### <span data-ttu-id="1af9e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1af9e-118">CommonParameters</span></span>
<span data-ttu-id="1af9e-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1af9e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1af9e-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1af9e-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1af9e-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1af9e-121">INPUTS</span></span>

### <span data-ttu-id="1af9e-122">System.String</span><span class="sxs-lookup"><span data-stu-id="1af9e-122">System.String</span></span>

## <span data-ttu-id="1af9e-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1af9e-123">OUTPUTS</span></span>

### <span data-ttu-id="1af9e-124">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1af9e-124">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="1af9e-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1af9e-125">NOTES</span></span>

## <span data-ttu-id="1af9e-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1af9e-126">RELATED LINKS</span></span>

[<span data-ttu-id="1af9e-127">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1af9e-127">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="1af9e-128">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1af9e-128">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)

[<span data-ttu-id="1af9e-129">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1af9e-129">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
