---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c7dff6c2d9c191d852420ab2c2017a0b9d1cf8d3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671774"
---
# <span data-ttu-id="50a9c-101">Start-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="50a9c-101">Start-AzsBackup</span></span>

## <span data-ttu-id="50a9c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="50a9c-102">SYNOPSIS</span></span>
<span data-ttu-id="50a9c-103">Adott helyről készítsen biztonsági másolatot.</span><span class="sxs-lookup"><span data-stu-id="50a9c-103">Back up a specific location.</span></span>

## <span data-ttu-id="50a9c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="50a9c-104">SYNTAX</span></span>

### <span data-ttu-id="50a9c-105">CreateBackup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="50a9c-105">CreateBackup (Default)</span></span>
```
Start-AzsBackup [-ResourceGroupName <String>] [-Location <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="50a9c-106">CreateBackup_FromResourceId</span><span class="sxs-lookup"><span data-stu-id="50a9c-106">CreateBackup_FromResourceId</span></span>
```
Start-AzsBackup -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50a9c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="50a9c-107">DESCRIPTION</span></span>
<span data-ttu-id="50a9c-108">Adott helyről készítsen biztonsági másolatot.</span><span class="sxs-lookup"><span data-stu-id="50a9c-108">Back up a specific location.</span></span>

## <span data-ttu-id="50a9c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="50a9c-109">EXAMPLES</span></span>

### <span data-ttu-id="50a9c-110">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="50a9c-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsBackup
```

<span data-ttu-id="50a9c-111">Nyisson meg egy Azure-halom biztonsági mentést.</span><span class="sxs-lookup"><span data-stu-id="50a9c-111">Start an Azure Stack backup.</span></span>

## <span data-ttu-id="50a9c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="50a9c-112">PARAMETERS</span></span>

### <span data-ttu-id="50a9c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="50a9c-113">-AsJob</span></span>
<span data-ttu-id="50a9c-114">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="50a9c-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="50a9c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="50a9c-115">-Force</span></span>
<span data-ttu-id="50a9c-116">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="50a9c-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="50a9c-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="50a9c-117">-Location</span></span>
<span data-ttu-id="50a9c-118">A biztonsági másolat helyének neve.</span><span class="sxs-lookup"><span data-stu-id="50a9c-118">Name of the backup location.</span></span>

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

### <span data-ttu-id="50a9c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50a9c-119">-ResourceGroupName</span></span>
<span data-ttu-id="50a9c-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="50a9c-120">Name of the resource group.</span></span>

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

### <span data-ttu-id="50a9c-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="50a9c-121">-ResourceId</span></span>
<span data-ttu-id="50a9c-122">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="50a9c-122">The resource id.</span></span>

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

### <span data-ttu-id="50a9c-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="50a9c-123">-Confirm</span></span>
<span data-ttu-id="50a9c-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="50a9c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50a9c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50a9c-125">-WhatIf</span></span>
<span data-ttu-id="50a9c-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="50a9c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50a9c-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="50a9c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50a9c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50a9c-128">CommonParameters</span></span>
<span data-ttu-id="50a9c-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="50a9c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50a9c-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50a9c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50a9c-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="50a9c-131">INPUTS</span></span>

## <span data-ttu-id="50a9c-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="50a9c-132">OUTPUTS</span></span>

### <span data-ttu-id="50a9c-133">Microsoft. AzureStack. Management. backup. admin. models. LongRunningOperationStatus</span><span class="sxs-lookup"><span data-stu-id="50a9c-133">Microsoft.AzureStack.Management.Backup.Admin.Models.LongRunningOperationStatus</span></span>

## <span data-ttu-id="50a9c-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="50a9c-134">NOTES</span></span>

## <span data-ttu-id="50a9c-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="50a9c-135">RELATED LINKS</span></span>

