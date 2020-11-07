---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobAgent.md
ms.openlocfilehash: 80835d33f75517bea6a91e65f110f441d20ab59c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839314"
---
# <span data-ttu-id="3a123-101">Get-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="3a123-101">Get-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="3a123-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3a123-102">SYNOPSIS</span></span>
<span data-ttu-id="3a123-103">Azure SQL elasztikus munkatárs beosztása</span><span class="sxs-lookup"><span data-stu-id="3a123-103">Gets a Azure SQL Elastic Job agent</span></span>

## <span data-ttu-id="3a123-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3a123-104">SYNTAX</span></span>

### <span data-ttu-id="3a123-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3a123-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a123-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="3a123-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobAgent [-ParentObject] <AzureSqlServerModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a123-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3a123-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobAgent [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a123-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3a123-108">DESCRIPTION</span></span>
<span data-ttu-id="3a123-109">Az Get-AzSqlElasticJobAgent parancsmag egy vagy több rugalmas munkatársat kap</span><span class="sxs-lookup"><span data-stu-id="3a123-109">The Get-AzSqlElasticJobAgent cmdlet gets one or more Elastic Job agents</span></span>

## <span data-ttu-id="3a123-110">Példák</span><span class="sxs-lookup"><span data-stu-id="3a123-110">EXAMPLES</span></span>

### <span data-ttu-id="3a123-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3a123-111">Example 1</span></span>
```
PS C:\> Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready
```

<span data-ttu-id="3a123-112">Rugalmas munkatárs kapja</span><span class="sxs-lookup"><span data-stu-id="3a123-112">Gets an Elastic Job agent</span></span>

## <span data-ttu-id="3a123-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3a123-113">PARAMETERS</span></span>

### <span data-ttu-id="3a123-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a123-114">-DefaultProfile</span></span>
<span data-ttu-id="3a123-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3a123-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a123-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3a123-116">-Name</span></span>
<span data-ttu-id="3a123-117">Az ügynök neve</span><span class="sxs-lookup"><span data-stu-id="3a123-117">The agent name</span></span>

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

### <span data-ttu-id="3a123-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="3a123-118">-ParentObject</span></span>
<span data-ttu-id="3a123-119">A kiszolgáló bemeneti objektuma</span><span class="sxs-lookup"><span data-stu-id="3a123-119">The server input object</span></span>

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

### <span data-ttu-id="3a123-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="3a123-120">-ParentResourceId</span></span>
<span data-ttu-id="3a123-121">A kiszolgálói erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="3a123-121">The server resource id</span></span>

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

### <span data-ttu-id="3a123-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a123-122">-ResourceGroupName</span></span>
<span data-ttu-id="3a123-123">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="3a123-123">The resource group name</span></span>

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

### <span data-ttu-id="3a123-124">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="3a123-124">-ServerName</span></span>
<span data-ttu-id="3a123-125">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="3a123-125">The server name</span></span>

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

### <span data-ttu-id="3a123-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a123-126">CommonParameters</span></span>
<span data-ttu-id="3a123-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3a123-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a123-128">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3a123-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a123-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a123-129">INPUTS</span></span>

### <span data-ttu-id="3a123-130">Microsoft. Azure. Command. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="3a123-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="3a123-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a123-131">OUTPUTS</span></span>

### <span data-ttu-id="3a123-132">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="3a123-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="3a123-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3a123-133">NOTES</span></span>

## <span data-ttu-id="3a123-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3a123-134">RELATED LINKS</span></span>
