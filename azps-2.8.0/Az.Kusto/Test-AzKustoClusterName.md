---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustoclustername
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Test-AzKustoClusterName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Test-AzKustoClusterName.md
ms.openlocfilehash: 9a3d8397914317d733c8da47e7d095e1acb541e4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666104"
---
# <span data-ttu-id="b2907-101">Test-AzKustoClusterName</span><span class="sxs-lookup"><span data-stu-id="b2907-101">Test-AzKustoClusterName</span></span>

## <span data-ttu-id="b2907-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b2907-102">SYNOPSIS</span></span>
<span data-ttu-id="b2907-103">Ellenőrizze, hogy elérhető-e egy adott Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="b2907-103">Check if a given Kusto cluster name is available.</span></span>

## <span data-ttu-id="b2907-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b2907-104">SYNTAX</span></span>

```
Test-AzKustoClusterName -Location <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b2907-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b2907-105">DESCRIPTION</span></span>
<span data-ttu-id="b2907-106">Ellenőrizze, hogy elérhető-e egy adott Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="b2907-106">Check if a given Kusto cluster name is available.</span></span>

## <span data-ttu-id="b2907-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b2907-107">EXAMPLES</span></span>

### <span data-ttu-id="b2907-108">Példa 1 – annak a Kusto a elérhetőségét ellenőrzi, amely használatban van</span><span class="sxs-lookup"><span data-stu-id="b2907-108">Example 1 - Check the availability of a Kusto cluster name which is in use</span></span>

```
PS C:\> Test-AzKustoClusterName -Location 'Central US' -Name mykustocluster

NameAvailable       Name                        Message
-------------           ----                            -------
False                   mykustocluster      Name 'mykustocluster' with type Engine is already taken. Please specify a different name
```

<span data-ttu-id="b2907-109">A fenti parancs azt jeleníti meg, hogy a "mykustocluster" nevű Kusto-fürt létezik-e a "Közép-amerikai" régióban.</span><span class="sxs-lookup"><span data-stu-id="b2907-109">The above command returns whether or not a Kusto cluster named "mykustocluster" exists in the "Central US" region.</span></span>

### <span data-ttu-id="b2907-110">Példa 2 – annak ellenőrzése, hogy nincs-e használatban a Kusto-fürt elérhetősége</span><span class="sxs-lookup"><span data-stu-id="b2907-110">Example 2 - Check the availability of a Kusto cluster name which is not in use</span></span>

```
PS C:\> Test-AzKustoClusterName -Location 'Central US' -Name mykustocluster

NameAvailable       Name                        Message
-------------           ----                            -------
 True                   mykustocluster
```

<span data-ttu-id="b2907-111">A fenti parancs azt jeleníti meg, hogy a "mykustocluster" nevű Kusto-fürt létezik-e a "Közép-amerikai" régióban.</span><span class="sxs-lookup"><span data-stu-id="b2907-111">The above command returns whether or not a Kusto cluster named "mykustocluster" exists in the "Central US" region.</span></span>

## <span data-ttu-id="b2907-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b2907-112">PARAMETERS</span></span>

### <span data-ttu-id="b2907-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2907-113">-DefaultProfile</span></span>
<span data-ttu-id="b2907-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b2907-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2907-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="b2907-115">-Location</span></span>
<span data-ttu-id="b2907-116">Az ellenőrzés helye.</span><span class="sxs-lookup"><span data-stu-id="b2907-116">The location where to check.</span></span>

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

### <span data-ttu-id="b2907-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b2907-117">-Name</span></span>
<span data-ttu-id="b2907-118">Egy adott fürt neve.</span><span class="sxs-lookup"><span data-stu-id="b2907-118">Name of a specific cluster.</span></span>

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

### <span data-ttu-id="b2907-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2907-119">CommonParameters</span></span>
<span data-ttu-id="b2907-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b2907-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2907-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2907-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2907-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2907-122">INPUTS</span></span>

### <span data-ttu-id="b2907-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="b2907-123">None</span></span>

## <span data-ttu-id="b2907-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2907-124">OUTPUTS</span></span>

### <span data-ttu-id="b2907-125">Microsoft. Azure. Command. Kusto. models. PSKustoClusterNameAvailability</span><span class="sxs-lookup"><span data-stu-id="b2907-125">Microsoft.Azure.Commands.Kusto.Models.PSKustoClusterNameAvailability</span></span>

## <span data-ttu-id="b2907-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b2907-126">NOTES</span></span>

## <span data-ttu-id="b2907-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b2907-127">RELATED LINKS</span></span>
