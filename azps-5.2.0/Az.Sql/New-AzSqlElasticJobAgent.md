---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobAgent.md
ms.openlocfilehash: f00c2e9cb7b9d0d35efdf99a6f81f24488dd8387
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325202"
---
# <span data-ttu-id="c3091-101">New-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="c3091-101">New-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="c3091-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3091-102">SYNOPSIS</span></span>
<span data-ttu-id="c3091-103">Új rugalmas ügynök létrehozása</span><span class="sxs-lookup"><span data-stu-id="c3091-103">Creates a new elastic job agent</span></span>

## <span data-ttu-id="c3091-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c3091-104">SYNTAX</span></span>

### <span data-ttu-id="c3091-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c3091-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-Name] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c3091-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="c3091-106">ObjectSet</span></span>
```
New-AzSqlElasticJobAgent [-DatabaseObject] <AzureSqlDatabaseModel> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3091-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c3091-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobAgent [-DatabaseResourceId] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3091-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c3091-108">DESCRIPTION</span></span>
<span data-ttu-id="c3091-109">A New-AzSqlElasticJobAgent parancsmag létrehoz egy új Rugalmas feladat ügynököt</span><span class="sxs-lookup"><span data-stu-id="c3091-109">The New-AzSqlElasticJobAgent cmdlet creates a new Elastic Job agent</span></span>

## <span data-ttu-id="c3091-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c3091-110">EXAMPLES</span></span>

### <span data-ttu-id="c3091-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="c3091-111">Example 1</span></span>
```
PS C:\> New-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -DatabaseName jobdb -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready
```

<span data-ttu-id="c3091-112">Új rugalmassági ügynök létrehozása</span><span class="sxs-lookup"><span data-stu-id="c3091-112">Creates a new Elastic Job agent</span></span>

## <span data-ttu-id="c3091-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3091-113">PARAMETERS</span></span>

### <span data-ttu-id="c3091-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c3091-114">-DatabaseName</span></span>
<span data-ttu-id="c3091-115">Az adatbázis neve</span><span class="sxs-lookup"><span data-stu-id="c3091-115">The database name</span></span>

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

### <span data-ttu-id="c3091-116">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="c3091-116">-DatabaseObject</span></span>
<span data-ttu-id="c3091-117">The Agent Control Database Object</span><span class="sxs-lookup"><span data-stu-id="c3091-117">The Agent Control Database Object</span></span>

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

### <span data-ttu-id="c3091-118">-DatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="c3091-118">-DatabaseResourceId</span></span>
<span data-ttu-id="c3091-119">The Agent Control Database Resource Id</span><span class="sxs-lookup"><span data-stu-id="c3091-119">The Agent Control Database Resource Id</span></span>

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

### <span data-ttu-id="c3091-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3091-120">-DefaultProfile</span></span>
<span data-ttu-id="c3091-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c3091-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3091-122">-Name</span><span class="sxs-lookup"><span data-stu-id="c3091-122">-Name</span></span>
<span data-ttu-id="c3091-123">Ügynök neve</span><span class="sxs-lookup"><span data-stu-id="c3091-123">The Agent Name</span></span>

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

### <span data-ttu-id="c3091-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3091-124">-ResourceGroupName</span></span>
<span data-ttu-id="c3091-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="c3091-125">The resource group name</span></span>

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

### <span data-ttu-id="c3091-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c3091-126">-ServerName</span></span>
<span data-ttu-id="c3091-127">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="c3091-127">The server name</span></span>

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

### <span data-ttu-id="c3091-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="c3091-128">-Tag</span></span>
<span data-ttu-id="c3091-129">Ügynökcímkék</span><span class="sxs-lookup"><span data-stu-id="c3091-129">The Agent Tags</span></span>

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

### <span data-ttu-id="c3091-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c3091-130">-Confirm</span></span>
<span data-ttu-id="c3091-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c3091-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3091-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3091-132">-WhatIf</span></span>
<span data-ttu-id="c3091-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c3091-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3091-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c3091-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3091-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3091-135">CommonParameters</span></span>
<span data-ttu-id="c3091-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3091-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3091-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c3091-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3091-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c3091-138">INPUTS</span></span>

### <span data-ttu-id="c3091-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="c3091-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="c3091-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3091-140">OUTPUTS</span></span>

### <span data-ttu-id="c3091-141">Microsoft.Azure.Commands.Sql.ElasticMods.Model.AzureSqlElasticAgentModel</span><span class="sxs-lookup"><span data-stu-id="c3091-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="c3091-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c3091-142">NOTES</span></span>

## <span data-ttu-id="c3091-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c3091-143">RELATED LINKS</span></span>
