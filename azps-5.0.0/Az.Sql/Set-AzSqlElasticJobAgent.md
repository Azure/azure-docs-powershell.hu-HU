---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
ms.openlocfilehash: 58adbb3b160272007899dc8740e211b6e81a10a4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301769"
---
# <span data-ttu-id="eb3d9-101">Set-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="eb3d9-101">Set-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="eb3d9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eb3d9-102">SYNOPSIS</span></span>
<span data-ttu-id="eb3d9-103">Rugalmas munkatárs frissítése</span><span class="sxs-lookup"><span data-stu-id="eb3d9-103">Updates an elastic job agent</span></span>

## <span data-ttu-id="eb3d9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eb3d9-104">SYNTAX</span></span>

### <span data-ttu-id="eb3d9-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="eb3d9-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb3d9-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="eb3d9-106">ObjectSet</span></span>
```
Set-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb3d9-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="eb3d9-107">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb3d9-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="eb3d9-108">DESCRIPTION</span></span>
<span data-ttu-id="eb3d9-109">A Set-AzSqlElasticJobAgent parancsmag rugalmas munkaügynököket frissít</span><span class="sxs-lookup"><span data-stu-id="eb3d9-109">The Set-AzSqlElasticJobAgent cmdlet updates an Elastic Job agents</span></span>

## <span data-ttu-id="eb3d9-110">Példák</span><span class="sxs-lookup"><span data-stu-id="eb3d9-110">EXAMPLES</span></span>

### <span data-ttu-id="eb3d9-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="eb3d9-111">Example 1</span></span>
```
PS C:\> Set-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent -Tag @{ Octopus = "Agent" }

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="eb3d9-112">Rugalmas munkatárs frissítése</span><span class="sxs-lookup"><span data-stu-id="eb3d9-112">Updates an Elastic Job agent</span></span>

## <span data-ttu-id="eb3d9-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eb3d9-113">PARAMETERS</span></span>

### <span data-ttu-id="eb3d9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb3d9-114">-DefaultProfile</span></span>
<span data-ttu-id="eb3d9-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eb3d9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb3d9-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eb3d9-116">-InputObject</span></span>
<span data-ttu-id="eb3d9-117">Ügynök beviteli objektuma</span><span class="sxs-lookup"><span data-stu-id="eb3d9-117">The agent input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb3d9-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="eb3d9-118">-Name</span></span>
<span data-ttu-id="eb3d9-119">Az ügynök neve</span><span class="sxs-lookup"><span data-stu-id="eb3d9-119">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: AgentName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb3d9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb3d9-120">-ResourceGroupName</span></span>
<span data-ttu-id="eb3d9-121">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="eb3d9-121">The resource group name</span></span>

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

### <span data-ttu-id="eb3d9-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb3d9-122">-ResourceId</span></span>
<span data-ttu-id="eb3d9-123">Az ügynök erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="eb3d9-123">The agent resource id</span></span>

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

### <span data-ttu-id="eb3d9-124">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="eb3d9-124">-ServerName</span></span>
<span data-ttu-id="eb3d9-125">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="eb3d9-125">The server name</span></span>

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

### <span data-ttu-id="eb3d9-126">-Címke</span><span class="sxs-lookup"><span data-stu-id="eb3d9-126">-Tag</span></span>
<span data-ttu-id="eb3d9-127">Az Azure SQL adatbázis-ügynökkel társítani kívánt Címkék</span><span class="sxs-lookup"><span data-stu-id="eb3d9-127">The tags to associate with the Azure SQL Database Agent</span></span>

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

### <span data-ttu-id="eb3d9-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="eb3d9-128">-Confirm</span></span>
<span data-ttu-id="eb3d9-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="eb3d9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb3d9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb3d9-130">-WhatIf</span></span>
<span data-ttu-id="eb3d9-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="eb3d9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb3d9-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="eb3d9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb3d9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb3d9-133">CommonParameters</span></span>
<span data-ttu-id="eb3d9-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eb3d9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb3d9-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="eb3d9-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb3d9-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb3d9-136">INPUTS</span></span>

### <span data-ttu-id="eb3d9-137">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="eb3d9-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="eb3d9-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb3d9-138">OUTPUTS</span></span>

### <span data-ttu-id="eb3d9-139">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="eb3d9-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="eb3d9-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eb3d9-140">NOTES</span></span>

## <span data-ttu-id="eb3d9-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eb3d9-141">RELATED LINKS</span></span>
