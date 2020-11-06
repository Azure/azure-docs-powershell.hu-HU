---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 385947ead1039103933cb7e752dc5dee768b388a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491499"
---
# <span data-ttu-id="c1420-101">Restore-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="c1420-101">Restore-AzsBackup</span></span>

## <span data-ttu-id="c1420-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c1420-102">SYNOPSIS</span></span>
<span data-ttu-id="c1420-103">Biztonsági másolat visszaállítása</span><span class="sxs-lookup"><span data-stu-id="c1420-103">Restore a backup.</span></span>

## <span data-ttu-id="c1420-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c1420-104">SYNTAX</span></span>

### <span data-ttu-id="c1420-105">Backups_Restore (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c1420-105">Backups_Restore (Default)</span></span>
```
Restore-AzsBackup [-ResourceGroupName <String>] -Name <String> [-Location <String>] [-AsJob] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1420-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1420-106">ResourceId</span></span>
```
Restore-AzsBackup -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1420-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c1420-107">DESCRIPTION</span></span>
<span data-ttu-id="c1420-108">Biztonsági másolat visszaállítása</span><span class="sxs-lookup"><span data-stu-id="c1420-108">Restore a backup.</span></span>

## <span data-ttu-id="c1420-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c1420-109">EXAMPLES</span></span>

### <span data-ttu-id="c1420-110">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c1420-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Restore-AzsBackup -Backup 4e90bd2f-c7ab-47a3-a3c7-908cddd1ad0e
```

<span data-ttu-id="c1420-111">Visszaállíthatja az Azure-halom biztonsági másolatát.</span><span class="sxs-lookup"><span data-stu-id="c1420-111">Restore from an Azure Stack backup.</span></span>

## <span data-ttu-id="c1420-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c1420-112">PARAMETERS</span></span>

### <span data-ttu-id="c1420-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c1420-113">-AsJob</span></span>
<span data-ttu-id="c1420-114">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="c1420-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="c1420-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c1420-115">-Force</span></span>
<span data-ttu-id="c1420-116">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c1420-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="c1420-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="c1420-117">-Location</span></span>
<span data-ttu-id="c1420-118">A biztonsági másolat helyének neve.</span><span class="sxs-lookup"><span data-stu-id="c1420-118">Name of location to backup.</span></span>

```yaml
Type: String
Parameter Sets: Backups_Restore
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1420-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c1420-119">-Name</span></span>
<span data-ttu-id="c1420-120">A biztonsági másolat neve.</span><span class="sxs-lookup"><span data-stu-id="c1420-120">Name of the backup.</span></span>

```yaml
Type: String
Parameter Sets: Backups_Restore
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1420-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1420-121">-ResourceGroupName</span></span>
<span data-ttu-id="c1420-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c1420-122">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: Backups_Restore
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1420-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1420-123">-ResourceId</span></span>
<span data-ttu-id="c1420-124">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="c1420-124">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1420-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c1420-125">-Confirm</span></span>
<span data-ttu-id="c1420-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c1420-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1420-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1420-127">-WhatIf</span></span>
<span data-ttu-id="c1420-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c1420-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1420-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c1420-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1420-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1420-130">CommonParameters</span></span>
<span data-ttu-id="c1420-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c1420-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1420-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1420-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1420-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1420-133">INPUTS</span></span>

## <span data-ttu-id="c1420-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1420-134">OUTPUTS</span></span>

## <span data-ttu-id="c1420-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c1420-135">NOTES</span></span>

## <span data-ttu-id="c1420-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c1420-136">RELATED LINKS</span></span>

