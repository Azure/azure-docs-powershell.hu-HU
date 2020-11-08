---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 01213154-DD8A-412F-A23D-5D9D09BEFA3A
online version: ''
schema: 2.0.0
ms.openlocfilehash: f0602015a63d28aecb498b0830619ea1560d6066
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016241"
---
# <span data-ttu-id="11276-101">Move-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="11276-101">Move-AzureRouteTable</span></span>

## <span data-ttu-id="11276-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="11276-102">SYNOPSIS</span></span>
<span data-ttu-id="11276-103">Áttelepíti az útválasztási táblázatot az Azure Resource Manager-kötegbe.</span><span class="sxs-lookup"><span data-stu-id="11276-103">Migrates a route table to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="11276-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="11276-104">SYNTAX</span></span>

### <span data-ttu-id="11276-105">ValidateMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="11276-105">ValidateMigrationParameterSet</span></span>
```
Move-AzureRouteTable [-RouteTableName] <String> [-Validate] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="11276-106">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="11276-106">AbortMigrationParameterSet</span></span>
```
Move-AzureRouteTable [-RouteTableName] <String> [-Abort] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="11276-107">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="11276-107">CommitMigrationParameterSet</span></span>
```
Move-AzureRouteTable [-RouteTableName] <String> [-Commit] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="11276-108">PrepareMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="11276-108">PrepareMigrationParameterSet</span></span>
```
Move-AzureRouteTable [-RouteTableName] <String> [-Prepare] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="11276-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="11276-109">DESCRIPTION</span></span>
<span data-ttu-id="11276-110">A **Move-AzureRouteTable** parancsmag az Azure Resource Manager-kötegben lévő erőforrás-csoportba áttelepíti az útválasztási táblázatot.</span><span class="sxs-lookup"><span data-stu-id="11276-110">The **Move-AzureRouteTable** cmdlet migrates a route table to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="11276-111">Példák</span><span class="sxs-lookup"><span data-stu-id="11276-111">EXAMPLES</span></span>

### <span data-ttu-id="11276-112">1:</span><span class="sxs-lookup"><span data-stu-id="11276-112">1:</span></span>
```

```

## <span data-ttu-id="11276-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="11276-113">PARAMETERS</span></span>

### <span data-ttu-id="11276-114">-Megszakítás</span><span class="sxs-lookup"><span data-stu-id="11276-114">-Abort</span></span>
<span data-ttu-id="11276-115">Jelzi, hogy ez a parancsmag lemondja az útválasztási táblázat áttelepítését.</span><span class="sxs-lookup"><span data-stu-id="11276-115">Indicates that this cmdlet cancels the route table migration.</span></span>

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

### <span data-ttu-id="11276-116">-Commit</span><span class="sxs-lookup"><span data-stu-id="11276-116">-Commit</span></span>
<span data-ttu-id="11276-117">Azt jelzi, hogy ez a parancsmag elindítja az útválasztási táblázat áttelepítését.</span><span class="sxs-lookup"><span data-stu-id="11276-117">Indicates that this cmdlet starts the route table migration.</span></span>

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

### <span data-ttu-id="11276-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="11276-118">-InformationAction</span></span>
<span data-ttu-id="11276-119">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="11276-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="11276-120">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="11276-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="11276-121">Folytassa</span><span class="sxs-lookup"><span data-stu-id="11276-121">Continue</span></span>
- <span data-ttu-id="11276-122">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="11276-122">Ignore</span></span>
- <span data-ttu-id="11276-123">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="11276-123">Inquire</span></span>
- <span data-ttu-id="11276-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="11276-124">SilentlyContinue</span></span>
- <span data-ttu-id="11276-125">állj</span><span class="sxs-lookup"><span data-stu-id="11276-125">Stop</span></span>
- <span data-ttu-id="11276-126">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="11276-126">Suspend</span></span>

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

### <span data-ttu-id="11276-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="11276-127">-InformationVariable</span></span>
<span data-ttu-id="11276-128">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="11276-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="11276-129">– Előkészületek</span><span class="sxs-lookup"><span data-stu-id="11276-129">-Prepare</span></span>
<span data-ttu-id="11276-130">Jelzi, hogy ez a parancsmag előkészíti az útválasztási táblázatot az áttelepítésre.</span><span class="sxs-lookup"><span data-stu-id="11276-130">Indicates that this cmdlet prepares the route table for migration.</span></span>

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

### <span data-ttu-id="11276-131">-Profil</span><span class="sxs-lookup"><span data-stu-id="11276-131">-Profile</span></span>
<span data-ttu-id="11276-132">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="11276-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="11276-133">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="11276-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="11276-134">-RouteTableName</span><span class="sxs-lookup"><span data-stu-id="11276-134">-RouteTableName</span></span>
<span data-ttu-id="11276-135">Annak az útválasztási táblázatnak a nevét adja meg, amelyre a parancsmag át van telepítve.</span><span class="sxs-lookup"><span data-stu-id="11276-135">Specifies the name of the route table that this cmdlet migrates.</span></span>

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

### <span data-ttu-id="11276-136">– Érvényesítés</span><span class="sxs-lookup"><span data-stu-id="11276-136">-Validate</span></span>
<span data-ttu-id="11276-137">Megadja, hogy ez a parancsmag ellenőrzi az útválasztási táblázatot az áttelepítéshez.</span><span class="sxs-lookup"><span data-stu-id="11276-137">Specifies that this cmdlet validates the route table for migration.</span></span>

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

### <span data-ttu-id="11276-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="11276-138">-Confirm</span></span>
<span data-ttu-id="11276-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="11276-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11276-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11276-140">-WhatIf</span></span>
<span data-ttu-id="11276-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="11276-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11276-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="11276-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11276-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11276-143">CommonParameters</span></span>
<span data-ttu-id="11276-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="11276-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11276-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11276-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11276-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="11276-146">INPUTS</span></span>

## <span data-ttu-id="11276-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="11276-147">OUTPUTS</span></span>

## <span data-ttu-id="11276-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="11276-148">NOTES</span></span>

## <span data-ttu-id="11276-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="11276-149">RELATED LINKS</span></span>

[<span data-ttu-id="11276-150">Move-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="11276-150">Move-AzureNetworkSecurityGroup</span></span>](./Move-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="11276-151">Move-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="11276-151">Move-AzureReservedIP</span></span>](./Move-AzureReservedIP.md)

[<span data-ttu-id="11276-152">Move-AzureService</span><span class="sxs-lookup"><span data-stu-id="11276-152">Move-AzureService</span></span>](./Move-AzureService.md)

[<span data-ttu-id="11276-153">Move-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="11276-153">Move-AzureStorageAccount</span></span>](./Move-AzureStorageAccount.md)

[<span data-ttu-id="11276-154">Move-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="11276-154">Move-AzureVirtualNetwork</span></span>](./Move-AzureVirtualNetwork.md)


