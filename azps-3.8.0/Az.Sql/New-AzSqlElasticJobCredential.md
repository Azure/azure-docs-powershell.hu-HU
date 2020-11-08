---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobCredential.md
ms.openlocfilehash: 404b34c7e0d169e1d123a5c1ded8e6b5bef2fe2e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014257"
---
# <span data-ttu-id="169fa-101">New-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="169fa-101">New-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="169fa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="169fa-102">SYNOPSIS</span></span>
<span data-ttu-id="169fa-103">Új munkahelyi hitelesítő adatok létrehozása</span><span class="sxs-lookup"><span data-stu-id="169fa-103">Creates a new job credential</span></span>

## <span data-ttu-id="169fa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="169fa-104">SYNTAX</span></span>

### <span data-ttu-id="169fa-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="169fa-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="169fa-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="169fa-106">ObjectSet</span></span>
```
New-AzSqlElasticJobCredential [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String>
 -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="169fa-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="169fa-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobCredential [-ParentResourceId] <String> [-Name] <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="169fa-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="169fa-108">DESCRIPTION</span></span>
<span data-ttu-id="169fa-109">A New-AzSqlElasticJobCredential parancsmag új munkahelyi hitelesítő adatokat hoz létre</span><span class="sxs-lookup"><span data-stu-id="169fa-109">The New-AzSqlElasticJobCredential cmdlet creates a new job credential</span></span>

## <span data-ttu-id="169fa-110">Példák</span><span class="sxs-lookup"><span data-stu-id="169fa-110">EXAMPLES</span></span>

### <span data-ttu-id="169fa-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="169fa-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJobCredential -Name cred1 -Credential (Get-Credential)

CredentialName UserName
-------------- --------
cred1          user1
```

<span data-ttu-id="169fa-112">Új munkahelyi hitelesítő adatok létrehozása</span><span class="sxs-lookup"><span data-stu-id="169fa-112">Creates a new job credential</span></span>

## <span data-ttu-id="169fa-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="169fa-113">PARAMETERS</span></span>

### <span data-ttu-id="169fa-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="169fa-114">-AgentName</span></span>
<span data-ttu-id="169fa-115">Az ügynök neve</span><span class="sxs-lookup"><span data-stu-id="169fa-115">The agent name</span></span>

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

### <span data-ttu-id="169fa-116">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="169fa-116">-Credential</span></span>
<span data-ttu-id="169fa-117">A hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="169fa-117">The credential</span></span>

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

### <span data-ttu-id="169fa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="169fa-118">-DefaultProfile</span></span>
<span data-ttu-id="169fa-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="169fa-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="169fa-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="169fa-120">-Name</span></span>
<span data-ttu-id="169fa-121">A munkahelyi hitelesítő adatok neve</span><span class="sxs-lookup"><span data-stu-id="169fa-121">The job credential name</span></span>

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

### <span data-ttu-id="169fa-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="169fa-122">-ParentObject</span></span>
<span data-ttu-id="169fa-123">Az Agent objektum</span><span class="sxs-lookup"><span data-stu-id="169fa-123">The agent object</span></span>

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

### <span data-ttu-id="169fa-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="169fa-124">-ParentResourceId</span></span>
<span data-ttu-id="169fa-125">Az ügynök erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="169fa-125">The agent resource id</span></span>

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

### <span data-ttu-id="169fa-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="169fa-126">-ResourceGroupName</span></span>
<span data-ttu-id="169fa-127">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="169fa-127">The resource group name</span></span>

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

### <span data-ttu-id="169fa-128">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="169fa-128">-ServerName</span></span>
<span data-ttu-id="169fa-129">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="169fa-129">The server name</span></span>

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

### <span data-ttu-id="169fa-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="169fa-130">-Confirm</span></span>
<span data-ttu-id="169fa-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="169fa-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="169fa-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="169fa-132">-WhatIf</span></span>
<span data-ttu-id="169fa-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="169fa-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="169fa-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="169fa-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="169fa-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="169fa-135">CommonParameters</span></span>
<span data-ttu-id="169fa-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="169fa-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="169fa-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="169fa-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="169fa-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="169fa-138">INPUTS</span></span>

### <span data-ttu-id="169fa-139">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="169fa-139">System.Management.Automation.PSCredential</span></span>
### <span data-ttu-id="169fa-140">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="169fa-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="169fa-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="169fa-141">OUTPUTS</span></span>

### <span data-ttu-id="169fa-142">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="169fa-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="169fa-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="169fa-143">NOTES</span></span>

## <span data-ttu-id="169fa-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="169fa-144">RELATED LINKS</span></span>
