---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: 5818bd11b3131ff340857e033053eb492a9178e6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014256"
---
# <span data-ttu-id="75f86-101">New-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="75f86-101">New-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="75f86-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="75f86-102">SYNOPSIS</span></span>
<span data-ttu-id="75f86-103">Új célcsoport létrehozása</span><span class="sxs-lookup"><span data-stu-id="75f86-103">Creates a new target group</span></span>

## <span data-ttu-id="75f86-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="75f86-104">SYNTAX</span></span>

### <span data-ttu-id="75f86-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="75f86-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75f86-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="75f86-106">ObjectSet</span></span>
```
New-AzSqlElasticJobTargetGroup [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75f86-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="75f86-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobTargetGroup [-ParentResourceId] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75f86-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="75f86-108">DESCRIPTION</span></span>
<span data-ttu-id="75f86-109">A New-AzSqlElasticJobTargetGroup parancsmag új célcsoportot hoz létre</span><span class="sxs-lookup"><span data-stu-id="75f86-109">The New-AzSqlElasticJobTargetGroup cmdlet creates a new target group</span></span>

## <span data-ttu-id="75f86-110">Példák</span><span class="sxs-lookup"><span data-stu-id="75f86-110">EXAMPLES</span></span>

### <span data-ttu-id="75f86-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="75f86-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1
```

<span data-ttu-id="75f86-112">Üres célcsoportot hoz létre</span><span class="sxs-lookup"><span data-stu-id="75f86-112">Creates an empty target group</span></span>

## <span data-ttu-id="75f86-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="75f86-113">PARAMETERS</span></span>

### <span data-ttu-id="75f86-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="75f86-114">-AgentName</span></span>
<span data-ttu-id="75f86-115">Az ügynök neve</span><span class="sxs-lookup"><span data-stu-id="75f86-115">The agent name</span></span>

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

### <span data-ttu-id="75f86-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75f86-116">-DefaultProfile</span></span>
<span data-ttu-id="75f86-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="75f86-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75f86-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="75f86-118">-Name</span></span>
<span data-ttu-id="75f86-119">A cél csoport neve</span><span class="sxs-lookup"><span data-stu-id="75f86-119">The target group name</span></span>

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

### <span data-ttu-id="75f86-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="75f86-120">-ParentObject</span></span>
<span data-ttu-id="75f86-121">Ügynök beviteli objektuma</span><span class="sxs-lookup"><span data-stu-id="75f86-121">The agent input object</span></span>

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

### <span data-ttu-id="75f86-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="75f86-122">-ParentResourceId</span></span>
<span data-ttu-id="75f86-123">Az ügynök erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="75f86-123">The agent resource id</span></span>

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

### <span data-ttu-id="75f86-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75f86-124">-ResourceGroupName</span></span>
<span data-ttu-id="75f86-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="75f86-125">The resource group name</span></span>

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

### <span data-ttu-id="75f86-126">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="75f86-126">-ServerName</span></span>
<span data-ttu-id="75f86-127">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="75f86-127">The server name</span></span>

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

### <span data-ttu-id="75f86-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="75f86-128">-Confirm</span></span>
<span data-ttu-id="75f86-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="75f86-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75f86-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75f86-130">-WhatIf</span></span>
<span data-ttu-id="75f86-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="75f86-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75f86-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="75f86-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75f86-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75f86-133">CommonParameters</span></span>
<span data-ttu-id="75f86-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="75f86-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75f86-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="75f86-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75f86-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="75f86-136">INPUTS</span></span>

### <span data-ttu-id="75f86-137">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="75f86-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="75f86-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="75f86-138">OUTPUTS</span></span>

### <span data-ttu-id="75f86-139">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="75f86-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="75f86-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="75f86-140">NOTES</span></span>

## <span data-ttu-id="75f86-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="75f86-141">RELATED LINKS</span></span>
