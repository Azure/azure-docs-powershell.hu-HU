---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionikesa
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionIkeSa.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionIkeSa.md
ms.openlocfilehash: 6b0eb456c2134e6ed64d8e6c441db041776fcf39
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147035"
---
# <span data-ttu-id="04056-101">Get-AzVirtualNetworkGatewayConnectionIkeSa</span><span class="sxs-lookup"><span data-stu-id="04056-101">Get-AzVirtualNetworkGatewayConnectionIkeSa</span></span>

## <span data-ttu-id="04056-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04056-102">SYNOPSIS</span></span>
<span data-ttu-id="04056-103">Virtuális hálózati átjárókapcsolat IKE biztonsági társításának lekésse</span><span class="sxs-lookup"><span data-stu-id="04056-103">Get IKE Security Associations of a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="04056-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="04056-104">SYNTAX</span></span>

### <span data-ttu-id="04056-105">ByName</span><span class="sxs-lookup"><span data-stu-id="04056-105">ByName</span></span>
```
Get-AzVirtualNetworkGatewayConnectionIkeSa [-Name <String>] -ResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04056-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="04056-106">ByInputObject</span></span>
```
Get-AzVirtualNetworkGatewayConnectionIkeSa -InputObject <PSVirtualNetworkGatewayConnection> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04056-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="04056-107">ByResourceId</span></span>
```
Get-AzVirtualNetworkGatewayConnectionIkeSa [-ResourceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04056-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="04056-108">DESCRIPTION</span></span>
<span data-ttu-id="04056-109">A **Get-AzVirtualNetworkGatewayConnectionIkeSa** parancsmag a kapcsolat IKE biztonsági társítását adja vissza a Kapcsolat neve és az Erőforráscsoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="04056-109">The **Get-AzVirtualNetworkGatewayConnectionIkeSa** cmdlet returns the IKE Security Associations of your connection based on the Connection Name and Resource Group Name.</span></span>
<span data-ttu-id="04056-110">Ha a **Get-AzVirtualNetworkGatewayConnection** parancsmagot a -Name paraméter megadása nélkül bocsátotta ki, a kimenet nem fogja az IKE biztonsági társításokat mutatni.</span><span class="sxs-lookup"><span data-stu-id="04056-110">If the **Get-AzVirtualNetworkGatewayConnection** cmdlet is issued without specifying the -Name parameter, the output will not show the IKE Security Associations.</span></span>

## <span data-ttu-id="04056-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="04056-111">EXAMPLES</span></span>

### <span data-ttu-id="04056-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="04056-112">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualNetworkGatewayConnectionIkeSa -ResourceGroupName myRG -Name myTunnel
localEndpoint              : 52.180.160.154
remoteEndpoint             : 104.208.54.1
initiatorCookie            : 5490733703579933026
responderCookie            : 15460013388959380535
localUdpEncapsulationPort  : 0
remoteUdpEncapsulationPort : 0
encryption                 : AES256
integrity                  : SHA1
dhGroup                    : DHGroup2
lifeTimeSeconds            : 28800
isSaInitiator              : True
elapsedTimeInseconds       : 23092
quickModeSa                : {}
```

<span data-ttu-id="04056-113">A "myRG" erőforráscsoporton belül a "myTunnel" nevű virtuális hálózati átjáró kapcsolat IKE biztonsági társítását adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="04056-113">Returns the IKE Security Associations for the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="04056-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04056-114">PARAMETERS</span></span>

### <span data-ttu-id="04056-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="04056-115">-AsJob</span></span>
<span data-ttu-id="04056-116">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="04056-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="04056-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04056-117">-DefaultProfile</span></span>
<span data-ttu-id="04056-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="04056-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04056-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="04056-119">-InputObject</span></span>
<span data-ttu-id="04056-120">Az a virtuális hálózati átjáró kapcsolati objektuma, amelyhez le kell kérni az IKE SAs-t.</span><span class="sxs-lookup"><span data-stu-id="04056-120">The virtual network gateway connection object for which IKE SAs needs to be fetched.</span></span>

```yaml
Type: PSVirtualNetworkGatewayConnection
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04056-121">-Name</span><span class="sxs-lookup"><span data-stu-id="04056-121">-Name</span></span>
<span data-ttu-id="04056-122">Az a virtuális hálózati átjáró kapcsolatneve, amelyhez le kell kérni az IKE SAs-t.</span><span class="sxs-lookup"><span data-stu-id="04056-122">The virtual network gateway connection name for which IKE SAs needs to be fetched.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ResourceName, ConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04056-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04056-123">-ResourceGroupName</span></span>
<span data-ttu-id="04056-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="04056-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04056-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="04056-125">-ResourceId</span></span>
<span data-ttu-id="04056-126">A virtuális hálózati átjáró kapcsolatának Azure-erőforrásazonosítója, amelyhez le kell kérni az IKE SAs-t.</span><span class="sxs-lookup"><span data-stu-id="04056-126">The Azure resource ID of the Virtual Network Gateway Connection for which IKE SAs needs to be fetched.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04056-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04056-127">CommonParameters</span></span>
<span data-ttu-id="04056-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04056-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04056-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="04056-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04056-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="04056-130">INPUTS</span></span>

### <span data-ttu-id="04056-131">System.String</span><span class="sxs-lookup"><span data-stu-id="04056-131">System.String</span></span>

## <span data-ttu-id="04056-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="04056-132">OUTPUTS</span></span>

### <span data-ttu-id="04056-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnectionIkeSa</span><span class="sxs-lookup"><span data-stu-id="04056-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnectionIkeSa</span></span>

## <span data-ttu-id="04056-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="04056-134">NOTES</span></span>

## <span data-ttu-id="04056-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="04056-135">RELATED LINKS</span></span>
