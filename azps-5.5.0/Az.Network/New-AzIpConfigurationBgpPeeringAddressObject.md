---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipconfigurationbgppeeringaddressobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpConfigurationBgpPeeringAddressObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpConfigurationBgpPeeringAddressObject.md
ms.openlocfilehash: 2a31aa9db3264dd24c6d77bdad7b10d6ecad10b1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151682"
---
# <span data-ttu-id="9668f-101">New-AzIpConfigurationBgpPeeringAddressObject</span><span class="sxs-lookup"><span data-stu-id="9668f-101">New-AzIpConfigurationBgpPeeringAddressObject</span></span>

## <span data-ttu-id="9668f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9668f-102">SYNOPSIS</span></span>
<span data-ttu-id="9668f-103">létrehoz egy új IpconfigurationBgpPeeringAddressObject</span><span class="sxs-lookup"><span data-stu-id="9668f-103">creates a new IpconfigurationBgpPeeringAddressObject</span></span>

## <span data-ttu-id="9668f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9668f-104">SYNTAX</span></span>

### <span data-ttu-id="9668f-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9668f-105">Default (Default)</span></span>
```
New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId <String>
 -CustomAddress <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```
## <span data-ttu-id="9668f-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9668f-106">DESCRIPTION</span></span>
<span data-ttu-id="9668f-107">A **New-AzIpConfigurationBgpPeeringAddressObject** létrehoz egy IpConfigurationBgpPeeringAddressObject objektumot, amely a BgpPeeringAddresses tulajdonságot képviseli a virtuális hálózati átjáró bgpsettings szolgáltatásában.</span><span class="sxs-lookup"><span data-stu-id="9668f-107">The **New-AzIpConfigurationBgpPeeringAddressObject** creates a IpConfigurationBgpPeeringAddressObject object which represents BgpPeeringAddresses property in your virtual network gateway bgpsettings.</span></span>

## <span data-ttu-id="9668f-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9668f-108">EXAMPLES</span></span>

### <span data-ttu-id="9668f-109">1: AzIpConfigurationBgpPeeringAddressObject létrehozása</span><span class="sxs-lookup"><span data-stu-id="9668f-109">1: Create a AzIpConfigurationBgpPeeringAddressObject</span></span>
```
$ipconfigurationId1 = '/subscriptions/c886bc58-0000-4e01-993f-e01ba3702aaf/resourceGroups/testRg/providers/Microsoft.Network/virtualNetworkGateways/gw1/ipConfigurations/default'
$addresslist1 = @('169.254.21.5')
$gw1ipconfBgp1 = New-AzIpConfigurationBgpPeeringAddresses -IpConfigurationId $ipconfigurationId1 -CustomAddress $addresslist1
```

<span data-ttu-id="9668f-110">A fenti ipConfigurationBgpPeeringAddressObject.Ez az új objektum a gw1ipconfBgp1 lesz.</span><span class="sxs-lookup"><span data-stu-id="9668f-110">The above will create a IpConfigurationBgpPeeringAddressObject.This new object will be to gw1ipconfBgp1.</span></span>

## <span data-ttu-id="9668f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9668f-111">PARAMETERS</span></span>

### <span data-ttu-id="9668f-112">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9668f-112">-Confirm</span></span>
<span data-ttu-id="9668f-113">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9668f-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9668f-114">-CustomAddress</span><span class="sxs-lookup"><span data-stu-id="9668f-114">-CustomAddress</span></span>
<span data-ttu-id="9668f-115">A virtual network gateway CustomAddress List for BgpPeeringAddresses.</span><span class="sxs-lookup"><span data-stu-id="9668f-115">The virtual network gateway CustomAddress List for BgpPeeringAddresses.</span></span>

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

### <span data-ttu-id="9668f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9668f-116">-DefaultProfile</span></span>
<span data-ttu-id="9668f-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9668f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9668f-118">-IpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="9668f-118">-IpConfigurationId</span></span>
<span data-ttu-id="9668f-119">A virtuális hálózati átjáró IpConfigurationId for BgpPeeringAddresses.</span><span class="sxs-lookup"><span data-stu-id="9668f-119">The virtual network gateway IpConfigurationId for BgpPeeringAddresses.</span></span>

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

### <span data-ttu-id="9668f-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9668f-120">-WhatIf</span></span>
<span data-ttu-id="9668f-121">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9668f-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9668f-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9668f-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9668f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9668f-123">CommonParameters</span></span>
<span data-ttu-id="9668f-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9668f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9668f-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9668f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9668f-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9668f-126">INPUTS</span></span>

### <span data-ttu-id="9668f-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="9668f-127">None</span></span>

## <span data-ttu-id="9668f-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9668f-128">OUTPUTS</span></span>

### <span data-ttu-id="9668f-129">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="9668f-129">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress</span></span>

## <span data-ttu-id="9668f-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9668f-130">NOTES</span></span>

## <span data-ttu-id="9668f-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9668f-131">RELATED LINKS</span></span>
