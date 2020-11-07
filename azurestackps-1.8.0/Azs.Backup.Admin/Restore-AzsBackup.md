---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 573a47b3684020817130e1d41c764abef717de0a
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93840386"
---
# <span data-ttu-id="1b6c5-101">Restore-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="1b6c5-101">Restore-AzsBackup</span></span>

## <span data-ttu-id="1b6c5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1b6c5-102">SYNOPSIS</span></span>
<span data-ttu-id="1b6c5-103">Biztonsági másolat visszaállítása</span><span class="sxs-lookup"><span data-stu-id="1b6c5-103">Restore a backup.</span></span>

## <span data-ttu-id="1b6c5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1b6c5-104">SYNTAX</span></span>

### <span data-ttu-id="1b6c5-105">Backups_Restore (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1b6c5-105">Backups_Restore (Default)</span></span>
```
Restore-AzsBackup [-ResourceGroupName <String>] -Name <String> [-Location <String>] [-AsJob] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b6c5-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="1b6c5-106">ResourceId</span></span>
```
Restore-AzsBackup -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b6c5-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="1b6c5-107">DESCRIPTION</span></span>
<span data-ttu-id="1b6c5-108">Biztonsági másolat visszaállítása</span><span class="sxs-lookup"><span data-stu-id="1b6c5-108">Restore a backup.</span></span>

## <span data-ttu-id="1b6c5-109">Példák</span><span class="sxs-lookup"><span data-stu-id="1b6c5-109">EXAMPLES</span></span>

### <span data-ttu-id="1b6c5-110">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1b6c5-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Restore-AzsBackup -Backup 4e90bd2f-c7ab-47a3-a3c7-908cddd1ad0e
```

<span data-ttu-id="1b6c5-111">Visszaállíthatja az Azure-halom biztonsági másolatát.</span><span class="sxs-lookup"><span data-stu-id="1b6c5-111">Restore from an Azure Stack backup.</span></span>

## <span data-ttu-id="1b6c5-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1b6c5-112">PARAMETERS</span></span>

### <span data-ttu-id="1b6c5-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1b6c5-113">-AsJob</span></span>
<span data-ttu-id="1b6c5-114">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="1b6c5-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="1b6c5-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1b6c5-115">-Force</span></span>
<span data-ttu-id="1b6c5-116">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1b6c5-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="1b6c5-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="1b6c5-117">-Location</span></span>
<span data-ttu-id="1b6c5-118">A biztonsági másolat helyének neve.</span><span class="sxs-lookup"><span data-stu-id="1b6c5-118">Name of location to backup.</span></span>

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

### <span data-ttu-id="1b6c5-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1b6c5-119">-Name</span></span>
<span data-ttu-id="1b6c5-120">A biztonsági másolat neve.</span><span class="sxs-lookup"><span data-stu-id="1b6c5-120">Name of the backup.</span></span>

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

### <span data-ttu-id="1b6c5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b6c5-121">-ResourceGroupName</span></span>
<span data-ttu-id="1b6c5-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1b6c5-122">Name of the resource group.</span></span>

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

### <span data-ttu-id="1b6c5-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1b6c5-123">-ResourceId</span></span>
<span data-ttu-id="1b6c5-124">{{Fill ResourceId Description}}</span><span class="sxs-lookup"><span data-stu-id="1b6c5-124">{{Fill ResourceId Description}}</span></span>

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

### <span data-ttu-id="1b6c5-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1b6c5-125">-Confirm</span></span>
<span data-ttu-id="1b6c5-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1b6c5-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b6c5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b6c5-127">-WhatIf</span></span>
<span data-ttu-id="1b6c5-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1b6c5-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b6c5-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1b6c5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b6c5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b6c5-130">CommonParameters</span></span>
<span data-ttu-id="1b6c5-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1b6c5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b6c5-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b6c5-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b6c5-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1b6c5-133">INPUTS</span></span>

## <span data-ttu-id="1b6c5-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1b6c5-134">OUTPUTS</span></span>

## <span data-ttu-id="1b6c5-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1b6c5-135">NOTES</span></span>

## <span data-ttu-id="1b6c5-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1b6c5-136">RELATED LINKS</span></span>

