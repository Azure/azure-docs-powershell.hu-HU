---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobCredential.md
ms.openlocfilehash: 1cd466581a89e49280d2a6cacdd74d4d37ac208d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847442"
---
# <span data-ttu-id="37f55-101">Get-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="37f55-101">Get-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="37f55-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="37f55-102">SYNOPSIS</span></span>
<span data-ttu-id="37f55-103">Egy vagy több hitelesítő adatok beolvasása</span><span class="sxs-lookup"><span data-stu-id="37f55-103">Gets one or more credentials</span></span>

## <span data-ttu-id="37f55-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="37f55-104">SYNTAX</span></span>

### <span data-ttu-id="37f55-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="37f55-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="37f55-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="37f55-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobCredential [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="37f55-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="37f55-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobCredential [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37f55-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="37f55-108">DESCRIPTION</span></span>
<span data-ttu-id="37f55-109">A Get-AzSqlElasticJobCredential parancsmag egy vagy több munkahelyi hitelesítő adatokat kap</span><span class="sxs-lookup"><span data-stu-id="37f55-109">The Get-AzSqlElasticJobCredential cmdlet gets one or more job credentials</span></span>

## <span data-ttu-id="37f55-110">Példák</span><span class="sxs-lookup"><span data-stu-id="37f55-110">EXAMPLES</span></span>

### <span data-ttu-id="37f55-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="37f55-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobCredential -Name cred1

CredentialName UserName
-------------- --------
cred1          user1
```

<span data-ttu-id="37f55-112">Munkahelyi hitelesítő adatok beolvasása</span><span class="sxs-lookup"><span data-stu-id="37f55-112">Gets a job credential</span></span>

## <span data-ttu-id="37f55-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="37f55-113">PARAMETERS</span></span>

### <span data-ttu-id="37f55-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="37f55-114">-AgentName</span></span>
<span data-ttu-id="37f55-115">Az ügynök neve</span><span class="sxs-lookup"><span data-stu-id="37f55-115">The agent name</span></span>

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

### <span data-ttu-id="37f55-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37f55-116">-DefaultProfile</span></span>
<span data-ttu-id="37f55-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="37f55-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37f55-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="37f55-118">-Name</span></span>
<span data-ttu-id="37f55-119">A munkahelyi hitelesítő adatok neve</span><span class="sxs-lookup"><span data-stu-id="37f55-119">The job credential name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CredentialName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37f55-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="37f55-120">-ParentObject</span></span>
<span data-ttu-id="37f55-121">Az Agent objektum</span><span class="sxs-lookup"><span data-stu-id="37f55-121">The agent object</span></span>

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

### <span data-ttu-id="37f55-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="37f55-122">-ParentResourceId</span></span>
<span data-ttu-id="37f55-123">Az ügynök erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="37f55-123">The agent resource id</span></span>

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

### <span data-ttu-id="37f55-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37f55-124">-ResourceGroupName</span></span>
<span data-ttu-id="37f55-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="37f55-125">The resource group name</span></span>

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

### <span data-ttu-id="37f55-126">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="37f55-126">-ServerName</span></span>
<span data-ttu-id="37f55-127">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="37f55-127">The server name</span></span>

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

### <span data-ttu-id="37f55-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37f55-128">CommonParameters</span></span>
<span data-ttu-id="37f55-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="37f55-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37f55-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="37f55-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37f55-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="37f55-131">INPUTS</span></span>

### <span data-ttu-id="37f55-132">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="37f55-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="37f55-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="37f55-133">OUTPUTS</span></span>

### <span data-ttu-id="37f55-134">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="37f55-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="37f55-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="37f55-135">NOTES</span></span>

## <span data-ttu-id="37f55-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="37f55-136">RELATED LINKS</span></span>
