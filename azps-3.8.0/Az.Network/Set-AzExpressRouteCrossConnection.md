---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecrossconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCrossConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCrossConnection.md
ms.openlocfilehash: 649ae6233f312dab4f18263bb65c4a9cd43b2aee
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011328"
---
# <span data-ttu-id="0ef06-101">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="0ef06-101">Set-AzExpressRouteCrossConnection</span></span>

## <span data-ttu-id="0ef06-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0ef06-102">SYNOPSIS</span></span>
<span data-ttu-id="0ef06-103">Módosítja egy ExpressRoute-kereszt kapcsolatát.</span><span class="sxs-lookup"><span data-stu-id="0ef06-103">Modifies an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="0ef06-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0ef06-104">SYNTAX</span></span>

### <span data-ttu-id="0ef06-105">ModifyByCircuitReference</span><span class="sxs-lookup"><span data-stu-id="0ef06-105">ModifyByCircuitReference</span></span>
```
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ef06-106">ModifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="0ef06-106">ModifyByParameterValues</span></span>
```
Set-AzExpressRouteCrossConnection -ResourceGroupName <String> -Name <String>
 [-ServiceProviderProvisioningState <String>] [-ServiceProviderNotes <String>]
 [-Peerings <PSExpressRouteCrossConnectionPeering[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ef06-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0ef06-107">DESCRIPTION</span></span>
<span data-ttu-id="0ef06-108">A **set-AzExpressRouteCrossConnection** parancsmag menti a módosított ExpressRoute Cross kapcsolatot az Azure-ra.</span><span class="sxs-lookup"><span data-stu-id="0ef06-108">The **Set-AzExpressRouteCrossConnection** cmdlet saves the modified ExpressRoute cross connection to Azure.</span></span>

## <span data-ttu-id="0ef06-109">Példák</span><span class="sxs-lookup"><span data-stu-id="0ef06-109">EXAMPLES</span></span>

### <span data-ttu-id="0ef06-110">Példa 1: a szolgáltató kiépítési állapotának módosítása ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="0ef06-110">Example 1: Change the Service Provider Provisioning State of an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
$cc.ServiceProviderProvisioningState = 'Provisioned'
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="0ef06-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0ef06-111">PARAMETERS</span></span>

### <span data-ttu-id="0ef06-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0ef06-112">-AsJob</span></span>
<span data-ttu-id="0ef06-113">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="0ef06-113">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ef06-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ef06-114">-DefaultProfile</span></span>
<span data-ttu-id="0ef06-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0ef06-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ef06-116">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="0ef06-116">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="0ef06-117">Azt a **ExpressRouteCrossConnection** objektumot adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="0ef06-117">Specifies the **ExpressRouteCrossConnection** object that this cmdlet modifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: ModifyByCircuitReference
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0ef06-118">-Force</span><span class="sxs-lookup"><span data-stu-id="0ef06-118">-Force</span></span>
<span data-ttu-id="0ef06-119">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0ef06-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ef06-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0ef06-120">-Name</span></span>
<span data-ttu-id="0ef06-121">Az Express Route Cross kapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="0ef06-121">The name of express route cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ModifyByParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ef06-122">-Munkatársak</span><span class="sxs-lookup"><span data-stu-id="0ef06-122">-Peerings</span></span>
<span data-ttu-id="0ef06-123">A kereszthivatkozások listája a kapcsolathoz</span><span class="sxs-lookup"><span data-stu-id="0ef06-123">The list of peerings for the cross connection</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnectionPeering[]
Parameter Sets: ModifyByParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0ef06-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ef06-124">-ResourceGroupName</span></span>
<span data-ttu-id="0ef06-125">A ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="0ef06-125">The ExpressRouteCrossConnection</span></span>

```yaml
Type: System.String
Parameter Sets: ModifyByParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0ef06-126">-ServiceProviderNotes</span><span class="sxs-lookup"><span data-stu-id="0ef06-126">-ServiceProviderNotes</span></span>
<span data-ttu-id="0ef06-127">A szolgáltató megjegyzései</span><span class="sxs-lookup"><span data-stu-id="0ef06-127">The service provider notes</span></span>

```yaml
Type: System.String
Parameter Sets: ModifyByParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0ef06-128">-ServiceProviderProvisioningState</span><span class="sxs-lookup"><span data-stu-id="0ef06-128">-ServiceProviderProvisioningState</span></span>
<span data-ttu-id="0ef06-129">A szolgáltató kiépítési állapotának beállítása</span><span class="sxs-lookup"><span data-stu-id="0ef06-129">The service provider provisioning state to be set</span></span>

```yaml
Type: System.String
Parameter Sets: ModifyByParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0ef06-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0ef06-130">-Confirm</span></span>
<span data-ttu-id="0ef06-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0ef06-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ef06-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ef06-132">-WhatIf</span></span>
<span data-ttu-id="0ef06-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0ef06-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0ef06-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0ef06-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ef06-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ef06-135">CommonParameters</span></span>
<span data-ttu-id="0ef06-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0ef06-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ef06-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ef06-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ef06-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ef06-138">INPUTS</span></span>

### <span data-ttu-id="0ef06-139">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="0ef06-139">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="0ef06-140">A ' ExpressRouteCrossConnection ' paraméter az "PSExpressRouteCrossConnection" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="0ef06-140">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="0ef06-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ef06-141">OUTPUTS</span></span>

### <span data-ttu-id="0ef06-142">Microsoft. Azure. commands. Network. models. PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="0ef06-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="0ef06-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0ef06-143">NOTES</span></span>

## <span data-ttu-id="0ef06-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0ef06-144">RELATED LINKS</span></span>

[<span data-ttu-id="0ef06-145">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="0ef06-145">Get-AzExpressRouteCrossConnection</span></span>](./Get-AzExpressRouteCrossConnection.md)
