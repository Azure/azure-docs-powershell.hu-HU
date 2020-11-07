---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5bf583c30d2faff1055debf366a84a0739789467
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840814"
---
# <span data-ttu-id="a4c28-101">Start-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="a4c28-101">Start-AzsBackup</span></span>

## <span data-ttu-id="a4c28-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a4c28-102">SYNOPSIS</span></span>
<span data-ttu-id="a4c28-103">Adott helyről készítsen biztonsági másolatot.</span><span class="sxs-lookup"><span data-stu-id="a4c28-103">Back up a specific location.</span></span>

## <span data-ttu-id="a4c28-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a4c28-104">SYNTAX</span></span>

### <span data-ttu-id="a4c28-105">CreateBackup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a4c28-105">CreateBackup (Default)</span></span>
```
Start-AzsBackup [-ResourceGroupName <String>] [-Location <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a4c28-106">CreateBackup_FromResourceId</span><span class="sxs-lookup"><span data-stu-id="a4c28-106">CreateBackup_FromResourceId</span></span>
```
Start-AzsBackup -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4c28-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a4c28-107">DESCRIPTION</span></span>
<span data-ttu-id="a4c28-108">Adott helyről készítsen biztonsági másolatot.</span><span class="sxs-lookup"><span data-stu-id="a4c28-108">Back up a specific location.</span></span>

## <span data-ttu-id="a4c28-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a4c28-109">EXAMPLES</span></span>

### <span data-ttu-id="a4c28-110">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a4c28-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsBackup
```

<span data-ttu-id="a4c28-111">Nyisson meg egy Azure-halom biztonsági mentést.</span><span class="sxs-lookup"><span data-stu-id="a4c28-111">Start an Azure Stack backup.</span></span>

## <span data-ttu-id="a4c28-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a4c28-112">PARAMETERS</span></span>

### <span data-ttu-id="a4c28-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a4c28-113">-AsJob</span></span>
<span data-ttu-id="a4c28-114">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="a4c28-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="a4c28-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a4c28-115">-Force</span></span>
<span data-ttu-id="a4c28-116">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a4c28-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="a4c28-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="a4c28-117">-Location</span></span>
<span data-ttu-id="a4c28-118">A biztonsági másolat helyének neve.</span><span class="sxs-lookup"><span data-stu-id="a4c28-118">Name of the backup location.</span></span>

```yaml
Type: String
Parameter Sets: CreateBackup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4c28-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4c28-119">-ResourceGroupName</span></span>
<span data-ttu-id="a4c28-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a4c28-120">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: CreateBackup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4c28-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4c28-121">-ResourceId</span></span>
<span data-ttu-id="a4c28-122">{{Fill ResourceId Description}}</span><span class="sxs-lookup"><span data-stu-id="a4c28-122">{{Fill ResourceId Description}}</span></span>

```yaml
Type: String
Parameter Sets: CreateBackup_FromResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4c28-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a4c28-123">-Confirm</span></span>
<span data-ttu-id="a4c28-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a4c28-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4c28-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4c28-125">-WhatIf</span></span>
<span data-ttu-id="a4c28-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a4c28-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4c28-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a4c28-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4c28-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4c28-128">CommonParameters</span></span>
<span data-ttu-id="a4c28-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a4c28-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4c28-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4c28-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4c28-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4c28-131">INPUTS</span></span>

## <span data-ttu-id="a4c28-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4c28-132">OUTPUTS</span></span>

### <span data-ttu-id="a4c28-133">Microsoft. AzureStack. Management. backup. admin. models. LongRunningOperationStatus</span><span class="sxs-lookup"><span data-stu-id="a4c28-133">Microsoft.AzureStack.Management.Backup.Admin.Models.LongRunningOperationStatus</span></span>

## <span data-ttu-id="a4c28-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a4c28-134">NOTES</span></span>

## <span data-ttu-id="a4c28-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a4c28-135">RELATED LINKS</span></span>

