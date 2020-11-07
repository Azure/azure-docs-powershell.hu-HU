---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ee1a9ae5a4d5ef7545ee9a3e071fcc06475034f4
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840564"
---
# <span data-ttu-id="8606a-101">Stop-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="8606a-101">Stop-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="8606a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8606a-102">SYNOPSIS</span></span>
<span data-ttu-id="8606a-103">Felügyelt áttelepítési feladat visszavonása</span><span class="sxs-lookup"><span data-stu-id="8606a-103">Cancel a managed disk migration job.</span></span>

## <span data-ttu-id="8606a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8606a-104">SYNTAX</span></span>

```
Stop-AzsDiskMigrationJob [[-Location] <String>] [[-Name] <String>] [<CommonParameters>]
```

## <span data-ttu-id="8606a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8606a-105">DESCRIPTION</span></span>
<span data-ttu-id="8606a-106">Áttelepítési feladat visszavonása</span><span class="sxs-lookup"><span data-stu-id="8606a-106">Cancel a disk migration job.</span></span>

## <span data-ttu-id="8606a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8606a-107">EXAMPLES</span></span>

### <span data-ttu-id="8606a-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8606a-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Stop-AzsDiskMigrationJob -Location local -MigrationId $migration.MigrationId
```

<span data-ttu-id="8606a-109">Felügyelt áttelepítési feladat visszavonása</span><span class="sxs-lookup"><span data-stu-id="8606a-109">Cancel a managed disk migration job.</span></span>

## <span data-ttu-id="8606a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8606a-110">PARAMETERS</span></span>

### <span data-ttu-id="8606a-111">-Hely</span><span class="sxs-lookup"><span data-stu-id="8606a-111">-Location</span></span>
<span data-ttu-id="8606a-112">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="8606a-112">Location of the resource.</span></span>

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

### <span data-ttu-id="8606a-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8606a-113">-Name</span></span>
<span data-ttu-id="8606a-114">Az áttelepítési feladat GUID-neve.</span><span class="sxs-lookup"><span data-stu-id="8606a-114">The migration job guid name.</span></span>

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

### <span data-ttu-id="8606a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8606a-115">CommonParameters</span></span>
<span data-ttu-id="8606a-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8606a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8606a-117">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8606a-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8606a-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8606a-118">INPUTS</span></span>

## <span data-ttu-id="8606a-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8606a-119">OUTPUTS</span></span>

### <span data-ttu-id="8606a-120">Microsoft. AzureStack. Management. kiszámítás. admin. models. DiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="8606a-120">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="8606a-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8606a-121">NOTES</span></span>

## <span data-ttu-id="8606a-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8606a-122">RELATED LINKS</span></span>

