---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJob.md
ms.openlocfilehash: c24793273e4da59b487702fb4d147bb6a7fb3ecb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185842"
---
# <span data-ttu-id="31b23-101">Get-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="31b23-101">Get-AzSqlElasticJob</span></span>

## <span data-ttu-id="31b23-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="31b23-102">SYNOPSIS</span></span>
<span data-ttu-id="31b23-103">Egy vagy több feladat beolvasása</span><span class="sxs-lookup"><span data-stu-id="31b23-103">Gets one or more jobs</span></span>

## <span data-ttu-id="31b23-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="31b23-104">SYNTAX</span></span>

### <span data-ttu-id="31b23-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="31b23-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31b23-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="31b23-106">ObjectSet</span></span>
```
Get-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31b23-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="31b23-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJob [-ParentResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="31b23-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="31b23-108">DESCRIPTION</span></span>
<span data-ttu-id="31b23-109">A Get-AzSqlElasticJob parancsmag egy vagy több feladatot kap</span><span class="sxs-lookup"><span data-stu-id="31b23-109">The Get-AzSqlElasticJob cmdlet gets one or more jobs</span></span>

## <span data-ttu-id="31b23-110">Példák</span><span class="sxs-lookup"><span data-stu-id="31b23-110">EXAMPLES</span></span>

### <span data-ttu-id="31b23-111">Példa 1: munkát kap</span><span class="sxs-lookup"><span data-stu-id="31b23-111">Example 1: Gets a job</span></span>
```powershell
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="31b23-112">Munkát kap</span><span class="sxs-lookup"><span data-stu-id="31b23-112">Gets a job</span></span>

### <span data-ttu-id="31b23-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="31b23-113">Example 2</span></span>

<span data-ttu-id="31b23-114">Egy vagy több feladatot kap.</span><span class="sxs-lookup"><span data-stu-id="31b23-114">Gets one or more jobs.</span></span> <span data-ttu-id="31b23-115">autogenerated</span><span class="sxs-lookup"><span data-stu-id="31b23-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Get-AzSqlElasticJob -AgentName agent -Name job1 -ResourceGroupName rg -ServerName elasticjobserver
```

## <span data-ttu-id="31b23-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="31b23-116">PARAMETERS</span></span>

### <span data-ttu-id="31b23-117">-AgentName</span><span class="sxs-lookup"><span data-stu-id="31b23-117">-AgentName</span></span>
<span data-ttu-id="31b23-118">Az ügynök neve</span><span class="sxs-lookup"><span data-stu-id="31b23-118">The agent name</span></span>

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

### <span data-ttu-id="31b23-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31b23-119">-DefaultProfile</span></span>
<span data-ttu-id="31b23-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="31b23-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31b23-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="31b23-121">-Name</span></span>
<span data-ttu-id="31b23-122">A feladat neve</span><span class="sxs-lookup"><span data-stu-id="31b23-122">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: JobName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b23-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="31b23-123">-ParentObject</span></span>
<span data-ttu-id="31b23-124">Ügynök beviteli objektuma</span><span class="sxs-lookup"><span data-stu-id="31b23-124">The agent input object</span></span>

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

### <span data-ttu-id="31b23-125">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="31b23-125">-ParentResourceId</span></span>
<span data-ttu-id="31b23-126">Az ügynök erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="31b23-126">The agent resource id</span></span>

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

### <span data-ttu-id="31b23-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31b23-127">-ResourceGroupName</span></span>
<span data-ttu-id="31b23-128">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="31b23-128">The resource group name</span></span>

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

### <span data-ttu-id="31b23-129">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="31b23-129">-ServerName</span></span>
<span data-ttu-id="31b23-130">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="31b23-130">The server name</span></span>

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

### <span data-ttu-id="31b23-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31b23-131">CommonParameters</span></span>
<span data-ttu-id="31b23-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="31b23-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31b23-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="31b23-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31b23-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="31b23-134">INPUTS</span></span>

### <span data-ttu-id="31b23-135">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="31b23-135">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="31b23-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="31b23-136">OUTPUTS</span></span>

### <span data-ttu-id="31b23-137">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="31b23-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="31b23-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="31b23-138">NOTES</span></span>

## <span data-ttu-id="31b23-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="31b23-139">RELATED LINKS</span></span>