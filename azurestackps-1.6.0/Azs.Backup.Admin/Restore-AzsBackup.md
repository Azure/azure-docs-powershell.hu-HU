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
ms.locfileid: "93491682"
---
# <span data-ttu-id="02ca1-101">Restore-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="02ca1-101">Restore-AzsBackup</span></span>

## <span data-ttu-id="02ca1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="02ca1-102">SYNOPSIS</span></span>
<span data-ttu-id="02ca1-103">Biztonsági másolat visszaállítása</span><span class="sxs-lookup"><span data-stu-id="02ca1-103">Restore a backup.</span></span>

## <span data-ttu-id="02ca1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="02ca1-104">SYNTAX</span></span>

### <span data-ttu-id="02ca1-105">Backups_Restore (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="02ca1-105">Backups_Restore (Default)</span></span>
```
Restore-AzsBackup [-ResourceGroupName <String>] -Name <String> [-Location <String>] [-AsJob] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02ca1-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="02ca1-106">ResourceId</span></span>
```
Restore-AzsBackup -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02ca1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="02ca1-107">DESCRIPTION</span></span>
<span data-ttu-id="02ca1-108">Biztonsági másolat visszaállítása</span><span class="sxs-lookup"><span data-stu-id="02ca1-108">Restore a backup.</span></span>

## <span data-ttu-id="02ca1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="02ca1-109">EXAMPLES</span></span>

### <span data-ttu-id="02ca1-110">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="02ca1-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Restore-AzsBackup -Backup 4e90bd2f-c7ab-47a3-a3c7-908cddd1ad0e
```

<span data-ttu-id="02ca1-111">Visszaállíthatja az Azure-halom biztonsági másolatát.</span><span class="sxs-lookup"><span data-stu-id="02ca1-111">Restore from an Azure Stack backup.</span></span>

## <span data-ttu-id="02ca1-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="02ca1-112">PARAMETERS</span></span>

### <span data-ttu-id="02ca1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="02ca1-113">-AsJob</span></span>
<span data-ttu-id="02ca1-114">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="02ca1-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="02ca1-115">-Force</span><span class="sxs-lookup"><span data-stu-id="02ca1-115">-Force</span></span>
<span data-ttu-id="02ca1-116">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="02ca1-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="02ca1-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="02ca1-117">-Location</span></span>
<span data-ttu-id="02ca1-118">A biztonsági másolat helyének neve.</span><span class="sxs-lookup"><span data-stu-id="02ca1-118">Name of location to backup.</span></span>

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

### <span data-ttu-id="02ca1-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="02ca1-119">-Name</span></span>
<span data-ttu-id="02ca1-120">A biztonsági másolat neve.</span><span class="sxs-lookup"><span data-stu-id="02ca1-120">Name of the backup.</span></span>

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

### <span data-ttu-id="02ca1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02ca1-121">-ResourceGroupName</span></span>
<span data-ttu-id="02ca1-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="02ca1-122">Name of the resource group.</span></span>

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

### <span data-ttu-id="02ca1-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02ca1-123">-ResourceId</span></span>
<span data-ttu-id="02ca1-124">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="02ca1-124">The resource id.</span></span>

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

### <span data-ttu-id="02ca1-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="02ca1-125">-Confirm</span></span>
<span data-ttu-id="02ca1-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="02ca1-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02ca1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02ca1-127">-WhatIf</span></span>
<span data-ttu-id="02ca1-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="02ca1-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02ca1-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="02ca1-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02ca1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02ca1-130">CommonParameters</span></span>
<span data-ttu-id="02ca1-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="02ca1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02ca1-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02ca1-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02ca1-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="02ca1-133">INPUTS</span></span>

## <span data-ttu-id="02ca1-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="02ca1-134">OUTPUTS</span></span>

## <span data-ttu-id="02ca1-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="02ca1-135">NOTES</span></span>

## <span data-ttu-id="02ca1-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="02ca1-136">RELATED LINKS</span></span>

