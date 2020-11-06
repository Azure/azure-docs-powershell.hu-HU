---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b30ae24d384667aa8d399f03c76ab886b2faa1c9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491051"
---
# <span data-ttu-id="50081-101">New-DataDiskObject</span><span class="sxs-lookup"><span data-stu-id="50081-101">New-DataDiskObject</span></span>

## <span data-ttu-id="50081-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="50081-102">SYNOPSIS</span></span>
<span data-ttu-id="50081-103">Létrehoz egy adatlemezt, amely egy új virtuális gép platformjának létrehozásakor használatos.</span><span class="sxs-lookup"><span data-stu-id="50081-103">Creates a data disk which is used to create a new virtual machine platform image.</span></span>

## <span data-ttu-id="50081-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="50081-104">SYNTAX</span></span>

```
New-DataDiskObject [[-Lun] <Int32>] [[-Uri] <String>] [<CommonParameters>]
```

## <span data-ttu-id="50081-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="50081-105">DESCRIPTION</span></span>
<span data-ttu-id="50081-106">Létrehoz egy olyan objektumot, amely információkat tárol egy adatlemezről.</span><span class="sxs-lookup"><span data-stu-id="50081-106">Creates an object holding information about a data disk.</span></span>

## <span data-ttu-id="50081-107">Példák</span><span class="sxs-lookup"><span data-stu-id="50081-107">EXAMPLES</span></span>

### <span data-ttu-id="50081-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="50081-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-DataDiskObject -Lun 5 -URI test.blob.windows.net/disks/datadisk5.vhd
```

<span data-ttu-id="50081-109">Új Data Disk objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="50081-109">Create a new data disk object.</span></span>

## <span data-ttu-id="50081-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="50081-110">PARAMETERS</span></span>

### <span data-ttu-id="50081-111">-LUN</span><span class="sxs-lookup"><span data-stu-id="50081-111">-Lun</span></span>
<span data-ttu-id="50081-112">Logikai egység száma</span><span class="sxs-lookup"><span data-stu-id="50081-112">Logical unit number.</span></span>

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

### <span data-ttu-id="50081-113">-URI</span><span class="sxs-lookup"><span data-stu-id="50081-113">-Uri</span></span>
<span data-ttu-id="50081-114">A sablonfájl helye.</span><span class="sxs-lookup"><span data-stu-id="50081-114">Location of the disk template.</span></span>

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

### <span data-ttu-id="50081-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50081-115">CommonParameters</span></span>
<span data-ttu-id="50081-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="50081-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50081-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50081-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50081-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="50081-118">INPUTS</span></span>

## <span data-ttu-id="50081-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="50081-119">OUTPUTS</span></span>

## <span data-ttu-id="50081-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="50081-120">NOTES</span></span>

## <span data-ttu-id="50081-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="50081-121">RELATED LINKS</span></span>

