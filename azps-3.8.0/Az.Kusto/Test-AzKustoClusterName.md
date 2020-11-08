---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustoclustername
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Test-AzKustoClusterName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Test-AzKustoClusterName.md
ms.openlocfilehash: c6b2f462ac66ab48b50e7555a3b5bf7c844aae3a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011115"
---
# <span data-ttu-id="ac9ca-101">Test-AzKustoClusterName</span><span class="sxs-lookup"><span data-stu-id="ac9ca-101">Test-AzKustoClusterName</span></span>

## <span data-ttu-id="ac9ca-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ac9ca-102">SYNOPSIS</span></span>
<span data-ttu-id="ac9ca-103">Ellenőrizze, hogy elérhető-e egy adott Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="ac9ca-103">Check if a given Kusto cluster name is available.</span></span>

## <span data-ttu-id="ac9ca-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ac9ca-104">SYNTAX</span></span>

```
Test-AzKustoClusterName -Location <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ac9ca-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ac9ca-105">DESCRIPTION</span></span>
<span data-ttu-id="ac9ca-106">Ellenőrizze, hogy elérhető-e egy adott Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="ac9ca-106">Check if a given Kusto cluster name is available.</span></span>

## <span data-ttu-id="ac9ca-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ac9ca-107">EXAMPLES</span></span>

### <span data-ttu-id="ac9ca-108">Példa 1 – annak a Kusto a elérhetőségét ellenőrzi, amely használatban van</span><span class="sxs-lookup"><span data-stu-id="ac9ca-108">Example 1 - Check the availability of a Kusto cluster name which is in use</span></span>

```
PS C:\> Test-AzKustoClusterName -Location 'Central US' -Name mykustocluster

NameAvailable       Name                        Message
-------------           ----                            -------
False                   mykustocluster      Name 'mykustocluster' with type Engine is already taken. Please specify a different name
```

<span data-ttu-id="ac9ca-109">A fenti parancs azt jeleníti meg, hogy a "mykustocluster" nevű Kusto-fürt létezik-e a "Közép-amerikai" régióban.</span><span class="sxs-lookup"><span data-stu-id="ac9ca-109">The above command returns whether or not a Kusto cluster named "mykustocluster" exists in the "Central US" region.</span></span>

### <span data-ttu-id="ac9ca-110">Példa 2 – annak ellenőrzése, hogy nincs-e használatban a Kusto-fürt elérhetősége</span><span class="sxs-lookup"><span data-stu-id="ac9ca-110">Example 2 - Check the availability of a Kusto cluster name which is not in use</span></span>

```
PS C:\> Test-AzKustoClusterName -Location 'Central US' -Name mykustocluster

NameAvailable       Name                        Message
-------------           ----                            -------
 True                   mykustocluster
```

<span data-ttu-id="ac9ca-111">A fenti parancs azt jeleníti meg, hogy a "mykustocluster" nevű Kusto-fürt létezik-e a "Közép-amerikai" régióban.</span><span class="sxs-lookup"><span data-stu-id="ac9ca-111">The above command returns whether or not a Kusto cluster named "mykustocluster" exists in the "Central US" region.</span></span>

## <span data-ttu-id="ac9ca-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ac9ca-112">PARAMETERS</span></span>

### <span data-ttu-id="ac9ca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac9ca-113">-DefaultProfile</span></span>
<span data-ttu-id="ac9ca-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ac9ca-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac9ca-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="ac9ca-115">-Location</span></span>
<span data-ttu-id="ac9ca-116">Az ellenőrzés helye.</span><span class="sxs-lookup"><span data-stu-id="ac9ca-116">The location where to check.</span></span>

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

### <span data-ttu-id="ac9ca-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ac9ca-117">-Name</span></span>
<span data-ttu-id="ac9ca-118">Egy adott fürt neve.</span><span class="sxs-lookup"><span data-stu-id="ac9ca-118">Name of a specific cluster.</span></span>

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

### <span data-ttu-id="ac9ca-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac9ca-119">CommonParameters</span></span>
<span data-ttu-id="ac9ca-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ac9ca-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac9ca-121">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac9ca-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac9ca-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac9ca-122">INPUTS</span></span>

### <span data-ttu-id="ac9ca-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="ac9ca-123">None</span></span>

## <span data-ttu-id="ac9ca-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac9ca-124">OUTPUTS</span></span>

### <span data-ttu-id="ac9ca-125">Microsoft. Azure. Command. Kusto. models. PSKustoClusterNameAvailability</span><span class="sxs-lookup"><span data-stu-id="ac9ca-125">Microsoft.Azure.Commands.Kusto.Models.PSKustoClusterNameAvailability</span></span>

## <span data-ttu-id="ac9ca-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ac9ca-126">NOTES</span></span>

## <span data-ttu-id="ac9ca-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ac9ca-127">RELATED LINKS</span></span>
