---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: 5818bd11b3131ff340857e033053eb492a9178e6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186674"
---
# <span data-ttu-id="c1320-101">New-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="c1320-101">New-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="c1320-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c1320-102">SYNOPSIS</span></span>
<span data-ttu-id="c1320-103">Új célcsoport létrehozása</span><span class="sxs-lookup"><span data-stu-id="c1320-103">Creates a new target group</span></span>

## <span data-ttu-id="c1320-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c1320-104">SYNTAX</span></span>

### <span data-ttu-id="c1320-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c1320-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1320-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="c1320-106">ObjectSet</span></span>
```
New-AzSqlElasticJobTargetGroup [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1320-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c1320-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobTargetGroup [-ParentResourceId] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1320-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c1320-108">DESCRIPTION</span></span>
<span data-ttu-id="c1320-109">A New-AzSqlElasticJobTargetGroup parancsmag új célcsoportot hoz létre</span><span class="sxs-lookup"><span data-stu-id="c1320-109">The New-AzSqlElasticJobTargetGroup cmdlet creates a new target group</span></span>

## <span data-ttu-id="c1320-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c1320-110">EXAMPLES</span></span>

### <span data-ttu-id="c1320-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c1320-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1
```

<span data-ttu-id="c1320-112">Üres célcsoportot hoz létre</span><span class="sxs-lookup"><span data-stu-id="c1320-112">Creates an empty target group</span></span>

## <span data-ttu-id="c1320-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c1320-113">PARAMETERS</span></span>

### <span data-ttu-id="c1320-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="c1320-114">-AgentName</span></span>
<span data-ttu-id="c1320-115">Az ügynök neve</span><span class="sxs-lookup"><span data-stu-id="c1320-115">The agent name</span></span>

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

### <span data-ttu-id="c1320-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1320-116">-DefaultProfile</span></span>
<span data-ttu-id="c1320-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c1320-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1320-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c1320-118">-Name</span></span>
<span data-ttu-id="c1320-119">A cél csoport neve</span><span class="sxs-lookup"><span data-stu-id="c1320-119">The target group name</span></span>

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

### <span data-ttu-id="c1320-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c1320-120">-ParentObject</span></span>
<span data-ttu-id="c1320-121">Ügynök beviteli objektuma</span><span class="sxs-lookup"><span data-stu-id="c1320-121">The agent input object</span></span>

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

### <span data-ttu-id="c1320-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="c1320-122">-ParentResourceId</span></span>
<span data-ttu-id="c1320-123">Az ügynök erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="c1320-123">The agent resource id</span></span>

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

### <span data-ttu-id="c1320-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1320-124">-ResourceGroupName</span></span>
<span data-ttu-id="c1320-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="c1320-125">The resource group name</span></span>

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

### <span data-ttu-id="c1320-126">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="c1320-126">-ServerName</span></span>
<span data-ttu-id="c1320-127">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="c1320-127">The server name</span></span>

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

### <span data-ttu-id="c1320-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c1320-128">-Confirm</span></span>
<span data-ttu-id="c1320-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c1320-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1320-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1320-130">-WhatIf</span></span>
<span data-ttu-id="c1320-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c1320-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1320-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c1320-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1320-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1320-133">CommonParameters</span></span>
<span data-ttu-id="c1320-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c1320-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1320-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c1320-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1320-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1320-136">INPUTS</span></span>

### <span data-ttu-id="c1320-137">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="c1320-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="c1320-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1320-138">OUTPUTS</span></span>

### <span data-ttu-id="c1320-139">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="c1320-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="c1320-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c1320-140">NOTES</span></span>

## <span data-ttu-id="c1320-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c1320-141">RELATED LINKS</span></span>
