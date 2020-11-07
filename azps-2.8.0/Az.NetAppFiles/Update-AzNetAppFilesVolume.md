---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
ms.openlocfilehash: 353d0595d4d3667a9324eab41170a2b10f916713
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837423"
---
# <span data-ttu-id="b3715-101">Update-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="b3715-101">Update-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="b3715-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b3715-102">SYNOPSIS</span></span>
<span data-ttu-id="b3715-103">Az Azure NetApp-fájlok (ANF) frissítését a megadható választható módosítók szerint frissítheti.</span><span class="sxs-lookup"><span data-stu-id="b3715-103">Updates an Azure NetApp Files (ANF) volume according to the optional modifiers provided.</span></span>

## <span data-ttu-id="b3715-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b3715-104">SYNTAX</span></span>

### <span data-ttu-id="b3715-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b3715-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3715-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3715-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Tag <Hashtable>] -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3715-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3715-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>] [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-Tag <Hashtable>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b3715-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3715-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>] [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-Tag <Hashtable>] -InputObject <PSNetAppFilesVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3715-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="b3715-109">DESCRIPTION</span></span>
<span data-ttu-id="b3715-110">Az **Update-AzNetAppFilesVolume** parancsmag ANF-kötetet frissít.</span><span class="sxs-lookup"><span data-stu-id="b3715-110">The **Update-AzNetAppFilesVolume** cmdlet updates an ANF volume.</span></span>

## <span data-ttu-id="b3715-111">Példák</span><span class="sxs-lookup"><span data-stu-id="b3715-111">EXAMPLES</span></span>

### <span data-ttu-id="b3715-112">Példa 1: ANF-kötet frissítése</span><span class="sxs-lookup"><span data-stu-id="b3715-112">Example 1: Update an ANF volume</span></span>
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

<span data-ttu-id="b3715-113">Ez a parancs frissíti a "MyAnfVolume" ANF-kötetet az új UsageThreshold méretével.</span><span class="sxs-lookup"><span data-stu-id="b3715-113">This command updates the ANF volume "MyAnfVolume" with the new UsageThreshold size.</span></span>

## <span data-ttu-id="b3715-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b3715-114">PARAMETERS</span></span>

### <span data-ttu-id="b3715-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b3715-115">-AccountName</span></span>
<span data-ttu-id="b3715-116">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="b3715-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="b3715-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3715-117">-DefaultProfile</span></span>
<span data-ttu-id="b3715-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b3715-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3715-119">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="b3715-119">-ExportPolicy</span></span>
<span data-ttu-id="b3715-120">Az exportálási házirendet reprezentáló Hashtable tömb</span><span class="sxs-lookup"><span data-stu-id="b3715-120">A hashtable array which represents the export policy</span></span>

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

### <span data-ttu-id="b3715-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3715-121">-InputObject</span></span>
<span data-ttu-id="b3715-122">A frissítendő kötet objektum</span><span class="sxs-lookup"><span data-stu-id="b3715-122">The volume object to update</span></span>

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

### <span data-ttu-id="b3715-123">-Hely</span><span class="sxs-lookup"><span data-stu-id="b3715-123">-Location</span></span>
<span data-ttu-id="b3715-124">Az erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="b3715-124">The location of the resource</span></span>

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

### <span data-ttu-id="b3715-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b3715-125">-Name</span></span>
<span data-ttu-id="b3715-126">A ANF-kötet neve</span><span class="sxs-lookup"><span data-stu-id="b3715-126">The name of the ANF volume</span></span>

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

### <span data-ttu-id="b3715-127">-PoolName</span><span class="sxs-lookup"><span data-stu-id="b3715-127">-PoolName</span></span>
<span data-ttu-id="b3715-128">A ANF-készlet neve</span><span class="sxs-lookup"><span data-stu-id="b3715-128">The name of the ANF pool</span></span>

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

### <span data-ttu-id="b3715-129">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="b3715-129">-PoolObject</span></span>
<span data-ttu-id="b3715-130">A frissítendő kötetet tartalmazó Pool objektum</span><span class="sxs-lookup"><span data-stu-id="b3715-130">The pool object containing the volume to update</span></span>

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

### <span data-ttu-id="b3715-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3715-131">-ResourceGroupName</span></span>
<span data-ttu-id="b3715-132">Az ANF-fiók erőforrás csoportja</span><span class="sxs-lookup"><span data-stu-id="b3715-132">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="b3715-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3715-133">-ResourceId</span></span>
<span data-ttu-id="b3715-134">A ANF-kötet erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="b3715-134">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="b3715-135">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="b3715-135">-ServiceLevel</span></span>
<span data-ttu-id="b3715-136">A ANF-kötet szolgáltatási szintje</span><span class="sxs-lookup"><span data-stu-id="b3715-136">The service level of the ANF volume</span></span>

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

### <span data-ttu-id="b3715-137">-Címke</span><span class="sxs-lookup"><span data-stu-id="b3715-137">-Tag</span></span>
<span data-ttu-id="b3715-138">Egy Hashtable, amely az erőforrás címkéit képviseli</span><span class="sxs-lookup"><span data-stu-id="b3715-138">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="b3715-139">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="b3715-139">-UsageThreshold</span></span>
<span data-ttu-id="b3715-140">A maximális tárterület kvótája a fájlrendszerben bájtban kifejezve</span><span class="sxs-lookup"><span data-stu-id="b3715-140">The maximum storage quota allowed for a file system in bytes</span></span>

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

### <span data-ttu-id="b3715-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b3715-141">-Confirm</span></span>
<span data-ttu-id="b3715-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b3715-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3715-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3715-143">-WhatIf</span></span>
<span data-ttu-id="b3715-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b3715-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3715-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b3715-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3715-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3715-146">CommonParameters</span></span>
<span data-ttu-id="b3715-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b3715-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b3715-148">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3715-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3715-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b3715-149">INPUTS</span></span>

### <span data-ttu-id="b3715-150">System. String</span><span class="sxs-lookup"><span data-stu-id="b3715-150">System.String</span></span>

### <span data-ttu-id="b3715-151">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="b3715-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="b3715-152">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="b3715-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="b3715-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b3715-153">OUTPUTS</span></span>

### <span data-ttu-id="b3715-154">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="b3715-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="b3715-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b3715-155">NOTES</span></span>

## <span data-ttu-id="b3715-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b3715-156">RELATED LINKS</span></span>
