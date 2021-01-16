---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: f33d644e9726d09f9f2314e74a6b5fb80b788952
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342018"
---
# <span data-ttu-id="f7df6-101">Get-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="f7df6-101">Get-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="f7df6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7df6-102">SYNOPSIS</span></span>
<span data-ttu-id="f7df6-103">A KQL-lekérdezésekben futtatható nyelvbővítmények listáját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="f7df6-103">Returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="f7df6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f7df6-104">SYNTAX</span></span>

```
Get-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f7df6-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f7df6-105">DESCRIPTION</span></span>
<span data-ttu-id="f7df6-106">A KQL-lekérdezésekben futtatható nyelvbővítmények listáját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="f7df6-106">Returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="f7df6-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f7df6-107">EXAMPLES</span></span>

### <span data-ttu-id="f7df6-108">1. példa: A fürthöz beállított összes nyelvi bővítmény felsorolása</span><span class="sxs-lookup"><span data-stu-id="f7df6-108">Example 1: List all language extensions set for a cluster</span></span>
```powershell
PS C:\> Get-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster

Name
----
R
PYTHON
```

<span data-ttu-id="f7df6-109">A fenti parancs a KQL-lekérdezésekben futtatható nyelvi bővítmények listáját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="f7df6-109">The above command returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="f7df6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7df6-110">PARAMETERS</span></span>

### <span data-ttu-id="f7df6-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f7df6-111">-ClusterName</span></span>
<span data-ttu-id="f7df6-112">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="f7df6-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="f7df6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7df6-113">-DefaultProfile</span></span>
<span data-ttu-id="f7df6-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f7df6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7df6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7df6-115">-ResourceGroupName</span></span>
<span data-ttu-id="f7df6-116">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f7df6-116">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="f7df6-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f7df6-117">-SubscriptionId</span></span>
<span data-ttu-id="f7df6-118">Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="f7df6-118">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f7df6-119">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="f7df6-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f7df6-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7df6-120">-Confirm</span></span>
<span data-ttu-id="f7df6-121">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f7df6-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7df6-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7df6-122">-WhatIf</span></span>
<span data-ttu-id="f7df6-123">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f7df6-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7df6-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f7df6-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7df6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7df6-125">CommonParameters</span></span>
<span data-ttu-id="f7df6-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7df6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7df6-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f7df6-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7df6-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f7df6-128">INPUTS</span></span>

## <span data-ttu-id="f7df6-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7df6-129">OUTPUTS</span></span>

### <span data-ttu-id="f7df6-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ILanguageExtension</span><span class="sxs-lookup"><span data-stu-id="f7df6-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ILanguageExtension</span></span>

## <span data-ttu-id="f7df6-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f7df6-131">NOTES</span></span>

<span data-ttu-id="f7df6-132">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="f7df6-132">ALIASES</span></span>

## <span data-ttu-id="f7df6-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f7df6-133">RELATED LINKS</span></span>

