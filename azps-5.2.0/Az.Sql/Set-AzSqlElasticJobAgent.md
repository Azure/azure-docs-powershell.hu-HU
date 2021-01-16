---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
ms.openlocfilehash: 58adbb3b160272007899dc8740e211b6e81a10a4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344009"
---
# <span data-ttu-id="61154-101">Set-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="61154-101">Set-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="61154-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61154-102">SYNOPSIS</span></span>
<span data-ttu-id="61154-103">Rugalmas ügynök frissítése</span><span class="sxs-lookup"><span data-stu-id="61154-103">Updates an elastic job agent</span></span>

## <span data-ttu-id="61154-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="61154-104">SYNTAX</span></span>

### <span data-ttu-id="61154-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="61154-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61154-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="61154-106">ObjectSet</span></span>
```
Set-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61154-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="61154-107">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61154-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="61154-108">DESCRIPTION</span></span>
<span data-ttu-id="61154-109">A Set-AzSqlElasticJobAgent parancsmag frissíti az Rugalmas feladat ügynököket</span><span class="sxs-lookup"><span data-stu-id="61154-109">The Set-AzSqlElasticJobAgent cmdlet updates an Elastic Job agents</span></span>

## <span data-ttu-id="61154-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="61154-110">EXAMPLES</span></span>

### <span data-ttu-id="61154-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="61154-111">Example 1</span></span>
```
PS C:\> Set-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent -Tag @{ Octopus = "Agent" }

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="61154-112">Rugalmas feladat ügynökének frissítése</span><span class="sxs-lookup"><span data-stu-id="61154-112">Updates an Elastic Job agent</span></span>

## <span data-ttu-id="61154-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61154-113">PARAMETERS</span></span>

### <span data-ttu-id="61154-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61154-114">-DefaultProfile</span></span>
<span data-ttu-id="61154-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="61154-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61154-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="61154-116">-InputObject</span></span>
<span data-ttu-id="61154-117">Az ügynök beviteli objektuma</span><span class="sxs-lookup"><span data-stu-id="61154-117">The agent input object</span></span>

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

### <span data-ttu-id="61154-118">-Name</span><span class="sxs-lookup"><span data-stu-id="61154-118">-Name</span></span>
<span data-ttu-id="61154-119">Az ügynök neve</span><span class="sxs-lookup"><span data-stu-id="61154-119">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: AgentName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61154-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61154-120">-ResourceGroupName</span></span>
<span data-ttu-id="61154-121">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="61154-121">The resource group name</span></span>

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

### <span data-ttu-id="61154-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="61154-122">-ResourceId</span></span>
<span data-ttu-id="61154-123">Az ügynök erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="61154-123">The agent resource id</span></span>

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

### <span data-ttu-id="61154-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="61154-124">-ServerName</span></span>
<span data-ttu-id="61154-125">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="61154-125">The server name</span></span>

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

### <span data-ttu-id="61154-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="61154-126">-Tag</span></span>
<span data-ttu-id="61154-127">Az Azure SQL-adatbázis ügynökkel társítva</span><span class="sxs-lookup"><span data-stu-id="61154-127">The tags to associate with the Azure SQL Database Agent</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61154-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="61154-128">-Confirm</span></span>
<span data-ttu-id="61154-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="61154-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61154-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61154-130">-WhatIf</span></span>
<span data-ttu-id="61154-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="61154-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61154-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="61154-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61154-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61154-133">CommonParameters</span></span>
<span data-ttu-id="61154-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61154-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61154-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="61154-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61154-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="61154-136">INPUTS</span></span>

### <span data-ttu-id="61154-137">Microsoft.Azure.Commands.Sql.ElasticMods.Model.AzureSqlElasticAgentModel</span><span class="sxs-lookup"><span data-stu-id="61154-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="61154-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="61154-138">OUTPUTS</span></span>

### <span data-ttu-id="61154-139">Microsoft.Azure.Commands.Sql.ElasticMods.Model.AzureSqlElasticAgentModel</span><span class="sxs-lookup"><span data-stu-id="61154-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="61154-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="61154-140">NOTES</span></span>

## <span data-ttu-id="61154-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="61154-141">RELATED LINKS</span></span>
