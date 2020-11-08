---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 27ECCBAD-0CFE-4309-B590-BB60E1872ED5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9d96f02374eb266cb9eaa3c1cc7c200a4f154043
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016243"
---
# <span data-ttu-id="8a4d8-101">Move-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8a4d8-101">Move-AzureNetworkSecurityGroup</span></span>

## <span data-ttu-id="8a4d8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8a4d8-102">SYNOPSIS</span></span>
<span data-ttu-id="8a4d8-103">Áttelepíti a hálózat biztonsági csoportját az Azure Resource Manager-kötegbe.</span><span class="sxs-lookup"><span data-stu-id="8a4d8-103">Migrates a Network Security Group to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="8a4d8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8a4d8-104">SYNTAX</span></span>

### <span data-ttu-id="8a4d8-105">ValidateMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a4d8-105">ValidateMigrationParameterSet</span></span>
```
Move-AzureNetworkSecurityGroup [-NetworkSecurityGroupName] <String> [-Validate] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8a4d8-106">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a4d8-106">AbortMigrationParameterSet</span></span>
```
Move-AzureNetworkSecurityGroup [-NetworkSecurityGroupName] <String> [-Abort] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8a4d8-107">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a4d8-107">CommitMigrationParameterSet</span></span>
```
Move-AzureNetworkSecurityGroup [-NetworkSecurityGroupName] <String> [-Commit] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8a4d8-108">PrepareMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a4d8-108">PrepareMigrationParameterSet</span></span>
```
Move-AzureNetworkSecurityGroup [-NetworkSecurityGroupName] <String> [-Prepare] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8a4d8-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="8a4d8-109">DESCRIPTION</span></span>
<span data-ttu-id="8a4d8-110">A **Move-AzureNetworkSecurityGroup** parancsmag a hálózat biztonsági csoportját az Azure Resource Manager-kötegben lévő erőforráscsoport-csoportba telepíti át.</span><span class="sxs-lookup"><span data-stu-id="8a4d8-110">The **Move-AzureNetworkSecurityGroup** cmdlet migrates a Network Security Group to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="8a4d8-111">Példák</span><span class="sxs-lookup"><span data-stu-id="8a4d8-111">EXAMPLES</span></span>

### <span data-ttu-id="8a4d8-112">1:</span><span class="sxs-lookup"><span data-stu-id="8a4d8-112">1:</span></span>
```

```

## <span data-ttu-id="8a4d8-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8a4d8-113">PARAMETERS</span></span>

### <span data-ttu-id="8a4d8-114">-Megszakítás</span><span class="sxs-lookup"><span data-stu-id="8a4d8-114">-Abort</span></span>
<span data-ttu-id="8a4d8-115">Jelzi, hogy ez a parancsmag lemondja a hálózati biztonsági csoport áttelepítését.</span><span class="sxs-lookup"><span data-stu-id="8a4d8-115">Indicates that this cmdlet cancels the Network Security Group migration.</span></span>

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

### <span data-ttu-id="8a4d8-116">-Commit</span><span class="sxs-lookup"><span data-stu-id="8a4d8-116">-Commit</span></span>
<span data-ttu-id="8a4d8-117">Jelzi, hogy ez a parancsmag elindítja a hálózat biztonsági csoportjának áttelepítését.</span><span class="sxs-lookup"><span data-stu-id="8a4d8-117">Indicates that this cmdlet starts the Network Security Group migration.</span></span>

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

### <span data-ttu-id="8a4d8-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="8a4d8-118">-InformationAction</span></span>
<span data-ttu-id="8a4d8-119">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="8a4d8-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8a4d8-120">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="8a4d8-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8a4d8-121">Folytassa</span><span class="sxs-lookup"><span data-stu-id="8a4d8-121">Continue</span></span>
- <span data-ttu-id="8a4d8-122">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="8a4d8-122">Ignore</span></span>
- <span data-ttu-id="8a4d8-123">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="8a4d8-123">Inquire</span></span>
- <span data-ttu-id="8a4d8-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8a4d8-124">SilentlyContinue</span></span>
- <span data-ttu-id="8a4d8-125">állj</span><span class="sxs-lookup"><span data-stu-id="8a4d8-125">Stop</span></span>
- <span data-ttu-id="8a4d8-126">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="8a4d8-126">Suspend</span></span>

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

