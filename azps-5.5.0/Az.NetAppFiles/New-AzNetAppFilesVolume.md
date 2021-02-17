---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
ms.openlocfilehash: 2326551a2b6a03e1904e8d0d90663ee796ccaa46
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147250"
---
# <span data-ttu-id="8cc03-101">New-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="8cc03-101">New-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="8cc03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8cc03-102">SYNOPSIS</span></span>
<span data-ttu-id="8cc03-103">Új Azure NetApp-fájlok (ANF)kötetet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="8cc03-103">Creates a new Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="8cc03-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8cc03-104">SYNTAX</span></span>

### <span data-ttu-id="8cc03-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8cc03-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String> [-VolumeType <String>]
 -ServiceLevel <String> [-SnapshotId <String>] [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ReplicationObject <PSNetAppFilesReplicationObject>] [-Snapshot <PSNetAppFilesVolumeSnapshot>]
 [-Backup <PSNetAppFilesVolumeBackupProperties>] [-ProtocolType <String[]>] [-SnapshotDirectoryVisible]
 [-BackupId <String>] [-SecurityStyle <String>] [-ThroughputMibps <Double>] [-KerberosEnabled]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cc03-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8cc03-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesVolume -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String>
 -ServiceLevel <String> [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ReplicationObject <PSNetAppFilesReplicationObject>] [-Snapshot <PSNetAppFilesVolumeSnapshot>]
 [-Backup <PSNetAppFilesVolumeBackupProperties>] [-ProtocolType <String[]>] [-SnapshotDirectoryVisible]
 [-SecurityStyle <String>] [-ThroughputMibps <Double>] [-KerberosEnabled] [-Tag <Hashtable>]
 -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8cc03-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8cc03-107">DESCRIPTION</span></span>
<span data-ttu-id="8cc03-108">A **New-AzNetAppFilesVolume** parancsmag ANF-kötetet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="8cc03-108">The **New-AzNetAppFilesVolume** cmdlet creates an ANF volume.</span></span>

## <span data-ttu-id="8cc03-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8cc03-109">EXAMPLES</span></span>

### <span data-ttu-id="8cc03-110">1. példa: ANF-hangerő létrehozása</span><span class="sxs-lookup"><span data-stu-id="8cc03-110">Example 1: Create an ANF volume</span></span>
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

<span data-ttu-id="8cc03-111">Ez a parancs létrehozza az új ANF-kötetet (MyAnfVolume) a "MyAnfPool" készleten belül.</span><span class="sxs-lookup"><span data-stu-id="8cc03-111">This command creates the new ANF volume "MyAnfVolume" within the pool "MyAnfPool".</span></span>

## <span data-ttu-id="8cc03-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8cc03-112">PARAMETERS</span></span>

### <span data-ttu-id="8cc03-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8cc03-113">-AccountName</span></span>
<span data-ttu-id="8cc03-114">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="8cc03-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="8cc03-115">-Backup</span><span class="sxs-lookup"><span data-stu-id="8cc03-115">-Backup</span></span>
<span data-ttu-id="8cc03-116">A biztonsági másolat objektumát képviselő hashtable array</span><span class="sxs-lookup"><span data-stu-id="8cc03-116">A hashtable array which represents the backup object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolumeBackupProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cc03-117">-BackupId</span><span class="sxs-lookup"><span data-stu-id="8cc03-117">-BackupId</span></span>
<span data-ttu-id="8cc03-118">Biztonsági másolat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8cc03-118">Backup ID.</span></span> <span data-ttu-id="8cc03-119">UUID v4 vagy erőforrás-azonosító a biztonsági másolat azonosításához</span><span class="sxs-lookup"><span data-stu-id="8cc03-119">UUID v4 or resource identifier used to identify the Backup</span></span>

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

### <span data-ttu-id="8cc03-120">-CreationToken</span><span class="sxs-lookup"><span data-stu-id="8cc03-120">-CreationToken</span></span>
<span data-ttu-id="8cc03-121">A hangerő egyedi elérési útja</span><span class="sxs-lookup"><span data-stu-id="8cc03-121">A unique file path for the volume</span></span>

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

