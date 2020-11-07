---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d38e4bd949a6118f55ce0096a8ca56d08137bb2a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93840120"
---
# <span data-ttu-id="bd3bc-101">Stop-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="bd3bc-101">Stop-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="bd3bc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bd3bc-102">SYNOPSIS</span></span>
<span data-ttu-id="bd3bc-103">Felügyelt áttelepítési feladat visszavonása</span><span class="sxs-lookup"><span data-stu-id="bd3bc-103">Cancel a managed disk migration job.</span></span>

## <span data-ttu-id="bd3bc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bd3bc-104">SYNTAX</span></span>

```
Stop-AzsDiskMigrationJob [[-Location] <String>] [[-Name] <String>] [<CommonParameters>]
```

## <span data-ttu-id="bd3bc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bd3bc-105">DESCRIPTION</span></span>
<span data-ttu-id="bd3bc-106">Áttelepítési feladat visszavonása</span><span class="sxs-lookup"><span data-stu-id="bd3bc-106">Cancel a disk migration job.</span></span>

## <span data-ttu-id="bd3bc-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bd3bc-107">EXAMPLES</span></span>

### <span data-ttu-id="bd3bc-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="bd3bc-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Stop-AzsDiskMigrationJob -Location local -MigrationId $migration.MigrationId
```

<span data-ttu-id="bd3bc-109">Felügyelt áttelepítési feladat visszavonása</span><span class="sxs-lookup"><span data-stu-id="bd3bc-109">Cancel a managed disk migration job.</span></span>

## <span data-ttu-id="bd3bc-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bd3bc-110">PARAMETERS</span></span>

### <span data-ttu-id="bd3bc-111">-Hely</span><span class="sxs-lookup"><span data-stu-id="bd3bc-111">-Location</span></span>
<span data-ttu-id="bd3bc-112">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="bd3bc-112">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd3bc-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bd3bc-113">-Name</span></span>
<span data-ttu-id="bd3bc-114">Az áttelepítési feladat GUID-neve.</span><span class="sxs-lookup"><span data-stu-id="bd3bc-114">The migration job guid name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: MigrationId

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd3bc-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd3bc-115">CommonParameters</span></span>
<span data-ttu-id="bd3bc-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bd3bc-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd3bc-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd3bc-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd3bc-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd3bc-118">INPUTS</span></span>

## <span data-ttu-id="bd3bc-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd3bc-119">OUTPUTS</span></span>

### <span data-ttu-id="bd3bc-120">Microsoft. AzureStack. Management. kiszámítás. admin. models. DiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="bd3bc-120">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="bd3bc-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bd3bc-121">NOTES</span></span>

## <span data-ttu-id="bd3bc-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bd3bc-122">RELATED LINKS</span></span>

