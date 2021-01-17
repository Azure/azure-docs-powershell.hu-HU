---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznatgateway.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNatGateway.md
ms.openlocfilehash: fe19aba38402519a77185062ac6192d6ff9915eb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479914"
---
# <span data-ttu-id="cd160-101">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="cd160-101">Set-AzNatGateway</span></span>

## <span data-ttu-id="cd160-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd160-102">SYNOPSIS</span></span>
<span data-ttu-id="cd160-103">A Nat Átjáróforrás frissítése nyilvános IP-címmel, nyilvános IP-előtaggal és IdleTimeoutInMinutes címmel.</span><span class="sxs-lookup"><span data-stu-id="cd160-103">Update Nat Gateway Resource with Public Ip Address, Public Ip Prefix and IdleTimeoutInMinutes.</span></span>

## <span data-ttu-id="cd160-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cd160-104">SYNTAX</span></span>

### <span data-ttu-id="cd160-105">SetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cd160-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzNatGateway -ResourceGroupName <String> -Name <String> [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-AsJob] [-IdleTimeoutInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd160-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd160-106">SetByResourceIdParameterSet</span></span>
```
Set-AzNatGateway -ResourceId <String> [-PublicIpAddress <PSResourceId[]>] [-PublicIpPrefix <PSResourceId[]>]
 [-AsJob] [-IdleTimeoutInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cd160-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd160-107">SetByInputObjectParameterSet</span></span>
```
Set-AzNatGateway -InputObject <PSNatGateway> [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-AsJob] [-IdleTimeoutInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd160-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cd160-108">DESCRIPTION</span></span>
<span data-ttu-id="cd160-109">A Nat Gateway Resource frissítése nyilvános IP-címmel, nyilvános IP-előtaggal és IdleTimeoutInMinutes címmel.</span><span class="sxs-lookup"><span data-stu-id="cd160-109">Update Nat Gateway Resource with Public Ip Address, Public Ip Prefix and IdleTimeoutInMinutes.</span></span>

## <span data-ttu-id="cd160-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cd160-110">EXAMPLES</span></span>

### <span data-ttu-id="cd160-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="cd160-111">Example 1</span></span>
```powershell
PS C:\> $nGateway = Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "ng1"
PS C:\> $pipArray = $pip, $pip2
PS C:\> $natUpdate = Set-AzNatGateway -InputObject $nGateway -IdleTimeoutInMinutes 5 -PublicIpAddress $pipArray
PS C:\> $natUpdate = Set-AzNatGateway -ResourceGroupName "natgateway_test" -Name "ng1" -PublicIpAddress $pipArray
PS C:\> $natUpdate = Set-AzNatGateway -ResourceId "natgateway_id" -PublicIpAddress $pipArray
```

## <span data-ttu-id="cd160-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd160-112">PARAMETERS</span></span>

### <span data-ttu-id="cd160-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd160-113">-AsJob</span></span>
<span data-ttu-id="cd160-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="cd160-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cd160-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd160-115">-DefaultProfile</span></span>
<span data-ttu-id="cd160-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cd160-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd160-117">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="cd160-117">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="cd160-118">A nat átjáró üresjárati időkorlátja.</span><span class="sxs-lookup"><span data-stu-id="cd160-118">The idle timeout of the nat gateway.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd160-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd160-119">-InputObject</span></span>
<span data-ttu-id="cd160-120">A Nat átjáró erőforrását adja meg.</span><span class="sxs-lookup"><span data-stu-id="cd160-120">Specifies Nat Gateway Resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNatGateway
Parameter Sets: SetByInputObjectParameterSet
Aliases: NatGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd160-121">-Name</span><span class="sxs-lookup"><span data-stu-id="cd160-121">-Name</span></span>
<span data-ttu-id="cd160-122">A Nat átjáróerőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="cd160-122">Name of the Nat Gateway Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd160-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="cd160-123">-PublicIpAddress</span></span>
<span data-ttu-id="cd160-124">A nat-átjáró erőforrásával társított nyilvános IP-címek tömbje.</span><span class="sxs-lookup"><span data-stu-id="cd160-124">An array of public ip addresses associated with the nat gateway resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd160-125">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="cd160-125">-PublicIpPrefix</span></span>
<span data-ttu-id="cd160-126">A nat átjáró erőforráshoz társított nyilvános IP-előtagok tömbje.</span><span class="sxs-lookup"><span data-stu-id="cd160-126">An array of public ip prefixes associated with the nat gateway resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd160-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd160-127">-ResourceGroupName</span></span>
<span data-ttu-id="cd160-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="cd160-128">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd160-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd160-129">-ResourceId</span></span>
<span data-ttu-id="cd160-130">A Nat Átjáró erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="cd160-130">Specifies the Id of the Nat Gateway resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases: NatGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd160-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cd160-131">-Confirm</span></span>
<span data-ttu-id="cd160-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="cd160-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd160-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd160-133">-WhatIf</span></span>
<span data-ttu-id="cd160-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="cd160-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd160-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cd160-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd160-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd160-136">CommonParameters</span></span>
<span data-ttu-id="cd160-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd160-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd160-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cd160-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd160-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cd160-139">INPUTS</span></span>

### <span data-ttu-id="cd160-140">System.String</span><span class="sxs-lookup"><span data-stu-id="cd160-140">System.String</span></span>

### <span data-ttu-id="cd160-141">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="cd160-141">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="cd160-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd160-142">OUTPUTS</span></span>

### <span data-ttu-id="cd160-143">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="cd160-143">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="cd160-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cd160-144">NOTES</span></span>

## <span data-ttu-id="cd160-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cd160-145">RELATED LINKS</span></span>