### <span data-ttu-id="8cc03-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cc03-122">-DefaultProfile</span></span>
<span data-ttu-id="8cc03-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8cc03-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cc03-124">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="8cc03-124">-ExportPolicy</span></span>
<span data-ttu-id="8cc03-125">Az exportálási házirendet képviselő kivonatos tömb</span><span class="sxs-lookup"><span data-stu-id="8cc03-125">A hashtable array which represents the export policy</span></span>

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

### <span data-ttu-id="8cc03-126">-KerberosEnabled</span><span class="sxs-lookup"><span data-stu-id="8cc03-126">-KerberosEnabled</span></span>
<span data-ttu-id="8cc03-127">A Kerberos-kompatibilis kötetek leírásának</span><span class="sxs-lookup"><span data-stu-id="8cc03-127">Describe if a volume is Kerberos Enabled</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cc03-128">-Location</span><span class="sxs-lookup"><span data-stu-id="8cc03-128">-Location</span></span>
<span data-ttu-id="8cc03-129">Az erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="8cc03-129">The location of the resource</span></span>

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

### <span data-ttu-id="8cc03-130">-Name</span><span class="sxs-lookup"><span data-stu-id="8cc03-130">-Name</span></span>
<span data-ttu-id="8cc03-131">Az ANF-kötet neve</span><span class="sxs-lookup"><span data-stu-id="8cc03-131">The name of the ANF volume</span></span>

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

### <span data-ttu-id="8cc03-132">-PoolName</span><span class="sxs-lookup"><span data-stu-id="8cc03-132">-PoolName</span></span>
<span data-ttu-id="8cc03-133">Az ANF-készlet neve</span><span class="sxs-lookup"><span data-stu-id="8cc03-133">The name of the ANF pool</span></span>

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

### <span data-ttu-id="8cc03-134">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="8cc03-134">-PoolObject</span></span>
<span data-ttu-id="8cc03-135">Az új kötetobjektum készlete</span><span class="sxs-lookup"><span data-stu-id="8cc03-135">The pool for the new volume object</span></span>

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

### <span data-ttu-id="8cc03-136">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="8cc03-136">-ProtocolType</span></span>
<span data-ttu-id="8cc03-137">Az exportálási házirendet képviselő kivonatos tömb</span><span class="sxs-lookup"><span data-stu-id="8cc03-137">A hashtable array which represents the export policy</span></span>

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

### <span data-ttu-id="8cc03-138">-ReplicationObject</span><span class="sxs-lookup"><span data-stu-id="8cc03-138">-ReplicationObject</span></span>
<span data-ttu-id="8cc03-139">A replikációs objektumot képviselő hashtable array</span><span class="sxs-lookup"><span data-stu-id="8cc03-139">A hashtable array which represents the replication object</span></span>

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

### <span data-ttu-id="8cc03-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cc03-140">-ResourceGroupName</span></span>
<span data-ttu-id="8cc03-141">Az ANF-fiók erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="8cc03-141">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="8cc03-142">-SecurityStyle</span><span class="sxs-lookup"><span data-stu-id="8cc03-142">-SecurityStyle</span></span>
<span data-ttu-id="8cc03-143">A hangerő biztonsági stílusa.</span><span class="sxs-lookup"><span data-stu-id="8cc03-143">The security style of volume.</span></span> <span data-ttu-id="8cc03-144">Lehetséges értékek: 'ntfs', 'unix'</span><span class="sxs-lookup"><span data-stu-id="8cc03-144">Possible values include: 'ntfs', 'unix'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cc03-145">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="8cc03-145">-ServiceLevel</span></span>
<span data-ttu-id="8cc03-146">Az ANF-kötet szolgáltatási szintje</span><span class="sxs-lookup"><span data-stu-id="8cc03-146">The service level of the ANF volume</span></span>

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

