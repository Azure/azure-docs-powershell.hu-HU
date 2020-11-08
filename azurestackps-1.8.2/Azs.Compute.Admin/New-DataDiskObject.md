---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b37d41ae2ec772cc755436bc01c3c4009c9c30f5
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016787"
---
# <span data-ttu-id="8f4e1-101">New-DataDiskObject</span><span class="sxs-lookup"><span data-stu-id="8f4e1-101">New-DataDiskObject</span></span>

## <span data-ttu-id="8f4e1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8f4e1-102">SYNOPSIS</span></span>
<span data-ttu-id="8f4e1-103">Létrehoz egy adatlemezt, amely egy új virtuális gép platformjának létrehozásakor használatos.</span><span class="sxs-lookup"><span data-stu-id="8f4e1-103">Creates a data disk which is used to create a new virtual machine platform image.</span></span>

## <span data-ttu-id="8f4e1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8f4e1-104">SYNTAX</span></span>

```
New-DataDiskObject [[-Lun] <Int32>] [[-Uri] <String>] [<CommonParameters>]
```

## <span data-ttu-id="8f4e1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8f4e1-105">DESCRIPTION</span></span>
<span data-ttu-id="8f4e1-106">Létrehoz egy olyan objektumot, amely információkat tárol egy adatlemezről.</span><span class="sxs-lookup"><span data-stu-id="8f4e1-106">Creates an object holding information about a data disk.</span></span>

## <span data-ttu-id="8f4e1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8f4e1-107">EXAMPLES</span></span>

### <span data-ttu-id="8f4e1-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8f4e1-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-DataDiskObject -Lun 5 -URI test.blob.windows.net/disks/datadisk5.vhd
```

<span data-ttu-id="8f4e1-109">Új Data Disk objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="8f4e1-109">Create a new data disk object.</span></span>

## <span data-ttu-id="8f4e1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8f4e1-110">PARAMETERS</span></span>

### <span data-ttu-id="8f4e1-111">-LUN</span><span class="sxs-lookup"><span data-stu-id="8f4e1-111">-Lun</span></span>
<span data-ttu-id="8f4e1-112">Logikai egység száma</span><span class="sxs-lookup"><span data-stu-id="8f4e1-112">Logical unit number.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f4e1-113">-URI</span><span class="sxs-lookup"><span data-stu-id="8f4e1-113">-Uri</span></span>
<span data-ttu-id="8f4e1-114">A sablonfájl helye.</span><span class="sxs-lookup"><span data-stu-id="8f4e1-114">Location of the disk template.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f4e1-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f4e1-115">CommonParameters</span></span>
<span data-ttu-id="8f4e1-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8f4e1-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f4e1-117">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f4e1-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f4e1-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f4e1-118">INPUTS</span></span>

## <span data-ttu-id="8f4e1-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f4e1-119">OUTPUTS</span></span>

## <span data-ttu-id="8f4e1-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8f4e1-120">NOTES</span></span>

## <span data-ttu-id="8f4e1-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8f4e1-121">RELATED LINKS</span></span>

