---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: af9c5d2c5ebb547a6e09d2e4f4302ed2da470a39
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840601"
---
# <span data-ttu-id="9404e-101">Start-AzsStorageContainerMigration</span><span class="sxs-lookup"><span data-stu-id="9404e-101">Start-AzsStorageContainerMigration</span></span>

## <span data-ttu-id="9404e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9404e-102">SYNOPSIS</span></span>
<span data-ttu-id="9404e-103">Tároló áttelepítési feladatot indít a tárolóknak a megadott célhelyre való áttelepítéséhez.</span><span class="sxs-lookup"><span data-stu-id="9404e-103">Starts a container migration job to migrate containers to the specified destination share.</span></span>

## <span data-ttu-id="9404e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9404e-104">SYNTAX</span></span>

```
Start-AzsStorageContainerMigration [-StorageAccountName] <String> [-ContainerName] <String>
 [-ShareName] <String> [[-ResourceGroupName] <String>] [-FarmName] <String> [-DestinationShareUncPath] <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9404e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9404e-105">DESCRIPTION</span></span>
<span data-ttu-id="9404e-106">Tároló áttelepítési feladatot indít a tárolóknak a megadott célhelyre való áttelepítéséhez.</span><span class="sxs-lookup"><span data-stu-id="9404e-106">Starts a container migration job to migrate containers to the specified destination share.</span></span>

## <span data-ttu-id="9404e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9404e-107">EXAMPLES</span></span>

### <span data-ttu-id="9404e-108">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="9404e-108">EXAMPLE 1</span></span>
```
Start-AzsStorageContainerMigration -StorageAccountName "accountTest" -ContainerName "containerTest" -ShareName "shareTest" -FarmName "10e8d576-d73c-454c-a40a-aee31a77a5f0" -DestinationShareUncPath "\\***.***.***.***\C$\Test"
```

<span data-ttu-id="9404e-109">Tároló-áttelepítés indítása.</span><span class="sxs-lookup"><span data-stu-id="9404e-109">Starts a container migration.</span></span>

## <span data-ttu-id="9404e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9404e-110">PARAMETERS</span></span>

### <span data-ttu-id="9404e-111">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9404e-111">-StorageAccountName</span></span>
<span data-ttu-id="9404e-112">A tároló által megtalált tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="9404e-112">The name of storage account where the container locates.</span></span>

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

### <span data-ttu-id="9404e-113">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="9404e-113">-ContainerName</span></span>
<span data-ttu-id="9404e-114">Az áttelepítendő tároló neve.</span><span class="sxs-lookup"><span data-stu-id="9404e-114">The name of the container to be migrated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9404e-115">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="9404e-115">-ShareName</span></span>
<span data-ttu-id="9404e-116">Az áttelepítéshez megadott tárolót tartalmazó megosztás neve.</span><span class="sxs-lookup"><span data-stu-id="9404e-116">Name of the share containing the container specified for migration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9404e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9404e-117">-ResourceGroupName</span></span>
<span data-ttu-id="9404e-118">Az erőforráscsoport neve, amelyben a tárolási erőforrás-szolgáltató be volt jegyezve.</span><span class="sxs-lookup"><span data-stu-id="9404e-118">The resource group name in which the storage resource provider was registered under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9404e-119">-FarmName</span><span class="sxs-lookup"><span data-stu-id="9404e-119">-FarmName</span></span>
<span data-ttu-id="9404e-120">Mezőgazdasági azonosító.</span><span class="sxs-lookup"><span data-stu-id="9404e-120">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9404e-121">-DestinationShareUncPath</span><span class="sxs-lookup"><span data-stu-id="9404e-121">-DestinationShareUncPath</span></span>
<span data-ttu-id="9404e-122">Az áttelepítés célhelyének UNC-elérési útja.</span><span class="sxs-lookup"><span data-stu-id="9404e-122">The UNC path of the destination share for migration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9404e-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9404e-123">-AsJob</span></span>
<span data-ttu-id="9404e-124">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="9404e-124">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9404e-125">-Force</span><span class="sxs-lookup"><span data-stu-id="9404e-125">-Force</span></span>
<span data-ttu-id="9404e-126">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9404e-126">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9404e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9404e-127">-WhatIf</span></span>
<span data-ttu-id="9404e-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9404e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9404e-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9404e-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9404e-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9404e-130">-Confirm</span></span>
<span data-ttu-id="9404e-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9404e-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9404e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9404e-132">CommonParameters</span></span>
<span data-ttu-id="9404e-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9404e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9404e-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9404e-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9404e-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9404e-135">INPUTS</span></span>

## <span data-ttu-id="9404e-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9404e-136">OUTPUTS</span></span>

## <span data-ttu-id="9404e-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9404e-137">NOTES</span></span>

## <span data-ttu-id="9404e-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9404e-138">RELATED LINKS</span></span>
