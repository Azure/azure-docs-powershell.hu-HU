---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzSecurityPartnerProvider.md
ms.openlocfilehash: 5af78bb1f915dec55f75749296340ca6d13a3b3d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301886"
---
# <span data-ttu-id="ffd5c-101">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="ffd5c-101">New-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="ffd5c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ffd5c-102">SYNOPSIS</span></span>
<span data-ttu-id="ffd5c-103">Azure-SecurityPartnerProvider hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ffd5c-103">Creates an Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="ffd5c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ffd5c-104">SYNTAX</span></span>

```
New-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String> -Location <String>
 -SecurityProviderName <String> [-VirtualHub <PSVirtualHub>] [-VirtualHubId <String>]
 [-VirtualHubName <String>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffd5c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ffd5c-105">DESCRIPTION</span></span>
<span data-ttu-id="ffd5c-106">A **New-AzSecurityPartnerProvider** parancsmag létrehoz egy Azure SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="ffd5c-106">The **New-AzSecurityPartnerProvider** cmdlet creates an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="ffd5c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ffd5c-107">EXAMPLES</span></span>

### <span data-ttu-id="ffd5c-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ffd5c-108">Example 1</span></span>
```powershell
 New-AzSecurityPartnerProvider -Name securityPartnerProviderName -ResourceGroupName rgname -Location 'West US' -SecurityProviderName 'ZScaler'
```

## <span data-ttu-id="ffd5c-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ffd5c-109">PARAMETERS</span></span>

### <span data-ttu-id="ffd5c-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ffd5c-110">-AsJob</span></span>
<span data-ttu-id="ffd5c-111">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ffd5c-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ffd5c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffd5c-112">-DefaultProfile</span></span>
<span data-ttu-id="ffd5c-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ffd5c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffd5c-114">-Force</span><span class="sxs-lookup"><span data-stu-id="ffd5c-114">-Force</span></span>
<span data-ttu-id="ffd5c-115">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ffd5c-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="ffd5c-116">-Hely</span><span class="sxs-lookup"><span data-stu-id="ffd5c-116">-Location</span></span>
<span data-ttu-id="ffd5c-117">helyre.</span><span class="sxs-lookup"><span data-stu-id="ffd5c-117">location.</span></span>

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

### <span data-ttu-id="ffd5c-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ffd5c-118">-Name</span></span>
<span data-ttu-id="ffd5c-119">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="ffd5c-119">The resource name.</span></span>

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

### <span data-ttu-id="ffd5c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffd5c-120">-ResourceGroupName</span></span>
<span data-ttu-id="ffd5c-121">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="ffd5c-121">The resource group name.</span></span>

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

### <span data-ttu-id="ffd5c-122">-SecurityProviderName</span><span class="sxs-lookup"><span data-stu-id="ffd5c-122">-SecurityProviderName</span></span>
<span data-ttu-id="ffd5c-123">A biztonsági szolgáltató neve</span><span class="sxs-lookup"><span data-stu-id="ffd5c-123">The Security Provider name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ZScaler, IBoss, Checkpoint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffd5c-124">-Címke</span><span class="sxs-lookup"><span data-stu-id="ffd5c-124">-Tag</span></span>
<span data-ttu-id="ffd5c-125">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="ffd5c-125">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffd5c-126">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="ffd5c-126">-VirtualHub</span></span>
<span data-ttu-id="ffd5c-127">A biztonsági partner szolgáltatója által csatolt virtuális hub-azonosító</span><span class="sxs-lookup"><span data-stu-id="ffd5c-127">The virtual hub Id that the security partner provider is attached to</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ffd5c-128">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="ffd5c-128">-VirtualHubId</span></span>
<span data-ttu-id="ffd5c-129">Annak a VirtualHub az azonosítóját, amelyre ezt a VpnGateway társítani kell.</span><span class="sxs-lookup"><span data-stu-id="ffd5c-129">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffd5c-130">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="ffd5c-130">-VirtualHubName</span></span>
<span data-ttu-id="ffd5c-131">Annak a VirtualHub az azonosítóját, amelyre ezt a VpnGateway társítani kell.</span><span class="sxs-lookup"><span data-stu-id="ffd5c-131">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffd5c-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ffd5c-132">-Confirm</span></span>
<span data-ttu-id="ffd5c-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ffd5c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffd5c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffd5c-134">-WhatIf</span></span>
<span data-ttu-id="ffd5c-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ffd5c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffd5c-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ffd5c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffd5c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffd5c-137">CommonParameters</span></span>
<span data-ttu-id="ffd5c-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ffd5c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffd5c-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ffd5c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffd5c-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ffd5c-140">INPUTS</span></span>

### <span data-ttu-id="ffd5c-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ffd5c-141">System.String</span></span>

### <span data-ttu-id="ffd5c-142">Microsoft. Azure. commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="ffd5c-142">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="ffd5c-143">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ffd5c-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ffd5c-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ffd5c-144">OUTPUTS</span></span>

### <span data-ttu-id="ffd5c-145">Microsoft. Azure. commands. Network. models. PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="ffd5c-145">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="ffd5c-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ffd5c-146">NOTES</span></span>

## <span data-ttu-id="ffd5c-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ffd5c-147">RELATED LINKS</span></span>
