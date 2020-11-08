---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: a20de2c2431e1ab6aea5da4d6dd61e6c745a3c56
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012463"
---
# <span data-ttu-id="b8d9b-101">Remove-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="b8d9b-101">Remove-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="b8d9b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b8d9b-102">SYNOPSIS</span></span>
<span data-ttu-id="b8d9b-103">A cél csoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="b8d9b-103">Removes the target group</span></span>

## <span data-ttu-id="b8d9b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b8d9b-104">SYNTAX</span></span>

### <span data-ttu-id="b8d9b-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b8d9b-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8d9b-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="b8d9b-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobTargetGroup [-InputObject] <AzureSqlElasticJobTargetGroupModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8d9b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b8d9b-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobTargetGroup [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8d9b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b8d9b-108">DESCRIPTION</span></span>
<span data-ttu-id="b8d9b-109">A Remove-AzSqlElasticJobTargetGroup parancsmag eltávolítja a célcsoportot és a cél</span><span class="sxs-lookup"><span data-stu-id="b8d9b-109">The Remove-AzSqlElasticJobTargetGroup cmdlet removes a target group and it's targets</span></span>

## <span data-ttu-id="b8d9b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b8d9b-110">EXAMPLES</span></span>

### <span data-ttu-id="b8d9b-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b8d9b-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent 
$agent | Remove-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1             (s1,db1)
```

<span data-ttu-id="b8d9b-112">A célcsoport és a cél eltávolítása</span><span class="sxs-lookup"><span data-stu-id="b8d9b-112">Removes a target group and it's targets</span></span>

## <span data-ttu-id="b8d9b-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b8d9b-113">PARAMETERS</span></span>

### <span data-ttu-id="b8d9b-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="b8d9b-114">-AgentName</span></span>
<span data-ttu-id="b8d9b-115">Az ügynök neve</span><span class="sxs-lookup"><span data-stu-id="b8d9b-115">The agent name</span></span>

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

### <span data-ttu-id="b8d9b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8d9b-116">-DefaultProfile</span></span>
<span data-ttu-id="b8d9b-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8d9b-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b8d9b-118">-Force</span></span>
<span data-ttu-id="b8d9b-119">A művelet végrehajtásához szükséges megerősítési üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="b8d9b-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="b8d9b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8d9b-120">-InputObject</span></span>
<span data-ttu-id="b8d9b-121">A cél csoport objektum</span><span class="sxs-lookup"><span data-stu-id="b8d9b-121">The target group object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8d9b-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b8d9b-122">-Name</span></span>
<span data-ttu-id="b8d9b-123">A cél csoport neve</span><span class="sxs-lookup"><span data-stu-id="b8d9b-123">The target group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: TargetGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8d9b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8d9b-124">-ResourceGroupName</span></span>
<span data-ttu-id="b8d9b-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="b8d9b-125">The resource group name</span></span>

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

### <span data-ttu-id="b8d9b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8d9b-126">-ResourceId</span></span>
<span data-ttu-id="b8d9b-127">A cél csoport erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="b8d9b-127">The target group resource id</span></span>

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

### <span data-ttu-id="b8d9b-128">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="b8d9b-128">-ServerName</span></span>
<span data-ttu-id="b8d9b-129">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="b8d9b-129">The server name</span></span>

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

### <span data-ttu-id="b8d9b-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b8d9b-130">-Confirm</span></span>
<span data-ttu-id="b8d9b-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8d9b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8d9b-132">-WhatIf</span></span>
<span data-ttu-id="b8d9b-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8d9b-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8d9b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8d9b-135">CommonParameters</span></span>
<span data-ttu-id="b8d9b-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b8d9b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8d9b-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b8d9b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8d9b-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8d9b-138">INPUTS</span></span>

### <span data-ttu-id="b8d9b-139">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="b8d9b-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="b8d9b-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8d9b-140">OUTPUTS</span></span>

### <span data-ttu-id="b8d9b-141">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="b8d9b-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="b8d9b-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b8d9b-142">NOTES</span></span>

## <span data-ttu-id="b8d9b-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b8d9b-143">RELATED LINKS</span></span>
