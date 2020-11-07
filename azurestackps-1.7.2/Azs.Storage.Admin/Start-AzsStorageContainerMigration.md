---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 54016a200b4304c7e37777202a8450fc9ad10e1e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839865"
---
# <span data-ttu-id="6a9c6-101">Start-AzsStorageContainerMigration</span><span class="sxs-lookup"><span data-stu-id="6a9c6-101">Start-AzsStorageContainerMigration</span></span>

## <span data-ttu-id="6a9c6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6a9c6-102">SYNOPSIS</span></span>
<span data-ttu-id="6a9c6-103">Tároló áttelepítési feladatot indít a tárolóknak a megadott célhelyre való áttelepítéséhez.</span><span class="sxs-lookup"><span data-stu-id="6a9c6-103">Starts a container migration job to migrate containers to the specified destination share.</span></span>

## <span data-ttu-id="6a9c6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6a9c6-104">SYNTAX</span></span>

```
Start-AzsStorageContainerMigration [-StorageAccountName] <String> [-Name] <String> [-ShareName] <String>
 [[-ResourceGroupName] <String>] [-FarmName] <String> [-DestinationShareUncPath] <String> [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a9c6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6a9c6-105">DESCRIPTION</span></span>
<span data-ttu-id="6a9c6-106">Tároló áttelepítési feladatot indít a tárolóknak a megadott célhelyre való áttelepítéséhez.</span><span class="sxs-lookup"><span data-stu-id="6a9c6-106">Starts a container migration job to migrate containers to the specified destination share.</span></span>

## <span data-ttu-id="6a9c6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6a9c6-107">EXAMPLES</span></span>

### <span data-ttu-id="6a9c6-108">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6a9c6-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsStorageContainerMigration -StorageAccountName "accountTest" -Name "containerTest" -ShareName "shareTest" -FarmName "10e8d576-d73c-454c-a40a-aee31a77a5f0" -DestinationShareUncPath "\\***.***.***.***\C$\Test"
```

<span data-ttu-id="6a9c6-109">Tároló-áttelepítés indítása.</span><span class="sxs-lookup"><span data-stu-id="6a9c6-109">Starts a container migration.</span></span>

## <span data-ttu-id="6a9c6-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6a9c6-110">PARAMETERS</span></span>

### <span data-ttu-id="6a9c6-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6a9c6-111">-AsJob</span></span>
<span data-ttu-id="6a9c6-112">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="6a9c6-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="6a9c6-113">-DestinationShareUncPath</span><span class="sxs-lookup"><span data-stu-id="6a9c6-113">-DestinationShareUncPath</span></span>
<span data-ttu-id="6a9c6-114">Az áttelepítés célhelyének UNC-elérési útja.</span><span class="sxs-lookup"><span data-stu-id="6a9c6-114">The UNC path of the destination share for migration.</span></span>

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

### <span data-ttu-id="6a9c6-115">-FarmName</span><span class="sxs-lookup"><span data-stu-id="6a9c6-115">-FarmName</span></span>
<span data-ttu-id="6a9c6-116">Mezőgazdasági azonosító.</span><span class="sxs-lookup"><span data-stu-id="6a9c6-116">Farm Id.</span></span>

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

### <span data-ttu-id="6a9c6-117">-Force</span><span class="sxs-lookup"><span data-stu-id="6a9c6-117">-Force</span></span>
<span data-ttu-id="6a9c6-118">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6a9c6-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6a9c6-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6a9c6-119">-Name</span></span>
<span data-ttu-id="6a9c6-120">Az áttelepítendő tároló neve.</span><span class="sxs-lookup"><span data-stu-id="6a9c6-120">The name of the container to be migrated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a9c6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a9c6-121">-ResourceGroupName</span></span>
<span data-ttu-id="6a9c6-122">Az erőforráscsoport neve, amelyben a tárolási erőforrás-szolgáltató be volt jegyezve.</span><span class="sxs-lookup"><span data-stu-id="6a9c6-122">The resource group name in which the storage resource provider was registered under.</span></span>

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

### <span data-ttu-id="6a9c6-123">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="6a9c6-123">-ShareName</span></span>
<span data-ttu-id="6a9c6-124">Az áttelepítéshez megadott tárolót tartalmazó megosztás neve.</span><span class="sxs-lookup"><span data-stu-id="6a9c6-124">Name of the share containing the container specified for migration.</span></span>

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

### <span data-ttu-id="6a9c6-125">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6a9c6-125">-StorageAccountName</span></span>
<span data-ttu-id="6a9c6-126">A tároló által megtalált tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="6a9c6-126">The name of storage account where the container locates.</span></span>

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

### <span data-ttu-id="6a9c6-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6a9c6-127">-Confirm</span></span>
<span data-ttu-id="6a9c6-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6a9c6-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a9c6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a9c6-129">-WhatIf</span></span>
<span data-ttu-id="6a9c6-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6a9c6-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a9c6-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6a9c6-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a9c6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a9c6-132">CommonParameters</span></span>
<span data-ttu-id="6a9c6-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6a9c6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a9c6-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a9c6-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a9c6-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a9c6-135">INPUTS</span></span>

## <span data-ttu-id="6a9c6-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a9c6-136">OUTPUTS</span></span>

## <span data-ttu-id="6a9c6-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6a9c6-137">NOTES</span></span>

## <span data-ttu-id="6a9c6-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6a9c6-138">RELATED LINKS</span></span>

