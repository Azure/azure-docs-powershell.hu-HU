---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDnsAlias.md
ms.openlocfilehash: d611f0bc14d657f47881cbdfbb1326111873114a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186525"
---
# <span data-ttu-id="1ece3-101">Remove-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="1ece3-101">Remove-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="1ece3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1ece3-102">SYNOPSIS</span></span>
<span data-ttu-id="1ece3-103">Eltávolítja az Azure SQL Server DNS-aliasát.</span><span class="sxs-lookup"><span data-stu-id="1ece3-103">Removes Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="1ece3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1ece3-104">SYNTAX</span></span>

### <span data-ttu-id="1ece3-105">Kiszolgáló DNS-aliasának eltávolítása a parancsmag bemeneti paramétereivel</span><span class="sxs-lookup"><span data-stu-id="1ece3-105">Remove a Server Dns Alias from cmdlet input parameters</span></span>
```
Remove-AzSqlServerDnsAlias -Name <String> -ServerName <String> [-ResourceGroupName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ece3-106">Kiszolgáló DNS-aliasának eltávolítása a AzureSqlServerDnsAliasModel-példány definícióból</span><span class="sxs-lookup"><span data-stu-id="1ece3-106">Remove a Server Dns Alias from AzureSqlServerDnsAliasModel instance definition</span></span>
```
Remove-AzSqlServerDnsAlias -InputObject <AzureSqlServerDnsAliasModel> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ece3-107">Kiszolgáló DNS-aliasának eltávolítása Azure-erőforrás-azonosítóból</span><span class="sxs-lookup"><span data-stu-id="1ece3-107">Remove a Server Dns Alias from an Azure resource id</span></span>
```
Remove-AzSqlServerDnsAlias -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ece3-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1ece3-108">DESCRIPTION</span></span>
<span data-ttu-id="1ece3-109">Ez a parancs eltávolítja az Azure SQL Server DNS-aliasát attól a kiszolgálótól, amely érintetlenül hagyja a kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="1ece3-109">This commands remove Azure SQL Server DNS Alias from the server leaving server intact.</span></span>

## <span data-ttu-id="1ece3-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1ece3-110">EXAMPLES</span></span>

### <span data-ttu-id="1ece3-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1ece3-111">Example 1</span></span>
```
PS C:\> Remove-AzSqlServerDnsAlias -DnsAliasName aliasName -ServerName serverName -ResourceGroupName rg
```

<span data-ttu-id="1ece3-112">Az Azure SQL Server DNS-aliasának eltávolítása a aliasName nevű kiszolgáló nevével a kiszolgálónév névvel</span><span class="sxs-lookup"><span data-stu-id="1ece3-112">Removes Azure SQL Server DNS Alias with the name aliasName from the server with the name serverName</span></span>

## <span data-ttu-id="1ece3-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1ece3-113">PARAMETERS</span></span>

### <span data-ttu-id="1ece3-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1ece3-114">-AsJob</span></span>
<span data-ttu-id="1ece3-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="1ece3-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1ece3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ece3-116">-DefaultProfile</span></span>
<span data-ttu-id="1ece3-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1ece3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ece3-118">-Force</span><span class="sxs-lookup"><span data-stu-id="1ece3-118">-Force</span></span>
<span data-ttu-id="1ece3-119">A művelet végrehajtásához szükséges megerősítési üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="1ece3-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="1ece3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ece3-120">-InputObject</span></span>
<span data-ttu-id="1ece3-121">A kiszolgáló DNS-alias objektum eltávolítása</span><span class="sxs-lookup"><span data-stu-id="1ece3-121">The Server Dns Alias object to remove</span></span>

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

### <span data-ttu-id="1ece3-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1ece3-122">-Name</span></span>
<span data-ttu-id="1ece3-123">Azure SQL Server DNS-alias neve</span><span class="sxs-lookup"><span data-stu-id="1ece3-123">Azure Sql Server Dns Alias name</span></span>

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

### <span data-ttu-id="1ece3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ece3-124">-ResourceGroupName</span></span>
<span data-ttu-id="1ece3-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1ece3-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="1ece3-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1ece3-126">-ResourceId</span></span>
<span data-ttu-id="1ece3-127">A kiszolgáló DNS-alias objektuma eltávolítandó erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="1ece3-127">The resource id of Server Dns Alias object to remove</span></span>

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

### <span data-ttu-id="1ece3-128">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="1ece3-128">-ServerName</span></span>
<span data-ttu-id="1ece3-129">Az Azure SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="1ece3-129">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="1ece3-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1ece3-130">-Confirm</span></span>
<span data-ttu-id="1ece3-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1ece3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ece3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ece3-132">-WhatIf</span></span>
<span data-ttu-id="1ece3-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1ece3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ece3-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1ece3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ece3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ece3-135">CommonParameters</span></span>
<span data-ttu-id="1ece3-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1ece3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ece3-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1ece3-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ece3-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ece3-138">INPUTS</span></span>

### <span data-ttu-id="1ece3-139">Microsoft. Azure. Command. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="1ece3-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

### <span data-ttu-id="1ece3-140">System. String</span><span class="sxs-lookup"><span data-stu-id="1ece3-140">System.String</span></span>

## <span data-ttu-id="1ece3-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ece3-141">OUTPUTS</span></span>

### <span data-ttu-id="1ece3-142">Microsoft. Azure. Command. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="1ece3-142">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="1ece3-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1ece3-143">NOTES</span></span>

## <span data-ttu-id="1ece3-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1ece3-144">RELATED LINKS</span></span>
