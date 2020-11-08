---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/restore-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Restore-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Restore-AzNetAppFilesVolume.md
ms.openlocfilehash: 486bd44d3f48213fde6fb9b6c1d15a5683c1fd82
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180600"
---
# <span data-ttu-id="2ee53-101">Restore-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="2ee53-101">Restore-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="2ee53-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2ee53-102">SYNOPSIS</span></span>
<span data-ttu-id="2ee53-103">Kötet visszaállítása/visszaállítása a pillanatképek egyikéhez</span><span class="sxs-lookup"><span data-stu-id="2ee53-103">Restore/Revert a volume to one of its snapshots</span></span>

## <span data-ttu-id="2ee53-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2ee53-104">SYNTAX</span></span>

### <span data-ttu-id="2ee53-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2ee53-105">ByFieldsParameterSet (Default)</span></span>
```
Revert-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-SnapshotId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2ee53-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ee53-106">ByParentObjectParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -Name <String> -PoolObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ee53-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ee53-107">ByResourceIdParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ee53-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ee53-108">ByObjectParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ee53-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="2ee53-109">DESCRIPTION</span></span>
<span data-ttu-id="2ee53-110">Kötet visszaállítása/visszaállítása a SnapshotId paraméter megadott pillanatképre</span><span class="sxs-lookup"><span data-stu-id="2ee53-110">Restore/Revert a volume to the snapshot specified in the SnapshotId paramter</span></span>

## <span data-ttu-id="2ee53-111">Példák</span><span class="sxs-lookup"><span data-stu-id="2ee53-111">EXAMPLES</span></span>

### <span data-ttu-id="2ee53-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2ee53-112">Example 1</span></span>
```powershell
PS C:\> Restore-AzNetAppFilesVolume -ResourceGroupName "MyRG" -Location "westus2" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -SnapshotId 7d6e4069-6c78-6c61-7bf6-c60968e45fbf
```

<span data-ttu-id="2ee53-113">Ez a parancs visszaállítja/visszaállítja a kötet MyVolume egyik pillanatképét a 7d6e4069-6c78-6c61-7bf6-c60968e45fbf snapshotId.</span><span class="sxs-lookup"><span data-stu-id="2ee53-113">This command Restores/Reverts the volume MyVolume to one of its snapshots with the snapshotId of 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span></span>

## <span data-ttu-id="2ee53-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2ee53-114">PARAMETERS</span></span>

### <span data-ttu-id="2ee53-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2ee53-115">-AccountName</span></span>
<span data-ttu-id="2ee53-116">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="2ee53-116">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ee53-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ee53-117">-DefaultProfile</span></span>
<span data-ttu-id="2ee53-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2ee53-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ee53-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ee53-119">-InputObject</span></span>
<span data-ttu-id="2ee53-120">Eltávolítandó kötet objektum</span><span class="sxs-lookup"><span data-stu-id="2ee53-120">The volume object to remove</span></span>

```yaml
Type: PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ee53-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2ee53-121">-Name</span></span>
<span data-ttu-id="2ee53-122">A ANF-kötet neve</span><span class="sxs-lookup"><span data-stu-id="2ee53-122">The name of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ee53-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2ee53-123">-PassThru</span></span>
<span data-ttu-id="2ee53-124">A megadott kötet sikeres visszaállítása és visszaállítása</span><span class="sxs-lookup"><span data-stu-id="2ee53-124">Return whether the specified volume was successfully restored/reverted</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ee53-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="2ee53-125">-PoolName</span></span>
<span data-ttu-id="2ee53-126">A ANF-készlet neve</span><span class="sxs-lookup"><span data-stu-id="2ee53-126">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ee53-127">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="2ee53-127">-PoolObject</span></span>
<span data-ttu-id="2ee53-128">Az eltávolítandó kötetet tartalmazó Pool objektum</span><span class="sxs-lookup"><span data-stu-id="2ee53-128">The pool object containing the volume to remove</span></span>

```yaml
Type: PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ee53-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ee53-129">-ResourceGroupName</span></span>
<span data-ttu-id="2ee53-130">A ANF-kötet erőforrás csoportja</span><span class="sxs-lookup"><span data-stu-id="2ee53-130">The resource group of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ee53-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ee53-131">-ResourceId</span></span>
<span data-ttu-id="2ee53-132">A ANF-kötet erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="2ee53-132">The resource id of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ee53-133">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="2ee53-133">-SnapshotId</span></span>
<span data-ttu-id="2ee53-134">A pillanatkép SnapshotId</span><span class="sxs-lookup"><span data-stu-id="2ee53-134">SnapshotId of the snapshot.</span></span>
<span data-ttu-id="2ee53-135">Az UUID v4 a pillanatkép felismerésére szolgál</span><span class="sxs-lookup"><span data-stu-id="2ee53-135">UUID v4 used to identify the Snapshot</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ee53-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2ee53-136">-Confirm</span></span>
<span data-ttu-id="2ee53-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2ee53-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ee53-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ee53-138">-WhatIf</span></span>
<span data-ttu-id="2ee53-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2ee53-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ee53-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2ee53-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ee53-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ee53-141">CommonParameters</span></span>
<span data-ttu-id="2ee53-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2ee53-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ee53-143">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2ee53-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ee53-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ee53-144">INPUTS</span></span>

### <span data-ttu-id="2ee53-145">System. String</span><span class="sxs-lookup"><span data-stu-id="2ee53-145">System.String</span></span>

### <span data-ttu-id="2ee53-146">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="2ee53-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="2ee53-147">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="2ee53-147">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="2ee53-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ee53-148">OUTPUTS</span></span>

### <span data-ttu-id="2ee53-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2ee53-149">System.Boolean</span></span>

## <span data-ttu-id="2ee53-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2ee53-150">NOTES</span></span>

## <span data-ttu-id="2ee53-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2ee53-151">RELATED LINKS</span></span>
