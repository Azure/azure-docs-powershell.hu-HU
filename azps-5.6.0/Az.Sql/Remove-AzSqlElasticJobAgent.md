---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/remove-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobAgent.md
ms.openlocfilehash: 3c6a92a205aef19b1e4cef4842de4cf0414c2397
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921561"
---
# <span data-ttu-id="12da8-101">Remove-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="12da8-101">Remove-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="12da8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12da8-102">SYNOPSIS</span></span>
<span data-ttu-id="12da8-103">A rugalmas munka ügynök eltávolítása</span><span class="sxs-lookup"><span data-stu-id="12da8-103">Removes the elastic job agent</span></span>

## <span data-ttu-id="12da8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="12da8-104">SYNTAX</span></span>

### <span data-ttu-id="12da8-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="12da8-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12da8-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="12da8-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12da8-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="12da8-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobAgent [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12da8-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="12da8-108">DESCRIPTION</span></span>
<span data-ttu-id="12da8-109">A Remove-AzSqlElasticJobAgent parancsmag eltávolítja a Rugalmas feladat ügynököt</span><span class="sxs-lookup"><span data-stu-id="12da8-109">The Remove-AzSqlElasticJobAgent cmdlet removes an Elastic Job agent</span></span>

## <span data-ttu-id="12da8-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="12da8-110">EXAMPLES</span></span>

### <span data-ttu-id="12da8-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="12da8-111">Example 1</span></span>
```
PS C:\> Remove-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="12da8-112">Rugalmas feladatú ügynök eltávolítása</span><span class="sxs-lookup"><span data-stu-id="12da8-112">Removes an Elastic Job agent</span></span>

## <span data-ttu-id="12da8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="12da8-113">PARAMETERS</span></span>

### <span data-ttu-id="12da8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12da8-114">-DefaultProfile</span></span>
<span data-ttu-id="12da8-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="12da8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12da8-116">-Force</span><span class="sxs-lookup"><span data-stu-id="12da8-116">-Force</span></span>
<span data-ttu-id="12da8-117">A művelet végrehajtásához szükséges megerősítő üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="12da8-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="12da8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="12da8-118">-InputObject</span></span>
<span data-ttu-id="12da8-119">Az ügynökobjektum</span><span class="sxs-lookup"><span data-stu-id="12da8-119">The agent object</span></span>

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

### <span data-ttu-id="12da8-120">-Name</span><span class="sxs-lookup"><span data-stu-id="12da8-120">-Name</span></span>
<span data-ttu-id="12da8-121">Az ügynök neve</span><span class="sxs-lookup"><span data-stu-id="12da8-121">The agent name</span></span>

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

### <span data-ttu-id="12da8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12da8-122">-ResourceGroupName</span></span>
<span data-ttu-id="12da8-123">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="12da8-123">The resource group name</span></span>

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

### <span data-ttu-id="12da8-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12da8-124">-ResourceId</span></span>
<span data-ttu-id="12da8-125">Az ügynök erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="12da8-125">The agent resource id</span></span>

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

### <span data-ttu-id="12da8-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="12da8-126">-ServerName</span></span>
<span data-ttu-id="12da8-127">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="12da8-127">The server name</span></span>

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

### <span data-ttu-id="12da8-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="12da8-128">-Confirm</span></span>
<span data-ttu-id="12da8-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="12da8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12da8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12da8-130">-WhatIf</span></span>
<span data-ttu-id="12da8-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="12da8-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12da8-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="12da8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12da8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12da8-133">CommonParameters</span></span>
<span data-ttu-id="12da8-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12da8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12da8-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="12da8-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12da8-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="12da8-136">INPUTS</span></span>

### <span data-ttu-id="12da8-137">Microsoft.Azure.Commands.Sql.ElasticMods.Model.AzureSqlElasticAgentModel</span><span class="sxs-lookup"><span data-stu-id="12da8-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="12da8-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="12da8-138">OUTPUTS</span></span>

### <span data-ttu-id="12da8-139">Microsoft.Azure.Commands.Sql.ElasticMods.Model.AzureSqlElasticAgentModel</span><span class="sxs-lookup"><span data-stu-id="12da8-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="12da8-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="12da8-140">NOTES</span></span>

## <span data-ttu-id="12da8-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="12da8-141">RELATED LINKS</span></span>
