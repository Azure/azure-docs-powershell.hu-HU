---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azradiusserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRadiusServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRadiusServer.md
ms.openlocfilehash: 0f92f09d3caf481f845c96942fd038a82c1078ee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154250"
---
# <span data-ttu-id="0d2b3-101">New-AzRadiusServer</span><span class="sxs-lookup"><span data-stu-id="0d2b3-101">New-AzRadiusServer</span></span>

## <span data-ttu-id="0d2b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d2b3-102">SYNOPSIS</span></span>
<span data-ttu-id="0d2b3-103">Külső sugárkiszolgáló-konfigurációt hoz létre</span><span class="sxs-lookup"><span data-stu-id="0d2b3-103">Creates an external radius server configuration</span></span>

## <span data-ttu-id="0d2b3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0d2b3-104">SYNTAX</span></span>

```
New-AzRadiusServer -RadiusServerAddress <String> -RadiusServerSecret <SecureString>
 [-RadiusServerScore <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d2b3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0d2b3-105">DESCRIPTION</span></span>
<span data-ttu-id="0d2b3-106">A New-AzRadiusServer parancsmag létrehoz egy külső sugárkiszolgáló-konfigurációt, amely a virtuális hálózati átjáró és a VPN-kiszolgáló konfigurációjában használható.</span><span class="sxs-lookup"><span data-stu-id="0d2b3-106">The New-AzRadiusServer cmdlet creates an external radius server configuration to be used in virtual network gateway and VPN server configuration.</span></span>

## <span data-ttu-id="0d2b3-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0d2b3-107">EXAMPLES</span></span>

### <span data-ttu-id="0d2b3-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="0d2b3-108">Example 1</span></span>
```powershell
PS C:\> $radiusServer1 = New-AzRadiusServer -RadiusServerAddress 10.1.0.1 -RadiusServerSecret $radiuspd -RadiusServerScore 30
PS C:\> $radiusServer2 = New-AzRadiusServer -RadiusServerAddress 10.1.0.2 -RadiusServerSecret $radiuspd -RadiusServerScore 1
PS C:\> New-AzVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku VpnGw1 -VpnClientAddressPool 201.169.0.0/16 -VpnClientProtocol "IkeV2" -RadiusServerList $radiusServers
```

<span data-ttu-id="0d2b3-109">Több külső sugárkiszolgáló-konfiguráció létrehozása a P2S új virtuális hálózati átjárón való konfigurálásához.</span><span class="sxs-lookup"><span data-stu-id="0d2b3-109">Creating multiple external radius server configurations to be used for configuring P2S on a new virtual network gateway.</span></span>

## <span data-ttu-id="0d2b3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0d2b3-110">PARAMETERS</span></span>

### <span data-ttu-id="0d2b3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d2b3-111">-DefaultProfile</span></span>
<span data-ttu-id="0d2b3-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0d2b3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d2b3-113">-ServerAddress</span><span class="sxs-lookup"><span data-stu-id="0d2b3-113">-RadiusServerAddress</span></span>
<span data-ttu-id="0d2b3-114">Külső sugárkiszolgáló címe</span><span class="sxs-lookup"><span data-stu-id="0d2b3-114">External radius server address</span></span>

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

### <span data-ttu-id="0d2b3-115">-ServerScore</span><span class="sxs-lookup"><span data-stu-id="0d2b3-115">-RadiusServerScore</span></span>
<span data-ttu-id="0d2b3-116">Külső sugárkiszolgáló pontszáma</span><span class="sxs-lookup"><span data-stu-id="0d2b3-116">External radius server score</span></span>

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

### <span data-ttu-id="0d2b3-117">-ServerSecret</span><span class="sxs-lookup"><span data-stu-id="0d2b3-117">-RadiusServerSecret</span></span>
<span data-ttu-id="0d2b3-118">Külső sugárkiszolgáló-titkos</span><span class="sxs-lookup"><span data-stu-id="0d2b3-118">External radius server secret</span></span>

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

### <span data-ttu-id="0d2b3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d2b3-119">CommonParameters</span></span>
<span data-ttu-id="0d2b3-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d2b3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d2b3-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0d2b3-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d2b3-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0d2b3-122">INPUTS</span></span>

### <span data-ttu-id="0d2b3-123">System.String</span><span class="sxs-lookup"><span data-stu-id="0d2b3-123">System.String</span></span>

### <span data-ttu-id="0d2b3-124">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="0d2b3-124">System.Security.SecureString</span></span>

### <span data-ttu-id="0d2b3-125">System.Int32</span><span class="sxs-lookup"><span data-stu-id="0d2b3-125">System.Int32</span></span>

## <span data-ttu-id="0d2b3-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0d2b3-126">OUTPUTS</span></span>

### <span data-ttu-id="0d2b3-127">Microsoft.Azure.Commands.Network.Models.PSRadiusServer</span><span class="sxs-lookup"><span data-stu-id="0d2b3-127">Microsoft.Azure.Commands.Network.Models.PSRadiusServer</span></span>

## <span data-ttu-id="0d2b3-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0d2b3-128">NOTES</span></span>

## <span data-ttu-id="0d2b3-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0d2b3-129">RELATED LINKS</span></span>
