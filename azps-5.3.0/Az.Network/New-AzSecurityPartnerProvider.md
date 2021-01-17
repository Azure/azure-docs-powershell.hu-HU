---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzSecurityPartnerProvider.md
ms.openlocfilehash: 5af78bb1f915dec55f75749296340ca6d13a3b3d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479984"
---
# <span data-ttu-id="a910f-101">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="a910f-101">New-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="a910f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a910f-102">SYNOPSIS</span></span>
<span data-ttu-id="a910f-103">Létrehoz egy Azure SecurityPartnerProvidert.</span><span class="sxs-lookup"><span data-stu-id="a910f-103">Creates an Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="a910f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a910f-104">SYNTAX</span></span>

```
New-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String> -Location <String>
 -SecurityProviderName <String> [-VirtualHub <PSVirtualHub>] [-VirtualHubId <String>]
 [-VirtualHubName <String>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a910f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a910f-105">DESCRIPTION</span></span>
<span data-ttu-id="a910f-106">A **New-AzSecurityPartnerProvider** parancsmag létrehoz egy Azure SecurityPartnerProvider-t</span><span class="sxs-lookup"><span data-stu-id="a910f-106">The **New-AzSecurityPartnerProvider** cmdlet creates an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="a910f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a910f-107">EXAMPLES</span></span>

### <span data-ttu-id="a910f-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="a910f-108">Example 1</span></span>
```powershell
 New-AzSecurityPartnerProvider -Name securityPartnerProviderName -ResourceGroupName rgname -Location 'West US' -SecurityProviderName 'ZScaler'
```

## <span data-ttu-id="a910f-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a910f-109">PARAMETERS</span></span>

### <span data-ttu-id="a910f-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a910f-110">-AsJob</span></span>
<span data-ttu-id="a910f-111">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a910f-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a910f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a910f-112">-DefaultProfile</span></span>
<span data-ttu-id="a910f-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a910f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a910f-114">-Force</span><span class="sxs-lookup"><span data-stu-id="a910f-114">-Force</span></span>
<span data-ttu-id="a910f-115">Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="a910f-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="a910f-116">-Location</span><span class="sxs-lookup"><span data-stu-id="a910f-116">-Location</span></span>
<span data-ttu-id="a910f-117">helyére.</span><span class="sxs-lookup"><span data-stu-id="a910f-117">location.</span></span>

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

### <span data-ttu-id="a910f-118">-Name</span><span class="sxs-lookup"><span data-stu-id="a910f-118">-Name</span></span>
<span data-ttu-id="a910f-119">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="a910f-119">The resource name.</span></span>

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

### <span data-ttu-id="a910f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a910f-120">-ResourceGroupName</span></span>
<span data-ttu-id="a910f-121">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a910f-121">The resource group name.</span></span>

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

### <span data-ttu-id="a910f-122">-SecurityProviderName</span><span class="sxs-lookup"><span data-stu-id="a910f-122">-SecurityProviderName</span></span>
<span data-ttu-id="a910f-123">A biztonsági szolgáltató neve</span><span class="sxs-lookup"><span data-stu-id="a910f-123">The Security Provider name</span></span>

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

### <span data-ttu-id="a910f-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="a910f-124">-Tag</span></span>
<span data-ttu-id="a910f-125">Erőforráscímkéket képviselő hashtable.</span><span class="sxs-lookup"><span data-stu-id="a910f-125">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="a910f-126">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="a910f-126">-VirtualHub</span></span>
<span data-ttu-id="a910f-127">A virtuális központi azonosító, amelyhez a biztonsági partnerszolgáltató csatolva van</span><span class="sxs-lookup"><span data-stu-id="a910f-127">The virtual hub Id that the security partner provider is attached to</span></span>

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

### <span data-ttu-id="a910f-128">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="a910f-128">-VirtualHubId</span></span>
<span data-ttu-id="a910f-129">Annak a VirtualHubnak az azonosítója, amelyhez a VpnGatewaynek társítva kell lennie.</span><span class="sxs-lookup"><span data-stu-id="a910f-129">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="a910f-130">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="a910f-130">-VirtualHubName</span></span>
<span data-ttu-id="a910f-131">Annak a VirtualHubnak az azonosítója, amelyhez a VpnGatewaynek társítva kell lennie.</span><span class="sxs-lookup"><span data-stu-id="a910f-131">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="a910f-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a910f-132">-Confirm</span></span>
<span data-ttu-id="a910f-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a910f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a910f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a910f-134">-WhatIf</span></span>
<span data-ttu-id="a910f-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a910f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a910f-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a910f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a910f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a910f-137">CommonParameters</span></span>
<span data-ttu-id="a910f-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a910f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a910f-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a910f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a910f-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a910f-140">INPUTS</span></span>

### <span data-ttu-id="a910f-141">System.String</span><span class="sxs-lookup"><span data-stu-id="a910f-141">System.String</span></span>

### <span data-ttu-id="a910f-142">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a910f-142">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="a910f-143">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="a910f-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a910f-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a910f-144">OUTPUTS</span></span>

### <span data-ttu-id="a910f-145">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="a910f-145">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="a910f-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a910f-146">NOTES</span></span>

## <span data-ttu-id="a910f-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a910f-147">RELATED LINKS</span></span>
