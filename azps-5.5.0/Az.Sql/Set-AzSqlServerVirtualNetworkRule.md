---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 55321b384a24e18a962b99cc40161eabbeb00160
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158211"
---
# <span data-ttu-id="37c7d-101">Set-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="37c7d-101">Set-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="37c7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37c7d-102">SYNOPSIS</span></span>
<span data-ttu-id="37c7d-103">Módosítja egy Azure SQL Server virtuális hálózati szabály konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="37c7d-103">Modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="37c7d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="37c7d-104">SYNTAX</span></span>

```
Set-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37c7d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="37c7d-105">DESCRIPTION</span></span>
<span data-ttu-id="37c7d-106">Ez a parancs módosítja az Azure SQL Server virtuális hálózati szabály konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="37c7d-106">This command modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>
<span data-ttu-id="37c7d-107">Ha szabályozni szeretné a virtuális hálózati szabályok halmazát a kiszolgálón, használja helyette az "Add-AzSqlServerVirtualNetworkRule" és a "Remove-AzSqlServerVirtualNetworkRule" parancsot.</span><span class="sxs-lookup"><span data-stu-id="37c7d-107">To control the set of virtual network rules in the server, use 'Add-AzSqlServerVirtualNetworkRule' and 'Remove-AzSqlServerVirtualNetworkRule' instead.</span></span>

## <span data-ttu-id="37c7d-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="37c7d-108">EXAMPLES</span></span>

### <span data-ttu-id="37c7d-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="37c7d-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Set-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="37c7d-110">Módosít egy meglévő virtuális hálózatszabályt az új virtuális hálózat alhálózati azonosítójával, amely az új virtuális hálózat adatait tartalmazza</span><span class="sxs-lookup"><span data-stu-id="37c7d-110">Modifies an existing virtual network rule with the new virtual network subnet id which contains information about the new virtual network</span></span>

## <span data-ttu-id="37c7d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37c7d-111">PARAMETERS</span></span>

### <span data-ttu-id="37c7d-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="37c7d-112">-AsJob</span></span>
<span data-ttu-id="37c7d-113">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="37c7d-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="37c7d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37c7d-114">-DefaultProfile</span></span>
<span data-ttu-id="37c7d-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="37c7d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="37c7d-116">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="37c7d-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="37c7d-117">Hozzon létre tűzfalszabályt, mielőtt a virtuális hálózat engedélyezné a vnet-szolgáltatás végpontját.</span><span class="sxs-lookup"><span data-stu-id="37c7d-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="37c7d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37c7d-118">-ResourceGroupName</span></span>
<span data-ttu-id="37c7d-119">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="37c7d-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="37c7d-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="37c7d-120">-ServerName</span></span>
<span data-ttu-id="37c7d-121">Az Azure Sql Server neve.</span><span class="sxs-lookup"><span data-stu-id="37c7d-121">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="37c7d-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="37c7d-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="37c7d-123">Az Azure Sql Server virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="37c7d-123">The name of the Azure Sql Server Virtual Network Rule.</span></span>

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

### <span data-ttu-id="37c7d-124">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="37c7d-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="37c7d-125">A szabály virtuális hálózat alhálózati azonosítója.</span><span class="sxs-lookup"><span data-stu-id="37c7d-125">The Virtual Network Subnet Id for the rule.</span></span>

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

### <span data-ttu-id="37c7d-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="37c7d-126">-Confirm</span></span>
<span data-ttu-id="37c7d-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="37c7d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37c7d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37c7d-128">-WhatIf</span></span>
<span data-ttu-id="37c7d-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="37c7d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37c7d-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="37c7d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37c7d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37c7d-131">CommonParameters</span></span>
<span data-ttu-id="37c7d-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37c7d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37c7d-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="37c7d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37c7d-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="37c7d-134">INPUTS</span></span>

### <span data-ttu-id="37c7d-135">System.String</span><span class="sxs-lookup"><span data-stu-id="37c7d-135">System.String</span></span>

## <span data-ttu-id="37c7d-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="37c7d-136">OUTPUTS</span></span>

### <span data-ttu-id="37c7d-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="37c7d-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="37c7d-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="37c7d-138">NOTES</span></span>

## <span data-ttu-id="37c7d-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="37c7d-139">RELATED LINKS</span></span>
