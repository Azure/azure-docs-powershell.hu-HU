---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/New-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/New-AzKustoCluster.md
ms.openlocfilehash: 9c18597da52900794e5f891fb06385249c173a0b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011132"
---
# <span data-ttu-id="deb4f-101">New-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="deb4f-101">New-AzKustoCluster</span></span>

## <span data-ttu-id="deb4f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="deb4f-102">SYNOPSIS</span></span>
<span data-ttu-id="deb4f-103">Új Kusto-fürtöt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="deb4f-103">Creates a new Kusto cluster.</span></span>

## <span data-ttu-id="deb4f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="deb4f-104">SYNTAX</span></span>

```
New-AzKustoCluster [-ResourceGroupName] <String> [-Name] <String> -Location <String> -Sku <String>
 [-Tier <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="deb4f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="deb4f-105">DESCRIPTION</span></span>
<span data-ttu-id="deb4f-106">Új Kusto-fürtöt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="deb4f-106">Creates a new Kusto cluster.</span></span>

## <span data-ttu-id="deb4f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="deb4f-107">EXAMPLES</span></span>

### <span data-ttu-id="deb4f-108">Példa 1 – új Kusto-fürt létrehozása</span><span class="sxs-lookup"><span data-stu-id="deb4f-108">Example 1 - Create a new Kusto cluster</span></span>

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

<span data-ttu-id="deb4f-109">A fenti parancs létrehoz egy új Kusto-fürtöt, az "mykustocluster" nevű erőforráscsoport "testrg" erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="deb4f-109">The above command creates a new Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="deb4f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="deb4f-110">PARAMETERS</span></span>

### <span data-ttu-id="deb4f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="deb4f-111">-DefaultProfile</span></span>
<span data-ttu-id="deb4f-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="deb4f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="deb4f-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="deb4f-113">-Location</span></span>
<span data-ttu-id="deb4f-114">Azure-terület, ahol a fürtöt létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="deb4f-114">Azure region where the cluster should be created.</span></span>

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

### <span data-ttu-id="deb4f-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="deb4f-115">-Name</span></span>
<span data-ttu-id="deb4f-116">A létrehozandó fürt neve.</span><span class="sxs-lookup"><span data-stu-id="deb4f-116">Name of the cluster to be created.</span></span>

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

### <span data-ttu-id="deb4f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="deb4f-117">-ResourceGroupName</span></span>
<span data-ttu-id="deb4f-118">Annak az erőforráscsoport-csoportnak a neve, amelybe a fürtöt létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="deb4f-118">Name of resource group under which you want to create the cluster.</span></span>

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

### <span data-ttu-id="deb4f-119">-SKU</span><span class="sxs-lookup"><span data-stu-id="deb4f-119">-Sku</span></span>
<span data-ttu-id="deb4f-120">A fürt létrehozásához használt SKU neve</span><span class="sxs-lookup"><span data-stu-id="deb4f-120">Name of the Sku used to create the cluster</span></span>

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

### <span data-ttu-id="deb4f-121">-Címke</span><span class="sxs-lookup"><span data-stu-id="deb4f-121">-Tag</span></span>
<span data-ttu-id="deb4f-122">A fürthöz társított címkék karakterlánca, karakterlánc-szótára</span><span class="sxs-lookup"><span data-stu-id="deb4f-122">A string,string dictionary of tags associated with this cluster</span></span>

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

### <span data-ttu-id="deb4f-123">-Tier (Tier)</span><span class="sxs-lookup"><span data-stu-id="deb4f-123">-Tier</span></span>
<span data-ttu-id="deb4f-124">A fürt létrehozásához használt szint neve</span><span class="sxs-lookup"><span data-stu-id="deb4f-124">Name of the Tier used to create the cluster</span></span>

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

### <span data-ttu-id="deb4f-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="deb4f-125">-Confirm</span></span>
<span data-ttu-id="deb4f-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="deb4f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="deb4f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="deb4f-127">-WhatIf</span></span>
<span data-ttu-id="deb4f-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="deb4f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="deb4f-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="deb4f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="deb4f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deb4f-130">CommonParameters</span></span>
<span data-ttu-id="deb4f-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="deb4f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="deb4f-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="deb4f-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deb4f-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="deb4f-133">INPUTS</span></span>

### <span data-ttu-id="deb4f-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="deb4f-134">None</span></span>

## <span data-ttu-id="deb4f-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="deb4f-135">OUTPUTS</span></span>

### <span data-ttu-id="deb4f-136">Microsoft. Azure. Command. Kusto. models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="deb4f-136">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="deb4f-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="deb4f-137">NOTES</span></span>

## <span data-ttu-id="deb4f-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="deb4f-138">RELATED LINKS</span></span>