### <span data-ttu-id="8cc03-147">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="8cc03-147">-Snapshot</span></span>
<span data-ttu-id="8cc03-148">A pillanatfelvételi objektumot képviselő hashtable array</span><span class="sxs-lookup"><span data-stu-id="8cc03-148">A hashtable array which represents the snapshot object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolumeSnapshot
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cc03-149">-SnapshotDirectoryVisible</span><span class="sxs-lookup"><span data-stu-id="8cc03-149">-SnapshotDirectoryVisible</span></span>
<span data-ttu-id="8cc03-150">Ha engedélyezve van (igaz), a kötet egy írásra képes .snapshot könyvtárat fog tartalmazni, amely hozzáférést biztosít a kötet egyes pillanatképeihez (alapértelmezés szerint igaz)</span><span class="sxs-lookup"><span data-stu-id="8cc03-150">If enabled (true) the volume will contain a read-only .snapshot directory which provides access to each of the volume's snapshots (default to true)</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cc03-151">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="8cc03-151">-SnapshotId</span></span>
<span data-ttu-id="8cc03-152">Hangerő létrehozása pillanatfelvételből.</span><span class="sxs-lookup"><span data-stu-id="8cc03-152">Create volume from a snapshot.</span></span> <span data-ttu-id="8cc03-153">UUID v4 vagy resource identifier used to identify the Snapshot</span><span class="sxs-lookup"><span data-stu-id="8cc03-153">UUID v4 or resource identifier used to identify the Snapshot</span></span>

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

### <span data-ttu-id="8cc03-154">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="8cc03-154">-SubnetId</span></span>
<span data-ttu-id="8cc03-155">Az Azure Resource URI egy delegált alhálózathoz</span><span class="sxs-lookup"><span data-stu-id="8cc03-155">The Azure Resource URI for a delegated subnet</span></span>

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

### <span data-ttu-id="8cc03-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="8cc03-156">-Tag</span></span>
<span data-ttu-id="8cc03-157">Erőforráscímkéket képviselő hashtable</span><span class="sxs-lookup"><span data-stu-id="8cc03-157">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="8cc03-158">-Átviteli sebességMibps</span><span class="sxs-lookup"><span data-stu-id="8cc03-158">-ThroughputMibps</span></span>
<span data-ttu-id="8cc03-159">Az ezzel a mennyiséghez elérhető maximális átviteli sebesség Mibps-ként</span><span class="sxs-lookup"><span data-stu-id="8cc03-159">Maximum throughput in Mibps that can be achieved by this volume</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cc03-160">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="8cc03-160">-UsageThreshold</span></span>
<span data-ttu-id="8cc03-161">A fájlrendszerhez bájtban engedélyezett maximális tárterületkvóta</span><span class="sxs-lookup"><span data-stu-id="8cc03-161">The maximum storage quota allowed for a file system in bytes</span></span>

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

### <span data-ttu-id="8cc03-162">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="8cc03-162">-VolumeType</span></span>
<span data-ttu-id="8cc03-163">Az ANF-hangerő típusa</span><span class="sxs-lookup"><span data-stu-id="8cc03-163">The type of the ANF volume</span></span>

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

### <span data-ttu-id="8cc03-164">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8cc03-164">-Confirm</span></span>
<span data-ttu-id="8cc03-165">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8cc03-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cc03-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cc03-166">-WhatIf</span></span>
<span data-ttu-id="8cc03-167">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8cc03-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cc03-168">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8cc03-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cc03-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cc03-169">CommonParameters</span></span>
<span data-ttu-id="8cc03-170">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cc03-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cc03-171">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8cc03-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cc03-172">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8cc03-172">INPUTS</span></span>

### <span data-ttu-id="8cc03-173">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="8cc03-173">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="8cc03-174">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8cc03-174">OUTPUTS</span></span>

### <span data-ttu-id="8cc03-175">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="8cc03-175">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="8cc03-176">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8cc03-176">NOTES</span></span>

## <span data-ttu-id="8cc03-177">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8cc03-177">RELATED LINKS</span></span>
