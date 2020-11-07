---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 47383ee57d527f6348781e57ed965e1ed8d36ef2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845057"
---
# <span data-ttu-id="23fb9-101">New-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="23fb9-101">New-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="23fb9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="23fb9-102">SYNOPSIS</span></span>
<span data-ttu-id="23fb9-103">Új Azure NetApp-fájlokat (ANF) tartalmazó pillanatképet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="23fb9-103">Creates a new Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="23fb9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="23fb9-104">SYNTAX</span></span>

### <span data-ttu-id="23fb9-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="23fb9-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesSnapshot -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -VolumeName <String> -Name <String> [-FileSystemId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23fb9-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="23fb9-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesSnapshot -Name <String> [-Tag <Hashtable>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23fb9-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="23fb9-107">DESCRIPTION</span></span>
<span data-ttu-id="23fb9-108">A **New-AzNetAppFilesSnapshot** PARANCSMAG egy ANF pillanatképet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="23fb9-108">The **New-AzNetAppFilesSnapshot** cmdlet creates an ANF snapshot.</span></span>

## <span data-ttu-id="23fb9-109">Példák</span><span class="sxs-lookup"><span data-stu-id="23fb9-109">EXAMPLES</span></span>

### <span data-ttu-id="23fb9-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="23fb9-110">Example 1</span></span>
```
PS C:\>New-AzNetAppFilesSnapshot -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -SnapshotName "MyAnfSnapshot" -FileSystemId "3e2773a7-2a72-d003-0637-1a8b1fa3eaaf"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume/snapshots/MyAnfSnapshot
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume/MyAnfSnapshot
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes/snapshots
Tags              :
SnapshotId        : ca7c4ebd-91cb-0e30-91f5-9154050033df
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
Created           :
ProvisioningState : Succeeded
```

<span data-ttu-id="23fb9-111">Ezzel a paranccsal létrehozhatja az új ANF-pillanatfelvételt "MyAnfSnapshot" a "MyAnfVolume" köteten belül.</span><span class="sxs-lookup"><span data-stu-id="23fb9-111">This command creates the new ANF snapshot "MyAnfSnapshot" within the volume "MyAnfVolume".</span></span>

## <span data-ttu-id="23fb9-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="23fb9-112">PARAMETERS</span></span>

### <span data-ttu-id="23fb9-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="23fb9-113">-AccountName</span></span>
<span data-ttu-id="23fb9-114">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="23fb9-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="23fb9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23fb9-115">-DefaultProfile</span></span>
<span data-ttu-id="23fb9-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="23fb9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23fb9-117">-FileSystemId</span><span class="sxs-lookup"><span data-stu-id="23fb9-117">-FileSystemId</span></span>
<span data-ttu-id="23fb9-118">A fájlrendszer azonosítója</span><span class="sxs-lookup"><span data-stu-id="23fb9-118">The file system id</span></span>

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

### <span data-ttu-id="23fb9-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="23fb9-119">-Location</span></span>
<span data-ttu-id="23fb9-120">Az erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="23fb9-120">The location of the resource</span></span>

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

### <span data-ttu-id="23fb9-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="23fb9-121">-Name</span></span>
<span data-ttu-id="23fb9-122">A ANF pillanatképének neve</span><span class="sxs-lookup"><span data-stu-id="23fb9-122">The name of the ANF snapshot</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SnapshotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23fb9-123">-PoolName</span><span class="sxs-lookup"><span data-stu-id="23fb9-123">-PoolName</span></span>
<span data-ttu-id="23fb9-124">A ANF-készlet neve</span><span class="sxs-lookup"><span data-stu-id="23fb9-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="23fb9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23fb9-125">-ResourceGroupName</span></span>
<span data-ttu-id="23fb9-126">Az ANF-fiók erőforrás csoportja</span><span class="sxs-lookup"><span data-stu-id="23fb9-126">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="23fb9-127">-Címke</span><span class="sxs-lookup"><span data-stu-id="23fb9-127">-Tag</span></span>
<span data-ttu-id="23fb9-128">Egy Hashtable, amely az erőforrás címkéit képviseli</span><span class="sxs-lookup"><span data-stu-id="23fb9-128">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="23fb9-129">-Kötetnév</span><span class="sxs-lookup"><span data-stu-id="23fb9-129">-VolumeName</span></span>
<span data-ttu-id="23fb9-130">A ANF-kötet neve</span><span class="sxs-lookup"><span data-stu-id="23fb9-130">The name of the ANF volume</span></span>

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

### <span data-ttu-id="23fb9-131">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="23fb9-131">-VolumeObject</span></span>
<span data-ttu-id="23fb9-132">Az új pillanatkép-objektum mennyisége</span><span class="sxs-lookup"><span data-stu-id="23fb9-132">The volume for the new snapshot object</span></span>

```yaml
Type: PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23fb9-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="23fb9-133">-Confirm</span></span>
<span data-ttu-id="23fb9-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="23fb9-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23fb9-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23fb9-135">-WhatIf</span></span>
<span data-ttu-id="23fb9-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="23fb9-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23fb9-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="23fb9-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23fb9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23fb9-138">CommonParameters</span></span>
<span data-ttu-id="23fb9-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="23fb9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="23fb9-140">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23fb9-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23fb9-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="23fb9-141">INPUTS</span></span>

### <span data-ttu-id="23fb9-142">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="23fb9-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="23fb9-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="23fb9-143">OUTPUTS</span></span>

### <span data-ttu-id="23fb9-144">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="23fb9-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="23fb9-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="23fb9-145">NOTES</span></span>

## <span data-ttu-id="23fb9-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="23fb9-146">RELATED LINKS</span></span>
