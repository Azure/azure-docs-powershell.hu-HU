---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2B0CC65A-0A73-4FFE-BF7C-B148871909D9
online version: ''
schema: 2.0.0
ms.openlocfilehash: df768878bf26c186751171edf7ed41acb3f7d15a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016238"
---
# <span data-ttu-id="0a0be-101">Move-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0a0be-101">Move-AzureVirtualNetwork</span></span>

## <span data-ttu-id="0a0be-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0a0be-102">SYNOPSIS</span></span>
<span data-ttu-id="0a0be-103">Virtuális hálózat áttelepítése az Azure Resource Manager-kötegbe.</span><span class="sxs-lookup"><span data-stu-id="0a0be-103">Migrates a virtual network to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="0a0be-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0a0be-104">SYNTAX</span></span>

### <span data-ttu-id="0a0be-105">ValidateMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a0be-105">ValidateMigrationParameterSet</span></span>
```
Move-AzureVirtualNetwork [-VirtualNetworkName] <String> [-Validate] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0a0be-106">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a0be-106">AbortMigrationParameterSet</span></span>
```
Move-AzureVirtualNetwork [-VirtualNetworkName] <String> [-Abort] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0a0be-107">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a0be-107">CommitMigrationParameterSet</span></span>
```
Move-AzureVirtualNetwork [-VirtualNetworkName] <String> [-Commit] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0a0be-108">PrepareMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a0be-108">PrepareMigrationParameterSet</span></span>
```
Move-AzureVirtualNetwork [-VirtualNetworkName] <String> [-Prepare] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0a0be-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="0a0be-109">DESCRIPTION</span></span>
<span data-ttu-id="0a0be-110">A **Move-AzureVirtualNetwork** parancsmag a virtuális hálózatokat az Azure Resource Manager-kötegben lévő erőforráscsoporthoz telepíti át.</span><span class="sxs-lookup"><span data-stu-id="0a0be-110">The **Move-AzureVirtualNetwork** cmdlet migrates a virtual network to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="0a0be-111">Példák</span><span class="sxs-lookup"><span data-stu-id="0a0be-111">EXAMPLES</span></span>

### <span data-ttu-id="0a0be-112">Példa 1: virtuális hálózati áttelepítés előkészítése</span><span class="sxs-lookup"><span data-stu-id="0a0be-112">Example 1: Prepare virtual network migration</span></span>
```
PS C:\> Move-AzureVirtualNetwork -Prepare -VirtualNetworkName "ContosoVNET"
```

<span data-ttu-id="0a0be-113">Ez a parancs felkészíti a ContosoVNET nevű virtuális hálózatot az Azure Resource Manager-kötegbe való áttelepítésre.</span><span class="sxs-lookup"><span data-stu-id="0a0be-113">This command prepares the virtual network named ContosoVNET for migration to the Azure Resource Manager stack.</span></span>

### <span data-ttu-id="0a0be-114">2. példa: a virtuális hálózati áttelepítés indítása</span><span class="sxs-lookup"><span data-stu-id="0a0be-114">Example 2: Start virtual network migration</span></span>
```
PS C:\> Move-AzureVirtualNetwork -Commit -VirtualNetworkName "ContosoVNET"
```

<span data-ttu-id="0a0be-115">Ez a parancs elindítja a ContosoVNET nevű virtuális hálózat áttelepítését az Azure Resource Manager-kötegbe.</span><span class="sxs-lookup"><span data-stu-id="0a0be-115">This command starts migration of the virtual network named ContosoVNET to the Azure Resource Manager stack.</span></span>

### <span data-ttu-id="0a0be-116">3. példa: a virtuális hálózati áttelepítés érvényesítése</span><span class="sxs-lookup"><span data-stu-id="0a0be-116">Example 3: Validate virtual network migration</span></span>
```
PS C:\> Move-AzureVirtualNetwork -Validate -VirtualNetworkName "ContosoVNET"
```

<span data-ttu-id="0a0be-117">Ez a parancs ellenőrzi a ContosoVNET nevű virtuális hálózat áttelepítését az Azure Resource Manager-köteg számára.</span><span class="sxs-lookup"><span data-stu-id="0a0be-117">This command validates migration for the virtual network named ContosoVNET to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="0a0be-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0a0be-118">PARAMETERS</span></span>

### <span data-ttu-id="0a0be-119">-Megszakítás</span><span class="sxs-lookup"><span data-stu-id="0a0be-119">-Abort</span></span>
<span data-ttu-id="0a0be-120">Jelzi, hogy ez a parancsmag lemondja a virtuális hálózati áttelepítést.</span><span class="sxs-lookup"><span data-stu-id="0a0be-120">Indicates that this cmdlet cancels the virtual network migration.</span></span>

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

