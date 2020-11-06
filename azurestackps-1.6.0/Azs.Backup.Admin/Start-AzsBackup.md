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
ms.locfileid: "93491680"
---
# <span data-ttu-id="fc257-101">Start-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="fc257-101">Start-AzsBackup</span></span>

## <span data-ttu-id="fc257-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fc257-102">SYNOPSIS</span></span>
<span data-ttu-id="fc257-103">Adott helyről készítsen biztonsági másolatot.</span><span class="sxs-lookup"><span data-stu-id="fc257-103">Back up a specific location.</span></span>

## <span data-ttu-id="fc257-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fc257-104">SYNTAX</span></span>

### <span data-ttu-id="fc257-105">CreateBackup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fc257-105">CreateBackup (Default)</span></span>
```
Start-AzsBackup [-ResourceGroupName <String>] [-Location <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fc257-106">CreateBackup_FromResourceId</span><span class="sxs-lookup"><span data-stu-id="fc257-106">CreateBackup_FromResourceId</span></span>
```
Start-AzsBackup -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc257-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="fc257-107">DESCRIPTION</span></span>
<span data-ttu-id="fc257-108">Adott helyről készítsen biztonsági másolatot.</span><span class="sxs-lookup"><span data-stu-id="fc257-108">Back up a specific location.</span></span>

## <span data-ttu-id="fc257-109">Példák</span><span class="sxs-lookup"><span data-stu-id="fc257-109">EXAMPLES</span></span>

### <span data-ttu-id="fc257-110">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="fc257-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsBackup
```

<span data-ttu-id="fc257-111">Nyisson meg egy Azure-halom biztonsági mentést.</span><span class="sxs-lookup"><span data-stu-id="fc257-111">Start an Azure Stack backup.</span></span>

## <span data-ttu-id="fc257-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fc257-112">PARAMETERS</span></span>

### <span data-ttu-id="fc257-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fc257-113">-AsJob</span></span>
<span data-ttu-id="fc257-114">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="fc257-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="fc257-115">-Force</span><span class="sxs-lookup"><span data-stu-id="fc257-115">-Force</span></span>
<span data-ttu-id="fc257-116">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fc257-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="fc257-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="fc257-117">-Location</span></span>
<span data-ttu-id="fc257-118">A biztonsági másolat helyének neve.</span><span class="sxs-lookup"><span data-stu-id="fc257-118">Name of the backup location.</span></span>

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

### <span data-ttu-id="fc257-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc257-119">-ResourceGroupName</span></span>
<span data-ttu-id="fc257-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fc257-120">Name of the resource group.</span></span>

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

### <span data-ttu-id="fc257-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc257-121">-ResourceId</span></span>
<span data-ttu-id="fc257-122">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="fc257-122">The resource id.</span></span>

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

### <span data-ttu-id="fc257-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fc257-123">-Confirm</span></span>
<span data-ttu-id="fc257-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fc257-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc257-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc257-125">-WhatIf</span></span>
<span data-ttu-id="fc257-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fc257-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc257-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fc257-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc257-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc257-128">CommonParameters</span></span>
<span data-ttu-id="fc257-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fc257-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc257-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc257-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc257-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc257-131">INPUTS</span></span>

## <span data-ttu-id="fc257-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc257-132">OUTPUTS</span></span>

### <span data-ttu-id="fc257-133">Microsoft. AzureStack. Management. backup. admin. models. LongRunningOperationStatus</span><span class="sxs-lookup"><span data-stu-id="fc257-133">Microsoft.AzureStack.Management.Backup.Admin.Models.LongRunningOperationStatus</span></span>

## <span data-ttu-id="fc257-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fc257-134">NOTES</span></span>

## <span data-ttu-id="fc257-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fc257-135">RELATED LINKS</span></span>

