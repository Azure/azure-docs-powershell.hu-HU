---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobAgent.md
ms.openlocfilehash: 1352ef72ffc6fd757b4019e217ecb439495ebb44
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467116"
---
# <span data-ttu-id="64a82-101">Remove-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="64a82-101">Remove-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="64a82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64a82-102">SYNOPSIS</span></span>
<span data-ttu-id="64a82-103">A rugalmas munka ügynök eltávolítása</span><span class="sxs-lookup"><span data-stu-id="64a82-103">Removes the elastic job agent</span></span>

## <span data-ttu-id="64a82-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="64a82-104">SYNTAX</span></span>

### <span data-ttu-id="64a82-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="64a82-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64a82-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="64a82-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64a82-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="64a82-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobAgent [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64a82-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="64a82-108">DESCRIPTION</span></span>
<span data-ttu-id="64a82-109">A Remove-AzSqlElasticJobAgent parancsmag eltávolítja a Rugalmas feladat ügynököt</span><span class="sxs-lookup"><span data-stu-id="64a82-109">The Remove-AzSqlElasticJobAgent cmdlet removes an Elastic Job agent</span></span>

## <span data-ttu-id="64a82-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="64a82-110">EXAMPLES</span></span>

### <span data-ttu-id="64a82-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="64a82-111">Example 1</span></span>
```
PS C:\> Remove-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="64a82-112">Rugalmas feladatú ügynök eltávolítása</span><span class="sxs-lookup"><span data-stu-id="64a82-112">Removes an Elastic Job agent</span></span>

## <span data-ttu-id="64a82-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64a82-113">PARAMETERS</span></span>

### <span data-ttu-id="64a82-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64a82-114">-DefaultProfile</span></span>
<span data-ttu-id="64a82-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="64a82-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64a82-116">-Force</span><span class="sxs-lookup"><span data-stu-id="64a82-116">-Force</span></span>
<span data-ttu-id="64a82-117">A művelet végrehajtásához szükséges megerősítő üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="64a82-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="64a82-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64a82-118">-InputObject</span></span>
<span data-ttu-id="64a82-119">Az ügynökobjektum</span><span class="sxs-lookup"><span data-stu-id="64a82-119">The agent object</span></span>

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

### <span data-ttu-id="64a82-120">-Name</span><span class="sxs-lookup"><span data-stu-id="64a82-120">-Name</span></span>
<span data-ttu-id="64a82-121">Az ügynök neve</span><span class="sxs-lookup"><span data-stu-id="64a82-121">The agent name</span></span>

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

### <span data-ttu-id="64a82-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64a82-122">-ResourceGroupName</span></span>
<span data-ttu-id="64a82-123">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="64a82-123">The resource group name</span></span>

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

### <span data-ttu-id="64a82-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="64a82-124">-ResourceId</span></span>
<span data-ttu-id="64a82-125">Az ügynök erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="64a82-125">The agent resource id</span></span>

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

### <span data-ttu-id="64a82-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="64a82-126">-ServerName</span></span>
<span data-ttu-id="64a82-127">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="64a82-127">The server name</span></span>

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

### <span data-ttu-id="64a82-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="64a82-128">-Confirm</span></span>
<span data-ttu-id="64a82-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="64a82-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64a82-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64a82-130">-WhatIf</span></span>
<span data-ttu-id="64a82-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="64a82-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64a82-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="64a82-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64a82-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64a82-133">CommonParameters</span></span>
<span data-ttu-id="64a82-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64a82-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64a82-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="64a82-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64a82-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="64a82-136">INPUTS</span></span>

### <span data-ttu-id="64a82-137">Microsoft.Azure.Commands.Sql.ElasticMods.Model.AzureSqlElasticAgentModel</span><span class="sxs-lookup"><span data-stu-id="64a82-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="64a82-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="64a82-138">OUTPUTS</span></span>

### <span data-ttu-id="64a82-139">Microsoft.Azure.Commands.Sql.ElasticMods.Model.AzureSqlElasticAgentModel</span><span class="sxs-lookup"><span data-stu-id="64a82-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="64a82-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="64a82-140">NOTES</span></span>

## <span data-ttu-id="64a82-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="64a82-141">RELATED LINKS</span></span>
