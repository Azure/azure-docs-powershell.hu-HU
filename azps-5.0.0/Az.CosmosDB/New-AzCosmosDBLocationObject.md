---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdblocationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBLocationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBLocationObject.md
ms.openlocfilehash: 59fee5840ec279c7ed11b9b9d738561caf03ec66
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299297"
---
# <span data-ttu-id="c6d0b-101">New-AzCosmosDBLocationObject</span><span class="sxs-lookup"><span data-stu-id="c6d0b-101">New-AzCosmosDBLocationObject</span></span>

## <span data-ttu-id="c6d0b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c6d0b-102">SYNOPSIS</span></span>
<span data-ttu-id="c6d0b-103">Hozzon létre egy új CosmosDB hely objektumot (PSLocation).</span><span class="sxs-lookup"><span data-stu-id="c6d0b-103">Create a new CosmosDB Location Object(PSLocation).</span></span>

## <span data-ttu-id="c6d0b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c6d0b-104">SYNTAX</span></span>

```
New-AzCosmosDBLocationObject -LocationName <String> [-FailoverPriority <Int32>] [-IsZoneRedundant <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6d0b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c6d0b-105">DESCRIPTION</span></span>
<span data-ttu-id="c6d0b-106">Hozzon létre egy új CosmosDB hely objektumot (PSLocation).</span><span class="sxs-lookup"><span data-stu-id="c6d0b-106">Create a new CosmosDB Location Object(PSLocation).</span></span>

## <span data-ttu-id="c6d0b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c6d0b-107">EXAMPLES</span></span>

### <span data-ttu-id="c6d0b-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c6d0b-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBLocationObject -LocationName {locationName} -FailoverPriority 2 -IsZoneRedundant 0

LocationName     FailoverPriority IsZoneRedundant
------------     ---------------- ---------------
{locationName}                 2           False
```

## <span data-ttu-id="c6d0b-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c6d0b-109">PARAMETERS</span></span>

### <span data-ttu-id="c6d0b-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6d0b-110">-DefaultProfile</span></span>
<span data-ttu-id="c6d0b-111">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c6d0b-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6d0b-112">-FailoverPriority</span><span class="sxs-lookup"><span data-stu-id="c6d0b-112">-FailoverPriority</span></span>
<span data-ttu-id="c6d0b-113">A hely feladatátvételi prioritása.</span><span class="sxs-lookup"><span data-stu-id="c6d0b-113">Failover priority of the location.</span></span>

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

### <span data-ttu-id="c6d0b-114">-IsZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="c6d0b-114">-IsZoneRedundant</span></span>
<span data-ttu-id="c6d0b-115">Logikai érték, amely azt jelzi, hogy a régió AvailabilityZone-e.</span><span class="sxs-lookup"><span data-stu-id="c6d0b-115">Boolean to indicate whether or not this region is an AvailabilityZone.</span></span>

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

### <span data-ttu-id="c6d0b-116">-LocationName</span><span class="sxs-lookup"><span data-stu-id="c6d0b-116">-LocationName</span></span>
<span data-ttu-id="c6d0b-117">A hely neve a karakterláncban.</span><span class="sxs-lookup"><span data-stu-id="c6d0b-117">Name of the Location in string.</span></span>

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

### <span data-ttu-id="c6d0b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6d0b-118">CommonParameters</span></span>
<span data-ttu-id="c6d0b-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c6d0b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6d0b-120">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c6d0b-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6d0b-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6d0b-121">INPUTS</span></span>

### <span data-ttu-id="c6d0b-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="c6d0b-122">None</span></span>

## <span data-ttu-id="c6d0b-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6d0b-123">OUTPUTS</span></span>

### <span data-ttu-id="c6d0b-124">Microsoft. Azure. Command. CosmosDB. models. PSLocation</span><span class="sxs-lookup"><span data-stu-id="c6d0b-124">Microsoft.Azure.Commands.CosmosDB.Models.PSLocation</span></span>

## <span data-ttu-id="c6d0b-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c6d0b-125">NOTES</span></span>

## <span data-ttu-id="c6d0b-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c6d0b-126">RELATED LINKS</span></span>
