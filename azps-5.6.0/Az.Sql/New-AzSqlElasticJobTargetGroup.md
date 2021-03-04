---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/new-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: 9a80504f1b3aff814d50b5b4aba98b488d1e55b6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927722"
---
# <span data-ttu-id="d8f52-101">New-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="d8f52-101">New-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="d8f52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8f52-102">SYNOPSIS</span></span>
<span data-ttu-id="d8f52-103">Új célcsoport létrehozása</span><span class="sxs-lookup"><span data-stu-id="d8f52-103">Creates a new target group</span></span>

## <span data-ttu-id="d8f52-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d8f52-104">SYNTAX</span></span>

### <span data-ttu-id="d8f52-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d8f52-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8f52-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="d8f52-106">ObjectSet</span></span>
```
New-AzSqlElasticJobTargetGroup [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8f52-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d8f52-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobTargetGroup [-ParentResourceId] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8f52-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d8f52-108">DESCRIPTION</span></span>
<span data-ttu-id="d8f52-109">A New-AzSqlElasticJobTargetGroup parancsmag létrehoz egy új célcsoportot</span><span class="sxs-lookup"><span data-stu-id="d8f52-109">The New-AzSqlElasticJobTargetGroup cmdlet creates a new target group</span></span>

## <span data-ttu-id="d8f52-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d8f52-110">EXAMPLES</span></span>

### <span data-ttu-id="d8f52-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="d8f52-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1
```

<span data-ttu-id="d8f52-112">Üres célcsoportot hoz létre</span><span class="sxs-lookup"><span data-stu-id="d8f52-112">Creates an empty target group</span></span>

## <span data-ttu-id="d8f52-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8f52-113">PARAMETERS</span></span>

### <span data-ttu-id="d8f52-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="d8f52-114">-AgentName</span></span>
<span data-ttu-id="d8f52-115">Az ügynök neve</span><span class="sxs-lookup"><span data-stu-id="d8f52-115">The agent name</span></span>

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

### <span data-ttu-id="d8f52-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8f52-116">-DefaultProfile</span></span>
<span data-ttu-id="d8f52-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d8f52-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8f52-118">-Name</span><span class="sxs-lookup"><span data-stu-id="d8f52-118">-Name</span></span>
<span data-ttu-id="d8f52-119">A célcsoport neve</span><span class="sxs-lookup"><span data-stu-id="d8f52-119">The target group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8f52-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d8f52-120">-ParentObject</span></span>
<span data-ttu-id="d8f52-121">Az ügynök beviteli objektuma</span><span class="sxs-lookup"><span data-stu-id="d8f52-121">The agent input object</span></span>

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

### <span data-ttu-id="d8f52-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d8f52-122">-ParentResourceId</span></span>
<span data-ttu-id="d8f52-123">Az ügynök erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="d8f52-123">The agent resource id</span></span>

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

### <span data-ttu-id="d8f52-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8f52-124">-ResourceGroupName</span></span>
<span data-ttu-id="d8f52-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="d8f52-125">The resource group name</span></span>

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

### <span data-ttu-id="d8f52-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d8f52-126">-ServerName</span></span>
<span data-ttu-id="d8f52-127">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="d8f52-127">The server name</span></span>

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

### <span data-ttu-id="d8f52-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d8f52-128">-Confirm</span></span>
<span data-ttu-id="d8f52-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d8f52-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8f52-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8f52-130">-WhatIf</span></span>
<span data-ttu-id="d8f52-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d8f52-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8f52-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d8f52-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8f52-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8f52-133">CommonParameters</span></span>
<span data-ttu-id="d8f52-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8f52-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8f52-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d8f52-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8f52-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d8f52-136">INPUTS</span></span>

### <span data-ttu-id="d8f52-137">Microsoft.Azure.Commands.Sql.ElasticMods.Model.AzureSqlElasticAgentModel</span><span class="sxs-lookup"><span data-stu-id="d8f52-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="d8f52-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d8f52-138">OUTPUTS</span></span>

### <span data-ttu-id="d8f52-139">Microsoft.Azure.Commands.Sql.ElasticMods.Model.AzureSqlElasticAsticTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="d8f52-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="d8f52-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d8f52-140">NOTES</span></span>

## <span data-ttu-id="d8f52-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d8f52-141">RELATED LINKS</span></span>
