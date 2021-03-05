---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/get-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobAgent.md
ms.openlocfilehash: 6ff5bdb6a3de7b1704ee41de0b6ff0b0f736ec5e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014597"
---
# <span data-ttu-id="a26ad-101">Get-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="a26ad-101">Get-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="a26ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a26ad-102">SYNOPSIS</span></span>
<span data-ttu-id="a26ad-103">Azure SQL-rugalmassági feladat ügynökhöz jut</span><span class="sxs-lookup"><span data-stu-id="a26ad-103">Gets a Azure SQL Elastic Job agent</span></span>

## <span data-ttu-id="a26ad-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a26ad-104">SYNTAX</span></span>

### <span data-ttu-id="a26ad-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a26ad-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a26ad-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="a26ad-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobAgent [-ParentObject] <AzureSqlServerModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a26ad-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a26ad-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobAgent [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a26ad-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a26ad-108">DESCRIPTION</span></span>
<span data-ttu-id="a26ad-109">A Get-AzSqlElasticJobAgent parancsmag egy vagy több Rugalmas feladat ügynökkel</span><span class="sxs-lookup"><span data-stu-id="a26ad-109">The Get-AzSqlElasticJobAgent cmdlet gets one or more Elastic Job agents</span></span>

## <span data-ttu-id="a26ad-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a26ad-110">EXAMPLES</span></span>

### <span data-ttu-id="a26ad-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="a26ad-111">Example 1</span></span>
```
PS C:\> Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready
```

<span data-ttu-id="a26ad-112">Rugalmas feladat ügynökhöz jut</span><span class="sxs-lookup"><span data-stu-id="a26ad-112">Gets an Elastic Job agent</span></span>

## <span data-ttu-id="a26ad-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a26ad-113">PARAMETERS</span></span>

### <span data-ttu-id="a26ad-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a26ad-114">-DefaultProfile</span></span>
<span data-ttu-id="a26ad-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a26ad-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a26ad-116">-Name</span><span class="sxs-lookup"><span data-stu-id="a26ad-116">-Name</span></span>
<span data-ttu-id="a26ad-117">Az ügynök neve</span><span class="sxs-lookup"><span data-stu-id="a26ad-117">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AgentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a26ad-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a26ad-118">-ParentObject</span></span>
<span data-ttu-id="a26ad-119">A kiszolgáló bemeneti objektuma</span><span class="sxs-lookup"><span data-stu-id="a26ad-119">The server input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a26ad-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="a26ad-120">-ParentResourceId</span></span>
<span data-ttu-id="a26ad-121">A kiszolgálóerőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="a26ad-121">The server resource id</span></span>

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

### <span data-ttu-id="a26ad-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a26ad-122">-ResourceGroupName</span></span>
<span data-ttu-id="a26ad-123">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="a26ad-123">The resource group name</span></span>

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

### <span data-ttu-id="a26ad-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a26ad-124">-ServerName</span></span>
<span data-ttu-id="a26ad-125">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="a26ad-125">The server name</span></span>

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

### <span data-ttu-id="a26ad-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a26ad-126">CommonParameters</span></span>
<span data-ttu-id="a26ad-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a26ad-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a26ad-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a26ad-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a26ad-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a26ad-129">INPUTS</span></span>

### <span data-ttu-id="a26ad-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="a26ad-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="a26ad-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a26ad-131">OUTPUTS</span></span>

### <span data-ttu-id="a26ad-132">Microsoft.Azure.Commands.Sql.ElasticMods.Model.AzureSqlElasticAgentModel</span><span class="sxs-lookup"><span data-stu-id="a26ad-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="a26ad-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a26ad-133">NOTES</span></span>

## <span data-ttu-id="a26ad-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a26ad-134">RELATED LINKS</span></span>
