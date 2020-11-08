---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: f33d644e9726d09f9f2314e74a6b5fb80b788952
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025679"
---
# <span data-ttu-id="b7aee-101">Get-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="b7aee-101">Get-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="b7aee-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b7aee-102">SYNOPSIS</span></span>
<span data-ttu-id="b7aee-103">A KQL-lekérdezéseken belül futtatható nyelvi bővítmények listáját jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="b7aee-103">Returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="b7aee-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b7aee-104">SYNTAX</span></span>

```
Get-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b7aee-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b7aee-105">DESCRIPTION</span></span>
<span data-ttu-id="b7aee-106">A KQL-lekérdezéseken belül futtatható nyelvi bővítmények listáját jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="b7aee-106">Returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="b7aee-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b7aee-107">EXAMPLES</span></span>

### <span data-ttu-id="b7aee-108">Példa 1: egy fürthöz beállított nyelvi bővítmények listázása</span><span class="sxs-lookup"><span data-stu-id="b7aee-108">Example 1: List all language extensions set for a cluster</span></span>
```powershell
PS C:\> Get-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster

Name
----
R
PYTHON
```

<span data-ttu-id="b7aee-109">A fenti parancs a KQL-lekérdezéseken belül futtatható nyelvi bővítmények listáját jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="b7aee-109">The above command returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="b7aee-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b7aee-110">PARAMETERS</span></span>

### <span data-ttu-id="b7aee-111">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="b7aee-111">-ClusterName</span></span>
<span data-ttu-id="b7aee-112">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="b7aee-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="b7aee-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7aee-113">-DefaultProfile</span></span>
<span data-ttu-id="b7aee-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b7aee-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7aee-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7aee-115">-ResourceGroupName</span></span>
<span data-ttu-id="b7aee-116">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b7aee-116">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="b7aee-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b7aee-117">-SubscriptionId</span></span>
<span data-ttu-id="b7aee-118">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b7aee-118">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b7aee-119">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="b7aee-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b7aee-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b7aee-120">-Confirm</span></span>
<span data-ttu-id="b7aee-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b7aee-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7aee-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7aee-122">-WhatIf</span></span>
<span data-ttu-id="b7aee-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b7aee-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7aee-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b7aee-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7aee-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7aee-125">CommonParameters</span></span>
<span data-ttu-id="b7aee-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b7aee-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7aee-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b7aee-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7aee-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7aee-128">INPUTS</span></span>

## <span data-ttu-id="b7aee-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7aee-129">OUTPUTS</span></span>

### <span data-ttu-id="b7aee-130">Microsoft. Azure. PowerShell. parancsmagok. Kusto. modellek. Api20200614. ILanguageExtension</span><span class="sxs-lookup"><span data-stu-id="b7aee-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ILanguageExtension</span></span>

## <span data-ttu-id="b7aee-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b7aee-131">NOTES</span></span>

<span data-ttu-id="b7aee-132">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="b7aee-132">ALIASES</span></span>

## <span data-ttu-id="b7aee-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b7aee-133">RELATED LINKS</span></span>

