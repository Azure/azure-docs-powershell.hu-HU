---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bdfb3714bbabcacd2805dc4198e2cfffde3f0e8d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490748"
---
# <span data-ttu-id="ceccd-101">New-AzsDataDiskObject</span><span class="sxs-lookup"><span data-stu-id="ceccd-101">New-AzsDataDiskObject</span></span>

## <span data-ttu-id="ceccd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ceccd-102">SYNOPSIS</span></span>
<span data-ttu-id="ceccd-103">Létrehoz egy adatlemezt, amely egy új virtuális gép platformjának létrehozásakor használatos.</span><span class="sxs-lookup"><span data-stu-id="ceccd-103">Creates a data disk which is used to create a new virtual machine platform image.</span></span>

## <span data-ttu-id="ceccd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ceccd-104">SYNTAX</span></span>

```
New-AzsDataDiskObject [[-Lun] <Int32>] [[-Uri] <String>] [<CommonParameters>]
```

## <span data-ttu-id="ceccd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ceccd-105">DESCRIPTION</span></span>
<span data-ttu-id="ceccd-106">Létrehoz egy olyan objektumot, amely információkat tárol egy adatlemezről.</span><span class="sxs-lookup"><span data-stu-id="ceccd-106">Creates an object holding information about a data disk.</span></span>

## <span data-ttu-id="ceccd-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ceccd-107">EXAMPLES</span></span>

### <span data-ttu-id="ceccd-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ceccd-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsDataDiskObject -Lun 5 -URI test.blob.windows.net/disks/datadisk5.vhd
```

<span data-ttu-id="ceccd-109">Új Data Disk objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="ceccd-109">Create a new data disk object.</span></span>

## <span data-ttu-id="ceccd-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ceccd-110">PARAMETERS</span></span>

### <span data-ttu-id="ceccd-111">-LUN</span><span class="sxs-lookup"><span data-stu-id="ceccd-111">-Lun</span></span>
<span data-ttu-id="ceccd-112">Logikai egység száma</span><span class="sxs-lookup"><span data-stu-id="ceccd-112">Logical unit number.</span></span>

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

### <span data-ttu-id="ceccd-113">-URI</span><span class="sxs-lookup"><span data-stu-id="ceccd-113">-Uri</span></span>
<span data-ttu-id="ceccd-114">A sablonfájl helye.</span><span class="sxs-lookup"><span data-stu-id="ceccd-114">Location of the disk template.</span></span>

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

### <span data-ttu-id="ceccd-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceccd-115">CommonParameters</span></span>
<span data-ttu-id="ceccd-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ceccd-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceccd-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ceccd-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceccd-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ceccd-118">INPUTS</span></span>

## <span data-ttu-id="ceccd-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ceccd-119">OUTPUTS</span></span>

## <span data-ttu-id="ceccd-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ceccd-120">NOTES</span></span>

## <span data-ttu-id="ceccd-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ceccd-121">RELATED LINKS</span></span>

