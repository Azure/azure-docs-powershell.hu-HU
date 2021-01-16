---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: 8ad074cf40074032fbab46cab6ee6c6c290eb2ce
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466372"
---
# <span data-ttu-id="7975e-101">Get-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="7975e-101">Get-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="7975e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7975e-102">SYNOPSIS</span></span>
<span data-ttu-id="7975e-103">A KQL-lekérdezésekben futtatható nyelvbővítmények listáját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="7975e-103">Returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="7975e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7975e-104">SYNTAX</span></span>

```
Get-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7975e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7975e-105">DESCRIPTION</span></span>
<span data-ttu-id="7975e-106">A KQL-lekérdezésekben futtatható nyelvbővítmények listáját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="7975e-106">Returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="7975e-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7975e-107">EXAMPLES</span></span>

### <span data-ttu-id="7975e-108">1. példa: A fürthöz beállított összes nyelvi bővítmény felsorolása</span><span class="sxs-lookup"><span data-stu-id="7975e-108">Example 1: List all language extensions set for a cluster</span></span>
```powershell
PS C:\> Get-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster

Name
----
R
PYTHON
```

<span data-ttu-id="7975e-109">A fenti parancs a KQL-lekérdezésekben futtatható nyelvi bővítmények listáját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="7975e-109">The above command returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="7975e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7975e-110">PARAMETERS</span></span>

### <span data-ttu-id="7975e-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="7975e-111">-ClusterName</span></span>
<span data-ttu-id="7975e-112">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="7975e-112">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7975e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7975e-113">-DefaultProfile</span></span>
<span data-ttu-id="7975e-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7975e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7975e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7975e-115">-ResourceGroupName</span></span>
<span data-ttu-id="7975e-116">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7975e-116">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7975e-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7975e-117">-SubscriptionId</span></span>
<span data-ttu-id="7975e-118">Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="7975e-118">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="7975e-119">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="7975e-119">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7975e-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7975e-120">-Confirm</span></span>
<span data-ttu-id="7975e-121">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7975e-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7975e-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7975e-122">-WhatIf</span></span>
<span data-ttu-id="7975e-123">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7975e-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7975e-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7975e-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7975e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7975e-125">CommonParameters</span></span>
<span data-ttu-id="7975e-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7975e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7975e-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7975e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7975e-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7975e-128">INPUTS</span></span>

## <span data-ttu-id="7975e-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7975e-129">OUTPUTS</span></span>

### <span data-ttu-id="7975e-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ILanguageExtension</span><span class="sxs-lookup"><span data-stu-id="7975e-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ILanguageExtension</span></span>

## <span data-ttu-id="7975e-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7975e-131">NOTES</span></span>

<span data-ttu-id="7975e-132">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="7975e-132">ALIASES</span></span>

## <span data-ttu-id="7975e-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7975e-133">RELATED LINKS</span></span>

