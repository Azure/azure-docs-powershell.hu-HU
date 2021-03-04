---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/set-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobCredential.md
ms.openlocfilehash: 9c0d7348a900690a49ebea96bc90c296c2d8e9a9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935929"
---
# <span data-ttu-id="1c1b6-101">Set-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="1c1b6-101">Set-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="1c1b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c1b6-102">SYNOPSIS</span></span>
<span data-ttu-id="1c1b6-103">A feladat hitelesítő adatainak frissítése</span><span class="sxs-lookup"><span data-stu-id="1c1b6-103">Updates a job credential</span></span>

## <span data-ttu-id="1c1b6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1c1b6-104">SYNTAX</span></span>

### <span data-ttu-id="1c1b6-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1c1b6-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1c1b6-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="1c1b6-106">ObjectSet</span></span>
```
Set-AzSqlElasticJobCredential [-InputObject] <AzureSqlElasticJobCredentialModel> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c1b6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1c1b6-107">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobCredential [-ResourceId] <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c1b6-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1c1b6-108">DESCRIPTION</span></span>
<span data-ttu-id="1c1b6-109">A Set-AzSqlElasticJobCredential parancsmag frissíti a feladat hitelesítő adatait</span><span class="sxs-lookup"><span data-stu-id="1c1b6-109">The Set-AzSqlElasticJobCredential cmdlet updates a job credential</span></span>

## <span data-ttu-id="1c1b6-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1c1b6-110">EXAMPLES</span></span>

### <span data-ttu-id="1c1b6-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="1c1b6-111">Example 1</span></span>
```
PS C:\> $cred = Get-AzSqlElasticJobCredential -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name cred1
$cred | Set-AzSqlElasticJobCredential -Name cred1 -Credential (Get-Credential)

CredentialName UserName
-------------- --------
cred1          user2
```

<span data-ttu-id="1c1b6-112">A feladat hitelesítő adatainak frissítése</span><span class="sxs-lookup"><span data-stu-id="1c1b6-112">Updates a job credential</span></span>

## <span data-ttu-id="1c1b6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c1b6-113">PARAMETERS</span></span>

### <span data-ttu-id="1c1b6-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="1c1b6-114">-AgentName</span></span>
<span data-ttu-id="1c1b6-115">Az ügynök neve</span><span class="sxs-lookup"><span data-stu-id="1c1b6-115">The agent name</span></span>

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

### <span data-ttu-id="1c1b6-116">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="1c1b6-116">-Credential</span></span>
<span data-ttu-id="1c1b6-117">A hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="1c1b6-117">The credential</span></span>

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

### <span data-ttu-id="1c1b6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c1b6-118">-DefaultProfile</span></span>
<span data-ttu-id="1c1b6-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1c1b6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c1b6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1c1b6-120">-InputObject</span></span>
<span data-ttu-id="1c1b6-121">A feladat hitelesítőadat-objektuma</span><span class="sxs-lookup"><span data-stu-id="1c1b6-121">The job credential object</span></span>

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

### <span data-ttu-id="1c1b6-122">-Name</span><span class="sxs-lookup"><span data-stu-id="1c1b6-122">-Name</span></span>
<span data-ttu-id="1c1b6-123">A feladat hitelesítő adatainak neve</span><span class="sxs-lookup"><span data-stu-id="1c1b6-123">The job credential name</span></span>

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

### <span data-ttu-id="1c1b6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c1b6-124">-ResourceGroupName</span></span>
<span data-ttu-id="1c1b6-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="1c1b6-125">The resource group name</span></span>

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

### <span data-ttu-id="1c1b6-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1c1b6-126">-ResourceId</span></span>
<span data-ttu-id="1c1b6-127">A feladat hitelesítő adatainak erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="1c1b6-127">The job credential resource id</span></span>

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

### <span data-ttu-id="1c1b6-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1c1b6-128">-ServerName</span></span>
<span data-ttu-id="1c1b6-129">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="1c1b6-129">The server name</span></span>

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

### <span data-ttu-id="1c1b6-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1c1b6-130">-Confirm</span></span>
<span data-ttu-id="1c1b6-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1c1b6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c1b6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c1b6-132">-WhatIf</span></span>
<span data-ttu-id="1c1b6-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1c1b6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c1b6-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1c1b6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c1b6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c1b6-135">CommonParameters</span></span>
<span data-ttu-id="1c1b6-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c1b6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c1b6-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1c1b6-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c1b6-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1c1b6-138">INPUTS</span></span>

### <span data-ttu-id="1c1b6-139">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="1c1b6-139">System.Management.Automation.PSCredential</span></span>
### <span data-ttu-id="1c1b6-140">Microsoft.Azure.Commands.Sql.ElasticMods.Model.AzureSqlElasticCredentialModel</span><span class="sxs-lookup"><span data-stu-id="1c1b6-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="1c1b6-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1c1b6-141">OUTPUTS</span></span>

### <span data-ttu-id="1c1b6-142">Microsoft.Azure.Commands.Sql.ElasticMods.Model.AzureSqlElasticCredentialModel</span><span class="sxs-lookup"><span data-stu-id="1c1b6-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="1c1b6-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1c1b6-143">NOTES</span></span>

## <span data-ttu-id="1c1b6-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1c1b6-144">RELATED LINKS</span></span>
