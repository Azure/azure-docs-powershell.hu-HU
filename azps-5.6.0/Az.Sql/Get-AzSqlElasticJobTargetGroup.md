---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/get-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: 022ef6979ddac4fa31c0a1dae42ae04c044498dc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999621"
---
# <span data-ttu-id="fa844-101">Get-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="fa844-101">Get-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="fa844-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa844-102">SYNOPSIS</span></span>
<span data-ttu-id="fa844-103">Egy vagy több célcsoportot kap a feladathoz</span><span class="sxs-lookup"><span data-stu-id="fa844-103">Gets one or more job target groups</span></span>

## <span data-ttu-id="fa844-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fa844-104">SYNTAX</span></span>

### <span data-ttu-id="fa844-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fa844-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa844-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="fa844-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa844-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fa844-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa844-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fa844-108">DESCRIPTION</span></span>
<span data-ttu-id="fa844-109">A Get-AzSqlElasticJobTargetGroup parancsmag kap egy célcsoportot és a célcsoportot</span><span class="sxs-lookup"><span data-stu-id="fa844-109">The Get-AzSqlElasticJobTargetGroup cmdlet gets a target group and it's targets</span></span>

## <span data-ttu-id="fa844-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fa844-110">EXAMPLES</span></span>

### <span data-ttu-id="fa844-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="fa844-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1             (s1,db1)
```

<span data-ttu-id="fa844-112">Célcsoportot és célcsoportot kap</span><span class="sxs-lookup"><span data-stu-id="fa844-112">Gets a target group and it's targets</span></span>

## <span data-ttu-id="fa844-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa844-113">PARAMETERS</span></span>

### <span data-ttu-id="fa844-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="fa844-114">-AgentName</span></span>
<span data-ttu-id="fa844-115">Az ügynök neve</span><span class="sxs-lookup"><span data-stu-id="fa844-115">The agent name</span></span>

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

### <span data-ttu-id="fa844-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa844-116">-DefaultProfile</span></span>
<span data-ttu-id="fa844-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fa844-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa844-118">-Name</span><span class="sxs-lookup"><span data-stu-id="fa844-118">-Name</span></span>
<span data-ttu-id="fa844-119">A célcsoport neve</span><span class="sxs-lookup"><span data-stu-id="fa844-119">The target group name</span></span>

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

### <span data-ttu-id="fa844-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="fa844-120">-ParentObject</span></span>
<span data-ttu-id="fa844-121">Az ügynökobjektum</span><span class="sxs-lookup"><span data-stu-id="fa844-121">The agent object</span></span>

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

### <span data-ttu-id="fa844-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="fa844-122">-ParentResourceId</span></span>
<span data-ttu-id="fa844-123">Az ügynök erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="fa844-123">The agent resource id</span></span>

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

### <span data-ttu-id="fa844-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa844-124">-ResourceGroupName</span></span>
<span data-ttu-id="fa844-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="fa844-125">The resource group name</span></span>

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

### <span data-ttu-id="fa844-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fa844-126">-ServerName</span></span>
<span data-ttu-id="fa844-127">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="fa844-127">The server name</span></span>

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

### <span data-ttu-id="fa844-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa844-128">CommonParameters</span></span>
<span data-ttu-id="fa844-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa844-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa844-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fa844-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa844-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fa844-131">INPUTS</span></span>

### <span data-ttu-id="fa844-132">Microsoft.Azure.Commands.Sql.ElasticMods.Model.AzureSqlElasticAgentModel</span><span class="sxs-lookup"><span data-stu-id="fa844-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="fa844-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fa844-133">OUTPUTS</span></span>

### <span data-ttu-id="fa844-134">Microsoft.Azure.Commands.Sql.ElasticMods.Model.AzureSqlElasticAsticTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="fa844-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="fa844-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fa844-135">NOTES</span></span>

## <span data-ttu-id="fa844-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fa844-136">RELATED LINKS</span></span>
