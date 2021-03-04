---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/remove-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobCredential.md
ms.openlocfilehash: d5ee112af595ba88672a26d0f8f64590ea670706
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923282"
---
# <span data-ttu-id="f9b45-101">Remove-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="f9b45-101">Remove-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="f9b45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9b45-102">SYNOPSIS</span></span>
<span data-ttu-id="f9b45-103">A rugalmas feladat hitelesítő adatainak eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f9b45-103">Removes the elastic job credential</span></span>

## <span data-ttu-id="f9b45-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f9b45-104">SYNTAX</span></span>

### <span data-ttu-id="f9b45-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f9b45-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9b45-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="f9b45-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobCredential [-InputObject] <AzureSqlElasticJobCredentialModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9b45-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f9b45-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobCredential [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9b45-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f9b45-108">DESCRIPTION</span></span>
<span data-ttu-id="f9b45-109">A Remove-AzSqlElasticJobCredential parancsmag eltávolítja a hitelesítő adatokat</span><span class="sxs-lookup"><span data-stu-id="f9b45-109">The Remove-AzSqlElasticJobCredential cmdlet removes a job credential</span></span>

## <span data-ttu-id="f9b45-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f9b45-110">EXAMPLES</span></span>

### <span data-ttu-id="f9b45-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="f9b45-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Remove-AzSqlElasticJobCredential -Name cred1

CredentialName UserName
-------------- --------
cred1          user2
```

<span data-ttu-id="f9b45-112">Feladat hitelesítő adatainak eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f9b45-112">Removes a job credential</span></span>

## <span data-ttu-id="f9b45-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f9b45-113">PARAMETERS</span></span>

### <span data-ttu-id="f9b45-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="f9b45-114">-AgentName</span></span>
<span data-ttu-id="f9b45-115">Az ügynök neve</span><span class="sxs-lookup"><span data-stu-id="f9b45-115">The agent name</span></span>

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

### <span data-ttu-id="f9b45-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9b45-116">-DefaultProfile</span></span>
<span data-ttu-id="f9b45-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f9b45-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9b45-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f9b45-118">-InputObject</span></span>
<span data-ttu-id="f9b45-119">A feladat hitelesítőadat-objektuma</span><span class="sxs-lookup"><span data-stu-id="f9b45-119">The job credential object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f9b45-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f9b45-120">-Name</span></span>
<span data-ttu-id="f9b45-121">A feladat hitelesítő adatainak neve</span><span class="sxs-lookup"><span data-stu-id="f9b45-121">The job credential name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: CredentialName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9b45-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9b45-122">-ResourceGroupName</span></span>
<span data-ttu-id="f9b45-123">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="f9b45-123">The resource group name</span></span>

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

### <span data-ttu-id="f9b45-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9b45-124">-ResourceId</span></span>
<span data-ttu-id="f9b45-125">A feladat hitelesítő adatainak erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="f9b45-125">The job credential resource id</span></span>

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

### <span data-ttu-id="f9b45-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f9b45-126">-ServerName</span></span>
<span data-ttu-id="f9b45-127">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="f9b45-127">The server name</span></span>

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

### <span data-ttu-id="f9b45-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f9b45-128">-Confirm</span></span>
<span data-ttu-id="f9b45-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f9b45-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9b45-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9b45-130">-WhatIf</span></span>
<span data-ttu-id="f9b45-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f9b45-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9b45-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f9b45-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9b45-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9b45-133">CommonParameters</span></span>
<span data-ttu-id="f9b45-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9b45-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9b45-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f9b45-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9b45-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f9b45-136">INPUTS</span></span>

### <span data-ttu-id="f9b45-137">Microsoft.Azure.Commands.Sql.ElasticMods.Model.AzureSqlElasticCredentialModel</span><span class="sxs-lookup"><span data-stu-id="f9b45-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="f9b45-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f9b45-138">OUTPUTS</span></span>

### <span data-ttu-id="f9b45-139">Microsoft.Azure.Commands.Sql.ElasticMods.Model.AzureSqlElasticCredentialModel</span><span class="sxs-lookup"><span data-stu-id="f9b45-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="f9b45-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f9b45-140">NOTES</span></span>

## <span data-ttu-id="f9b45-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f9b45-141">RELATED LINKS</span></span>
