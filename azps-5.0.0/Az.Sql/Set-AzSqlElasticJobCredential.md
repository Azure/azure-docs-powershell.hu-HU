---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobCredential.md
ms.openlocfilehash: 87ac0ddaa205c2b257a3aadf9ceea5a6ec302eab
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300464"
---
# <span data-ttu-id="a6e2e-101">Set-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="a6e2e-101">Set-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="a6e2e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a6e2e-102">SYNOPSIS</span></span>
<span data-ttu-id="a6e2e-103">Munkahelyi hitelesítő adatok frissítése</span><span class="sxs-lookup"><span data-stu-id="a6e2e-103">Updates a job credential</span></span>

## <span data-ttu-id="a6e2e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a6e2e-104">SYNTAX</span></span>

### <span data-ttu-id="a6e2e-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a6e2e-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a6e2e-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="a6e2e-106">ObjectSet</span></span>
```
Set-AzSqlElasticJobCredential [-InputObject] <AzureSqlElasticJobCredentialModel> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6e2e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a6e2e-107">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobCredential [-ResourceId] <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6e2e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a6e2e-108">DESCRIPTION</span></span>
<span data-ttu-id="a6e2e-109">A Set-AzSqlElasticJobCredential parancsmag frissíti a feladat hitelesítő adatait</span><span class="sxs-lookup"><span data-stu-id="a6e2e-109">The Set-AzSqlElasticJobCredential cmdlet updates a job credential</span></span>

## <span data-ttu-id="a6e2e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a6e2e-110">EXAMPLES</span></span>

### <span data-ttu-id="a6e2e-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a6e2e-111">Example 1</span></span>
```
PS C:\> $cred = Get-AzSqlElasticJobCredential -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name cred1
$cred | Set-AzSqlElasticJobCredential -Name cred1 -Credential (Get-Credential)

CredentialName UserName
-------------- --------
cred1          user2
```

<span data-ttu-id="a6e2e-112">Munkahelyi hitelesítő adatok frissítése</span><span class="sxs-lookup"><span data-stu-id="a6e2e-112">Updates a job credential</span></span>

## <span data-ttu-id="a6e2e-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a6e2e-113">PARAMETERS</span></span>

### <span data-ttu-id="a6e2e-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="a6e2e-114">-AgentName</span></span>
<span data-ttu-id="a6e2e-115">Az ügynök neve</span><span class="sxs-lookup"><span data-stu-id="a6e2e-115">The agent name</span></span>

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

### <span data-ttu-id="a6e2e-116">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="a6e2e-116">-Credential</span></span>
<span data-ttu-id="a6e2e-117">A hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="a6e2e-117">The credential</span></span>

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

### <span data-ttu-id="a6e2e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6e2e-118">-DefaultProfile</span></span>
<span data-ttu-id="a6e2e-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a6e2e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6e2e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6e2e-120">-InputObject</span></span>
<span data-ttu-id="a6e2e-121">A feladat hitelesítőadat-objektuma</span><span class="sxs-lookup"><span data-stu-id="a6e2e-121">The job credential object</span></span>

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

### <span data-ttu-id="a6e2e-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a6e2e-122">-Name</span></span>
<span data-ttu-id="a6e2e-123">A munkahelyi hitelesítő adatok neve</span><span class="sxs-lookup"><span data-stu-id="a6e2e-123">The job credential name</span></span>

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

### <span data-ttu-id="a6e2e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6e2e-124">-ResourceGroupName</span></span>
<span data-ttu-id="a6e2e-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="a6e2e-125">The resource group name</span></span>

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

### <span data-ttu-id="a6e2e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6e2e-126">-ResourceId</span></span>
<span data-ttu-id="a6e2e-127">A munkahelyi hitelesítőadat-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="a6e2e-127">The job credential resource id</span></span>

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

### <span data-ttu-id="a6e2e-128">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="a6e2e-128">-ServerName</span></span>
<span data-ttu-id="a6e2e-129">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="a6e2e-129">The server name</span></span>

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

### <span data-ttu-id="a6e2e-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a6e2e-130">-Confirm</span></span>
<span data-ttu-id="a6e2e-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a6e2e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6e2e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6e2e-132">-WhatIf</span></span>
<span data-ttu-id="a6e2e-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a6e2e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6e2e-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a6e2e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6e2e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6e2e-135">CommonParameters</span></span>
<span data-ttu-id="a6e2e-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a6e2e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6e2e-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a6e2e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6e2e-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a6e2e-138">INPUTS</span></span>

### <span data-ttu-id="a6e2e-139">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="a6e2e-139">System.Management.Automation.PSCredential</span></span>
### <span data-ttu-id="a6e2e-140">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="a6e2e-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="a6e2e-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a6e2e-141">OUTPUTS</span></span>

### <span data-ttu-id="a6e2e-142">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="a6e2e-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="a6e2e-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a6e2e-143">NOTES</span></span>

## <span data-ttu-id="a6e2e-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a6e2e-144">RELATED LINKS</span></span>
