---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 70d8ded2b2954746a97d6144f33c043c27341da4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491192"
---
# <span data-ttu-id="ff5a3-101">New-AzsScaleUnitNodeObject</span><span class="sxs-lookup"><span data-stu-id="ff5a3-101">New-AzsScaleUnitNodeObject</span></span>

## <span data-ttu-id="ff5a3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ff5a3-102">SYNOPSIS</span></span>
<span data-ttu-id="ff5a3-103">Olyan bemeneti adatok, amelyek lehetővé teszik a méretarányos csomópont hozzáadását.</span><span class="sxs-lookup"><span data-stu-id="ff5a3-103">Input data that allows for adding a scale unit node.</span></span>

## <span data-ttu-id="ff5a3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ff5a3-104">SYNTAX</span></span>

```
New-AzsScaleUnitNodeObject [[-BMCIPv4Address] <String>] [[-ComputerName] <String>] [<CommonParameters>]
```

## <span data-ttu-id="ff5a3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ff5a3-105">DESCRIPTION</span></span>
<span data-ttu-id="ff5a3-106">Olyan bemeneti adatok, amelyek lehetővé teszik a méretarányos csomópont hozzáadását.</span><span class="sxs-lookup"><span data-stu-id="ff5a3-106">Input data that allows for adding a scale unit node.</span></span>

## <span data-ttu-id="ff5a3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ff5a3-107">EXAMPLES</span></span>

### <span data-ttu-id="ff5a3-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ff5a3-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsScaleUnitNodeObject -BMCIPv4Address 192.168.1.1 -ComputeName 'NodeName'
```

<span data-ttu-id="ff5a3-109">Új csomópont-objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="ff5a3-109">Create a new node object.</span></span>

## <span data-ttu-id="ff5a3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ff5a3-110">PARAMETERS</span></span>

### <span data-ttu-id="ff5a3-111">-BMCIPv4Address</span><span class="sxs-lookup"><span data-stu-id="ff5a3-111">-BMCIPv4Address</span></span>
<span data-ttu-id="ff5a3-112">A fizikai gép bmc-címe.</span><span class="sxs-lookup"><span data-stu-id="ff5a3-112">Bmc address of the physical machine.</span></span>

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

### <span data-ttu-id="ff5a3-113">-Számítógépnév</span><span class="sxs-lookup"><span data-stu-id="ff5a3-113">-ComputerName</span></span>
<span data-ttu-id="ff5a3-114">A fizikai gép számítógépnevét.</span><span class="sxs-lookup"><span data-stu-id="ff5a3-114">Computer name of the physical machine.</span></span>

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

### <span data-ttu-id="ff5a3-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff5a3-115">CommonParameters</span></span>
<span data-ttu-id="ff5a3-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ff5a3-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff5a3-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff5a3-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff5a3-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff5a3-118">INPUTS</span></span>

## <span data-ttu-id="ff5a3-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff5a3-119">OUTPUTS</span></span>

## <span data-ttu-id="ff5a3-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ff5a3-120">NOTES</span></span>

## <span data-ttu-id="ff5a3-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ff5a3-121">RELATED LINKS</span></span>

