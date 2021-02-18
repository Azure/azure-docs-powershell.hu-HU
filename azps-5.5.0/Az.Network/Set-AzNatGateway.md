---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznatgateway.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNatGateway.md
ms.openlocfilehash: fe19aba38402519a77185062ac6192d6ff9915eb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202454"
---
# <span data-ttu-id="b03b1-101">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="b03b1-101">Set-AzNatGateway</span></span>

## <span data-ttu-id="b03b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b03b1-102">SYNOPSIS</span></span>
<span data-ttu-id="b03b1-103">A Nat Átjáróforrás frissítése nyilvános IP-címmel, nyilvános IP-előtaggal és IdleTimeoutInMinutes címmel.</span><span class="sxs-lookup"><span data-stu-id="b03b1-103">Update Nat Gateway Resource with Public Ip Address, Public Ip Prefix and IdleTimeoutInMinutes.</span></span>

## <span data-ttu-id="b03b1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b03b1-104">SYNTAX</span></span>

### <span data-ttu-id="b03b1-105">SetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b03b1-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzNatGateway -ResourceGroupName <String> -Name <String> [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-AsJob] [-IdleTimeoutInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b03b1-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b03b1-106">SetByResourceIdParameterSet</span></span>
```
Set-AzNatGateway -ResourceId <String> [-PublicIpAddress <PSResourceId[]>] [-PublicIpPrefix <PSResourceId[]>]
 [-AsJob] [-IdleTimeoutInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b03b1-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b03b1-107">SetByInputObjectParameterSet</span></span>
```
Set-AzNatGateway -InputObject <PSNatGateway> [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-AsJob] [-IdleTimeoutInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b03b1-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b03b1-108">DESCRIPTION</span></span>
<span data-ttu-id="b03b1-109">A Nat Átjáróforrás frissítése nyilvános IP-címmel, nyilvános IP-előtaggal és IdleTimeoutInMinutes címmel.</span><span class="sxs-lookup"><span data-stu-id="b03b1-109">Update Nat Gateway Resource with Public Ip Address, Public Ip Prefix and IdleTimeoutInMinutes.</span></span>

## <span data-ttu-id="b03b1-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b03b1-110">EXAMPLES</span></span>

### <span data-ttu-id="b03b1-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="b03b1-111">Example 1</span></span>
```powershell
PS C:\> $nGateway = Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "ng1"
PS C:\> $pipArray = $pip, $pip2
PS C:\> $natUpdate = Set-AzNatGateway -InputObject $nGateway -IdleTimeoutInMinutes 5 -PublicIpAddress $pipArray
PS C:\> $natUpdate = Set-AzNatGateway -ResourceGroupName "natgateway_test" -Name "ng1" -PublicIpAddress $pipArray
PS C:\> $natUpdate = Set-AzNatGateway -ResourceId "natgateway_id" -PublicIpAddress $pipArray
```

## <span data-ttu-id="b03b1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b03b1-112">PARAMETERS</span></span>

### <span data-ttu-id="b03b1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b03b1-113">-AsJob</span></span>
<span data-ttu-id="b03b1-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b03b1-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b03b1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b03b1-115">-DefaultProfile</span></span>
<span data-ttu-id="b03b1-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b03b1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b03b1-117">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="b03b1-117">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="b03b1-118">A nat átjáró üresjárati időkorlátja.</span><span class="sxs-lookup"><span data-stu-id="b03b1-118">The idle timeout of the nat gateway.</span></span>

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

### <span data-ttu-id="b03b1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b03b1-119">-InputObject</span></span>
<span data-ttu-id="b03b1-120">A Nat átjáró erőforrását adja meg.</span><span class="sxs-lookup"><span data-stu-id="b03b1-120">Specifies Nat Gateway Resource.</span></span>

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

### <span data-ttu-id="b03b1-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b03b1-121">-Name</span></span>
<span data-ttu-id="b03b1-122">A Nat Átjáró erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="b03b1-122">Name of the Nat Gateway Resource.</span></span>

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

### <span data-ttu-id="b03b1-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b03b1-123">-PublicIpAddress</span></span>
<span data-ttu-id="b03b1-124">A nat-átjáró erőforrásával társított nyilvános IP-címek tömbje.</span><span class="sxs-lookup"><span data-stu-id="b03b1-124">An array of public ip addresses associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="b03b1-125">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="b03b1-125">-PublicIpPrefix</span></span>
<span data-ttu-id="b03b1-126">A nat átjáró erőforráshoz társított nyilvános IP-előtagok tömbje.</span><span class="sxs-lookup"><span data-stu-id="b03b1-126">An array of public ip prefixes associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="b03b1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b03b1-127">-ResourceGroupName</span></span>
<span data-ttu-id="b03b1-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b03b1-128">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="b03b1-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b03b1-129">-ResourceId</span></span>
<span data-ttu-id="b03b1-130">A Nat átjáró erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b03b1-130">Specifies the Id of the Nat Gateway resource.</span></span>

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

### <span data-ttu-id="b03b1-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b03b1-131">-Confirm</span></span>
<span data-ttu-id="b03b1-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b03b1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b03b1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b03b1-133">-WhatIf</span></span>
<span data-ttu-id="b03b1-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b03b1-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b03b1-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b03b1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b03b1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b03b1-136">CommonParameters</span></span>
<span data-ttu-id="b03b1-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b03b1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b03b1-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b03b1-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b03b1-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b03b1-139">INPUTS</span></span>

### <span data-ttu-id="b03b1-140">System.String</span><span class="sxs-lookup"><span data-stu-id="b03b1-140">System.String</span></span>

### <span data-ttu-id="b03b1-141">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="b03b1-141">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="b03b1-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b03b1-142">OUTPUTS</span></span>

### <span data-ttu-id="b03b1-143">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="b03b1-143">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="b03b1-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b03b1-144">NOTES</span></span>

## <span data-ttu-id="b03b1-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b03b1-145">RELATED LINKS</span></span>
