---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: f68baa997fd808a6e31bbb499f621f7ce303a25a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296681"
---
# <span data-ttu-id="f95c5-101">Get-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="f95c5-101">Get-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="f95c5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f95c5-102">SYNOPSIS</span></span>
<span data-ttu-id="f95c5-103">Egy vagy több projektfeladat-csoport kapja meg</span><span class="sxs-lookup"><span data-stu-id="f95c5-103">Gets one or more job target groups</span></span>

## <span data-ttu-id="f95c5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f95c5-104">SYNTAX</span></span>

### <span data-ttu-id="f95c5-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f95c5-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f95c5-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="f95c5-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f95c5-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f95c5-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f95c5-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f95c5-108">DESCRIPTION</span></span>
<span data-ttu-id="f95c5-109">A Get-AzSqlElasticJobTargetGroup parancsmag a célcsoportot kapja, és célja</span><span class="sxs-lookup"><span data-stu-id="f95c5-109">The Get-AzSqlElasticJobTargetGroup cmdlet gets a target group and it's targets</span></span>

## <span data-ttu-id="f95c5-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f95c5-110">EXAMPLES</span></span>

### <span data-ttu-id="f95c5-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f95c5-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1             (s1,db1)
```

<span data-ttu-id="f95c5-112">Célcsoportot kap, és célja</span><span class="sxs-lookup"><span data-stu-id="f95c5-112">Gets a target group and it's targets</span></span>

## <span data-ttu-id="f95c5-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f95c5-113">PARAMETERS</span></span>

### <span data-ttu-id="f95c5-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="f95c5-114">-AgentName</span></span>
<span data-ttu-id="f95c5-115">Az ügynök neve</span><span class="sxs-lookup"><span data-stu-id="f95c5-115">The agent name</span></span>

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

### <span data-ttu-id="f95c5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f95c5-116">-DefaultProfile</span></span>
<span data-ttu-id="f95c5-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f95c5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f95c5-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f95c5-118">-Name</span></span>
<span data-ttu-id="f95c5-119">A cél csoport neve</span><span class="sxs-lookup"><span data-stu-id="f95c5-119">The target group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f95c5-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f95c5-120">-ParentObject</span></span>
<span data-ttu-id="f95c5-121">Az Agent objektum</span><span class="sxs-lookup"><span data-stu-id="f95c5-121">The agent object</span></span>

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

### <span data-ttu-id="f95c5-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f95c5-122">-ParentResourceId</span></span>
<span data-ttu-id="f95c5-123">Az ügynök erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="f95c5-123">The agent resource id</span></span>

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

### <span data-ttu-id="f95c5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f95c5-124">-ResourceGroupName</span></span>
<span data-ttu-id="f95c5-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="f95c5-125">The resource group name</span></span>

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

### <span data-ttu-id="f95c5-126">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="f95c5-126">-ServerName</span></span>
<span data-ttu-id="f95c5-127">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="f95c5-127">The server name</span></span>

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

### <span data-ttu-id="f95c5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f95c5-128">CommonParameters</span></span>
<span data-ttu-id="f95c5-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f95c5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f95c5-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f95c5-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f95c5-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f95c5-131">INPUTS</span></span>

### <span data-ttu-id="f95c5-132">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="f95c5-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="f95c5-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f95c5-133">OUTPUTS</span></span>

### <span data-ttu-id="f95c5-134">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="f95c5-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="f95c5-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f95c5-135">NOTES</span></span>

## <span data-ttu-id="f95c5-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f95c5-136">RELATED LINKS</span></span>
