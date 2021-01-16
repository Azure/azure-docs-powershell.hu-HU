---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecrossconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCrossConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCrossConnection.md
ms.openlocfilehash: 649ae6233f312dab4f18263bb65c4a9cd43b2aee
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327022"
---
# <span data-ttu-id="fc82f-101">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="fc82f-101">Set-AzExpressRouteCrossConnection</span></span>

## <span data-ttu-id="fc82f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc82f-102">SYNOPSIS</span></span>
<span data-ttu-id="fc82f-103">Egy ExpressRoute-keresztkapcsolatot módosít.</span><span class="sxs-lookup"><span data-stu-id="fc82f-103">Modifies an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="fc82f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fc82f-104">SYNTAX</span></span>

### <span data-ttu-id="fc82f-105">ModifyByCircuitReference</span><span class="sxs-lookup"><span data-stu-id="fc82f-105">ModifyByCircuitReference</span></span>
```
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc82f-106">ModifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="fc82f-106">ModifyByParameterValues</span></span>
```
Set-AzExpressRouteCrossConnection -ResourceGroupName <String> -Name <String>
 [-ServiceProviderProvisioningState <String>] [-ServiceProviderNotes <String>]
 [-Peerings <PSExpressRouteCrossConnectionPeering[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc82f-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fc82f-107">DESCRIPTION</span></span>
<span data-ttu-id="fc82f-108">A **Set-AzExpressRouteCrossConnection** parancsmag menti a módosított ExpressRoute-keresztkapcsolatot az Azure-sal.</span><span class="sxs-lookup"><span data-stu-id="fc82f-108">The **Set-AzExpressRouteCrossConnection** cmdlet saves the modified ExpressRoute cross connection to Azure.</span></span>

## <span data-ttu-id="fc82f-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fc82f-109">EXAMPLES</span></span>

### <span data-ttu-id="fc82f-110">1. példa: Az ExpressRoute-kapcsolat szolgáltató kiépítési állapotának módosítása</span><span class="sxs-lookup"><span data-stu-id="fc82f-110">Example 1: Change the Service Provider Provisioning State of an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
$cc.ServiceProviderProvisioningState = 'Provisioned'
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="fc82f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc82f-111">PARAMETERS</span></span>

### <span data-ttu-id="fc82f-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fc82f-112">-AsJob</span></span>
<span data-ttu-id="fc82f-113">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="fc82f-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fc82f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc82f-114">-DefaultProfile</span></span>
<span data-ttu-id="fc82f-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fc82f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc82f-116">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="fc82f-116">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="fc82f-117">Megadja az **ExpressRouteCrossConnection** objektumot, amit ez a parancsmag módosít.</span><span class="sxs-lookup"><span data-stu-id="fc82f-117">Specifies the **ExpressRouteCrossConnection** object that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="fc82f-118">-Force</span><span class="sxs-lookup"><span data-stu-id="fc82f-118">-Force</span></span>
<span data-ttu-id="fc82f-119">Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="fc82f-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="fc82f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="fc82f-120">-Name</span></span>
<span data-ttu-id="fc82f-121">Az express route cross connection neve.</span><span class="sxs-lookup"><span data-stu-id="fc82f-121">The name of express route cross connection.</span></span>

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

### <span data-ttu-id="fc82f-122">-Társviszonyok</span><span class="sxs-lookup"><span data-stu-id="fc82f-122">-Peerings</span></span>
<span data-ttu-id="fc82f-123">A keresztkapcsolat társviszony-listája</span><span class="sxs-lookup"><span data-stu-id="fc82f-123">The list of peerings for the cross connection</span></span>

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

### <span data-ttu-id="fc82f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc82f-124">-ResourceGroupName</span></span>
<span data-ttu-id="fc82f-125">Az ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="fc82f-125">The ExpressRouteCrossConnection</span></span>

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

### <span data-ttu-id="fc82f-126">-ServiceProviderNotes</span><span class="sxs-lookup"><span data-stu-id="fc82f-126">-ServiceProviderNotes</span></span>
<span data-ttu-id="fc82f-127">A szolgáltató megjegyzései</span><span class="sxs-lookup"><span data-stu-id="fc82f-127">The service provider notes</span></span>

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

### <span data-ttu-id="fc82f-128">-ServiceProviderProvisioningState</span><span class="sxs-lookup"><span data-stu-id="fc82f-128">-ServiceProviderProvisioningState</span></span>
<span data-ttu-id="fc82f-129">A szolgáltató kiépítési állapotát be kell állítani</span><span class="sxs-lookup"><span data-stu-id="fc82f-129">The service provider provisioning state to be set</span></span>

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

### <span data-ttu-id="fc82f-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fc82f-130">-Confirm</span></span>
<span data-ttu-id="fc82f-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="fc82f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc82f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc82f-132">-WhatIf</span></span>
<span data-ttu-id="fc82f-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="fc82f-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fc82f-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fc82f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc82f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc82f-135">CommonParameters</span></span>
<span data-ttu-id="fc82f-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc82f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc82f-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc82f-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc82f-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fc82f-138">INPUTS</span></span>

### <span data-ttu-id="fc82f-139">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="fc82f-139">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="fc82f-140">Az "ExpressRouteCrossConnection" paraméter a "PSExpressRouteCrossConnection" típusú értéket fogadja el a folyamatból.</span><span class="sxs-lookup"><span data-stu-id="fc82f-140">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="fc82f-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc82f-141">OUTPUTS</span></span>

### <span data-ttu-id="fc82f-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="fc82f-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="fc82f-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fc82f-143">NOTES</span></span>

## <span data-ttu-id="fc82f-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fc82f-144">RELATED LINKS</span></span>

[<span data-ttu-id="fc82f-145">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="fc82f-145">Get-AzExpressRouteCrossConnection</span></span>](./Get-AzExpressRouteCrossConnection.md)
