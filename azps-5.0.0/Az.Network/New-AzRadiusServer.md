---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azradiusserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRadiusServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRadiusServer.md
ms.openlocfilehash: 0f92f09d3caf481f845c96942fd038a82c1078ee
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301919"
---
# <span data-ttu-id="01a03-101">New-AzRadiusServer</span><span class="sxs-lookup"><span data-stu-id="01a03-101">New-AzRadiusServer</span></span>

## <span data-ttu-id="01a03-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="01a03-102">SYNOPSIS</span></span>
<span data-ttu-id="01a03-103">Külső RADIUS-kiszolgáló konfigurációjának létrehozása</span><span class="sxs-lookup"><span data-stu-id="01a03-103">Creates an external radius server configuration</span></span>

## <span data-ttu-id="01a03-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="01a03-104">SYNTAX</span></span>

```
New-AzRadiusServer -RadiusServerAddress <String> -RadiusServerSecret <SecureString>
 [-RadiusServerScore <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01a03-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="01a03-105">DESCRIPTION</span></span>
<span data-ttu-id="01a03-106">Az New-AzRadiusServer parancsmag létrehoz egy külső RADIUS-kiszolgáló konfigurációt, amelyet a virtuális hálózati átjáró és a VPN-kiszolgáló konfigurációja hoz létre.</span><span class="sxs-lookup"><span data-stu-id="01a03-106">The New-AzRadiusServer cmdlet creates an external radius server configuration to be used in virtual network gateway and VPN server configuration.</span></span>

## <span data-ttu-id="01a03-107">Példák</span><span class="sxs-lookup"><span data-stu-id="01a03-107">EXAMPLES</span></span>

### <span data-ttu-id="01a03-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="01a03-108">Example 1</span></span>
```powershell
PS C:\> $radiusServer1 = New-AzRadiusServer -RadiusServerAddress 10.1.0.1 -RadiusServerSecret $radiuspd -RadiusServerScore 30
PS C:\> $radiusServer2 = New-AzRadiusServer -RadiusServerAddress 10.1.0.2 -RadiusServerSecret $radiuspd -RadiusServerScore 1
PS C:\> New-AzVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku VpnGw1 -VpnClientAddressPool 201.169.0.0/16 -VpnClientProtocol "IkeV2" -RadiusServerList $radiusServers
```

<span data-ttu-id="01a03-109">Több külső RADIUS-kiszolgáló konfigurációjának létrehozása az új virtuális hálózati átjáró P2S konfigurálásához.</span><span class="sxs-lookup"><span data-stu-id="01a03-109">Creating multiple external radius server configurations to be used for configuring P2S on a new virtual network gateway.</span></span>

## <span data-ttu-id="01a03-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="01a03-110">PARAMETERS</span></span>

### <span data-ttu-id="01a03-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01a03-111">-DefaultProfile</span></span>
<span data-ttu-id="01a03-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="01a03-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01a03-113">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="01a03-113">-RadiusServerAddress</span></span>
<span data-ttu-id="01a03-114">Külső RADIUS-kiszolgáló címe</span><span class="sxs-lookup"><span data-stu-id="01a03-114">External radius server address</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01a03-115">-RadiusServerScore</span><span class="sxs-lookup"><span data-stu-id="01a03-115">-RadiusServerScore</span></span>
<span data-ttu-id="01a03-116">Külső RADIUS-kiszolgáló pontszáma</span><span class="sxs-lookup"><span data-stu-id="01a03-116">External radius server score</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01a03-117">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="01a03-117">-RadiusServerSecret</span></span>
<span data-ttu-id="01a03-118">Külső RADIUS-kiszolgáló titka</span><span class="sxs-lookup"><span data-stu-id="01a03-118">External radius server secret</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01a03-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01a03-119">CommonParameters</span></span>
<span data-ttu-id="01a03-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="01a03-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01a03-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="01a03-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01a03-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="01a03-122">INPUTS</span></span>

### <span data-ttu-id="01a03-123">System. String</span><span class="sxs-lookup"><span data-stu-id="01a03-123">System.String</span></span>

### <span data-ttu-id="01a03-124">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="01a03-124">System.Security.SecureString</span></span>

### <span data-ttu-id="01a03-125">System. Int32</span><span class="sxs-lookup"><span data-stu-id="01a03-125">System.Int32</span></span>

## <span data-ttu-id="01a03-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="01a03-126">OUTPUTS</span></span>

### <span data-ttu-id="01a03-127">Microsoft. Azure. commands. Network. models. PSRadiusServer</span><span class="sxs-lookup"><span data-stu-id="01a03-127">Microsoft.Azure.Commands.Network.Models.PSRadiusServer</span></span>

## <span data-ttu-id="01a03-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="01a03-128">NOTES</span></span>

## <span data-ttu-id="01a03-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="01a03-129">RELATED LINKS</span></span>
