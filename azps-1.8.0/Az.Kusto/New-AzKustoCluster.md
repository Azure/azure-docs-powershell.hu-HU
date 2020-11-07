---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/New-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/New-AzKustoCluster.md
ms.openlocfilehash: 9157c5dfff46893cfee88d02d8f1564801f889fe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835581"
---
# <span data-ttu-id="aa2b2-101">New-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="aa2b2-101">New-AzKustoCluster</span></span>

## <span data-ttu-id="aa2b2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aa2b2-102">SYNOPSIS</span></span>
<span data-ttu-id="aa2b2-103">Új Kusto-fürtöt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="aa2b2-103">Creates a new Kusto cluster.</span></span>

## <span data-ttu-id="aa2b2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aa2b2-104">SYNTAX</span></span>

```
New-AzKustoCluster [-ResourceGroupName] <String> [-Name] <String> -Location <String> -Sku <String>
 [-Tier <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aa2b2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="aa2b2-105">DESCRIPTION</span></span>
<span data-ttu-id="aa2b2-106">Új Kusto-fürtöt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="aa2b2-106">Creates a new Kusto cluster.</span></span>

## <span data-ttu-id="aa2b2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="aa2b2-107">EXAMPLES</span></span>

### <span data-ttu-id="aa2b2-108">Példa 1 – új Kusto-fürt létrehozása</span><span class="sxs-lookup"><span data-stu-id="aa2b2-108">Example 1 - Create a new Kusto cluster</span></span>

```
PS C:\> New-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster -Location 'Central US' -Sku D13_v2 -Capacity 10

Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Capacity          : 10
Sku               : D13_v2
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster.centralus.kusto.windows.net
```

<span data-ttu-id="aa2b2-109">A fenti parancs létrehoz egy új Kusto-fürtöt, az "mykustocluster" nevű erőforráscsoport "testrg" erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="aa2b2-109">The above command creates a new Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="aa2b2-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aa2b2-110">PARAMETERS</span></span>

### <span data-ttu-id="aa2b2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa2b2-111">-DefaultProfile</span></span>
<span data-ttu-id="aa2b2-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aa2b2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa2b2-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="aa2b2-113">-Location</span></span>
<span data-ttu-id="aa2b2-114">Azure-terület, ahol a fürtöt létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="aa2b2-114">Azure region where the cluster should be created.</span></span>

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

### <span data-ttu-id="aa2b2-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="aa2b2-115">-Name</span></span>
<span data-ttu-id="aa2b2-116">A létrehozandó fürt neve.</span><span class="sxs-lookup"><span data-stu-id="aa2b2-116">Name of the cluster to be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa2b2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa2b2-117">-ResourceGroupName</span></span>
<span data-ttu-id="aa2b2-118">Annak az erőforráscsoport-csoportnak a neve, amelybe a fürtöt létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="aa2b2-118">Name of resource group under which you want to create the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa2b2-119">-SKU</span><span class="sxs-lookup"><span data-stu-id="aa2b2-119">-Sku</span></span>
<span data-ttu-id="aa2b2-120">A fürt létrehozásához használt SKU neve</span><span class="sxs-lookup"><span data-stu-id="aa2b2-120">Name of the Sku used to create the cluster</span></span>

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

### <span data-ttu-id="aa2b2-121">-Címke</span><span class="sxs-lookup"><span data-stu-id="aa2b2-121">-Tag</span></span>
<span data-ttu-id="aa2b2-122">A fürthöz társított címkék karakterlánca, karakterlánc-szótára</span><span class="sxs-lookup"><span data-stu-id="aa2b2-122">A string,string dictionary of tags associated with this cluster</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa2b2-123">-Tier (Tier)</span><span class="sxs-lookup"><span data-stu-id="aa2b2-123">-Tier</span></span>
<span data-ttu-id="aa2b2-124">A fürt létrehozásához használt szint neve</span><span class="sxs-lookup"><span data-stu-id="aa2b2-124">Name of the Tier used to create the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa2b2-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="aa2b2-125">-Confirm</span></span>
<span data-ttu-id="aa2b2-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="aa2b2-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa2b2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa2b2-127">-WhatIf</span></span>
<span data-ttu-id="aa2b2-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="aa2b2-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa2b2-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="aa2b2-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa2b2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa2b2-130">CommonParameters</span></span>
<span data-ttu-id="aa2b2-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aa2b2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa2b2-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa2b2-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa2b2-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa2b2-133">INPUTS</span></span>

### <span data-ttu-id="aa2b2-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="aa2b2-134">None</span></span>

## <span data-ttu-id="aa2b2-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa2b2-135">OUTPUTS</span></span>

### <span data-ttu-id="aa2b2-136">Microsoft. Azure. Command. Kusto. models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="aa2b2-136">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="aa2b2-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aa2b2-137">NOTES</span></span>

## <span data-ttu-id="aa2b2-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aa2b2-138">RELATED LINKS</span></span>
