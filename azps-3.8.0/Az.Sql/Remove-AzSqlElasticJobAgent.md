---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobAgent.md
ms.openlocfilehash: 1352ef72ffc6fd757b4019e217ecb439495ebb44
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013190"
---
# <span data-ttu-id="5fb6b-101">Remove-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="5fb6b-101">Remove-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="5fb6b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5fb6b-102">SYNOPSIS</span></span>
<span data-ttu-id="5fb6b-103">A rugalmas munkatárs eltávolítása</span><span class="sxs-lookup"><span data-stu-id="5fb6b-103">Removes the elastic job agent</span></span>

## <span data-ttu-id="5fb6b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5fb6b-104">SYNTAX</span></span>

### <span data-ttu-id="5fb6b-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5fb6b-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5fb6b-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="5fb6b-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5fb6b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5fb6b-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobAgent [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fb6b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="5fb6b-108">DESCRIPTION</span></span>
<span data-ttu-id="5fb6b-109">A Remove-AzSqlElasticJobAgent parancsmag egy rugalmas munkaügynököt távolít el</span><span class="sxs-lookup"><span data-stu-id="5fb6b-109">The Remove-AzSqlElasticJobAgent cmdlet removes an Elastic Job agent</span></span>

## <span data-ttu-id="5fb6b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="5fb6b-110">EXAMPLES</span></span>

### <span data-ttu-id="5fb6b-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5fb6b-111">Example 1</span></span>
```
PS C:\> Remove-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="5fb6b-112">Rugalmas munkatárs eltávolítása</span><span class="sxs-lookup"><span data-stu-id="5fb6b-112">Removes an Elastic Job agent</span></span>

## <span data-ttu-id="5fb6b-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5fb6b-113">PARAMETERS</span></span>

### <span data-ttu-id="5fb6b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fb6b-114">-DefaultProfile</span></span>
<span data-ttu-id="5fb6b-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5fb6b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5fb6b-116">-Force</span><span class="sxs-lookup"><span data-stu-id="5fb6b-116">-Force</span></span>
<span data-ttu-id="5fb6b-117">A művelet végrehajtásához szükséges megerősítési üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="5fb6b-117">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fb6b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5fb6b-118">-InputObject</span></span>
<span data-ttu-id="5fb6b-119">Az Agent objektum</span><span class="sxs-lookup"><span data-stu-id="5fb6b-119">The agent object</span></span>

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

### <span data-ttu-id="5fb6b-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5fb6b-120">-Name</span></span>
<span data-ttu-id="5fb6b-121">Az ügynök neve</span><span class="sxs-lookup"><span data-stu-id="5fb6b-121">The agent name</span></span>

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

### <span data-ttu-id="5fb6b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fb6b-122">-ResourceGroupName</span></span>
<span data-ttu-id="5fb6b-123">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="5fb6b-123">The resource group name</span></span>

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

### <span data-ttu-id="5fb6b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5fb6b-124">-ResourceId</span></span>
<span data-ttu-id="5fb6b-125">Az ügynök erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="5fb6b-125">The agent resource id</span></span>

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

### <span data-ttu-id="5fb6b-126">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="5fb6b-126">-ServerName</span></span>
<span data-ttu-id="5fb6b-127">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="5fb6b-127">The server name</span></span>

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

### <span data-ttu-id="5fb6b-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5fb6b-128">-Confirm</span></span>
<span data-ttu-id="5fb6b-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5fb6b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fb6b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fb6b-130">-WhatIf</span></span>
<span data-ttu-id="5fb6b-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5fb6b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fb6b-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5fb6b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fb6b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fb6b-133">CommonParameters</span></span>
<span data-ttu-id="5fb6b-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5fb6b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fb6b-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5fb6b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fb6b-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5fb6b-136">INPUTS</span></span>

### <span data-ttu-id="5fb6b-137">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="5fb6b-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="5fb6b-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5fb6b-138">OUTPUTS</span></span>

### <span data-ttu-id="5fb6b-139">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="5fb6b-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="5fb6b-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5fb6b-140">NOTES</span></span>

## <span data-ttu-id="5fb6b-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5fb6b-141">RELATED LINKS</span></span>