### <span data-ttu-id="0a0be-121">-Commit</span><span class="sxs-lookup"><span data-stu-id="0a0be-121">-Commit</span></span>
<span data-ttu-id="0a0be-122">Jelzi, hogy ez a parancsmag elindítja a virtuális hálózat áttelepítését.</span><span class="sxs-lookup"><span data-stu-id="0a0be-122">Indicates that this cmdlet starts the virtual network migration.</span></span>

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

### <span data-ttu-id="0a0be-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="0a0be-123">-InformationAction</span></span>
<span data-ttu-id="0a0be-124">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="0a0be-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="0a0be-125">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="0a0be-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0a0be-126">Folytassa</span><span class="sxs-lookup"><span data-stu-id="0a0be-126">Continue</span></span>
- <span data-ttu-id="0a0be-127">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="0a0be-127">Ignore</span></span>
- <span data-ttu-id="0a0be-128">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="0a0be-128">Inquire</span></span>
- <span data-ttu-id="0a0be-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="0a0be-129">SilentlyContinue</span></span>
- <span data-ttu-id="0a0be-130">állj</span><span class="sxs-lookup"><span data-stu-id="0a0be-130">Stop</span></span>
- <span data-ttu-id="0a0be-131">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="0a0be-131">Suspend</span></span>

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

### <span data-ttu-id="0a0be-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="0a0be-132">-InformationVariable</span></span>
<span data-ttu-id="0a0be-133">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="0a0be-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="0a0be-134">– Előkészületek</span><span class="sxs-lookup"><span data-stu-id="0a0be-134">-Prepare</span></span>
<span data-ttu-id="0a0be-135">Jelzi, hogy ez a parancsmag felkészíti a virtuális hálózatot az áttelepítésre.</span><span class="sxs-lookup"><span data-stu-id="0a0be-135">Indicates that this cmdlet prepares the virtual network for migration.</span></span>

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

### <span data-ttu-id="0a0be-136">-Profil</span><span class="sxs-lookup"><span data-stu-id="0a0be-136">-Profile</span></span>
<span data-ttu-id="0a0be-137">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="0a0be-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0a0be-138">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="0a0be-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0a0be-139">– Érvényesítés</span><span class="sxs-lookup"><span data-stu-id="0a0be-139">-Validate</span></span>
<span data-ttu-id="0a0be-140">Azt adja meg, hogy a parancsmag ellenőrzi-e a virtuális hálózatot az áttelepítés során.</span><span class="sxs-lookup"><span data-stu-id="0a0be-140">Specifies that this cmdlet validates the virtual network for migration.</span></span>

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

### <span data-ttu-id="0a0be-141">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="0a0be-141">-VirtualNetworkName</span></span>
<span data-ttu-id="0a0be-142">Az áttelepítendő virtuális hálózat neve</span><span class="sxs-lookup"><span data-stu-id="0a0be-142">Name of the Virtual Network to migrate</span></span>

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

### <span data-ttu-id="0a0be-143">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0a0be-143">-Confirm</span></span>
<span data-ttu-id="0a0be-144">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0a0be-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a0be-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a0be-145">-WhatIf</span></span>
<span data-ttu-id="0a0be-146">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0a0be-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a0be-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0a0be-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a0be-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a0be-148">CommonParameters</span></span>
<span data-ttu-id="0a0be-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0a0be-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a0be-150">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a0be-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a0be-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a0be-151">INPUTS</span></span>

## <span data-ttu-id="0a0be-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a0be-152">OUTPUTS</span></span>

## <span data-ttu-id="0a0be-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0a0be-153">NOTES</span></span>

## <span data-ttu-id="0a0be-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0a0be-154">RELATED LINKS</span></span>

[<span data-ttu-id="0a0be-155">Move-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0a0be-155">Move-AzureNetworkSecurityGroup</span></span>](./Move-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="0a0be-156">Move-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="0a0be-156">Move-AzureReservedIP</span></span>](./Move-AzureReservedIP.md)

[<span data-ttu-id="0a0be-157">Move-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="0a0be-157">Move-AzureRouteTable</span></span>](./Move-AzureRouteTable.md)

[<span data-ttu-id="0a0be-158">Move-AzureService</span><span class="sxs-lookup"><span data-stu-id="0a0be-158">Move-AzureService</span></span>](./Move-AzureService.md)

[<span data-ttu-id="0a0be-159">Move-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0a0be-159">Move-AzureStorageAccount</span></span>](./Move-AzureStorageAccount.md)


