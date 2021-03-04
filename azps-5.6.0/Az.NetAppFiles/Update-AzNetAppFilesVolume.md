---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/update-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
ms.openlocfilehash: b7947f4224c667ed8332b0f3206588dda49fd1af
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926650"
---
# <span data-ttu-id="f60b0-101">Update-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="f60b0-101">Update-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="f60b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f60b0-102">SYNOPSIS</span></span>
<span data-ttu-id="f60b0-103">Frissíti az Azure NetApp-fájlok (ANF) kötetét a megadott opcionális módosítóknak megfelelően.</span><span class="sxs-lookup"><span data-stu-id="f60b0-103">Updates an Azure NetApp Files (ANF) volume according to the optional modifiers provided.</span></span>

## <span data-ttu-id="f60b0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f60b0-104">SYNTAX</span></span>

### <span data-ttu-id="f60b0-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f60b0-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f60b0-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f60b0-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f60b0-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f60b0-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f60b0-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f60b0-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] -InputObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f60b0-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f60b0-109">DESCRIPTION</span></span>
<span data-ttu-id="f60b0-110">Az **Update-AzNetAppFilesVolume** parancsmag frissíti az ANF-kötetet.</span><span class="sxs-lookup"><span data-stu-id="f60b0-110">The **Update-AzNetAppFilesVolume** cmdlet updates an ANF volume.</span></span>

## <span data-ttu-id="f60b0-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f60b0-111">EXAMPLES</span></span>

### <span data-ttu-id="f60b0-112">1. példa: ANF-hangerő frissítése</span><span class="sxs-lookup"><span data-stu-id="f60b0-112">Example 1: Update an ANF volume</span></span>
```
PS C:\>Update-AzNetAppFilesVolume -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume" -UsageThreshold Size

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
CreationToken     : MyAnfVolume
ServiceLevel      : Premium
UsageThreshold    : 2199023255552
ProvisioningState : Succeeded
SubnetId          : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyRG-vnet/subnets/default
```

<span data-ttu-id="f60b0-113">Ez a parancs frissíti az ANF "MyAnfVolume" hangerejét az új UsageThreshold méretével.</span><span class="sxs-lookup"><span data-stu-id="f60b0-113">This command updates the ANF volume "MyAnfVolume" with the new UsageThreshold size.</span></span>

## <span data-ttu-id="f60b0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f60b0-114">PARAMETERS</span></span>

### <span data-ttu-id="f60b0-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f60b0-115">-AccountName</span></span>
<span data-ttu-id="f60b0-116">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="f60b0-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="f60b0-117">-Backup</span><span class="sxs-lookup"><span data-stu-id="f60b0-117">-Backup</span></span>
<span data-ttu-id="f60b0-118">A biztonsági másolat objektumát képviselő hashtable array</span><span class="sxs-lookup"><span data-stu-id="f60b0-118">A hashtable array which represents the backup object</span></span>

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

### <span data-ttu-id="f60b0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f60b0-119">-DefaultProfile</span></span>
<span data-ttu-id="f60b0-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f60b0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f60b0-121">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="f60b0-121">-ExportPolicy</span></span>
<span data-ttu-id="f60b0-122">Az exportálási házirendet képviselő kivonatos tömb</span><span class="sxs-lookup"><span data-stu-id="f60b0-122">A hashtable array which represents the export policy</span></span>

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

### <span data-ttu-id="f60b0-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f60b0-123">-InputObject</span></span>
<span data-ttu-id="f60b0-124">A frissítendve elérhető hangerő-objektum</span><span class="sxs-lookup"><span data-stu-id="f60b0-124">The volume object to update</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f60b0-125">-Location</span><span class="sxs-lookup"><span data-stu-id="f60b0-125">-Location</span></span>
<span data-ttu-id="f60b0-126">Az erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="f60b0-126">The location of the resource</span></span>

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

### <span data-ttu-id="f60b0-127">-Name</span><span class="sxs-lookup"><span data-stu-id="f60b0-127">-Name</span></span>
<span data-ttu-id="f60b0-128">Az ANF-kötet neve</span><span class="sxs-lookup"><span data-stu-id="f60b0-128">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f60b0-129">-PoolName</span><span class="sxs-lookup"><span data-stu-id="f60b0-129">-PoolName</span></span>
<span data-ttu-id="f60b0-130">Az ANF-készlet neve</span><span class="sxs-lookup"><span data-stu-id="f60b0-130">The name of the ANF pool</span></span>

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

### <span data-ttu-id="f60b0-131">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="f60b0-131">-PoolObject</span></span>
<span data-ttu-id="f60b0-132">A frissítend0 kötetet tartalmazó készletobjektum</span><span class="sxs-lookup"><span data-stu-id="f60b0-132">The pool object containing the volume to update</span></span>

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

### <span data-ttu-id="f60b0-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f60b0-133">-ResourceGroupName</span></span>
<span data-ttu-id="f60b0-134">Az ANF-fiók erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="f60b0-134">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="f60b0-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f60b0-135">-ResourceId</span></span>
<span data-ttu-id="f60b0-136">Az ANF-mennyiség erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="f60b0-136">The resource id of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f60b0-137">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="f60b0-137">-ServiceLevel</span></span>
<span data-ttu-id="f60b0-138">Az ANF-kötet szolgáltatási szintje</span><span class="sxs-lookup"><span data-stu-id="f60b0-138">The service level of the ANF volume</span></span>

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

### <span data-ttu-id="f60b0-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="f60b0-139">-Tag</span></span>
<span data-ttu-id="f60b0-140">Erőforráscímkéket képviselő hashtable</span><span class="sxs-lookup"><span data-stu-id="f60b0-140">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="f60b0-141">-Átviteli sebességMibps</span><span class="sxs-lookup"><span data-stu-id="f60b0-141">-ThroughputMibps</span></span>
<span data-ttu-id="f60b0-142">Az ezzel a mennyiséghez elérhető maximális átviteli sebesség Mibps-ként</span><span class="sxs-lookup"><span data-stu-id="f60b0-142">Maximum throughput in Mibps that can be achieved by this volume</span></span>

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

### <span data-ttu-id="f60b0-143">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="f60b0-143">-UsageThreshold</span></span>
<span data-ttu-id="f60b0-144">A fájlrendszerhez bájtban engedélyezett maximális tárterületkvóta</span><span class="sxs-lookup"><span data-stu-id="f60b0-144">The maximum storage quota allowed for a file system in bytes</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f60b0-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f60b0-145">-Confirm</span></span>
<span data-ttu-id="f60b0-146">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f60b0-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f60b0-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f60b0-147">-WhatIf</span></span>
<span data-ttu-id="f60b0-148">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f60b0-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f60b0-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f60b0-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f60b0-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f60b0-150">CommonParameters</span></span>
<span data-ttu-id="f60b0-151">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f60b0-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f60b0-152">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f60b0-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f60b0-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f60b0-153">INPUTS</span></span>

### <span data-ttu-id="f60b0-154">System.String</span><span class="sxs-lookup"><span data-stu-id="f60b0-154">System.String</span></span>

### <span data-ttu-id="f60b0-155">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="f60b0-155">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="f60b0-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="f60b0-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="f60b0-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f60b0-157">OUTPUTS</span></span>

### <span data-ttu-id="f60b0-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="f60b0-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="f60b0-159">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f60b0-159">NOTES</span></span>

## <span data-ttu-id="f60b0-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f60b0-160">RELATED LINKS</span></span>
