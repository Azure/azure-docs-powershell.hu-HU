---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobCredential.md
ms.openlocfilehash: 1cd466581a89e49280d2a6cacdd74d4d37ac208d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145691"
---
# <span data-ttu-id="03495-101">Get-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="03495-101">Get-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="03495-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03495-102">SYNOPSIS</span></span>
<span data-ttu-id="03495-103">Egy vagy több hitelesítő adatokat kap</span><span class="sxs-lookup"><span data-stu-id="03495-103">Gets one or more credentials</span></span>

## <span data-ttu-id="03495-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="03495-104">SYNTAX</span></span>

### <span data-ttu-id="03495-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="03495-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03495-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="03495-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobCredential [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03495-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="03495-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobCredential [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03495-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="03495-108">DESCRIPTION</span></span>
<span data-ttu-id="03495-109">A Get-AzSqlElasticJobCredential parancsmag egy vagy több hitelesítő adatokat kap</span><span class="sxs-lookup"><span data-stu-id="03495-109">The Get-AzSqlElasticJobCredential cmdlet gets one or more job credentials</span></span>

## <span data-ttu-id="03495-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="03495-110">EXAMPLES</span></span>

### <span data-ttu-id="03495-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="03495-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobCredential -Name cred1

CredentialName UserName
-------------- --------
cred1          user1
```

<span data-ttu-id="03495-112">Hitelesítő adatokat kap a feladathoz</span><span class="sxs-lookup"><span data-stu-id="03495-112">Gets a job credential</span></span>

## <span data-ttu-id="03495-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03495-113">PARAMETERS</span></span>

### <span data-ttu-id="03495-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="03495-114">-AgentName</span></span>
<span data-ttu-id="03495-115">Az ügynök neve</span><span class="sxs-lookup"><span data-stu-id="03495-115">The agent name</span></span>

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

### <span data-ttu-id="03495-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03495-116">-DefaultProfile</span></span>
<span data-ttu-id="03495-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="03495-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03495-118">-Name</span><span class="sxs-lookup"><span data-stu-id="03495-118">-Name</span></span>
<span data-ttu-id="03495-119">A feladat hitelesítő adatainak neve</span><span class="sxs-lookup"><span data-stu-id="03495-119">The job credential name</span></span>

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

### <span data-ttu-id="03495-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="03495-120">-ParentObject</span></span>
<span data-ttu-id="03495-121">Az ügynökobjektum</span><span class="sxs-lookup"><span data-stu-id="03495-121">The agent object</span></span>

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

### <span data-ttu-id="03495-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="03495-122">-ParentResourceId</span></span>
<span data-ttu-id="03495-123">Az ügynök erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="03495-123">The agent resource id</span></span>

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

### <span data-ttu-id="03495-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03495-124">-ResourceGroupName</span></span>
<span data-ttu-id="03495-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="03495-125">The resource group name</span></span>

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

### <span data-ttu-id="03495-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="03495-126">-ServerName</span></span>
<span data-ttu-id="03495-127">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="03495-127">The server name</span></span>

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

### <span data-ttu-id="03495-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03495-128">CommonParameters</span></span>
<span data-ttu-id="03495-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03495-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03495-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="03495-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03495-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="03495-131">INPUTS</span></span>

### <span data-ttu-id="03495-132">Microsoft.Azure.Commands.Sql.ElasticMods.Model.AzureSqlElasticAgentModel</span><span class="sxs-lookup"><span data-stu-id="03495-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="03495-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="03495-133">OUTPUTS</span></span>

### <span data-ttu-id="03495-134">Microsoft.Azure.Commands.Sql.ElasticMods.Model.AzureSqlElasticCredentialModel</span><span class="sxs-lookup"><span data-stu-id="03495-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="03495-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="03495-135">NOTES</span></span>

## <span data-ttu-id="03495-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="03495-136">RELATED LINKS</span></span>
