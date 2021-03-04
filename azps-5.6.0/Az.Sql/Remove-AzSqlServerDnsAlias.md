---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDnsAlias.md
ms.openlocfilehash: 07065c18b9e06f75863ddd41f8a6f0155a3699f9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926306"
---
# <span data-ttu-id="d3f2c-101">Remove-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="d3f2c-101">Remove-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="d3f2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3f2c-102">SYNOPSIS</span></span>
<span data-ttu-id="d3f2c-103">Eltávolítja az Azure SQL Server DNS-aliasát.</span><span class="sxs-lookup"><span data-stu-id="d3f2c-103">Removes Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="d3f2c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d3f2c-104">SYNTAX</span></span>

### <span data-ttu-id="d3f2c-105">Kiszolgálói DNS-alias eltávolítása a parancsmag bemeneti paramétereiből</span><span class="sxs-lookup"><span data-stu-id="d3f2c-105">Remove a Server Dns Alias from cmdlet input parameters</span></span>
```
Remove-AzSqlServerDnsAlias -Name <String> -ServerName <String> [-ResourceGroupName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3f2c-106">Kiszolgálói DNS-alias eltávolítása az AzureSqlServerDnsAliasModel példánydefinícióból</span><span class="sxs-lookup"><span data-stu-id="d3f2c-106">Remove a Server Dns Alias from AzureSqlServerDnsAliasModel instance definition</span></span>
```
Remove-AzSqlServerDnsAlias -InputObject <AzureSqlServerDnsAliasModel> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3f2c-107">Kiszolgálói DNS-alias eltávolítása Azure-erőforrás-azonosítóból</span><span class="sxs-lookup"><span data-stu-id="d3f2c-107">Remove a Server Dns Alias from an Azure resource id</span></span>
```
Remove-AzSqlServerDnsAlias -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3f2c-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d3f2c-108">DESCRIPTION</span></span>
<span data-ttu-id="d3f2c-109">Ez a parancs eltávolítja az Azure SQL Server DNS-aliasát a kiszolgálóról, változatlanul hagyva a kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="d3f2c-109">This commands remove Azure SQL Server DNS Alias from the server leaving server intact.</span></span>

## <span data-ttu-id="d3f2c-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d3f2c-110">EXAMPLES</span></span>

### <span data-ttu-id="d3f2c-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="d3f2c-111">Example 1</span></span>
```
PS C:\> Remove-AzSqlServerDnsAlias -DnsAliasName aliasName -ServerName serverName -ResourceGroupName rg
```

<span data-ttu-id="d3f2c-112">Eltávolítja az Azure SQL Server DNS-aliasát aName nevű névvel a kiszolgálóról aName névvel</span><span class="sxs-lookup"><span data-stu-id="d3f2c-112">Removes Azure SQL Server DNS Alias with the name aliasName from the server with the name serverName</span></span>

## <span data-ttu-id="d3f2c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3f2c-113">PARAMETERS</span></span>

### <span data-ttu-id="d3f2c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d3f2c-114">-AsJob</span></span>
<span data-ttu-id="d3f2c-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="d3f2c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d3f2c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3f2c-116">-DefaultProfile</span></span>
<span data-ttu-id="d3f2c-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d3f2c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3f2c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="d3f2c-118">-Force</span></span>
<span data-ttu-id="d3f2c-119">A művelet végrehajtásához szükséges megerősítő üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="d3f2c-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="d3f2c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3f2c-120">-InputObject</span></span>
<span data-ttu-id="d3f2c-121">The Server Dns Alias object to remove</span><span class="sxs-lookup"><span data-stu-id="d3f2c-121">The Server Dns Alias object to remove</span></span>

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

### <span data-ttu-id="d3f2c-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d3f2c-122">-Name</span></span>
<span data-ttu-id="d3f2c-123">Azure Sql Server DNS-alias neve</span><span class="sxs-lookup"><span data-stu-id="d3f2c-123">Azure Sql Server Dns Alias name</span></span>

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

### <span data-ttu-id="d3f2c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3f2c-124">-ResourceGroupName</span></span>
<span data-ttu-id="d3f2c-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d3f2c-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="d3f2c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3f2c-126">-ResourceId</span></span>
<span data-ttu-id="d3f2c-127">Az eltávolítható Kiszolgáló dns-alias objektum erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="d3f2c-127">The resource id of Server Dns Alias object to remove</span></span>

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

### <span data-ttu-id="d3f2c-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d3f2c-128">-ServerName</span></span>
<span data-ttu-id="d3f2c-129">Az Azure Sql Server neve.</span><span class="sxs-lookup"><span data-stu-id="d3f2c-129">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="d3f2c-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d3f2c-130">-Confirm</span></span>
<span data-ttu-id="d3f2c-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d3f2c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3f2c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3f2c-132">-WhatIf</span></span>
<span data-ttu-id="d3f2c-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d3f2c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3f2c-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d3f2c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3f2c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3f2c-135">CommonParameters</span></span>
<span data-ttu-id="d3f2c-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3f2c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3f2c-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d3f2c-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3f2c-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d3f2c-138">INPUTS</span></span>

### <span data-ttu-id="d3f2c-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="d3f2c-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

### <span data-ttu-id="d3f2c-140">System.String</span><span class="sxs-lookup"><span data-stu-id="d3f2c-140">System.String</span></span>

## <span data-ttu-id="d3f2c-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3f2c-141">OUTPUTS</span></span>

### <span data-ttu-id="d3f2c-142">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="d3f2c-142">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="d3f2c-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d3f2c-143">NOTES</span></span>

## <span data-ttu-id="d3f2c-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d3f2c-144">RELATED LINKS</span></span>
