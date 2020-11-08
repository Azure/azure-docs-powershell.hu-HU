---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
ms.openlocfilehash: c28b53fcd9b65198554f34cacd6f628d977e703a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194093"
---
# <span data-ttu-id="eb5ee-101">Update-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="eb5ee-101">Update-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="eb5ee-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eb5ee-102">SYNOPSIS</span></span>
<span data-ttu-id="eb5ee-103">Az Azure NetApp-fájlok (ANF) frissítését a megadható választható módosítók szerint frissítheti.</span><span class="sxs-lookup"><span data-stu-id="eb5ee-103">Updates an Azure NetApp Files (ANF) volume according to the optional modifiers provided.</span></span>

## <span data-ttu-id="eb5ee-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eb5ee-104">SYNTAX</span></span>

### <span data-ttu-id="eb5ee-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="eb5ee-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb5ee-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb5ee-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Tag <Hashtable>] -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb5ee-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb5ee-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb5ee-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb5ee-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Tag <Hashtable>] -InputObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb5ee-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="eb5ee-109">DESCRIPTION</span></span>
<span data-ttu-id="eb5ee-110">Az **Update-AzNetAppFilesVolume** parancsmag ANF-kötetet frissít.</span><span class="sxs-lookup"><span data-stu-id="eb5ee-110">The **Update-AzNetAppFilesVolume** cmdlet updates an ANF volume.</span></span>

## <span data-ttu-id="eb5ee-111">Példák</span><span class="sxs-lookup"><span data-stu-id="eb5ee-111">EXAMPLES</span></span>

### <span data-ttu-id="eb5ee-112">Példa 1: ANF-kötet frissítése</span><span class="sxs-lookup"><span data-stu-id="eb5ee-112">Example 1: Update an ANF volume</span></span>
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

<span data-ttu-id="eb5ee-113">Ez a parancs frissíti a "MyAnfVolume" ANF-kötetet az új UsageThreshold méretével.</span><span class="sxs-lookup"><span data-stu-id="eb5ee-113">This command updates the ANF volume "MyAnfVolume" with the new UsageThreshold size.</span></span>

## <span data-ttu-id="eb5ee-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eb5ee-114">PARAMETERS</span></span>

### <span data-ttu-id="eb5ee-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="eb5ee-115">-AccountName</span></span>
<span data-ttu-id="eb5ee-116">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="eb5ee-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="eb5ee-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb5ee-117">-DefaultProfile</span></span>
<span data-ttu-id="eb5ee-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eb5ee-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb5ee-119">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="eb5ee-119">-ExportPolicy</span></span>
<span data-ttu-id="eb5ee-120">Az exportálási házirendet reprezentáló Hashtable tömb</span><span class="sxs-lookup"><span data-stu-id="eb5ee-120">A hashtable array which represents the export policy</span></span>

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

### <span data-ttu-id="eb5ee-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eb5ee-121">-InputObject</span></span>
<span data-ttu-id="eb5ee-122">A frissítendő kötet objektum</span><span class="sxs-lookup"><span data-stu-id="eb5ee-122">The volume object to update</span></span>

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

### <span data-ttu-id="eb5ee-123">-Hely</span><span class="sxs-lookup"><span data-stu-id="eb5ee-123">-Location</span></span>
<span data-ttu-id="eb5ee-124">Az erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="eb5ee-124">The location of the resource</span></span>

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

### <span data-ttu-id="eb5ee-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="eb5ee-125">-Name</span></span>
<span data-ttu-id="eb5ee-126">A ANF-kötet neve</span><span class="sxs-lookup"><span data-stu-id="eb5ee-126">The name of the ANF volume</span></span>

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

### <span data-ttu-id="eb5ee-127">-PoolName</span><span class="sxs-lookup"><span data-stu-id="eb5ee-127">-PoolName</span></span>
<span data-ttu-id="eb5ee-128">A ANF-készlet neve</span><span class="sxs-lookup"><span data-stu-id="eb5ee-128">The name of the ANF pool</span></span>

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

### <span data-ttu-id="eb5ee-129">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="eb5ee-129">-PoolObject</span></span>
<span data-ttu-id="eb5ee-130">A frissítendő kötetet tartalmazó Pool objektum</span><span class="sxs-lookup"><span data-stu-id="eb5ee-130">The pool object containing the volume to update</span></span>

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

### <span data-ttu-id="eb5ee-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb5ee-131">-ResourceGroupName</span></span>
<span data-ttu-id="eb5ee-132">Az ANF-fiók erőforrás csoportja</span><span class="sxs-lookup"><span data-stu-id="eb5ee-132">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="eb5ee-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb5ee-133">-ResourceId</span></span>
<span data-ttu-id="eb5ee-134">A ANF-kötet erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="eb5ee-134">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="eb5ee-135">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="eb5ee-135">-ServiceLevel</span></span>
<span data-ttu-id="eb5ee-136">A ANF-kötet szolgáltatási szintje</span><span class="sxs-lookup"><span data-stu-id="eb5ee-136">The service level of the ANF volume</span></span>

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

### <span data-ttu-id="eb5ee-137">-Címke</span><span class="sxs-lookup"><span data-stu-id="eb5ee-137">-Tag</span></span>
<span data-ttu-id="eb5ee-138">Egy Hashtable, amely az erőforrás címkéit képviseli</span><span class="sxs-lookup"><span data-stu-id="eb5ee-138">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="eb5ee-139">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="eb5ee-139">-UsageThreshold</span></span>
<span data-ttu-id="eb5ee-140">A maximális tárterület kvótája a fájlrendszerben bájtban kifejezve</span><span class="sxs-lookup"><span data-stu-id="eb5ee-140">The maximum storage quota allowed for a file system in bytes</span></span>

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

### <span data-ttu-id="eb5ee-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="eb5ee-141">-Confirm</span></span>
<span data-ttu-id="eb5ee-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="eb5ee-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb5ee-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb5ee-143">-WhatIf</span></span>
<span data-ttu-id="eb5ee-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="eb5ee-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb5ee-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="eb5ee-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb5ee-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb5ee-146">CommonParameters</span></span>
<span data-ttu-id="eb5ee-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eb5ee-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb5ee-148">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="eb5ee-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb5ee-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb5ee-149">INPUTS</span></span>

### <span data-ttu-id="eb5ee-150">System. String</span><span class="sxs-lookup"><span data-stu-id="eb5ee-150">System.String</span></span>

### <span data-ttu-id="eb5ee-151">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="eb5ee-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="eb5ee-152">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="eb5ee-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="eb5ee-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb5ee-153">OUTPUTS</span></span>

### <span data-ttu-id="eb5ee-154">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="eb5ee-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="eb5ee-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eb5ee-155">NOTES</span></span>

## <span data-ttu-id="eb5ee-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eb5ee-156">RELATED LINKS</span></span>