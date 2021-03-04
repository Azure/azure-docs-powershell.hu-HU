---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/new-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobCredential.md
ms.openlocfilehash: 8f82162b0f1e5b1f43852880c77d1be1427e3ca1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927745"
---
# <span data-ttu-id="80689-101">New-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="80689-101">New-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="80689-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80689-102">SYNOPSIS</span></span>
<span data-ttu-id="80689-103">Új feladat hitelesítő adatainak létrehozása</span><span class="sxs-lookup"><span data-stu-id="80689-103">Creates a new job credential</span></span>

## <span data-ttu-id="80689-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="80689-104">SYNTAX</span></span>

### <span data-ttu-id="80689-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="80689-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="80689-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="80689-106">ObjectSet</span></span>
```
New-AzSqlElasticJobCredential [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String>
 -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="80689-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="80689-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobCredential [-ParentResourceId] <String> [-Name] <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80689-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="80689-108">DESCRIPTION</span></span>
<span data-ttu-id="80689-109">A New-AzSqlElasticJobCredential parancsmag létrehoz egy új feladat hitelesítő adatait</span><span class="sxs-lookup"><span data-stu-id="80689-109">The New-AzSqlElasticJobCredential cmdlet creates a new job credential</span></span>

## <span data-ttu-id="80689-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="80689-110">EXAMPLES</span></span>

### <span data-ttu-id="80689-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="80689-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJobCredential -Name cred1 -Credential (Get-Credential)

CredentialName UserName
-------------- --------
cred1          user1
```

<span data-ttu-id="80689-112">Új feladat hitelesítő adatainak létrehozása</span><span class="sxs-lookup"><span data-stu-id="80689-112">Creates a new job credential</span></span>

## <span data-ttu-id="80689-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="80689-113">PARAMETERS</span></span>

### <span data-ttu-id="80689-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="80689-114">-AgentName</span></span>
<span data-ttu-id="80689-115">Az ügynök neve</span><span class="sxs-lookup"><span data-stu-id="80689-115">The agent name</span></span>

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

### <span data-ttu-id="80689-116">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="80689-116">-Credential</span></span>
<span data-ttu-id="80689-117">A hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="80689-117">The credential</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80689-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80689-118">-DefaultProfile</span></span>
<span data-ttu-id="80689-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="80689-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80689-120">-Name</span><span class="sxs-lookup"><span data-stu-id="80689-120">-Name</span></span>
<span data-ttu-id="80689-121">A feladat hitelesítő adatainak neve</span><span class="sxs-lookup"><span data-stu-id="80689-121">The job credential name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CredentialName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80689-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="80689-122">-ParentObject</span></span>
<span data-ttu-id="80689-123">Az ügynökobjektum</span><span class="sxs-lookup"><span data-stu-id="80689-123">The agent object</span></span>

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

### <span data-ttu-id="80689-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="80689-124">-ParentResourceId</span></span>
<span data-ttu-id="80689-125">Az ügynök erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="80689-125">The agent resource id</span></span>

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

### <span data-ttu-id="80689-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80689-126">-ResourceGroupName</span></span>
<span data-ttu-id="80689-127">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="80689-127">The resource group name</span></span>

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

### <span data-ttu-id="80689-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="80689-128">-ServerName</span></span>
<span data-ttu-id="80689-129">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="80689-129">The server name</span></span>

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

### <span data-ttu-id="80689-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="80689-130">-Confirm</span></span>
<span data-ttu-id="80689-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="80689-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80689-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80689-132">-WhatIf</span></span>
<span data-ttu-id="80689-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="80689-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80689-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="80689-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80689-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80689-135">CommonParameters</span></span>
<span data-ttu-id="80689-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80689-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80689-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="80689-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80689-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="80689-138">INPUTS</span></span>

### <span data-ttu-id="80689-139">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="80689-139">System.Management.Automation.PSCredential</span></span>
### <span data-ttu-id="80689-140">Microsoft.Azure.Commands.Sql.ElasticMods.Model.AzureSqlElasticAgentModel</span><span class="sxs-lookup"><span data-stu-id="80689-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="80689-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="80689-141">OUTPUTS</span></span>

### <span data-ttu-id="80689-142">Microsoft.Azure.Commands.Sql.ElasticMods.Model.AzureSqlElasticCredentialModel</span><span class="sxs-lookup"><span data-stu-id="80689-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="80689-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="80689-143">NOTES</span></span>

## <span data-ttu-id="80689-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="80689-144">RELATED LINKS</span></span>
