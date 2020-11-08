---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ee1a9ae5a4d5ef7545ee9a3e071fcc06475034f4
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016779"
---
# <span data-ttu-id="d0b57-101">Stop-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="d0b57-101">Stop-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="d0b57-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d0b57-102">SYNOPSIS</span></span>
<span data-ttu-id="d0b57-103">Felügyelt áttelepítési feladat visszavonása</span><span class="sxs-lookup"><span data-stu-id="d0b57-103">Cancel a managed disk migration job.</span></span>

## <span data-ttu-id="d0b57-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d0b57-104">SYNTAX</span></span>

```
Stop-AzsDiskMigrationJob [[-Location] <String>] [[-Name] <String>] [<CommonParameters>]
```

## <span data-ttu-id="d0b57-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d0b57-105">DESCRIPTION</span></span>
<span data-ttu-id="d0b57-106">Áttelepítési feladat visszavonása</span><span class="sxs-lookup"><span data-stu-id="d0b57-106">Cancel a disk migration job.</span></span>

## <span data-ttu-id="d0b57-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d0b57-107">EXAMPLES</span></span>

### <span data-ttu-id="d0b57-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d0b57-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Stop-AzsDiskMigrationJob -Location local -MigrationId $migration.MigrationId
```

<span data-ttu-id="d0b57-109">Felügyelt áttelepítési feladat visszavonása</span><span class="sxs-lookup"><span data-stu-id="d0b57-109">Cancel a managed disk migration job.</span></span>

## <span data-ttu-id="d0b57-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d0b57-110">PARAMETERS</span></span>

### <span data-ttu-id="d0b57-111">-Hely</span><span class="sxs-lookup"><span data-stu-id="d0b57-111">-Location</span></span>
<span data-ttu-id="d0b57-112">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="d0b57-112">Location of the resource.</span></span>

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

### <span data-ttu-id="d0b57-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d0b57-113">-Name</span></span>
<span data-ttu-id="d0b57-114">Az áttelepítési feladat GUID-neve.</span><span class="sxs-lookup"><span data-stu-id="d0b57-114">The migration job guid name.</span></span>

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

### <span data-ttu-id="d0b57-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0b57-115">CommonParameters</span></span>
<span data-ttu-id="d0b57-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d0b57-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0b57-117">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0b57-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0b57-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d0b57-118">INPUTS</span></span>

## <span data-ttu-id="d0b57-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d0b57-119">OUTPUTS</span></span>

### <span data-ttu-id="d0b57-120">Microsoft. AzureStack. Management. kiszámítás. admin. models. DiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="d0b57-120">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="d0b57-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d0b57-121">NOTES</span></span>

## <span data-ttu-id="d0b57-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d0b57-122">RELATED LINKS</span></span>

