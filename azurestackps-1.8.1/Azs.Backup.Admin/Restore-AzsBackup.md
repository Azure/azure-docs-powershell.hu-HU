---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 573a47b3684020817130e1d41c764abef717de0a
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840913"
---
# <span data-ttu-id="7963d-101">Restore-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="7963d-101">Restore-AzsBackup</span></span>

## <span data-ttu-id="7963d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7963d-102">SYNOPSIS</span></span>
<span data-ttu-id="7963d-103">Biztonsági másolat visszaállítása</span><span class="sxs-lookup"><span data-stu-id="7963d-103">Restore a backup.</span></span>

## <span data-ttu-id="7963d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7963d-104">SYNTAX</span></span>

### <span data-ttu-id="7963d-105">Backups_Restore (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7963d-105">Backups_Restore (Default)</span></span>
```
Restore-AzsBackup [-ResourceGroupName <String>] -Name <String> [-Location <String>] [-AsJob] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7963d-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7963d-106">ResourceId</span></span>
```
Restore-AzsBackup -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7963d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7963d-107">DESCRIPTION</span></span>
<span data-ttu-id="7963d-108">Biztonsági másolat visszaállítása</span><span class="sxs-lookup"><span data-stu-id="7963d-108">Restore a backup.</span></span>

## <span data-ttu-id="7963d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="7963d-109">EXAMPLES</span></span>

### <span data-ttu-id="7963d-110">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7963d-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Restore-AzsBackup -Backup 4e90bd2f-c7ab-47a3-a3c7-908cddd1ad0e
```

<span data-ttu-id="7963d-111">Visszaállíthatja az Azure-halom biztonsági másolatát.</span><span class="sxs-lookup"><span data-stu-id="7963d-111">Restore from an Azure Stack backup.</span></span>

## <span data-ttu-id="7963d-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7963d-112">PARAMETERS</span></span>

### <span data-ttu-id="7963d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7963d-113">-AsJob</span></span>
<span data-ttu-id="7963d-114">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="7963d-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="7963d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7963d-115">-Force</span></span>
<span data-ttu-id="7963d-116">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7963d-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="7963d-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="7963d-117">-Location</span></span>
<span data-ttu-id="7963d-118">A biztonsági másolat helyének neve.</span><span class="sxs-lookup"><span data-stu-id="7963d-118">Name of location to backup.</span></span>

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

### <span data-ttu-id="7963d-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7963d-119">-Name</span></span>
<span data-ttu-id="7963d-120">A biztonsági másolat neve.</span><span class="sxs-lookup"><span data-stu-id="7963d-120">Name of the backup.</span></span>

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

### <span data-ttu-id="7963d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7963d-121">-ResourceGroupName</span></span>
<span data-ttu-id="7963d-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7963d-122">Name of the resource group.</span></span>

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

### <span data-ttu-id="7963d-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7963d-123">-ResourceId</span></span>
<span data-ttu-id="7963d-124">{{Fill ResourceId Description}}</span><span class="sxs-lookup"><span data-stu-id="7963d-124">{{Fill ResourceId Description}}</span></span>

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

### <span data-ttu-id="7963d-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7963d-125">-Confirm</span></span>
<span data-ttu-id="7963d-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7963d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7963d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7963d-127">-WhatIf</span></span>
<span data-ttu-id="7963d-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7963d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7963d-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7963d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7963d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7963d-130">CommonParameters</span></span>
<span data-ttu-id="7963d-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7963d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7963d-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7963d-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7963d-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7963d-133">INPUTS</span></span>

## <span data-ttu-id="7963d-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7963d-134">OUTPUTS</span></span>

## <span data-ttu-id="7963d-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7963d-135">NOTES</span></span>

## <span data-ttu-id="7963d-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7963d-136">RELATED LINKS</span></span>

