---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
ms.openlocfilehash: d59bd7bea42e442aace3817f985098c4b2344ce4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845030"
---
# <span data-ttu-id="9d80e-101">Update-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="9d80e-101">Update-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="9d80e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9d80e-102">SYNOPSIS</span></span>
<span data-ttu-id="9d80e-103">Az Azure NetApp-fájlok (ANF) frissítését a megadható választható módosítók szerint frissítheti.</span><span class="sxs-lookup"><span data-stu-id="9d80e-103">Updates an Azure NetApp Files (ANF) volume according to the optional modifiers provided.</span></span>

## <span data-ttu-id="9d80e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9d80e-104">SYNTAX</span></span>

### <span data-ttu-id="9d80e-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9d80e-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d80e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d80e-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Tag <Hashtable>] -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d80e-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d80e-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>] [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-Tag <Hashtable>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9d80e-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d80e-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>] [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-Tag <Hashtable>] -InputObject <PSNetAppFilesVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d80e-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="9d80e-109">DESCRIPTION</span></span>
<span data-ttu-id="9d80e-110">Az **Update-AzNetAppFilesVolume** parancsmag ANF-kötetet frissít.</span><span class="sxs-lookup"><span data-stu-id="9d80e-110">The **Update-AzNetAppFilesVolume** cmdlet updates an ANF volume.</span></span>

## <span data-ttu-id="9d80e-111">Példák</span><span class="sxs-lookup"><span data-stu-id="9d80e-111">EXAMPLES</span></span>

### <span data-ttu-id="9d80e-112">Példa 1: ANF-kötet frissítése</span><span class="sxs-lookup"><span data-stu-id="9d80e-112">Example 1: Update an ANF volume</span></span>
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

<span data-ttu-id="9d80e-113">Ez a parancs frissíti a "MyAnfVolume" ANF-kötetet az új UsageThreshold méretével.</span><span class="sxs-lookup"><span data-stu-id="9d80e-113">This command updates the ANF volume "MyAnfVolume" with the new UsageThreshold size.</span></span>

## <span data-ttu-id="9d80e-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9d80e-114">PARAMETERS</span></span>

### <span data-ttu-id="9d80e-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9d80e-115">-AccountName</span></span>
<span data-ttu-id="9d80e-116">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="9d80e-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="9d80e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d80e-117">-DefaultProfile</span></span>
<span data-ttu-id="9d80e-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9d80e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d80e-119">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="9d80e-119">-ExportPolicy</span></span>
<span data-ttu-id="9d80e-120">Az exportálási házirendet reprezentáló Hashtable tömb</span><span class="sxs-lookup"><span data-stu-id="9d80e-120">A hashtable array which represents the export policy</span></span>

```yaml
Type: PSNetAppFilesVolumeExportPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d80e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9d80e-121">-InputObject</span></span>
<span data-ttu-id="9d80e-122">A frissítendő kötet objektum</span><span class="sxs-lookup"><span data-stu-id="9d80e-122">The volume object to update</span></span>

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

### <span data-ttu-id="9d80e-123">-Hely</span><span class="sxs-lookup"><span data-stu-id="9d80e-123">-Location</span></span>
<span data-ttu-id="9d80e-124">Az erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="9d80e-124">The location of the resource</span></span>

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

### <span data-ttu-id="9d80e-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9d80e-125">-Name</span></span>
<span data-ttu-id="9d80e-126">A ANF-kötet neve</span><span class="sxs-lookup"><span data-stu-id="9d80e-126">The name of the ANF volume</span></span>

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

### <span data-ttu-id="9d80e-127">-PoolName</span><span class="sxs-lookup"><span data-stu-id="9d80e-127">-PoolName</span></span>
<span data-ttu-id="9d80e-128">A ANF-készlet neve</span><span class="sxs-lookup"><span data-stu-id="9d80e-128">The name of the ANF pool</span></span>

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

### <span data-ttu-id="9d80e-129">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="9d80e-129">-PoolObject</span></span>
<span data-ttu-id="9d80e-130">A frissítendő kötetet tartalmazó Pool objektum</span><span class="sxs-lookup"><span data-stu-id="9d80e-130">The pool object containing the volume to update</span></span>

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

### <span data-ttu-id="9d80e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d80e-131">-ResourceGroupName</span></span>
<span data-ttu-id="9d80e-132">Az ANF-fiók erőforrás csoportja</span><span class="sxs-lookup"><span data-stu-id="9d80e-132">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="9d80e-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d80e-133">-ResourceId</span></span>
<span data-ttu-id="9d80e-134">A ANF-kötet erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="9d80e-134">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="9d80e-135">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="9d80e-135">-ServiceLevel</span></span>
<span data-ttu-id="9d80e-136">A ANF-kötet szolgáltatási szintje</span><span class="sxs-lookup"><span data-stu-id="9d80e-136">The service level of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d80e-137">-Címke</span><span class="sxs-lookup"><span data-stu-id="9d80e-137">-Tag</span></span>
<span data-ttu-id="9d80e-138">Egy Hashtable, amely az erőforrás címkéit képviseli</span><span class="sxs-lookup"><span data-stu-id="9d80e-138">A hashtable which represents resource tags</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d80e-139">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="9d80e-139">-UsageThreshold</span></span>
<span data-ttu-id="9d80e-140">A maximális tárterület kvótája a fájlrendszerben bájtban kifejezve</span><span class="sxs-lookup"><span data-stu-id="9d80e-140">The maximum storage quota allowed for a file system in bytes</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d80e-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9d80e-141">-Confirm</span></span>
<span data-ttu-id="9d80e-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9d80e-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d80e-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d80e-143">-WhatIf</span></span>
<span data-ttu-id="9d80e-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9d80e-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d80e-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9d80e-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d80e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d80e-146">CommonParameters</span></span>
<span data-ttu-id="9d80e-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9d80e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="9d80e-148">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d80e-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d80e-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9d80e-149">INPUTS</span></span>

### <span data-ttu-id="9d80e-150">System. String</span><span class="sxs-lookup"><span data-stu-id="9d80e-150">System.String</span></span>

### <span data-ttu-id="9d80e-151">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="9d80e-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="9d80e-152">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="9d80e-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="9d80e-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9d80e-153">OUTPUTS</span></span>

### <span data-ttu-id="9d80e-154">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="9d80e-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="9d80e-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9d80e-155">NOTES</span></span>

## <span data-ttu-id="9d80e-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9d80e-156">RELATED LINKS</span></span>
