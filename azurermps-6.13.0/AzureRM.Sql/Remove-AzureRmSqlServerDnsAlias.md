---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerDnsAlias.md
ms.openlocfilehash: 5afd12ac027b19f888eb6a5110db2179dd6df24d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504280"
---
# <span data-ttu-id="0255a-101">Remove-AzureRmSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="0255a-101">Remove-AzureRmSqlServerDnsAlias</span></span>

## <span data-ttu-id="0255a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0255a-102">SYNOPSIS</span></span>
<span data-ttu-id="0255a-103">Eltávolítja az Azure SQL Server DNS-aliasát.</span><span class="sxs-lookup"><span data-stu-id="0255a-103">Removes Azure SQL Server DNS Alias.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0255a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0255a-104">SYNTAX</span></span>

### <span data-ttu-id="0255a-105">Kiszolgáló DNS-aliasának eltávolítása a parancsmag bemeneti paramétereivel</span><span class="sxs-lookup"><span data-stu-id="0255a-105">Remove a Server Dns Alias from cmdlet input parameters</span></span>
```
Remove-AzureRmSqlServerDnsAlias -Name <String> -ServerName <String> [-ResourceGroupName] <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0255a-106">Kiszolgáló DNS-aliasának eltávolítása a AzureSqlServerDnsAliasModel-példány definícióból</span><span class="sxs-lookup"><span data-stu-id="0255a-106">Remove a Server Dns Alias from AzureSqlServerDnsAliasModel instance definition</span></span>
```
Remove-AzureRmSqlServerDnsAlias -InputObject <AzureSqlServerDnsAliasModel> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0255a-107">Kiszolgáló DNS-aliasának eltávolítása Azure-erőforrás-azonosítóból</span><span class="sxs-lookup"><span data-stu-id="0255a-107">Remove a Server Dns Alias from an Azure resource id</span></span>
```
Remove-AzureRmSqlServerDnsAlias -ResourceId <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0255a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="0255a-108">DESCRIPTION</span></span>
<span data-ttu-id="0255a-109">Ez a parancs eltávolítja az Azure SQL Server DNS-aliasát attól a kiszolgálótól, amely érintetlenül hagyja a kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="0255a-109">This commands remove Azure SQL Server DNS Alias from the server leaving server intact.</span></span>

## <span data-ttu-id="0255a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="0255a-110">EXAMPLES</span></span>

### <span data-ttu-id="0255a-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0255a-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmSqlServerDnsAlias -DnsAliasName aliasName -ServerName serverName -ResourceGroupName rg
```

<span data-ttu-id="0255a-112">Az Azure SQL Server DNS-aliasának eltávolítása a aliasName nevű kiszolgáló nevével a kiszolgálónév névvel</span><span class="sxs-lookup"><span data-stu-id="0255a-112">Removes Azure SQL Server DNS Alias with the name aliasName from the server with the name serverName</span></span>

## <span data-ttu-id="0255a-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0255a-113">PARAMETERS</span></span>

### <span data-ttu-id="0255a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0255a-114">-AsJob</span></span>
<span data-ttu-id="0255a-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="0255a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0255a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0255a-116">-DefaultProfile</span></span>
<span data-ttu-id="0255a-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0255a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0255a-118">-Force</span><span class="sxs-lookup"><span data-stu-id="0255a-118">-Force</span></span>
<span data-ttu-id="0255a-119">A művelet végrehajtásához szükséges megerősítési üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="0255a-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="0255a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0255a-120">-InputObject</span></span>
<span data-ttu-id="0255a-121">A kiszolgáló DNS-alias objektum eltávolítása</span><span class="sxs-lookup"><span data-stu-id="0255a-121">The Server Dns Alias object to remove</span></span>

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

### <span data-ttu-id="0255a-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0255a-122">-Name</span></span>
<span data-ttu-id="0255a-123">Azure SQL Server DNS-alias neve</span><span class="sxs-lookup"><span data-stu-id="0255a-123">Azure Sql Server Dns Alias name</span></span>

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

### <span data-ttu-id="0255a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0255a-124">-ResourceGroupName</span></span>
<span data-ttu-id="0255a-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0255a-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="0255a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0255a-126">-ResourceId</span></span>
<span data-ttu-id="0255a-127">A kiszolgáló DNS-alias objektuma eltávolítandó erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="0255a-127">The resource id of Server Dns Alias object to remove</span></span>

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

### <span data-ttu-id="0255a-128">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="0255a-128">-ServerName</span></span>
<span data-ttu-id="0255a-129">Az Azure SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="0255a-129">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="0255a-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0255a-130">-Confirm</span></span>
<span data-ttu-id="0255a-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0255a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0255a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0255a-132">-WhatIf</span></span>
<span data-ttu-id="0255a-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0255a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0255a-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0255a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0255a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0255a-135">CommonParameters</span></span>
<span data-ttu-id="0255a-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0255a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0255a-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0255a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0255a-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0255a-138">INPUTS</span></span>

### <span data-ttu-id="0255a-139">Microsoft. Azure. Command. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="0255a-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>
<span data-ttu-id="0255a-140">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0255a-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="0255a-141">System. String</span><span class="sxs-lookup"><span data-stu-id="0255a-141">System.String</span></span>

## <span data-ttu-id="0255a-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0255a-142">OUTPUTS</span></span>

### <span data-ttu-id="0255a-143">Microsoft. Azure. Command. SQL. ServerDnsAlias. Model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="0255a-143">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="0255a-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0255a-144">NOTES</span></span>

## <span data-ttu-id="0255a-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0255a-145">RELATED LINKS</span></span>
