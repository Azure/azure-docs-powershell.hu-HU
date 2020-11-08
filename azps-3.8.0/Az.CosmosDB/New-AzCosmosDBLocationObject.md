---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdblocationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBLocationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBLocationObject.md
ms.openlocfilehash: 59fee5840ec279c7ed11b9b9d738561caf03ec66
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013646"
---
# <span data-ttu-id="fc43e-101">New-AzCosmosDBLocationObject</span><span class="sxs-lookup"><span data-stu-id="fc43e-101">New-AzCosmosDBLocationObject</span></span>

## <span data-ttu-id="fc43e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fc43e-102">SYNOPSIS</span></span>
<span data-ttu-id="fc43e-103">Hozzon létre egy új CosmosDB hely objektumot (PSLocation).</span><span class="sxs-lookup"><span data-stu-id="fc43e-103">Create a new CosmosDB Location Object(PSLocation).</span></span>

## <span data-ttu-id="fc43e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fc43e-104">SYNTAX</span></span>

```
New-AzCosmosDBLocationObject -LocationName <String> [-FailoverPriority <Int32>] [-IsZoneRedundant <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc43e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fc43e-105">DESCRIPTION</span></span>
<span data-ttu-id="fc43e-106">Hozzon létre egy új CosmosDB hely objektumot (PSLocation).</span><span class="sxs-lookup"><span data-stu-id="fc43e-106">Create a new CosmosDB Location Object(PSLocation).</span></span>

## <span data-ttu-id="fc43e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fc43e-107">EXAMPLES</span></span>

### <span data-ttu-id="fc43e-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fc43e-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBLocationObject -LocationName {locationName} -FailoverPriority 2 -IsZoneRedundant 0

LocationName     FailoverPriority IsZoneRedundant
------------     ---------------- ---------------
{locationName}                 2           False
```

## <span data-ttu-id="fc43e-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fc43e-109">PARAMETERS</span></span>

### <span data-ttu-id="fc43e-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc43e-110">-DefaultProfile</span></span>
<span data-ttu-id="fc43e-111">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fc43e-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc43e-112">-FailoverPriority</span><span class="sxs-lookup"><span data-stu-id="fc43e-112">-FailoverPriority</span></span>
<span data-ttu-id="fc43e-113">A hely feladatátvételi prioritása.</span><span class="sxs-lookup"><span data-stu-id="fc43e-113">Failover priority of the location.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc43e-114">-IsZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="fc43e-114">-IsZoneRedundant</span></span>
<span data-ttu-id="fc43e-115">Logikai érték, amely azt jelzi, hogy a régió AvailabilityZone-e.</span><span class="sxs-lookup"><span data-stu-id="fc43e-115">Boolean to indicate whether or not this region is an AvailabilityZone.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc43e-116">-LocationName</span><span class="sxs-lookup"><span data-stu-id="fc43e-116">-LocationName</span></span>
<span data-ttu-id="fc43e-117">A hely neve a karakterláncban.</span><span class="sxs-lookup"><span data-stu-id="fc43e-117">Name of the Location in string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc43e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc43e-118">CommonParameters</span></span>
<span data-ttu-id="fc43e-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fc43e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc43e-120">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fc43e-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc43e-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc43e-121">INPUTS</span></span>

### <span data-ttu-id="fc43e-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="fc43e-122">None</span></span>

## <span data-ttu-id="fc43e-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc43e-123">OUTPUTS</span></span>

### <span data-ttu-id="fc43e-124">Microsoft. Azure. Command. CosmosDB. models. PSLocation</span><span class="sxs-lookup"><span data-stu-id="fc43e-124">Microsoft.Azure.Commands.CosmosDB.Models.PSLocation</span></span>

## <span data-ttu-id="fc43e-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fc43e-125">NOTES</span></span>

## <span data-ttu-id="fc43e-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fc43e-126">RELATED LINKS</span></span>
