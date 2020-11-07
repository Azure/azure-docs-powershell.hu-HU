---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJob.md
ms.openlocfilehash: b758c3a76c27fb2a1f06c7b6c940d3c3a7ef1c11
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839122"
---
# <span data-ttu-id="dc245-101">Remove-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="dc245-101">Remove-AzSqlElasticJob</span></span>

## <span data-ttu-id="dc245-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dc245-102">SYNOPSIS</span></span>
<span data-ttu-id="dc245-103">Feladat eltávolítása</span><span class="sxs-lookup"><span data-stu-id="dc245-103">Removes a job</span></span>

## <span data-ttu-id="dc245-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dc245-104">SYNTAX</span></span>

### <span data-ttu-id="dc245-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dc245-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc245-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="dc245-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc245-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="dc245-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJob [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc245-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="dc245-108">DESCRIPTION</span></span>
<span data-ttu-id="dc245-109">A Remove-AzSqlElasticJob parancsmag eltávolítja a feladatot</span><span class="sxs-lookup"><span data-stu-id="dc245-109">The Remove-AzSqlElasticJob cmdlet removes a job</span></span>

## <span data-ttu-id="dc245-110">Példák</span><span class="sxs-lookup"><span data-stu-id="dc245-110">EXAMPLES</span></span>

### <span data-ttu-id="dc245-111">Példa 1 – feladat eltávolítása</span><span class="sxs-lookup"><span data-stu-id="dc245-111">Example 1 - Removes a job</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Remove-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="dc245-112">Feladat eltávolítása</span><span class="sxs-lookup"><span data-stu-id="dc245-112">Removes a job</span></span>

## <span data-ttu-id="dc245-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dc245-113">PARAMETERS</span></span>

### <span data-ttu-id="dc245-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="dc245-114">-AgentName</span></span>
<span data-ttu-id="dc245-115">Az ügynök neve</span><span class="sxs-lookup"><span data-stu-id="dc245-115">The agent name</span></span>

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

### <span data-ttu-id="dc245-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc245-116">-DefaultProfile</span></span>
<span data-ttu-id="dc245-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dc245-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc245-118">-Force</span><span class="sxs-lookup"><span data-stu-id="dc245-118">-Force</span></span>
<span data-ttu-id="dc245-119">A művelet végrehajtásához szükséges megerősítési üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="dc245-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="dc245-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc245-120">-InputObject</span></span>
<span data-ttu-id="dc245-121">A projekt bemeneti objektuma</span><span class="sxs-lookup"><span data-stu-id="dc245-121">The job input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc245-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dc245-122">-Name</span></span>
<span data-ttu-id="dc245-123">A feladat neve</span><span class="sxs-lookup"><span data-stu-id="dc245-123">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: JobName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc245-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc245-124">-ResourceGroupName</span></span>
<span data-ttu-id="dc245-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="dc245-125">The resource group name</span></span>

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

### <span data-ttu-id="dc245-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc245-126">-ResourceId</span></span>
<span data-ttu-id="dc245-127">Az ügynök erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="dc245-127">The agent resource id</span></span>

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

### <span data-ttu-id="dc245-128">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="dc245-128">-ServerName</span></span>
<span data-ttu-id="dc245-129">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="dc245-129">The server name</span></span>

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

### <span data-ttu-id="dc245-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dc245-130">-Confirm</span></span>
<span data-ttu-id="dc245-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dc245-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc245-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc245-132">-WhatIf</span></span>
<span data-ttu-id="dc245-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dc245-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc245-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dc245-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc245-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc245-135">CommonParameters</span></span>
<span data-ttu-id="dc245-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dc245-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc245-137">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="dc245-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc245-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dc245-138">INPUTS</span></span>

### <span data-ttu-id="dc245-139">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="dc245-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="dc245-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dc245-140">OUTPUTS</span></span>

### <span data-ttu-id="dc245-141">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="dc245-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="dc245-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dc245-142">NOTES</span></span>

## <span data-ttu-id="dc245-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dc245-143">RELATED LINKS</span></span>