### <span data-ttu-id="8a4d8-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8a4d8-127">-InformationVariable</span></span>
<span data-ttu-id="8a4d8-128">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="8a4d8-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8a4d8-129">-NetworkSecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="8a4d8-129">-NetworkSecurityGroupName</span></span>
<span data-ttu-id="8a4d8-130">Annak a hálózati biztonsági csoportnak a nevét adja meg, amelyre a parancsmag át van telepítve.</span><span class="sxs-lookup"><span data-stu-id="8a4d8-130">Specifies the name of the Network Security Group that this cmdlet migrates.</span></span>

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

### <span data-ttu-id="8a4d8-131">– Előkészületek</span><span class="sxs-lookup"><span data-stu-id="8a4d8-131">-Prepare</span></span>
<span data-ttu-id="8a4d8-132">Jelzi, hogy ez a parancsmag előkészíti a hálózati biztonsági csoportot az áttelepítésre.</span><span class="sxs-lookup"><span data-stu-id="8a4d8-132">Indicates that this cmdlet prepares the Network Security Group for migration.</span></span>

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

### <span data-ttu-id="8a4d8-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="8a4d8-133">-Profile</span></span>
<span data-ttu-id="8a4d8-134">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="8a4d8-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8a4d8-135">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="8a4d8-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8a4d8-136">– Érvényesítés</span><span class="sxs-lookup"><span data-stu-id="8a4d8-136">-Validate</span></span>
<span data-ttu-id="8a4d8-137">Meghatározza, hogy ez a parancsmag ellenőrzi-e az áttelepítés hálózati biztonsági csoportját.</span><span class="sxs-lookup"><span data-stu-id="8a4d8-137">Specifies that this cmdlet validates the Network Security Group for migration.</span></span>

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

### <span data-ttu-id="8a4d8-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8a4d8-138">-Confirm</span></span>
<span data-ttu-id="8a4d8-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8a4d8-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a4d8-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a4d8-140">-WhatIf</span></span>
<span data-ttu-id="8a4d8-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8a4d8-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a4d8-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8a4d8-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a4d8-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a4d8-143">CommonParameters</span></span>
<span data-ttu-id="8a4d8-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8a4d8-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a4d8-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a4d8-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a4d8-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8a4d8-146">INPUTS</span></span>

## <span data-ttu-id="8a4d8-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8a4d8-147">OUTPUTS</span></span>

## <span data-ttu-id="8a4d8-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8a4d8-148">NOTES</span></span>

## <span data-ttu-id="8a4d8-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8a4d8-149">RELATED LINKS</span></span>

[<span data-ttu-id="8a4d8-150">Move-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="8a4d8-150">Move-AzureReservedIP</span></span>](./Move-AzureReservedIP.md)

[<span data-ttu-id="8a4d8-151">Move-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="8a4d8-151">Move-AzureRouteTable</span></span>](./Move-AzureRouteTable.md)

[<span data-ttu-id="8a4d8-152">Move-AzureService</span><span class="sxs-lookup"><span data-stu-id="8a4d8-152">Move-AzureService</span></span>](./Move-AzureService.md)

[<span data-ttu-id="8a4d8-153">Move-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8a4d8-153">Move-AzureStorageAccount</span></span>](./Move-AzureStorageAccount.md)

[<span data-ttu-id="8a4d8-154">Move-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8a4d8-154">Move-AzureVirtualNetwork</span></span>](./Move-AzureVirtualNetwork.md)


