---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
ms.openlocfilehash: dce91ee25cac4a716dc604e38f1ac38e5a3f3f1d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194099"
---
# <span data-ttu-id="f676e-101">New-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="f676e-101">New-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="f676e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f676e-102">SYNOPSIS</span></span>
<span data-ttu-id="f676e-103">Új Azure NetApp-fájlok (ANF-kötet) létrehozása.</span><span class="sxs-lookup"><span data-stu-id="f676e-103">Creates a new Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="f676e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f676e-104">SYNTAX</span></span>

### <span data-ttu-id="f676e-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f676e-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String> [-VolumeType <String>]
 -ServiceLevel <String> [-SnapshotId <String>] [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ReplicationObject <PSNetAppFilesReplicationObject>] [-ProtocolType <String[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f676e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f676e-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesVolume -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String>
 -ServiceLevel <String> [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ReplicationObject <PSNetAppFilesReplicationObject>] [-ProtocolType <String[]>] [-Tag <Hashtable>]
 -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f676e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f676e-107">DESCRIPTION</span></span>
<span data-ttu-id="f676e-108">A **New-AzNetAppFilesVolume** parancsmag ANF-kötetet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f676e-108">The **New-AzNetAppFilesVolume** cmdlet creates an ANF volume.</span></span>

## <span data-ttu-id="f676e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f676e-109">EXAMPLES</span></span>

### <span data-ttu-id="f676e-110">1. példa: ANF-kötet létrehozása</span><span class="sxs-lookup"><span data-stu-id="f676e-110">Example 1: Create an ANF volume</span></span>
```
PS C:\>New-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume" -l "westus2" -CreationToken "MyAnfVolume" -UsageThreshold 1099511627776 -ServiceLevel "Premium" -SubnetId "/subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyVnetName/subnets/MySubNetName"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
CreationToken     : MyAnfVolume
ServiceLevel      : Premium
UsageThreshold    : 1099511627776
ProvisioningState : Succeeded
SubnetId          : /subscriptions/f557b96d-2308-4a18-aae1-b8f7e7e70cc7/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyVnetName/subnets/default
```

<span data-ttu-id="f676e-111">Ezzel a paranccsal létrejön az új ANF-kötet "MyAnfVolume" a "MyAnfPool" alkalmazáskészleten belül.</span><span class="sxs-lookup"><span data-stu-id="f676e-111">This command creates the new ANF volume "MyAnfVolume" within the pool "MyAnfPool".</span></span>

## <span data-ttu-id="f676e-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f676e-112">PARAMETERS</span></span>

### <span data-ttu-id="f676e-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f676e-113">-AccountName</span></span>
<span data-ttu-id="f676e-114">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="f676e-114">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f676e-115">-CreationToken</span><span class="sxs-lookup"><span data-stu-id="f676e-115">-CreationToken</span></span>
<span data-ttu-id="f676e-116">A kötet egyedi fájlelérési útja</span><span class="sxs-lookup"><span data-stu-id="f676e-116">A unique file path for the volume</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f676e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f676e-117">-DefaultProfile</span></span>
<span data-ttu-id="f676e-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f676e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f676e-119">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="f676e-119">-ExportPolicy</span></span>
<span data-ttu-id="f676e-120">Az exportálási házirendet reprezentáló Hashtable tömb</span><span class="sxs-lookup"><span data-stu-id="f676e-120">A hashtable array which represents the export policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolumeExportPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f676e-121">-Hely</span><span class="sxs-lookup"><span data-stu-id="f676e-121">-Location</span></span>
<span data-ttu-id="f676e-122">Az erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="f676e-122">The location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f676e-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f676e-123">-Name</span></span>
<span data-ttu-id="f676e-124">A ANF-kötet neve</span><span class="sxs-lookup"><span data-stu-id="f676e-124">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f676e-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="f676e-125">-PoolName</span></span>
<span data-ttu-id="f676e-126">A ANF-készlet neve</span><span class="sxs-lookup"><span data-stu-id="f676e-126">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f676e-127">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="f676e-127">-PoolObject</span></span>
<span data-ttu-id="f676e-128">Az új kötet objektum készlete</span><span class="sxs-lookup"><span data-stu-id="f676e-128">The pool for the new volume object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f676e-129">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="f676e-129">-ProtocolType</span></span>
<span data-ttu-id="f676e-130">Az exportálási házirendet reprezentáló Hashtable tömb</span><span class="sxs-lookup"><span data-stu-id="f676e-130">A hashtable array which represents the export policy</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f676e-131">-ReplicationObject</span><span class="sxs-lookup"><span data-stu-id="f676e-131">-ReplicationObject</span></span>
<span data-ttu-id="f676e-132">A replikációs objektumot reprezentáló Hashtable tömb</span><span class="sxs-lookup"><span data-stu-id="f676e-132">A hashtable array which represents the replication object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesReplicationObject
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f676e-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f676e-133">-ResourceGroupName</span></span>
<span data-ttu-id="f676e-134">Az ANF-fiók erőforrás csoportja</span><span class="sxs-lookup"><span data-stu-id="f676e-134">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f676e-135">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="f676e-135">-ServiceLevel</span></span>
<span data-ttu-id="f676e-136">A ANF-kötet szolgáltatási szintje</span><span class="sxs-lookup"><span data-stu-id="f676e-136">The service level of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f676e-137">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="f676e-137">-SnapshotId</span></span>
<span data-ttu-id="f676e-138">Kötet létrehozása pillanatképből</span><span class="sxs-lookup"><span data-stu-id="f676e-138">Create volume from a snapshot.</span></span> <span data-ttu-id="f676e-139">A pillanatkép azonosításához használt UUID v4 vagy erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="f676e-139">UUID v4 or resource identifier used to identify the Snapshot</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f676e-140">– NetI</span><span class="sxs-lookup"><span data-stu-id="f676e-140">-SubnetId</span></span>
<span data-ttu-id="f676e-141">Egy delegált alhálózat Azure Resource URI azonosítója</span><span class="sxs-lookup"><span data-stu-id="f676e-141">The Azure Resource URI for a delegated subnet</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f676e-142">-Címke</span><span class="sxs-lookup"><span data-stu-id="f676e-142">-Tag</span></span>
<span data-ttu-id="f676e-143">Egy Hashtable, amely az erőforrás címkéit képviseli</span><span class="sxs-lookup"><span data-stu-id="f676e-143">A hashtable which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f676e-144">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="f676e-144">-UsageThreshold</span></span>
<span data-ttu-id="f676e-145">A maximális tárterület kvótája a fájlrendszerben bájtban kifejezve</span><span class="sxs-lookup"><span data-stu-id="f676e-145">The maximum storage quota allowed for a file system in bytes</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f676e-146">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="f676e-146">-VolumeType</span></span>
<span data-ttu-id="f676e-147">A ANF-kötet típusa</span><span class="sxs-lookup"><span data-stu-id="f676e-147">The type of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f676e-148">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f676e-148">-Confirm</span></span>
<span data-ttu-id="f676e-149">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f676e-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f676e-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f676e-150">-WhatIf</span></span>
<span data-ttu-id="f676e-151">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f676e-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f676e-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f676e-152">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f676e-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f676e-153">CommonParameters</span></span>
<span data-ttu-id="f676e-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f676e-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f676e-155">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f676e-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f676e-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f676e-156">INPUTS</span></span>

### <span data-ttu-id="f676e-157">System. String</span><span class="sxs-lookup"><span data-stu-id="f676e-157">System.String</span></span>

### <span data-ttu-id="f676e-158">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="f676e-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="f676e-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f676e-159">OUTPUTS</span></span>

### <span data-ttu-id="f676e-160">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="f676e-160">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="f676e-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f676e-161">NOTES</span></span>

## <span data-ttu-id="f676e-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f676e-162">RELATED LINKS</span></span>