---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobCredential.md
ms.openlocfilehash: e9d684be7119ccc0ed991f825d8c7c372e7fdc6e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181316"
---
# <span data-ttu-id="30bd6-101">Remove-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="30bd6-101">Remove-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="30bd6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="30bd6-102">SYNOPSIS</span></span>
<span data-ttu-id="30bd6-103">A rugalmas munka hitelesítő adatainak eltávolítása</span><span class="sxs-lookup"><span data-stu-id="30bd6-103">Removes the elastic job credential</span></span>

## <span data-ttu-id="30bd6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="30bd6-104">SYNTAX</span></span>

### <span data-ttu-id="30bd6-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="30bd6-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30bd6-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="30bd6-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobCredential [-InputObject] <AzureSqlElasticJobCredentialModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30bd6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="30bd6-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobCredential [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30bd6-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="30bd6-108">DESCRIPTION</span></span>
<span data-ttu-id="30bd6-109">A Remove-AzSqlElasticJobCredential parancsmag eltávolítja a feladat hitelesítő adatait</span><span class="sxs-lookup"><span data-stu-id="30bd6-109">The Remove-AzSqlElasticJobCredential cmdlet removes a job credential</span></span>

## <span data-ttu-id="30bd6-110">Példák</span><span class="sxs-lookup"><span data-stu-id="30bd6-110">EXAMPLES</span></span>

### <span data-ttu-id="30bd6-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="30bd6-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Remove-AzSqlElasticJobCredential -Name cred1

CredentialName UserName
-------------- --------
cred1          user2
```

<span data-ttu-id="30bd6-112">Munkahelyi hitelesítő adatok eltávolítása</span><span class="sxs-lookup"><span data-stu-id="30bd6-112">Removes a job credential</span></span>

## <span data-ttu-id="30bd6-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="30bd6-113">PARAMETERS</span></span>

### <span data-ttu-id="30bd6-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="30bd6-114">-AgentName</span></span>
<span data-ttu-id="30bd6-115">Az ügynök neve</span><span class="sxs-lookup"><span data-stu-id="30bd6-115">The agent name</span></span>

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

### <span data-ttu-id="30bd6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30bd6-116">-DefaultProfile</span></span>
<span data-ttu-id="30bd6-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="30bd6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30bd6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="30bd6-118">-InputObject</span></span>
<span data-ttu-id="30bd6-119">A feladat hitelesítőadat-objektuma</span><span class="sxs-lookup"><span data-stu-id="30bd6-119">The job credential object</span></span>

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

### <span data-ttu-id="30bd6-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="30bd6-120">-Name</span></span>
<span data-ttu-id="30bd6-121">A munkahelyi hitelesítő adatok neve</span><span class="sxs-lookup"><span data-stu-id="30bd6-121">The job credential name</span></span>

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

### <span data-ttu-id="30bd6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30bd6-122">-ResourceGroupName</span></span>
<span data-ttu-id="30bd6-123">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="30bd6-123">The resource group name</span></span>

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

### <span data-ttu-id="30bd6-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="30bd6-124">-ResourceId</span></span>
<span data-ttu-id="30bd6-125">A munkahelyi hitelesítőadat-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="30bd6-125">The job credential resource id</span></span>

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

### <span data-ttu-id="30bd6-126">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="30bd6-126">-ServerName</span></span>
<span data-ttu-id="30bd6-127">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="30bd6-127">The server name</span></span>

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

### <span data-ttu-id="30bd6-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="30bd6-128">-Confirm</span></span>
<span data-ttu-id="30bd6-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="30bd6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30bd6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30bd6-130">-WhatIf</span></span>
<span data-ttu-id="30bd6-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="30bd6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30bd6-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="30bd6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30bd6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30bd6-133">CommonParameters</span></span>
<span data-ttu-id="30bd6-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="30bd6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30bd6-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="30bd6-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30bd6-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="30bd6-136">INPUTS</span></span>

### <span data-ttu-id="30bd6-137">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="30bd6-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="30bd6-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="30bd6-138">OUTPUTS</span></span>

### <span data-ttu-id="30bd6-139">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="30bd6-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="30bd6-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="30bd6-140">NOTES</span></span>

## <span data-ttu-id="30bd6-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="30bd6-141">RELATED LINKS</span></span>
