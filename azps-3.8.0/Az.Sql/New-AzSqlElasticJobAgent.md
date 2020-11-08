---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobAgent.md
ms.openlocfilehash: f00c2e9cb7b9d0d35efdf99a6f81f24488dd8387
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011670"
---
# <span data-ttu-id="2536b-101">New-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="2536b-101">New-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="2536b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2536b-102">SYNOPSIS</span></span>
<span data-ttu-id="2536b-103">Új elasztikus munkatárs létrehozása</span><span class="sxs-lookup"><span data-stu-id="2536b-103">Creates a new elastic job agent</span></span>

## <span data-ttu-id="2536b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2536b-104">SYNTAX</span></span>

### <span data-ttu-id="2536b-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2536b-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-Name] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2536b-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="2536b-106">ObjectSet</span></span>
```
New-AzSqlElasticJobAgent [-DatabaseObject] <AzureSqlDatabaseModel> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2536b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2536b-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobAgent [-DatabaseResourceId] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2536b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2536b-108">DESCRIPTION</span></span>
<span data-ttu-id="2536b-109">A New-AzSqlElasticJobAgent parancsmag új rugalmas munkatársat hoz létre</span><span class="sxs-lookup"><span data-stu-id="2536b-109">The New-AzSqlElasticJobAgent cmdlet creates a new Elastic Job agent</span></span>

## <span data-ttu-id="2536b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="2536b-110">EXAMPLES</span></span>

### <span data-ttu-id="2536b-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2536b-111">Example 1</span></span>
```
PS C:\> New-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -DatabaseName jobdb -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready
```

<span data-ttu-id="2536b-112">Új elasztikus munkatárs létrehozása</span><span class="sxs-lookup"><span data-stu-id="2536b-112">Creates a new Elastic Job agent</span></span>

## <span data-ttu-id="2536b-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2536b-113">PARAMETERS</span></span>

### <span data-ttu-id="2536b-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2536b-114">-DatabaseName</span></span>
<span data-ttu-id="2536b-115">Az adatbázis neve</span><span class="sxs-lookup"><span data-stu-id="2536b-115">The database name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2536b-116">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="2536b-116">-DatabaseObject</span></span>
<span data-ttu-id="2536b-117">Az Agent Control Database objektum</span><span class="sxs-lookup"><span data-stu-id="2536b-117">The Agent Control Database Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2536b-118">-DatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="2536b-118">-DatabaseResourceId</span></span>
<span data-ttu-id="2536b-119">Az Agent vezérlő adatbázis-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="2536b-119">The Agent Control Database Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2536b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2536b-120">-DefaultProfile</span></span>
<span data-ttu-id="2536b-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2536b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2536b-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2536b-122">-Name</span></span>
<span data-ttu-id="2536b-123">Az ügynök neve</span><span class="sxs-lookup"><span data-stu-id="2536b-123">The Agent Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AgentName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2536b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2536b-124">-ResourceGroupName</span></span>
<span data-ttu-id="2536b-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="2536b-125">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2536b-126">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="2536b-126">-ServerName</span></span>
<span data-ttu-id="2536b-127">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="2536b-127">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2536b-128">-Címke</span><span class="sxs-lookup"><span data-stu-id="2536b-128">-Tag</span></span>
<span data-ttu-id="2536b-129">Az ügynök címkéi</span><span class="sxs-lookup"><span data-stu-id="2536b-129">The Agent Tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2536b-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2536b-130">-Confirm</span></span>
<span data-ttu-id="2536b-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2536b-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2536b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2536b-132">-WhatIf</span></span>
<span data-ttu-id="2536b-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2536b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2536b-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2536b-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2536b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2536b-135">CommonParameters</span></span>
<span data-ttu-id="2536b-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2536b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2536b-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2536b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2536b-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2536b-138">INPUTS</span></span>

### <span data-ttu-id="2536b-139">Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="2536b-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="2536b-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2536b-140">OUTPUTS</span></span>

### <span data-ttu-id="2536b-141">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="2536b-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="2536b-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2536b-142">NOTES</span></span>

## <span data-ttu-id="2536b-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2536b-143">RELATED LINKS</span></span>
