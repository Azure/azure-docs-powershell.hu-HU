---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: f68baa997fd808a6e31bbb499f621f7ce303a25a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98465931"
---
# <span data-ttu-id="a7ccd-101">Get-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="a7ccd-101">Get-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="a7ccd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7ccd-102">SYNOPSIS</span></span>
<span data-ttu-id="a7ccd-103">Egy vagy több célcsoportot kap a feladathoz</span><span class="sxs-lookup"><span data-stu-id="a7ccd-103">Gets one or more job target groups</span></span>

## <span data-ttu-id="a7ccd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a7ccd-104">SYNTAX</span></span>

### <span data-ttu-id="a7ccd-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a7ccd-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7ccd-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="a7ccd-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7ccd-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a7ccd-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7ccd-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a7ccd-108">DESCRIPTION</span></span>
<span data-ttu-id="a7ccd-109">A Get-AzSqlElasticJobTargetGroup parancsmag kap egy célcsoportot és a célcsoportot</span><span class="sxs-lookup"><span data-stu-id="a7ccd-109">The Get-AzSqlElasticJobTargetGroup cmdlet gets a target group and it's targets</span></span>

## <span data-ttu-id="a7ccd-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a7ccd-110">EXAMPLES</span></span>

### <span data-ttu-id="a7ccd-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="a7ccd-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1             (s1,db1)
```

<span data-ttu-id="a7ccd-112">Célcsoportot és célcsoportot kap</span><span class="sxs-lookup"><span data-stu-id="a7ccd-112">Gets a target group and it's targets</span></span>

## <span data-ttu-id="a7ccd-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7ccd-113">PARAMETERS</span></span>

### <span data-ttu-id="a7ccd-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="a7ccd-114">-AgentName</span></span>
<span data-ttu-id="a7ccd-115">Az ügynök neve</span><span class="sxs-lookup"><span data-stu-id="a7ccd-115">The agent name</span></span>

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

### <span data-ttu-id="a7ccd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7ccd-116">-DefaultProfile</span></span>
<span data-ttu-id="a7ccd-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a7ccd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7ccd-118">-Name</span><span class="sxs-lookup"><span data-stu-id="a7ccd-118">-Name</span></span>
<span data-ttu-id="a7ccd-119">A célcsoport neve</span><span class="sxs-lookup"><span data-stu-id="a7ccd-119">The target group name</span></span>

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

### <span data-ttu-id="a7ccd-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a7ccd-120">-ParentObject</span></span>
<span data-ttu-id="a7ccd-121">Az ügynökobjektum</span><span class="sxs-lookup"><span data-stu-id="a7ccd-121">The agent object</span></span>

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

### <span data-ttu-id="a7ccd-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="a7ccd-122">-ParentResourceId</span></span>
<span data-ttu-id="a7ccd-123">Az ügynök erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="a7ccd-123">The agent resource id</span></span>

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

### <span data-ttu-id="a7ccd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7ccd-124">-ResourceGroupName</span></span>
<span data-ttu-id="a7ccd-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="a7ccd-125">The resource group name</span></span>

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

### <span data-ttu-id="a7ccd-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a7ccd-126">-ServerName</span></span>
<span data-ttu-id="a7ccd-127">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="a7ccd-127">The server name</span></span>

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

### <span data-ttu-id="a7ccd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7ccd-128">CommonParameters</span></span>
<span data-ttu-id="a7ccd-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7ccd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7ccd-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a7ccd-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7ccd-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a7ccd-131">INPUTS</span></span>

### <span data-ttu-id="a7ccd-132">Microsoft.Azure.Commands.Sql.ElasticMods.Model.AzureSqlElasticAgentModel</span><span class="sxs-lookup"><span data-stu-id="a7ccd-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="a7ccd-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a7ccd-133">OUTPUTS</span></span>

### <span data-ttu-id="a7ccd-134">Microsoft.Azure.Commands.Sql.ElasticMods.Model.AzureSqlElasticAsticTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="a7ccd-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="a7ccd-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a7ccd-135">NOTES</span></span>

## <span data-ttu-id="a7ccd-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a7ccd-136">RELATED LINKS</span></span>
