---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D1A4FA07-C25E-472B-9C64-695AD41274FA
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb8b6a502d6abe5520cadcf776ece1f077c7d91f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016242"
---
# <span data-ttu-id="5816f-101">Move-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="5816f-101">Move-AzureReservedIP</span></span>

## <span data-ttu-id="5816f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5816f-102">SYNOPSIS</span></span>
<span data-ttu-id="5816f-103">A lefoglalt IP-címet áttelepíti az Azure Resource Manager-kötegbe.</span><span class="sxs-lookup"><span data-stu-id="5816f-103">Migrates a reserved IP address to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="5816f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5816f-104">SYNTAX</span></span>

### <span data-ttu-id="5816f-105">ValidateMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="5816f-105">ValidateMigrationParameterSet</span></span>
```
Move-AzureReservedIP [-ReservedIPName] <String> [-Validate] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5816f-106">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="5816f-106">AbortMigrationParameterSet</span></span>
```
Move-AzureReservedIP [-ReservedIPName] <String> [-Abort] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5816f-107">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="5816f-107">CommitMigrationParameterSet</span></span>
```
Move-AzureReservedIP [-ReservedIPName] <String> [-Commit] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5816f-108">PrepareMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="5816f-108">PrepareMigrationParameterSet</span></span>
```
Move-AzureReservedIP [-ReservedIPName] <String> [-Prepare] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5816f-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="5816f-109">DESCRIPTION</span></span>
<span data-ttu-id="5816f-110">A **Move-AzureReservedIP** parancsmag a lefoglalt IP-címet az Azure Resource Manager-kötegben lévő erőforráscsoport számára telepíti át.</span><span class="sxs-lookup"><span data-stu-id="5816f-110">The **Move-AzureReservedIP** cmdlet migrates a reserved IP address to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="5816f-111">Példák</span><span class="sxs-lookup"><span data-stu-id="5816f-111">EXAMPLES</span></span>

### <span data-ttu-id="5816f-112">1:</span><span class="sxs-lookup"><span data-stu-id="5816f-112">1:</span></span>
```

```

## <span data-ttu-id="5816f-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5816f-113">PARAMETERS</span></span>

### <span data-ttu-id="5816f-114">-Megszakítás</span><span class="sxs-lookup"><span data-stu-id="5816f-114">-Abort</span></span>
<span data-ttu-id="5816f-115">Jelzi, hogy ez a parancsmag lemondja a lefoglalt IP-cím áttelepítését.</span><span class="sxs-lookup"><span data-stu-id="5816f-115">Indicates that this cmdlet cancels the reserved IP address migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AbortMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5816f-116">-Commit</span><span class="sxs-lookup"><span data-stu-id="5816f-116">-Commit</span></span>
<span data-ttu-id="5816f-117">Jelzi, hogy ez a parancsmag elindítja a lefoglalt IP-cím áttelepítését.</span><span class="sxs-lookup"><span data-stu-id="5816f-117">Indicates that this cmdlet starts the reserved IP address migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CommitMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5816f-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="5816f-118">-InformationAction</span></span>
<span data-ttu-id="5816f-119">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="5816f-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="5816f-120">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="5816f-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5816f-121">Folytassa</span><span class="sxs-lookup"><span data-stu-id="5816f-121">Continue</span></span>
- <span data-ttu-id="5816f-122">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="5816f-122">Ignore</span></span>
- <span data-ttu-id="5816f-123">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="5816f-123">Inquire</span></span>
- <span data-ttu-id="5816f-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="5816f-124">SilentlyContinue</span></span>
- <span data-ttu-id="5816f-125">állj</span><span class="sxs-lookup"><span data-stu-id="5816f-125">Stop</span></span>
- <span data-ttu-id="5816f-126">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="5816f-126">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5816f-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="5816f-127">-InformationVariable</span></span>
<span data-ttu-id="5816f-128">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="5816f-128">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5816f-129">– Előkészületek</span><span class="sxs-lookup"><span data-stu-id="5816f-129">-Prepare</span></span>
<span data-ttu-id="5816f-130">Jelzi, hogy ez a parancsmag a lefoglalt IP-címet készíti el az áttelepítéshez.</span><span class="sxs-lookup"><span data-stu-id="5816f-130">Indicates that this cmdlet prepares the reserved IP address for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PrepareMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5816f-131">-Profil</span><span class="sxs-lookup"><span data-stu-id="5816f-131">-Profile</span></span>
<span data-ttu-id="5816f-132">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="5816f-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5816f-133">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="5816f-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5816f-134">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="5816f-134">-ReservedIPName</span></span>
<span data-ttu-id="5816f-135">Annak a fenntartott IP-címnek a nevét adja meg, amelyre a parancsmag áttelepíti.</span><span class="sxs-lookup"><span data-stu-id="5816f-135">Specifies the name of the reserved IP address that this cmdlet migrates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5816f-136">– Érvényesítés</span><span class="sxs-lookup"><span data-stu-id="5816f-136">-Validate</span></span>
<span data-ttu-id="5816f-137">Megadja, hogy ez a parancsmag ellenőrzi a lefoglalt IP-címet az áttelepítéshez.</span><span class="sxs-lookup"><span data-stu-id="5816f-137">Specifies that this cmdlet validates the reserved IP address for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ValidateMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5816f-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5816f-138">-Confirm</span></span>
<span data-ttu-id="5816f-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5816f-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5816f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5816f-140">-WhatIf</span></span>
<span data-ttu-id="5816f-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5816f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5816f-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5816f-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5816f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5816f-143">CommonParameters</span></span>
<span data-ttu-id="5816f-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5816f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5816f-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5816f-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5816f-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5816f-146">INPUTS</span></span>

## <span data-ttu-id="5816f-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5816f-147">OUTPUTS</span></span>

## <span data-ttu-id="5816f-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5816f-148">NOTES</span></span>

## <span data-ttu-id="5816f-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5816f-149">RELATED LINKS</span></span>

[<span data-ttu-id="5816f-150">Move-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5816f-150">Move-AzureNetworkSecurityGroup</span></span>](./Move-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="5816f-151">Move-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="5816f-151">Move-AzureRouteTable</span></span>](./Move-AzureRouteTable.md)

[<span data-ttu-id="5816f-152">Move-AzureService</span><span class="sxs-lookup"><span data-stu-id="5816f-152">Move-AzureService</span></span>](./Move-AzureService.md)

[<span data-ttu-id="5816f-153">Move-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5816f-153">Move-AzureStorageAccount</span></span>](./Move-AzureStorageAccount.md)

[<span data-ttu-id="5816f-154">Move-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5816f-154">Move-AzureVirtualNetwork</span></span>](./Move-AzureVirtualNetwork.md)


