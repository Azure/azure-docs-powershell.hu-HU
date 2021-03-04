---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: b583c8339ebec74fdf8df4116204b7ad5523c258
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942177"
---
# <span data-ttu-id="b64e4-101">Set-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b64e4-101">Set-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="b64e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b64e4-102">SYNOPSIS</span></span>
<span data-ttu-id="b64e4-103">Módosítja egy Azure SQL Server virtuális hálózati szabály konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="b64e4-103">Modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="b64e4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b64e4-104">SYNTAX</span></span>

```
Set-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b64e4-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b64e4-105">DESCRIPTION</span></span>
<span data-ttu-id="b64e4-106">Ez a parancs módosítja az Azure SQL Server virtuális hálózati szabály konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="b64e4-106">This command modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>
<span data-ttu-id="b64e4-107">Ha szabályozni szeretné a virtuális hálózati szabályok készletét a kiszolgálón, használja helyette az "Add-AzSqlServerVirtualNetworkRule" és a "Remove-AzSqlServerVirtualNetworkRule" parancsot.</span><span class="sxs-lookup"><span data-stu-id="b64e4-107">To control the set of virtual network rules in the server, use 'Add-AzSqlServerVirtualNetworkRule' and 'Remove-AzSqlServerVirtualNetworkRule' instead.</span></span>

## <span data-ttu-id="b64e4-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b64e4-108">EXAMPLES</span></span>

### <span data-ttu-id="b64e4-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="b64e4-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Set-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="b64e4-110">Módosít egy meglévő virtuális hálózatszabályt az új virtuális hálózat alhálózati azonosítójával, amely az új virtuális hálózat adatait tartalmazza</span><span class="sxs-lookup"><span data-stu-id="b64e4-110">Modifies an existing virtual network rule with the new virtual network subnet id which contains information about the new virtual network</span></span>

## <span data-ttu-id="b64e4-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b64e4-111">PARAMETERS</span></span>

### <span data-ttu-id="b64e4-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b64e4-112">-AsJob</span></span>
<span data-ttu-id="b64e4-113">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b64e4-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b64e4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b64e4-114">-DefaultProfile</span></span>
<span data-ttu-id="b64e4-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b64e4-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b64e4-116">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="b64e4-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="b64e4-117">Hozzon létre tűzfalszabályt, mielőtt a virtuális hálózat engedélyezné a vnet-szolgáltatás végpontját.</span><span class="sxs-lookup"><span data-stu-id="b64e4-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="b64e4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b64e4-118">-ResourceGroupName</span></span>
<span data-ttu-id="b64e4-119">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b64e4-119">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b64e4-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b64e4-120">-ServerName</span></span>
<span data-ttu-id="b64e4-121">Az Azure Sql Server neve.</span><span class="sxs-lookup"><span data-stu-id="b64e4-121">The Azure Sql Server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b64e4-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="b64e4-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="b64e4-123">Az Azure Sql Server virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="b64e4-123">The name of the Azure Sql Server Virtual Network Rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b64e4-124">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="b64e4-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="b64e4-125">A szabály virtuális hálózat alhálózati azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b64e4-125">The Virtual Network Subnet Id for the rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b64e4-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b64e4-126">-Confirm</span></span>
<span data-ttu-id="b64e4-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b64e4-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b64e4-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b64e4-128">-WhatIf</span></span>
<span data-ttu-id="b64e4-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b64e4-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b64e4-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b64e4-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b64e4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b64e4-131">CommonParameters</span></span>
<span data-ttu-id="b64e4-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b64e4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b64e4-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b64e4-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b64e4-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b64e4-134">INPUTS</span></span>

### <span data-ttu-id="b64e4-135">System.String</span><span class="sxs-lookup"><span data-stu-id="b64e4-135">System.String</span></span>

## <span data-ttu-id="b64e4-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b64e4-136">OUTPUTS</span></span>

### <span data-ttu-id="b64e4-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="b64e4-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="b64e4-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b64e4-138">NOTES</span></span>

## <span data-ttu-id="b64e4-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b64e4-139">RELATED LINKS</span></span>
