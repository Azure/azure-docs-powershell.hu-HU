---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 265600b201a6333b8dcd7c14f0cefe429f92619e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185654"
---
# <span data-ttu-id="fffe8-101">Remove-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="fffe8-101">Remove-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="fffe8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fffe8-102">SYNOPSIS</span></span>
<span data-ttu-id="fffe8-103">Azure SQL Server virtuális hálózati szabály törlése</span><span class="sxs-lookup"><span data-stu-id="fffe8-103">Deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="fffe8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fffe8-104">SYNTAX</span></span>

```
Remove-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> [-AsJob] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fffe8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fffe8-105">DESCRIPTION</span></span>
<span data-ttu-id="fffe8-106">Ez a parancs törli az Azure SQL Server virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="fffe8-106">This command deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="fffe8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fffe8-107">EXAMPLES</span></span>

### <span data-ttu-id="fffe8-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fffe8-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Remove-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="fffe8-109">Meglévő Azure SQL Server-alapú virtuális hálózati szabály törlése</span><span class="sxs-lookup"><span data-stu-id="fffe8-109">Deletes an existing Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="fffe8-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fffe8-110">PARAMETERS</span></span>

### <span data-ttu-id="fffe8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fffe8-111">-AsJob</span></span>
<span data-ttu-id="fffe8-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="fffe8-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fffe8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fffe8-113">-DefaultProfile</span></span>
<span data-ttu-id="fffe8-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fffe8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fffe8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fffe8-115">-ResourceGroupName</span></span>
<span data-ttu-id="fffe8-116">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fffe8-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="fffe8-117">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="fffe8-117">-ServerName</span></span>
<span data-ttu-id="fffe8-118">Az Azure SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="fffe8-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="fffe8-119">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="fffe8-119">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="fffe8-120">Azure SQL Server virtuális hálózati szabály neve</span><span class="sxs-lookup"><span data-stu-id="fffe8-120">Azure Sql Server Virtual Network Rule name</span></span>

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

### <span data-ttu-id="fffe8-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fffe8-121">-Confirm</span></span>
<span data-ttu-id="fffe8-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fffe8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fffe8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fffe8-123">-WhatIf</span></span>
<span data-ttu-id="fffe8-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fffe8-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fffe8-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fffe8-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fffe8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fffe8-126">CommonParameters</span></span>
<span data-ttu-id="fffe8-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fffe8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fffe8-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fffe8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fffe8-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fffe8-129">INPUTS</span></span>

### <span data-ttu-id="fffe8-130">System. String</span><span class="sxs-lookup"><span data-stu-id="fffe8-130">System.String</span></span>

## <span data-ttu-id="fffe8-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fffe8-131">OUTPUTS</span></span>

### <span data-ttu-id="fffe8-132">Microsoft. Azure. Command. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="fffe8-132">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="fffe8-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fffe8-133">NOTES</span></span>

## <span data-ttu-id="fffe8-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fffe8-134">RELATED LINKS</span></span>