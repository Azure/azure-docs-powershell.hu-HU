---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4847310f65a0b652d15321cd49583212ef5844d8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839917"
---
# <span data-ttu-id="9ab4f-101">Get-AzsStorageContainer</span><span class="sxs-lookup"><span data-stu-id="9ab4f-101">Get-AzsStorageContainer</span></span>

## <span data-ttu-id="9ab4f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9ab4f-102">SYNOPSIS</span></span>
<span data-ttu-id="9ab4f-103">Azoknak a tárolóknak a listáját adja eredményül, amelyek áttelepíthetők a megadott megosztásban.</span><span class="sxs-lookup"><span data-stu-id="9ab4f-103">Returns the list of containers which can be migrated in the specified share.</span></span>

## <span data-ttu-id="9ab4f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9ab4f-104">SYNTAX</span></span>

```
Get-AzsStorageContainer [-FarmName] <String> [-ShareName] <String> [[-ResourceGroupName] <String>]
 [[-MaxCount] <Int32>] [[-StartIndex] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="9ab4f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9ab4f-105">DESCRIPTION</span></span>
<span data-ttu-id="9ab4f-106">Azoknak a tárolóknak a listáját adja eredményül, amelyek áttelepíthetők a megadott megosztásban.</span><span class="sxs-lookup"><span data-stu-id="9ab4f-106">Returns the list of containers which can be migrated in the specified share.</span></span>

## <span data-ttu-id="9ab4f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9ab4f-107">EXAMPLES</span></span>

### <span data-ttu-id="9ab4f-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="9ab4f-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageContainer -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -ShareName "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

<span data-ttu-id="9ab4f-109">A megadott megosztásban áttelepíthető tárolók listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="9ab4f-109">Get a list of containers which can be migrated in the specified share.</span></span>

## <span data-ttu-id="9ab4f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9ab4f-110">PARAMETERS</span></span>

### <span data-ttu-id="9ab4f-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="9ab4f-111">-FarmName</span></span>
<span data-ttu-id="9ab4f-112">Mezőgazdasági azonosító.</span><span class="sxs-lookup"><span data-stu-id="9ab4f-112">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ab4f-113">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="9ab4f-113">-MaxCount</span></span>
<span data-ttu-id="9ab4f-114">A tárolók maximális száma.</span><span class="sxs-lookup"><span data-stu-id="9ab4f-114">The max count of containers.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: 100000000
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ab4f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ab4f-115">-ResourceGroupName</span></span>
<span data-ttu-id="9ab4f-116">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="9ab4f-116">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ab4f-117">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="9ab4f-117">-ShareName</span></span>
<span data-ttu-id="9ab4f-118">Megoszthatja a tároló tárolóját tároló nevet.</span><span class="sxs-lookup"><span data-stu-id="9ab4f-118">Share name which holds the storage containers.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ab4f-119">-StartIndex</span><span class="sxs-lookup"><span data-stu-id="9ab4f-119">-StartIndex</span></span>
<span data-ttu-id="9ab4f-120">A tárolók beszerzésének kezdő indexe.</span><span class="sxs-lookup"><span data-stu-id="9ab4f-120">The start index of get containers.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ab4f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ab4f-121">CommonParameters</span></span>
<span data-ttu-id="9ab4f-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9ab4f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ab4f-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ab4f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ab4f-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ab4f-124">INPUTS</span></span>

## <span data-ttu-id="9ab4f-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ab4f-125">OUTPUTS</span></span>

## <span data-ttu-id="9ab4f-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9ab4f-126">NOTES</span></span>

## <span data-ttu-id="9ab4f-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9ab4f-127">RELATED LINKS</span></span>

