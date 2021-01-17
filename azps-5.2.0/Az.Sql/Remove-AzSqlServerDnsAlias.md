---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDnsAlias.md
ms.openlocfilehash: d611f0bc14d657f47881cbdfbb1326111873114a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322709"
---
# <span data-ttu-id="d3baf-101">Remove-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="d3baf-101">Remove-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="d3baf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3baf-102">SYNOPSIS</span></span>
<span data-ttu-id="d3baf-103">Eltávolítja az Azure SQL Server DNS-aliasát.</span><span class="sxs-lookup"><span data-stu-id="d3baf-103">Removes Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="d3baf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d3baf-104">SYNTAX</span></span>

### <span data-ttu-id="d3baf-105">Kiszolgálói DNS-alias eltávolítása a parancsmag bemeneti paramétereiből</span><span class="sxs-lookup"><span data-stu-id="d3baf-105">Remove a Server Dns Alias from cmdlet input parameters</span></span>
```
Remove-AzSqlServerDnsAlias -Name <String> -ServerName <String> [-ResourceGroupName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3baf-106">Kiszolgálói DNS-alias eltávolítása az AzureSqlServerDnsAliasModel példánydefinícióból</span><span class="sxs-lookup"><span data-stu-id="d3baf-106">Remove a Server Dns Alias from AzureSqlServerDnsAliasModel instance definition</span></span>
```
Remove-AzSqlServerDnsAlias -InputObject <AzureSqlServerDnsAliasModel> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3baf-107">Kiszolgálói DNS-alias eltávolítása Azure-erőforrás-azonosítóból</span><span class="sxs-lookup"><span data-stu-id="d3baf-107">Remove a Server Dns Alias from an Azure resource id</span></span>
```
Remove-AzSqlServerDnsAlias -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3baf-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d3baf-108">DESCRIPTION</span></span>
<span data-ttu-id="d3baf-109">Ez a parancs eltávolítja az Azure SQL Server DNS-aliasát a kiszolgálóról, változatlanul hagyva a kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="d3baf-109">This commands remove Azure SQL Server DNS Alias from the server leaving server intact.</span></span>

## <span data-ttu-id="d3baf-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d3baf-110">EXAMPLES</span></span>

### <span data-ttu-id="d3baf-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="d3baf-111">Example 1</span></span>
```
PS C:\> Remove-AzSqlServerDnsAlias -DnsAliasName aliasName -ServerName serverName -ResourceGroupName rg
```

<span data-ttu-id="d3baf-112">Eltávolítja az Azure SQL Server DNS-aliasát aName nevű kiszolgálóról a name serverName névvel</span><span class="sxs-lookup"><span data-stu-id="d3baf-112">Removes Azure SQL Server DNS Alias with the name aliasName from the server with the name serverName</span></span>

## <span data-ttu-id="d3baf-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3baf-113">PARAMETERS</span></span>

### <span data-ttu-id="d3baf-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d3baf-114">-AsJob</span></span>
<span data-ttu-id="d3baf-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="d3baf-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d3baf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3baf-116">-DefaultProfile</span></span>
<span data-ttu-id="d3baf-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d3baf-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3baf-118">-Force</span><span class="sxs-lookup"><span data-stu-id="d3baf-118">-Force</span></span>
<span data-ttu-id="d3baf-119">A művelet végrehajtásához szükséges megerősítő üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="d3baf-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="d3baf-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3baf-120">-InputObject</span></span>
<span data-ttu-id="d3baf-121">The Server Dns Alias object to remove</span><span class="sxs-lookup"><span data-stu-id="d3baf-121">The Server Dns Alias object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel
Parameter Sets: Remove a Server Dns Alias from AzureSqlServerDnsAliasModel instance definition
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3baf-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d3baf-122">-Name</span></span>
<span data-ttu-id="d3baf-123">Azure Sql Server DNS-alias neve</span><span class="sxs-lookup"><span data-stu-id="d3baf-123">Azure Sql Server Dns Alias name</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Server Dns Alias from cmdlet input parameters
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3baf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3baf-124">-ResourceGroupName</span></span>
<span data-ttu-id="d3baf-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d3baf-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Server Dns Alias from cmdlet input parameters
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3baf-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3baf-126">-ResourceId</span></span>
<span data-ttu-id="d3baf-127">Az eltávolítható Kiszolgáló dns-alias objektum erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="d3baf-127">The resource id of Server Dns Alias object to remove</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Server Dns Alias from an Azure resource id
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3baf-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d3baf-128">-ServerName</span></span>
<span data-ttu-id="d3baf-129">Az Azure Sql Server neve.</span><span class="sxs-lookup"><span data-stu-id="d3baf-129">The Azure Sql Server name.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Server Dns Alias from cmdlet input parameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3baf-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d3baf-130">-Confirm</span></span>
<span data-ttu-id="d3baf-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d3baf-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3baf-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3baf-132">-WhatIf</span></span>
<span data-ttu-id="d3baf-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d3baf-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3baf-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d3baf-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3baf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3baf-135">CommonParameters</span></span>
<span data-ttu-id="d3baf-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3baf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3baf-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d3baf-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3baf-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d3baf-138">INPUTS</span></span>

### <span data-ttu-id="d3baf-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="d3baf-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

### <span data-ttu-id="d3baf-140">System.String</span><span class="sxs-lookup"><span data-stu-id="d3baf-140">System.String</span></span>

## <span data-ttu-id="d3baf-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3baf-141">OUTPUTS</span></span>

### <span data-ttu-id="d3baf-142">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="d3baf-142">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="d3baf-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d3baf-143">NOTES</span></span>

## <span data-ttu-id="d3baf-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d3baf-144">RELATED LINKS</span></span>
