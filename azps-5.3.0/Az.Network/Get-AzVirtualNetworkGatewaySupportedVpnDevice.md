---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaysupportedvpndevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
ms.openlocfilehash: f643b280e0777f3251380ecf36f4fcc070b545c1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380993"
---
# <span data-ttu-id="11933-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span><span class="sxs-lookup"><span data-stu-id="11933-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span></span>

## <span data-ttu-id="11933-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11933-102">SYNOPSIS</span></span>
<span data-ttu-id="11933-103">Ez a parancsmag a támogatott VPN-eszközök márkáinak, modelljeinek és belső vezérlőprogram-verzióinak listáját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="11933-103">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="11933-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="11933-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewaySupportedVpnDevice -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11933-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="11933-105">DESCRIPTION</span></span>
<span data-ttu-id="11933-106">Ez a parancsmag a támogatott VPN-eszközök márkáinak, modelljeinek és belső vezérlőprogram-verzióinak listáját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="11933-106">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="11933-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="11933-107">EXAMPLES</span></span>

### <span data-ttu-id="11933-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="11933-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway 
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>
```

<span data-ttu-id="11933-109">A támogatott VPN-eszközök márkáinak, modelljeinek és belső vezérlőprogram-verzióinak listáját adja vissza:</span><span class="sxs-lookup"><span data-stu-id="11933-109">Returns list of supported VPN device brands, models and firmware versions:</span></span>
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>

## <span data-ttu-id="11933-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11933-110">PARAMETERS</span></span>

### <span data-ttu-id="11933-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11933-111">-DefaultProfile</span></span>
<span data-ttu-id="11933-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="11933-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11933-113">-Name</span><span class="sxs-lookup"><span data-stu-id="11933-113">-Name</span></span>
<span data-ttu-id="11933-114">A virtuális hálózati átjáró neve.</span><span class="sxs-lookup"><span data-stu-id="11933-114">The virtual network gateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11933-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11933-115">-ResourceGroupName</span></span>
<span data-ttu-id="11933-116">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="11933-116">The resource group name.</span></span>

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

### <span data-ttu-id="11933-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11933-117">CommonParameters</span></span>
<span data-ttu-id="11933-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11933-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11933-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11933-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11933-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="11933-120">INPUTS</span></span>

### <span data-ttu-id="11933-121">System.String</span><span class="sxs-lookup"><span data-stu-id="11933-121">System.String</span></span>

## <span data-ttu-id="11933-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="11933-122">OUTPUTS</span></span>

### <span data-ttu-id="11933-123">System.String</span><span class="sxs-lookup"><span data-stu-id="11933-123">System.String</span></span>

## <span data-ttu-id="11933-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="11933-124">NOTES</span></span>

## <span data-ttu-id="11933-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="11933-125">RELATED LINKS</span></span>
