---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
ms.openlocfilehash: cad30d489b53ccfd9f45cbc619ce4384cc904903
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837432"
---
# <span data-ttu-id="69903-101">New-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="69903-101">New-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="69903-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="69903-102">SYNOPSIS</span></span>
<span data-ttu-id="69903-103">Új Azure NetApp-fájlok (ANF-kötet) létrehozása.</span><span class="sxs-lookup"><span data-stu-id="69903-103">Creates a new Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="69903-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="69903-104">SYNTAX</span></span>

### <span data-ttu-id="69903-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="69903-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String> -ServiceLevel <String>
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ProtocolType <System.String[]>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69903-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="69903-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesVolume -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String>
 -ServiceLevel <String> [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ProtocolType <System.String[]>]
 [-Tag <Hashtable>] -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69903-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="69903-107">DESCRIPTION</span></span>
<span data-ttu-id="69903-108">A **New-AzNetAppFilesVolume** parancsmag ANF-kötetet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="69903-108">The **New-AzNetAppFilesVolume** cmdlet creates an ANF volume.</span></span>

## <span data-ttu-id="69903-109">Példák</span><span class="sxs-lookup"><span data-stu-id="69903-109">EXAMPLES</span></span>

### <span data-ttu-id="69903-110">1. példa: ANF-kötet létrehozása</span><span class="sxs-lookup"><span data-stu-id="69903-110">Example 1: Create an ANF volume</span></span>
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

<span data-ttu-id="69903-111">Ezzel a paranccsal létrejön az új ANF-kötet "MyAnfVolume" a "MyAnfPool" alkalmazáskészleten belül.</span><span class="sxs-lookup"><span data-stu-id="69903-111">This command creates the new ANF volume "MyAnfVolume" within the pool "MyAnfPool".</span></span>

## <span data-ttu-id="69903-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="69903-112">PARAMETERS</span></span>

### <span data-ttu-id="69903-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="69903-113">-AccountName</span></span>
<span data-ttu-id="69903-114">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="69903-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="69903-115">-CreationToken</span><span class="sxs-lookup"><span data-stu-id="69903-115">-CreationToken</span></span>
<span data-ttu-id="69903-116">A kötet egyedi fájlelérési útja</span><span class="sxs-lookup"><span data-stu-id="69903-116">A unique file path for the volume</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69903-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69903-117">-DefaultProfile</span></span>
<span data-ttu-id="69903-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="69903-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69903-119">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="69903-119">-ExportPolicy</span></span>
<span data-ttu-id="69903-120">Az exportálási házirendet reprezentáló Hashtable tömb</span><span class="sxs-lookup"><span data-stu-id="69903-120">A hashtable array which represents the export policy</span></span>

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

### <span data-ttu-id="69903-121">-Hely</span><span class="sxs-lookup"><span data-stu-id="69903-121">-Location</span></span>
<span data-ttu-id="69903-122">Az erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="69903-122">The location of the resource</span></span>

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

### <span data-ttu-id="69903-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="69903-123">-Name</span></span>
<span data-ttu-id="69903-124">A ANF-kötet neve</span><span class="sxs-lookup"><span data-stu-id="69903-124">The name of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69903-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="69903-125">-PoolName</span></span>
<span data-ttu-id="69903-126">A ANF-készlet neve</span><span class="sxs-lookup"><span data-stu-id="69903-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="69903-127">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="69903-127">-PoolObject</span></span>
<span data-ttu-id="69903-128">Az új kötet objektum készlete</span><span class="sxs-lookup"><span data-stu-id="69903-128">The pool for the new volume object</span></span>

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

### <span data-ttu-id="69903-129">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="69903-129">-ProtocolType</span></span>
<span data-ttu-id="69903-130">Az exportálási házirendet reprezentáló Hashtable tömb</span><span class="sxs-lookup"><span data-stu-id="69903-130">A hashtable array which represents the export policy</span></span>

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

### <span data-ttu-id="69903-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69903-131">-ResourceGroupName</span></span>
<span data-ttu-id="69903-132">Az ANF-fiók erőforrás csoportja</span><span class="sxs-lookup"><span data-stu-id="69903-132">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="69903-133">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="69903-133">-ServiceLevel</span></span>
<span data-ttu-id="69903-134">A ANF-kötet szolgáltatási szintje</span><span class="sxs-lookup"><span data-stu-id="69903-134">The service level of the ANF volume</span></span>

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

```yaml
Type: String
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69903-135">– NetI</span><span class="sxs-lookup"><span data-stu-id="69903-135">-SubnetId</span></span>
<span data-ttu-id="69903-136">Egy delegált alhálózat Azure Resource URI azonosítója</span><span class="sxs-lookup"><span data-stu-id="69903-136">The Azure Resource URI for a delegated subnet</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69903-137">-Címke</span><span class="sxs-lookup"><span data-stu-id="69903-137">-Tag</span></span>
<span data-ttu-id="69903-138">Egy Hashtable, amely az erőforrás címkéit képviseli</span><span class="sxs-lookup"><span data-stu-id="69903-138">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="69903-139">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="69903-139">-UsageThreshold</span></span>
<span data-ttu-id="69903-140">A maximális tárterület kvótája a fájlrendszerben bájtban kifejezve</span><span class="sxs-lookup"><span data-stu-id="69903-140">The maximum storage quota allowed for a file system in bytes</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69903-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="69903-141">-Confirm</span></span>
<span data-ttu-id="69903-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="69903-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69903-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69903-143">-WhatIf</span></span>
<span data-ttu-id="69903-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="69903-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69903-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="69903-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69903-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69903-146">CommonParameters</span></span>
<span data-ttu-id="69903-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="69903-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="69903-148">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69903-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69903-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="69903-149">INPUTS</span></span>

### <span data-ttu-id="69903-150">System. String</span><span class="sxs-lookup"><span data-stu-id="69903-150">System.String</span></span>

### <span data-ttu-id="69903-151">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="69903-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="69903-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="69903-152">OUTPUTS</span></span>

### <span data-ttu-id="69903-153">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="69903-153">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="69903-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="69903-154">NOTES</span></span>

## <span data-ttu-id="69903-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="69903-155">RELATED LINKS</span></span>
