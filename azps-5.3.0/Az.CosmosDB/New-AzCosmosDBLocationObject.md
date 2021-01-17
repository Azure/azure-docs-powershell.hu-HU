---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdblocationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBLocationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBLocationObject.md
ms.openlocfilehash: 59fee5840ec279c7ed11b9b9d738561caf03ec66
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477445"
---
# <span data-ttu-id="a2370-101">New-AzCosmosDBLocationObject</span><span class="sxs-lookup"><span data-stu-id="a2370-101">New-AzCosmosDBLocationObject</span></span>

## <span data-ttu-id="a2370-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2370-102">SYNOPSIS</span></span>
<span data-ttu-id="a2370-103">Hozzon létre egy új tárolóhelyobjektumot (PSLocation).</span><span class="sxs-lookup"><span data-stu-id="a2370-103">Create a new CosmosDB Location Object(PSLocation).</span></span>

## <span data-ttu-id="a2370-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a2370-104">SYNTAX</span></span>

```
New-AzCosmosDBLocationObject -LocationName <String> [-FailoverPriority <Int32>] [-IsZoneRedundant <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2370-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a2370-105">DESCRIPTION</span></span>
<span data-ttu-id="a2370-106">Hozzon létre egy új tárolóhelyobjektumot (PSLocation).</span><span class="sxs-lookup"><span data-stu-id="a2370-106">Create a new CosmosDB Location Object(PSLocation).</span></span>

## <span data-ttu-id="a2370-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a2370-107">EXAMPLES</span></span>

### <span data-ttu-id="a2370-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="a2370-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBLocationObject -LocationName {locationName} -FailoverPriority 2 -IsZoneRedundant 0

LocationName     FailoverPriority IsZoneRedundant
------------     ---------------- ---------------
{locationName}                 2           False
```

## <span data-ttu-id="a2370-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2370-109">PARAMETERS</span></span>

### <span data-ttu-id="a2370-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2370-110">-DefaultProfile</span></span>
<span data-ttu-id="a2370-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a2370-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2370-112">-FailoverPriority</span><span class="sxs-lookup"><span data-stu-id="a2370-112">-FailoverPriority</span></span>
<span data-ttu-id="a2370-113">A hely feladatátvételi prioritása.</span><span class="sxs-lookup"><span data-stu-id="a2370-113">Failover priority of the location.</span></span>

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

### <span data-ttu-id="a2370-114">-IsZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="a2370-114">-IsZoneRedundant</span></span>
<span data-ttu-id="a2370-115">Logikai érték, amely azt jelzi, hogy ez a régió rendelkezésre állási zóna-e.</span><span class="sxs-lookup"><span data-stu-id="a2370-115">Boolean to indicate whether or not this region is an AvailabilityZone.</span></span>

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

### <span data-ttu-id="a2370-116">-LocationName</span><span class="sxs-lookup"><span data-stu-id="a2370-116">-LocationName</span></span>
<span data-ttu-id="a2370-117">A hely neve a karakterláncban.</span><span class="sxs-lookup"><span data-stu-id="a2370-117">Name of the Location in string.</span></span>

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

### <span data-ttu-id="a2370-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2370-118">CommonParameters</span></span>
<span data-ttu-id="a2370-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2370-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2370-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a2370-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2370-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a2370-121">INPUTS</span></span>

### <span data-ttu-id="a2370-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="a2370-122">None</span></span>

## <span data-ttu-id="a2370-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2370-123">OUTPUTS</span></span>

### <span data-ttu-id="a2370-124">Microsoft.Azure.Commands.CossDB.Models.PSLocation</span><span class="sxs-lookup"><span data-stu-id="a2370-124">Microsoft.Azure.Commands.CosmosDB.Models.PSLocation</span></span>

## <span data-ttu-id="a2370-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a2370-125">NOTES</span></span>

## <span data-ttu-id="a2370-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a2370-126">RELATED LINKS</span></span>
