---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 265600b201a6333b8dcd7c14f0cefe429f92619e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155250"
---
# <span data-ttu-id="58a00-101">Remove-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="58a00-101">Remove-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="58a00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58a00-102">SYNOPSIS</span></span>
<span data-ttu-id="58a00-103">Törli az Azure SQL Server virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="58a00-103">Deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="58a00-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="58a00-104">SYNTAX</span></span>

```
Remove-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> [-AsJob] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="58a00-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="58a00-105">DESCRIPTION</span></span>
<span data-ttu-id="58a00-106">Ez a parancs törli az Azure SQL Server virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="58a00-106">This command deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="58a00-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="58a00-107">EXAMPLES</span></span>

### <span data-ttu-id="58a00-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="58a00-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Remove-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="58a00-109">Meglévő Azure SQL Server virtuális hálózati szabály törlése</span><span class="sxs-lookup"><span data-stu-id="58a00-109">Deletes an existing Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="58a00-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58a00-110">PARAMETERS</span></span>

### <span data-ttu-id="58a00-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="58a00-111">-AsJob</span></span>
<span data-ttu-id="58a00-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="58a00-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="58a00-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58a00-113">-DefaultProfile</span></span>
<span data-ttu-id="58a00-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="58a00-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="58a00-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58a00-115">-ResourceGroupName</span></span>
<span data-ttu-id="58a00-116">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="58a00-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="58a00-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="58a00-117">-ServerName</span></span>
<span data-ttu-id="58a00-118">Az Azure Sql Server neve.</span><span class="sxs-lookup"><span data-stu-id="58a00-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="58a00-119">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="58a00-119">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="58a00-120">Azure Sql Server Virtuális hálózat szabály neve</span><span class="sxs-lookup"><span data-stu-id="58a00-120">Azure Sql Server Virtual Network Rule name</span></span>

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

### <span data-ttu-id="58a00-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="58a00-121">-Confirm</span></span>
<span data-ttu-id="58a00-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="58a00-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58a00-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58a00-123">-WhatIf</span></span>
<span data-ttu-id="58a00-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="58a00-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58a00-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="58a00-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58a00-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58a00-126">CommonParameters</span></span>
<span data-ttu-id="58a00-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58a00-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58a00-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="58a00-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58a00-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="58a00-129">INPUTS</span></span>

### <span data-ttu-id="58a00-130">System.String</span><span class="sxs-lookup"><span data-stu-id="58a00-130">System.String</span></span>

## <span data-ttu-id="58a00-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="58a00-131">OUTPUTS</span></span>

### <span data-ttu-id="58a00-132">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="58a00-132">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="58a00-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="58a00-133">NOTES</span></span>

## <span data-ttu-id="58a00-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="58a00-134">RELATED LINKS</span></span>
