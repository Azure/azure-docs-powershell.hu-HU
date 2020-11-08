---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: f8ac34526691f3bdacdd0736189e063c969f63ff
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010775"
---
# <span data-ttu-id="46d3e-101">Get-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="46d3e-101">Get-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="46d3e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="46d3e-102">SYNOPSIS</span></span>
<span data-ttu-id="46d3e-103">Azure SQL Server virtuális hálózati szabály beolvasása vagy listázása.</span><span class="sxs-lookup"><span data-stu-id="46d3e-103">Gets or lists Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="46d3e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="46d3e-104">SYNTAX</span></span>

```
Get-AzSqlServerVirtualNetworkRule [-VirtualNetworkRuleName <String>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46d3e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="46d3e-105">DESCRIPTION</span></span>
<span data-ttu-id="46d3e-106">Ez a parancs egy bizonyos Azure SQL Server virtuális hálózati szabályt vagy az Azure SQL Server virtuális hálózati szabályait tartalmazó listát kap a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="46d3e-106">This command gets a specific Azure SQL Server Virtual Network Rule or a list of Azure SQL Server Virtual Network Rules under a server.</span></span>

## <span data-ttu-id="46d3e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="46d3e-107">EXAMPLES</span></span>

### <span data-ttu-id="46d3e-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="46d3e-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="46d3e-109">Egyetlen Azure SQL Server-alapú virtuális hálózati szabály kap</span><span class="sxs-lookup"><span data-stu-id="46d3e-109">Gets an single Azure SQL Server virtual network rule</span></span>

### <span data-ttu-id="46d3e-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="46d3e-110">Example 2</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName
```

<span data-ttu-id="46d3e-111">Az Azure SQL Server virtuális hálózati szabályainak listája a megadott kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="46d3e-111">Gets the list of Azure SQL Server virtual network rules under the specified server</span></span>

### <span data-ttu-id="46d3e-112">3. példa</span><span class="sxs-lookup"><span data-stu-id="46d3e-112">Example 3</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRule*
```

<span data-ttu-id="46d3e-113">Az Azure SQL Server virtuális hálózati szabályainak listája az "virtualNetworkRule" kezdetű megadott kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="46d3e-113">Gets the list of Azure SQL Server virtual network rules under the specified server that start with "virtualNetworkRule".</span></span>

## <span data-ttu-id="46d3e-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="46d3e-114">PARAMETERS</span></span>

### <span data-ttu-id="46d3e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46d3e-115">-DefaultProfile</span></span>
<span data-ttu-id="46d3e-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="46d3e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="46d3e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46d3e-117">-ResourceGroupName</span></span>
<span data-ttu-id="46d3e-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="46d3e-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="46d3e-119">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="46d3e-119">-ServerName</span></span>
<span data-ttu-id="46d3e-120">Az Azure SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="46d3e-120">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="46d3e-121">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="46d3e-121">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="46d3e-122">Az Azure SQL Server virtuális hálózati szabály neve.</span><span class="sxs-lookup"><span data-stu-id="46d3e-122">The Azure Sql Server Virtual Network Rule name.</span></span>

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

### <span data-ttu-id="46d3e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46d3e-123">CommonParameters</span></span>
<span data-ttu-id="46d3e-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="46d3e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46d3e-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="46d3e-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46d3e-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="46d3e-126">INPUTS</span></span>

### <span data-ttu-id="46d3e-127">System. String</span><span class="sxs-lookup"><span data-stu-id="46d3e-127">System.String</span></span>

## <span data-ttu-id="46d3e-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="46d3e-128">OUTPUTS</span></span>

### <span data-ttu-id="46d3e-129">Microsoft. Azure. Command. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="46d3e-129">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="46d3e-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="46d3e-130">NOTES</span></span>

## <span data-ttu-id="46d3e-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="46d3e-131">RELATED LINKS</span></span>
