---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 265600b201a6333b8dcd7c14f0cefe429f92619e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343673"
---
# <span data-ttu-id="616a3-101">Remove-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="616a3-101">Remove-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="616a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="616a3-102">SYNOPSIS</span></span>
<span data-ttu-id="616a3-103">Törli az Azure SQL Server virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="616a3-103">Deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="616a3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="616a3-104">SYNTAX</span></span>

```
Remove-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> [-AsJob] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="616a3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="616a3-105">DESCRIPTION</span></span>
<span data-ttu-id="616a3-106">Ez a parancs törli az Azure SQL Server virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="616a3-106">This command deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="616a3-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="616a3-107">EXAMPLES</span></span>

### <span data-ttu-id="616a3-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="616a3-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Remove-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="616a3-109">Meglévő Azure SQL Server virtuális hálózati szabály törlése</span><span class="sxs-lookup"><span data-stu-id="616a3-109">Deletes an existing Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="616a3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="616a3-110">PARAMETERS</span></span>

### <span data-ttu-id="616a3-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="616a3-111">-AsJob</span></span>
<span data-ttu-id="616a3-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="616a3-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="616a3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="616a3-113">-DefaultProfile</span></span>
<span data-ttu-id="616a3-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="616a3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="616a3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="616a3-115">-ResourceGroupName</span></span>
<span data-ttu-id="616a3-116">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="616a3-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="616a3-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="616a3-117">-ServerName</span></span>
<span data-ttu-id="616a3-118">Az Azure Sql Server neve.</span><span class="sxs-lookup"><span data-stu-id="616a3-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="616a3-119">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="616a3-119">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="616a3-120">Azure Sql Server Virtuális hálózat szabály neve</span><span class="sxs-lookup"><span data-stu-id="616a3-120">Azure Sql Server Virtual Network Rule name</span></span>

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

### <span data-ttu-id="616a3-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="616a3-121">-Confirm</span></span>
<span data-ttu-id="616a3-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="616a3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="616a3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="616a3-123">-WhatIf</span></span>
<span data-ttu-id="616a3-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="616a3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="616a3-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="616a3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="616a3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="616a3-126">CommonParameters</span></span>
<span data-ttu-id="616a3-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="616a3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="616a3-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="616a3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="616a3-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="616a3-129">INPUTS</span></span>

### <span data-ttu-id="616a3-130">System.String</span><span class="sxs-lookup"><span data-stu-id="616a3-130">System.String</span></span>

## <span data-ttu-id="616a3-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="616a3-131">OUTPUTS</span></span>

### <span data-ttu-id="616a3-132">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="616a3-132">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="616a3-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="616a3-133">NOTES</span></span>

## <span data-ttu-id="616a3-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="616a3-134">RELATED LINKS</span></span>
