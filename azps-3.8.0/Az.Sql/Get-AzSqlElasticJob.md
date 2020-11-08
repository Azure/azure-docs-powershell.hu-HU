---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJob.md
ms.openlocfilehash: 60dac0ad09f30f339da82d84cf6200a44fe11859
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011515"
---
# <span data-ttu-id="892f9-101">Get-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="892f9-101">Get-AzSqlElasticJob</span></span>

## <span data-ttu-id="892f9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="892f9-102">SYNOPSIS</span></span>
<span data-ttu-id="892f9-103">Egy vagy több feladat beolvasása</span><span class="sxs-lookup"><span data-stu-id="892f9-103">Gets one or more jobs</span></span>

## <span data-ttu-id="892f9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="892f9-104">SYNTAX</span></span>

### <span data-ttu-id="892f9-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="892f9-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="892f9-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="892f9-106">ObjectSet</span></span>
```
Get-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="892f9-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="892f9-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJob [-ParentResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="892f9-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="892f9-108">DESCRIPTION</span></span>
<span data-ttu-id="892f9-109">A Get-AzSqlElasticJob parancsmag egy vagy több feladatot kap</span><span class="sxs-lookup"><span data-stu-id="892f9-109">The Get-AzSqlElasticJob cmdlet gets one or more jobs</span></span>

## <span data-ttu-id="892f9-110">Példák</span><span class="sxs-lookup"><span data-stu-id="892f9-110">EXAMPLES</span></span>

### <span data-ttu-id="892f9-111">Példa 1 – munkát kap</span><span class="sxs-lookup"><span data-stu-id="892f9-111">Example 1 - Gets a job</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="892f9-112">Munkát kap</span><span class="sxs-lookup"><span data-stu-id="892f9-112">Gets a job</span></span>

## <span data-ttu-id="892f9-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="892f9-113">PARAMETERS</span></span>

### <span data-ttu-id="892f9-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="892f9-114">-AgentName</span></span>
<span data-ttu-id="892f9-115">Az ügynök neve</span><span class="sxs-lookup"><span data-stu-id="892f9-115">The agent name</span></span>

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

### <span data-ttu-id="892f9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="892f9-116">-DefaultProfile</span></span>
<span data-ttu-id="892f9-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="892f9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="892f9-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="892f9-118">-Name</span></span>
<span data-ttu-id="892f9-119">A feladat neve</span><span class="sxs-lookup"><span data-stu-id="892f9-119">The job name</span></span>

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

### <span data-ttu-id="892f9-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="892f9-120">-ParentObject</span></span>
<span data-ttu-id="892f9-121">Ügynök beviteli objektuma</span><span class="sxs-lookup"><span data-stu-id="892f9-121">The agent input object</span></span>

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

### <span data-ttu-id="892f9-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="892f9-122">-ParentResourceId</span></span>
<span data-ttu-id="892f9-123">Az ügynök erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="892f9-123">The agent resource id</span></span>

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

### <span data-ttu-id="892f9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="892f9-124">-ResourceGroupName</span></span>
<span data-ttu-id="892f9-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="892f9-125">The resource group name</span></span>

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

### <span data-ttu-id="892f9-126">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="892f9-126">-ServerName</span></span>
<span data-ttu-id="892f9-127">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="892f9-127">The server name</span></span>

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

### <span data-ttu-id="892f9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="892f9-128">CommonParameters</span></span>
<span data-ttu-id="892f9-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="892f9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="892f9-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="892f9-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="892f9-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="892f9-131">INPUTS</span></span>

### <span data-ttu-id="892f9-132">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="892f9-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="892f9-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="892f9-133">OUTPUTS</span></span>

### <span data-ttu-id="892f9-134">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="892f9-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="892f9-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="892f9-135">NOTES</span></span>

## <span data-ttu-id="892f9-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="892f9-136">RELATED LINKS</span></span>
