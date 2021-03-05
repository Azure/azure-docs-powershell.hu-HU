---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azipconfigurationbgppeeringaddressobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpConfigurationBgpPeeringAddressObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpConfigurationBgpPeeringAddressObject.md
ms.openlocfilehash: ba713650670abdeb9c64242109b30f47d99724f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001109"
---
# <span data-ttu-id="71c98-101">New-AzIpConfigurationBgpPeeringAddressObject</span><span class="sxs-lookup"><span data-stu-id="71c98-101">New-AzIpConfigurationBgpPeeringAddressObject</span></span>

## <span data-ttu-id="71c98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71c98-102">SYNOPSIS</span></span>
<span data-ttu-id="71c98-103">létrehoz egy új IpconfigurationBgpPeeringAddressObject</span><span class="sxs-lookup"><span data-stu-id="71c98-103">creates a new IpconfigurationBgpPeeringAddressObject</span></span>

## <span data-ttu-id="71c98-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="71c98-104">SYNTAX</span></span>

### <span data-ttu-id="71c98-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="71c98-105">Default (Default)</span></span>
```
New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId <String>
 -CustomAddress <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```
## <span data-ttu-id="71c98-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="71c98-106">DESCRIPTION</span></span>
<span data-ttu-id="71c98-107">A **New-AzIpConfigurationBgpPeeringAddressObject** létrehoz egy IpConfigurationBgpPeeringAddressObject objektumot, amely a BgpPeeringAddresses tulajdonságot képviseli a virtuális hálózati átjáró bgpsettings szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="71c98-107">The **New-AzIpConfigurationBgpPeeringAddressObject** creates a IpConfigurationBgpPeeringAddressObject object which represents BgpPeeringAddresses property in your virtual network gateway bgpsettings.</span></span>

## <span data-ttu-id="71c98-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="71c98-108">EXAMPLES</span></span>

### <span data-ttu-id="71c98-109">1: AzIpConfigurationBgpPeeringAddressObject létrehozása</span><span class="sxs-lookup"><span data-stu-id="71c98-109">1: Create a AzIpConfigurationBgpPeeringAddressObject</span></span>
```
$ipconfigurationId1 = '/subscriptions/c886bc58-0000-4e01-993f-e01ba3702aaf/resourceGroups/testRg/providers/Microsoft.Network/virtualNetworkGateways/gw1/ipConfigurations/default'
$addresslist1 = @('169.254.21.5')
$gw1ipconfBgp1 = New-AzIpConfigurationBgpPeeringAddresses -IpConfigurationId $ipconfigurationId1 -CustomAddress $addresslist1
```

<span data-ttu-id="71c98-110">A fenti ipConfigurationBgpPeeringAddressObject.Ez az új objektum a gw1ipconfBgp1 lesz.</span><span class="sxs-lookup"><span data-stu-id="71c98-110">The above will create a IpConfigurationBgpPeeringAddressObject.This new object will be to gw1ipconfBgp1.</span></span>

## <span data-ttu-id="71c98-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71c98-111">PARAMETERS</span></span>

### <span data-ttu-id="71c98-112">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71c98-112">-Confirm</span></span>
<span data-ttu-id="71c98-113">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="71c98-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71c98-114">-CustomAddress</span><span class="sxs-lookup"><span data-stu-id="71c98-114">-CustomAddress</span></span>
<span data-ttu-id="71c98-115">A virtual network gateway CustomAddress List for BgpPeeringAddresses.</span><span class="sxs-lookup"><span data-stu-id="71c98-115">The virtual network gateway CustomAddress List for BgpPeeringAddresses.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71c98-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71c98-116">-DefaultProfile</span></span>
<span data-ttu-id="71c98-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="71c98-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71c98-118">-IpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="71c98-118">-IpConfigurationId</span></span>
<span data-ttu-id="71c98-119">A virtuális hálózati átjáró IpConfigurationId for BgpPeeringAddresses.</span><span class="sxs-lookup"><span data-stu-id="71c98-119">The virtual network gateway IpConfigurationId for BgpPeeringAddresses.</span></span>

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

### <span data-ttu-id="71c98-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71c98-120">-WhatIf</span></span>
<span data-ttu-id="71c98-121">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="71c98-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71c98-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="71c98-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71c98-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71c98-123">CommonParameters</span></span>
<span data-ttu-id="71c98-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71c98-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71c98-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="71c98-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71c98-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="71c98-126">INPUTS</span></span>

### <span data-ttu-id="71c98-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="71c98-127">None</span></span>

## <span data-ttu-id="71c98-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="71c98-128">OUTPUTS</span></span>

### <span data-ttu-id="71c98-129">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="71c98-129">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress</span></span>

## <span data-ttu-id="71c98-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="71c98-130">NOTES</span></span>

## <span data-ttu-id="71c98-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="71c98-131">RELATED LINKS</span></span>
