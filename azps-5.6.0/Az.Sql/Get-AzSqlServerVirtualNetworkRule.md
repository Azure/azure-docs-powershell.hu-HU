---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: f4744eee1e93867ea150819a8f4bcadc5ac8a35b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003062"
---
# <span data-ttu-id="54ee3-101">Get-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="54ee3-101">Get-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="54ee3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54ee3-102">SYNOPSIS</span></span>
<span data-ttu-id="54ee3-103">Az Azure SQL Server Virtuális hálózati szabály lekérte vagy felsorolja azokat.</span><span class="sxs-lookup"><span data-stu-id="54ee3-103">Gets or lists Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="54ee3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="54ee3-104">SYNTAX</span></span>

```
Get-AzSqlServerVirtualNetworkRule [-VirtualNetworkRuleName <String>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54ee3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="54ee3-105">DESCRIPTION</span></span>
<span data-ttu-id="54ee3-106">Ez a parancs egy adott Azure SQL Server virtuális hálózati szabályt vagy az Azure SQL Server Virtuális hálózat szabályainak listáját kapja meg egy kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="54ee3-106">This command gets a specific Azure SQL Server Virtual Network Rule or a list of Azure SQL Server Virtual Network Rules under a server.</span></span>

## <span data-ttu-id="54ee3-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="54ee3-107">EXAMPLES</span></span>

### <span data-ttu-id="54ee3-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="54ee3-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="54ee3-109">Egyetlen Azure SQL Server virtuális hálózati szabályt kap</span><span class="sxs-lookup"><span data-stu-id="54ee3-109">Gets an single Azure SQL Server virtual network rule</span></span>

### <span data-ttu-id="54ee3-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="54ee3-110">Example 2</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName
```

<span data-ttu-id="54ee3-111">A virtuális Azure SQL Server-szabályok listájának lekérte a megadott kiszolgálóhoz</span><span class="sxs-lookup"><span data-stu-id="54ee3-111">Gets the list of Azure SQL Server virtual network rules under the specified server</span></span>

### <span data-ttu-id="54ee3-112">3. példa</span><span class="sxs-lookup"><span data-stu-id="54ee3-112">Example 3</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRule*
```

<span data-ttu-id="54ee3-113">Az Azure SQL Server virtuális hálózati szabályainak listáját a megadott kiszolgáló alatt tartalmazza, amelyek a "virtualNetworkRule" kezdetűvel kezdődnek.</span><span class="sxs-lookup"><span data-stu-id="54ee3-113">Gets the list of Azure SQL Server virtual network rules under the specified server that start with "virtualNetworkRule".</span></span>

## <span data-ttu-id="54ee3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54ee3-114">PARAMETERS</span></span>

### <span data-ttu-id="54ee3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54ee3-115">-DefaultProfile</span></span>
<span data-ttu-id="54ee3-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="54ee3-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54ee3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54ee3-117">-ResourceGroupName</span></span>
<span data-ttu-id="54ee3-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="54ee3-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="54ee3-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="54ee3-119">-ServerName</span></span>
<span data-ttu-id="54ee3-120">Az Azure Sql Server neve.</span><span class="sxs-lookup"><span data-stu-id="54ee3-120">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="54ee3-121">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="54ee3-121">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="54ee3-122">Az Azure Sql Server virtuális hálózat szabályának neve.</span><span class="sxs-lookup"><span data-stu-id="54ee3-122">The Azure Sql Server Virtual Network Rule name.</span></span>

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

### <span data-ttu-id="54ee3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54ee3-123">CommonParameters</span></span>
<span data-ttu-id="54ee3-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54ee3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54ee3-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="54ee3-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54ee3-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="54ee3-126">INPUTS</span></span>

### <span data-ttu-id="54ee3-127">System.String</span><span class="sxs-lookup"><span data-stu-id="54ee3-127">System.String</span></span>

## <span data-ttu-id="54ee3-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="54ee3-128">OUTPUTS</span></span>

### <span data-ttu-id="54ee3-129">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="54ee3-129">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="54ee3-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="54ee3-130">NOTES</span></span>

## <span data-ttu-id="54ee3-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="54ee3-131">RELATED LINKS</span></span>
