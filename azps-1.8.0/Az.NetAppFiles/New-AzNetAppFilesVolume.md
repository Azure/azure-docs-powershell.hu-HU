---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
ms.openlocfilehash: b742c8af0e8c36d07b2c608e74f0a02349502104
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670770"
---
# <span data-ttu-id="98e92-101">New-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="98e92-101">New-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="98e92-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="98e92-102">SYNOPSIS</span></span>
<span data-ttu-id="98e92-103">Új Azure NetApp-fájlok (ANF-kötet) létrehozása.</span><span class="sxs-lookup"><span data-stu-id="98e92-103">Creates a new Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="98e92-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="98e92-104">SYNTAX</span></span>

### <span data-ttu-id="98e92-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="98e92-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String> -ServiceLevel <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98e92-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="98e92-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesVolume -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String>
 -ServiceLevel <String> [-Tag <Hashtable>] -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98e92-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="98e92-107">DESCRIPTION</span></span>
<span data-ttu-id="98e92-108">A **New-AzNetAppFilesVolume** parancsmag ANF-kötetet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="98e92-108">The **New-AzNetAppFilesVolume** cmdlet creates an ANF volume.</span></span>

## <span data-ttu-id="98e92-109">Példák</span><span class="sxs-lookup"><span data-stu-id="98e92-109">EXAMPLES</span></span>

### <span data-ttu-id="98e92-110">1. példa: ANF-kötet létrehozása</span><span class="sxs-lookup"><span data-stu-id="98e92-110">Example 1: Create an ANF volume</span></span>
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

<span data-ttu-id="98e92-111">Ezzel a paranccsal létrejön az új ANF-kötet "MyAnfVolume" a "MyAnfPool" alkalmazáskészleten belül.</span><span class="sxs-lookup"><span data-stu-id="98e92-111">This command creates the new ANF volume "MyAnfVolume" within the pool "MyAnfPool".</span></span>

## <span data-ttu-id="98e92-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="98e92-112">PARAMETERS</span></span>

### <span data-ttu-id="98e92-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="98e92-113">-AccountName</span></span>
<span data-ttu-id="98e92-114">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="98e92-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="98e92-115">-CreationToken</span><span class="sxs-lookup"><span data-stu-id="98e92-115">-CreationToken</span></span>
<span data-ttu-id="98e92-116">A kötet egyedi fájlelérési útja</span><span class="sxs-lookup"><span data-stu-id="98e92-116">A unique file path for the volume</span></span>

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

### <span data-ttu-id="98e92-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98e92-117">-DefaultProfile</span></span>
<span data-ttu-id="98e92-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="98e92-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98e92-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="98e92-119">-Location</span></span>
<span data-ttu-id="98e92-120">Az erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="98e92-120">The location of the resource</span></span>

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

### <span data-ttu-id="98e92-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="98e92-121">-Name</span></span>
<span data-ttu-id="98e92-122">A ANF-kötet neve</span><span class="sxs-lookup"><span data-stu-id="98e92-122">The name of the ANF volume</span></span>

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

### <span data-ttu-id="98e92-123">-PoolName</span><span class="sxs-lookup"><span data-stu-id="98e92-123">-PoolName</span></span>
<span data-ttu-id="98e92-124">A ANF-készlet neve</span><span class="sxs-lookup"><span data-stu-id="98e92-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="98e92-125">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="98e92-125">-PoolObject</span></span>
<span data-ttu-id="98e92-126">Az új kötet objektum készlete</span><span class="sxs-lookup"><span data-stu-id="98e92-126">The pool for the new volume object</span></span>

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

### <span data-ttu-id="98e92-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98e92-127">-ResourceGroupName</span></span>
<span data-ttu-id="98e92-128">Az ANF-fiók erőforrás csoportja</span><span class="sxs-lookup"><span data-stu-id="98e92-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="98e92-129">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="98e92-129">-ServiceLevel</span></span>
<span data-ttu-id="98e92-130">A ANF-kötet szolgáltatási szintje</span><span class="sxs-lookup"><span data-stu-id="98e92-130">The service level of the ANF volume</span></span>

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

### <span data-ttu-id="98e92-131">– NetI</span><span class="sxs-lookup"><span data-stu-id="98e92-131">-SubnetId</span></span>
<span data-ttu-id="98e92-132">Egy delegált alhálózat Azure Resource URI azonosítója</span><span class="sxs-lookup"><span data-stu-id="98e92-132">The Azure Resource URI for a delegated subnet</span></span>

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

### <span data-ttu-id="98e92-133">-Címke</span><span class="sxs-lookup"><span data-stu-id="98e92-133">-Tag</span></span>
<span data-ttu-id="98e92-134">Egy Hashtable, amely az erőforrás címkéit képviseli</span><span class="sxs-lookup"><span data-stu-id="98e92-134">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="98e92-135">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="98e92-135">-UsageThreshold</span></span>
<span data-ttu-id="98e92-136">A maximális tárterület kvótája a fájlrendszerben bájtban kifejezve</span><span class="sxs-lookup"><span data-stu-id="98e92-136">The maximum storage quota allowed for a file system in bytes</span></span>

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

### <span data-ttu-id="98e92-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="98e92-137">-Confirm</span></span>
<span data-ttu-id="98e92-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="98e92-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98e92-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98e92-139">-WhatIf</span></span>
<span data-ttu-id="98e92-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="98e92-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98e92-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="98e92-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98e92-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98e92-142">CommonParameters</span></span>
<span data-ttu-id="98e92-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="98e92-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="98e92-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98e92-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98e92-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="98e92-145">INPUTS</span></span>

### <span data-ttu-id="98e92-146">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="98e92-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="98e92-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="98e92-147">OUTPUTS</span></span>

### <span data-ttu-id="98e92-148">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="98e92-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="98e92-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="98e92-149">NOTES</span></span>

## <span data-ttu-id="98e92-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="98e92-150">RELATED LINKS</span></span>
