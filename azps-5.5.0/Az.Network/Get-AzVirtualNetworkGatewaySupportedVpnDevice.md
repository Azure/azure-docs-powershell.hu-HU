---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaysupportedvpndevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
ms.openlocfilehash: f643b280e0777f3251380ecf36f4fcc070b545c1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151874"
---
# <span data-ttu-id="23526-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span><span class="sxs-lookup"><span data-stu-id="23526-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span></span>

## <span data-ttu-id="23526-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23526-102">SYNOPSIS</span></span>
<span data-ttu-id="23526-103">Ez a parancsmag a támogatott VPN-eszközök márkáinak, modelljeinek és belső vezérlőprogram-verzióinak listáját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="23526-103">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="23526-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="23526-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewaySupportedVpnDevice -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23526-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="23526-105">DESCRIPTION</span></span>
<span data-ttu-id="23526-106">Ez a parancsmag a támogatott VPN-eszközök márkáinak, modelljeinek és belső vezérlőprogram-verzióinak listáját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="23526-106">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="23526-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="23526-107">EXAMPLES</span></span>

### <span data-ttu-id="23526-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="23526-108">Example 1</span></span>
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

<span data-ttu-id="23526-109">A támogatott VPN-eszközök márkáinak, modelljeinek és belső vezérlőprogram-verzióinak listáját adja vissza:</span><span class="sxs-lookup"><span data-stu-id="23526-109">Returns list of supported VPN device brands, models and firmware versions:</span></span>
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>

## <span data-ttu-id="23526-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="23526-110">PARAMETERS</span></span>

### <span data-ttu-id="23526-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23526-111">-DefaultProfile</span></span>
<span data-ttu-id="23526-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="23526-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23526-113">-Name</span><span class="sxs-lookup"><span data-stu-id="23526-113">-Name</span></span>
<span data-ttu-id="23526-114">A virtuális hálózati átjáró neve.</span><span class="sxs-lookup"><span data-stu-id="23526-114">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="23526-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23526-115">-ResourceGroupName</span></span>
<span data-ttu-id="23526-116">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="23526-116">The resource group name.</span></span>

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

### <span data-ttu-id="23526-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23526-117">CommonParameters</span></span>
<span data-ttu-id="23526-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23526-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23526-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="23526-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23526-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="23526-120">INPUTS</span></span>

### <span data-ttu-id="23526-121">System.String</span><span class="sxs-lookup"><span data-stu-id="23526-121">System.String</span></span>

## <span data-ttu-id="23526-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="23526-122">OUTPUTS</span></span>

### <span data-ttu-id="23526-123">System.String</span><span class="sxs-lookup"><span data-stu-id="23526-123">System.String</span></span>

## <span data-ttu-id="23526-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="23526-124">NOTES</span></span>

## <span data-ttu-id="23526-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="23526-125">RELATED LINKS</span></span>
