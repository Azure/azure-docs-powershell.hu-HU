---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStep.md
ms.openlocfilehash: 16899acb35270e01b80e267aab6fe6ab03827c02
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839205"
---
# <span data-ttu-id="a1d3e-101">Get-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="a1d3e-101">Get-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="a1d3e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a1d3e-102">SYNOPSIS</span></span>
<span data-ttu-id="a1d3e-103">Egy vagy több feladat lépéseit kapja</span><span class="sxs-lookup"><span data-stu-id="a1d3e-103">Gets one or more job steps</span></span>

## <span data-ttu-id="a1d3e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a1d3e-104">SYNTAX</span></span>

### <span data-ttu-id="a1d3e-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a1d3e-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1d3e-106">GetVersion</span><span class="sxs-lookup"><span data-stu-id="a1d3e-106">GetVersion</span></span>
```
Get-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> -Version <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a1d3e-107">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="a1d3e-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1d3e-108">GetVersionUsingJobObject</span><span class="sxs-lookup"><span data-stu-id="a1d3e-108">GetVersionUsingJobObject</span></span>
```
Get-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -Name <String> -Version <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1d3e-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a1d3e-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobStep [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1d3e-110">GetVersionUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="a1d3e-110">GetVersionUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobStep [-ParentResourceId] <String> -Name <String> -Version <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1d3e-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="a1d3e-111">DESCRIPTION</span></span>
<span data-ttu-id="a1d3e-112">A Get-AzSqlElasticJobStep parancsmag egy vagy több feladatot kap egy munkából.</span><span class="sxs-lookup"><span data-stu-id="a1d3e-112">The Get-AzSqlElasticJobStep cmdlet gets one or more job steps from a job</span></span>

## <span data-ttu-id="a1d3e-113">Példák</span><span class="sxs-lookup"><span data-stu-id="a1d3e-113">EXAMPLES</span></span>

### <span data-ttu-id="a1d3e-114">Példa 1 – Job-lépés beolvasása egy projektből</span><span class="sxs-lookup"><span data-stu-id="a1d3e-114">Example 1 - Gets a job step from a job</span></span>
```
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Get-AzSqlElasticJobStep -Name step1

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg1             cred1                 (43200,10,1,120,2) SELECT 1
```

<span data-ttu-id="a1d3e-115">Munkahelyi lépés beolvasása egy munkából</span><span class="sxs-lookup"><span data-stu-id="a1d3e-115">Gets a job step from a job</span></span>

## <span data-ttu-id="a1d3e-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a1d3e-116">PARAMETERS</span></span>

### <span data-ttu-id="a1d3e-117">-AgentName</span><span class="sxs-lookup"><span data-stu-id="a1d3e-117">-AgentName</span></span>
<span data-ttu-id="a1d3e-118">Az ügynök neve</span><span class="sxs-lookup"><span data-stu-id="a1d3e-118">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, GetVersion
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1d3e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1d3e-119">-DefaultProfile</span></span>
<span data-ttu-id="a1d3e-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a1d3e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1d3e-121">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="a1d3e-121">-JobName</span></span>
<span data-ttu-id="a1d3e-122">A feladat neve</span><span class="sxs-lookup"><span data-stu-id="a1d3e-122">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, GetVersion
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1d3e-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a1d3e-123">-Name</span></span>
<span data-ttu-id="a1d3e-124">A feladat lépéseinek neve</span><span class="sxs-lookup"><span data-stu-id="a1d3e-124">The job step name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases: StepName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetVersion, GetVersionUsingJobObject, GetVersionUsingParentResourceId
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1d3e-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a1d3e-125">-ParentObject</span></span>
<span data-ttu-id="a1d3e-126">A projekt bemeneti objektuma</span><span class="sxs-lookup"><span data-stu-id="a1d3e-126">The job input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel
Parameter Sets: ObjectSet, GetVersionUsingJobObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1d3e-127">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="a1d3e-127">-ParentResourceId</span></span>
<span data-ttu-id="a1d3e-128">A projekt erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="a1d3e-128">The job resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, GetVersionUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1d3e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1d3e-129">-ResourceGroupName</span></span>
<span data-ttu-id="a1d3e-130">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="a1d3e-130">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, GetVersion
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1d3e-131">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="a1d3e-131">-ServerName</span></span>
<span data-ttu-id="a1d3e-132">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="a1d3e-132">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, GetVersion
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1d3e-133">-Verzió</span><span class="sxs-lookup"><span data-stu-id="a1d3e-133">-Version</span></span>
<span data-ttu-id="a1d3e-134">A feladat lépéseinek neve</span><span class="sxs-lookup"><span data-stu-id="a1d3e-134">The job step name</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetVersionUsingJobObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetVersionUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1d3e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1d3e-135">CommonParameters</span></span>
<span data-ttu-id="a1d3e-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a1d3e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1d3e-137">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a1d3e-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1d3e-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1d3e-138">INPUTS</span></span>

### <span data-ttu-id="a1d3e-139">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="a1d3e-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="a1d3e-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1d3e-140">OUTPUTS</span></span>

### <span data-ttu-id="a1d3e-141">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="a1d3e-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="a1d3e-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a1d3e-142">NOTES</span></span>

## <span data-ttu-id="a1d3e-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a1d3e-143">RELATED LINKS</span></span>
