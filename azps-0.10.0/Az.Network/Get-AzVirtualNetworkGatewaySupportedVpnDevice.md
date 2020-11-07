---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaysupportedvpndevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
ms.openlocfilehash: 794f432b06c693d6758603975a98ca6b2f5e3511
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841486"
---
# <span data-ttu-id="13850-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span><span class="sxs-lookup"><span data-stu-id="13850-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span></span>

## <span data-ttu-id="13850-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="13850-102">SYNOPSIS</span></span>
<span data-ttu-id="13850-103">Ez a parancsmagot a támogatott VPN-eszközök márkái, modelljei és firmware-verziói listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="13850-103">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="13850-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="13850-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewaySupportedVpnDevice -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13850-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="13850-105">DESCRIPTION</span></span>
<span data-ttu-id="13850-106">Ez a parancsmagot a támogatott VPN-eszközök márkái, modelljei és firmware-verziói listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="13850-106">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="13850-107">Példák</span><span class="sxs-lookup"><span data-stu-id="13850-107">EXAMPLES</span></span>

### <span data-ttu-id="13850-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="13850-108">Example 1</span></span>
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

<span data-ttu-id="13850-109">A támogatott VPN-eszközök márkái, modelljei és firmware-verziói listáját jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="13850-109">Returns list of supported VPN device brands, models and firmware versions:</span></span>
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>

## <span data-ttu-id="13850-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="13850-110">PARAMETERS</span></span>

### <span data-ttu-id="13850-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13850-111">-DefaultProfile</span></span>
<span data-ttu-id="13850-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="13850-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13850-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="13850-113">-Name</span></span>
<span data-ttu-id="13850-114">A virtuális hálózat átjárójának neve.</span><span class="sxs-lookup"><span data-stu-id="13850-114">The virtual network gateway name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13850-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13850-115">-ResourceGroupName</span></span>
<span data-ttu-id="13850-116">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="13850-116">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13850-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13850-117">CommonParameters</span></span>
<span data-ttu-id="13850-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="13850-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13850-119">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13850-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13850-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="13850-120">INPUTS</span></span>

### <span data-ttu-id="13850-121">System. String</span><span class="sxs-lookup"><span data-stu-id="13850-121">System.String</span></span>

## <span data-ttu-id="13850-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="13850-122">OUTPUTS</span></span>

### <span data-ttu-id="13850-123">System. String</span><span class="sxs-lookup"><span data-stu-id="13850-123">System.String</span></span>

## <span data-ttu-id="13850-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="13850-124">NOTES</span></span>

## <span data-ttu-id="13850-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="13850-125">RELATED LINKS</span></span>

