---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStep.md
ms.openlocfilehash: 3a749f02854a915792a12271b2cf59b1091fef70
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165803"
---
# <span data-ttu-id="5b946-101">Get-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="5b946-101">Get-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="5b946-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b946-102">SYNOPSIS</span></span>
<span data-ttu-id="5b946-103">Egy vagy több feladat lépéseit kapja meg</span><span class="sxs-lookup"><span data-stu-id="5b946-103">Gets one or more job steps</span></span>

## <span data-ttu-id="5b946-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5b946-104">SYNTAX</span></span>

### <span data-ttu-id="5b946-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5b946-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b946-106">GetVersion</span><span class="sxs-lookup"><span data-stu-id="5b946-106">GetVersion</span></span>
```
Get-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> -Version <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5b946-107">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="5b946-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b946-108">GetVersionUsingObject</span><span class="sxs-lookup"><span data-stu-id="5b946-108">GetVersionUsingJobObject</span></span>
```
Get-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -Name <String> -Version <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b946-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5b946-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobStep [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b946-110">GetVersionUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="5b946-110">GetVersionUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobStep [-ParentResourceId] <String> -Name <String> -Version <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b946-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5b946-111">DESCRIPTION</span></span>
<span data-ttu-id="5b946-112">A Get-AzSqlElasticJobStep parancsmag egy vagy több feladat lépéseit kapja meg egy feladatból</span><span class="sxs-lookup"><span data-stu-id="5b946-112">The Get-AzSqlElasticJobStep cmdlet gets one or more job steps from a job</span></span>

## <span data-ttu-id="5b946-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5b946-113">EXAMPLES</span></span>

### <span data-ttu-id="5b946-114">1. példa: Álláslépést kap egy állásból</span><span class="sxs-lookup"><span data-stu-id="5b946-114">Example 1: Gets a job step from a job</span></span>
```powershell
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Get-AzSqlElasticJobStep -Name step1

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg1             cred1                 (43200,10,1,120,2) SELECT 1
```

<span data-ttu-id="5b946-115">Álláslépést kap egy állásból</span><span class="sxs-lookup"><span data-stu-id="5b946-115">Gets a job step from a job</span></span>

## <span data-ttu-id="5b946-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b946-116">PARAMETERS</span></span>

### <span data-ttu-id="5b946-117">-AgentName</span><span class="sxs-lookup"><span data-stu-id="5b946-117">-AgentName</span></span>
<span data-ttu-id="5b946-118">Az ügynök neve</span><span class="sxs-lookup"><span data-stu-id="5b946-118">The agent name</span></span>

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

### <span data-ttu-id="5b946-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b946-119">-DefaultProfile</span></span>
<span data-ttu-id="5b946-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5b946-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b946-121">-JobName</span><span class="sxs-lookup"><span data-stu-id="5b946-121">-JobName</span></span>
<span data-ttu-id="5b946-122">A feladat neve</span><span class="sxs-lookup"><span data-stu-id="5b946-122">The job name</span></span>

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

### <span data-ttu-id="5b946-123">-Name</span><span class="sxs-lookup"><span data-stu-id="5b946-123">-Name</span></span>
<span data-ttu-id="5b946-124">A feladat lépésének neve</span><span class="sxs-lookup"><span data-stu-id="5b946-124">The job step name</span></span>

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

### <span data-ttu-id="5b946-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5b946-125">-ParentObject</span></span>
<span data-ttu-id="5b946-126">A feladat beviteli objektuma</span><span class="sxs-lookup"><span data-stu-id="5b946-126">The job input object</span></span>

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

### <span data-ttu-id="5b946-127">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="5b946-127">-ParentResourceId</span></span>
<span data-ttu-id="5b946-128">A feladaterőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="5b946-128">The job resource id</span></span>

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

### <span data-ttu-id="5b946-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b946-129">-ResourceGroupName</span></span>
<span data-ttu-id="5b946-130">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="5b946-130">The resource group name</span></span>

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

### <span data-ttu-id="5b946-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5b946-131">-ServerName</span></span>
<span data-ttu-id="5b946-132">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="5b946-132">The server name</span></span>

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

### <span data-ttu-id="5b946-133">-Verzió</span><span class="sxs-lookup"><span data-stu-id="5b946-133">-Version</span></span>
<span data-ttu-id="5b946-134">A feladat lépésének neve</span><span class="sxs-lookup"><span data-stu-id="5b946-134">The job step name</span></span>

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

### <span data-ttu-id="5b946-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b946-135">CommonParameters</span></span>
<span data-ttu-id="5b946-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b946-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b946-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5b946-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b946-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5b946-138">INPUTS</span></span>

### <span data-ttu-id="5b946-139">Microsoft.Azure.Commands.Sql.Rugasz.Model.AzureSqlElasticModel</span><span class="sxs-lookup"><span data-stu-id="5b946-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="5b946-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b946-140">OUTPUTS</span></span>

### <span data-ttu-id="5b946-141">Microsoft.Azure.Commands.Sql.ElasticMods.Model.AzureSqlElasticModel</span><span class="sxs-lookup"><span data-stu-id="5b946-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="5b946-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5b946-142">NOTES</span></span>

## <span data-ttu-id="5b946-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5b946-143">RELATED LINKS</span></span>
