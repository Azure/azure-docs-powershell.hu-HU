---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobAgent.md
ms.openlocfilehash: 7d2985d2e5361f7594dbccac2e67c7c550c9b0a5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185841"
---
# <span data-ttu-id="da9a4-101">Get-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="da9a4-101">Get-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="da9a4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="da9a4-102">SYNOPSIS</span></span>
<span data-ttu-id="da9a4-103">Azure SQL elasztikus munkatárs beosztása</span><span class="sxs-lookup"><span data-stu-id="da9a4-103">Gets a Azure SQL Elastic Job agent</span></span>

## <span data-ttu-id="da9a4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="da9a4-104">SYNTAX</span></span>

### <span data-ttu-id="da9a4-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="da9a4-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da9a4-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="da9a4-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobAgent [-ParentObject] <AzureSqlServerModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da9a4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="da9a4-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobAgent [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da9a4-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="da9a4-108">DESCRIPTION</span></span>
<span data-ttu-id="da9a4-109">Az Get-AzSqlElasticJobAgent parancsmag egy vagy több rugalmas munkatársat kap</span><span class="sxs-lookup"><span data-stu-id="da9a4-109">The Get-AzSqlElasticJobAgent cmdlet gets one or more Elastic Job agents</span></span>

## <span data-ttu-id="da9a4-110">Példák</span><span class="sxs-lookup"><span data-stu-id="da9a4-110">EXAMPLES</span></span>

### <span data-ttu-id="da9a4-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="da9a4-111">Example 1</span></span>
```
PS C:\> Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready
```

<span data-ttu-id="da9a4-112">Rugalmas munkatárs kapja</span><span class="sxs-lookup"><span data-stu-id="da9a4-112">Gets an Elastic Job agent</span></span>

## <span data-ttu-id="da9a4-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="da9a4-113">PARAMETERS</span></span>

### <span data-ttu-id="da9a4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da9a4-114">-DefaultProfile</span></span>
<span data-ttu-id="da9a4-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="da9a4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da9a4-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="da9a4-116">-Name</span></span>
<span data-ttu-id="da9a4-117">Az ügynök neve</span><span class="sxs-lookup"><span data-stu-id="da9a4-117">The agent name</span></span>

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

### <span data-ttu-id="da9a4-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="da9a4-118">-ParentObject</span></span>
<span data-ttu-id="da9a4-119">A kiszolgáló bemeneti objektuma</span><span class="sxs-lookup"><span data-stu-id="da9a4-119">The server input object</span></span>

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

### <span data-ttu-id="da9a4-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="da9a4-120">-ParentResourceId</span></span>
<span data-ttu-id="da9a4-121">A kiszolgálói erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="da9a4-121">The server resource id</span></span>

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

### <span data-ttu-id="da9a4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da9a4-122">-ResourceGroupName</span></span>
<span data-ttu-id="da9a4-123">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="da9a4-123">The resource group name</span></span>

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

### <span data-ttu-id="da9a4-124">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="da9a4-124">-ServerName</span></span>
<span data-ttu-id="da9a4-125">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="da9a4-125">The server name</span></span>

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

### <span data-ttu-id="da9a4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da9a4-126">CommonParameters</span></span>
<span data-ttu-id="da9a4-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="da9a4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da9a4-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="da9a4-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da9a4-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="da9a4-129">INPUTS</span></span>

### <span data-ttu-id="da9a4-130">Microsoft. Azure. Command. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="da9a4-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="da9a4-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="da9a4-131">OUTPUTS</span></span>

### <span data-ttu-id="da9a4-132">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="da9a4-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="da9a4-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="da9a4-133">NOTES</span></span>

## <span data-ttu-id="da9a4-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="da9a4-134">RELATED LINKS</span></span>
