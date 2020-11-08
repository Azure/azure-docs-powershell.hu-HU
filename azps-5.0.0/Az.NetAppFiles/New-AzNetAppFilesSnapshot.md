---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 1fe8da5c9ee899b7aa1a77a9fbb0ac7a2bf3b35c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194104"
---
# <span data-ttu-id="fc063-101">New-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="fc063-101">New-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="fc063-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fc063-102">SYNOPSIS</span></span>
<span data-ttu-id="fc063-103">Új Azure NetApp-fájlokat (ANF) tartalmazó pillanatképet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="fc063-103">Creates a new Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="fc063-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fc063-104">SYNTAX</span></span>

### <span data-ttu-id="fc063-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fc063-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesSnapshot -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -VolumeName <String> -Name <String> [-FileSystemId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc063-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc063-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesSnapshot -Name <String> [-Tag <Hashtable>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc063-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="fc063-107">DESCRIPTION</span></span>
<span data-ttu-id="fc063-108">A **New-AzNetAppFilesSnapshot** PARANCSMAG egy ANF pillanatképet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="fc063-108">The **New-AzNetAppFilesSnapshot** cmdlet creates an ANF snapshot.</span></span>

## <span data-ttu-id="fc063-109">Példák</span><span class="sxs-lookup"><span data-stu-id="fc063-109">EXAMPLES</span></span>

### <span data-ttu-id="fc063-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fc063-110">Example 1</span></span>
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

<span data-ttu-id="fc063-111">Ezzel a paranccsal létrehozhatja az új ANF-pillanatfelvételt "MyAnfSnapshot" a "MyAnfVolume" köteten belül.</span><span class="sxs-lookup"><span data-stu-id="fc063-111">This command creates the new ANF snapshot "MyAnfSnapshot" within the volume "MyAnfVolume".</span></span>

## <span data-ttu-id="fc063-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fc063-112">PARAMETERS</span></span>

### <span data-ttu-id="fc063-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fc063-113">-AccountName</span></span>
<span data-ttu-id="fc063-114">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="fc063-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="fc063-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc063-115">-DefaultProfile</span></span>
<span data-ttu-id="fc063-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fc063-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc063-117">-FileSystemId</span><span class="sxs-lookup"><span data-stu-id="fc063-117">-FileSystemId</span></span>
<span data-ttu-id="fc063-118">A fájlrendszer azonosítója</span><span class="sxs-lookup"><span data-stu-id="fc063-118">The file system id</span></span>

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

### <span data-ttu-id="fc063-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="fc063-119">-Location</span></span>
<span data-ttu-id="fc063-120">Az erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="fc063-120">The location of the resource</span></span>

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

### <span data-ttu-id="fc063-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fc063-121">-Name</span></span>
<span data-ttu-id="fc063-122">A ANF pillanatképének neve</span><span class="sxs-lookup"><span data-stu-id="fc063-122">The name of the ANF snapshot</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SnapshotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc063-123">-PoolName</span><span class="sxs-lookup"><span data-stu-id="fc063-123">-PoolName</span></span>
<span data-ttu-id="fc063-124">A ANF-készlet neve</span><span class="sxs-lookup"><span data-stu-id="fc063-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="fc063-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc063-125">-ResourceGroupName</span></span>
<span data-ttu-id="fc063-126">Az ANF-fiók erőforrás csoportja</span><span class="sxs-lookup"><span data-stu-id="fc063-126">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="fc063-127">-Címke</span><span class="sxs-lookup"><span data-stu-id="fc063-127">-Tag</span></span>
<span data-ttu-id="fc063-128">Egy Hashtable, amely az erőforrás címkéit képviseli</span><span class="sxs-lookup"><span data-stu-id="fc063-128">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="fc063-129">-Kötetnév</span><span class="sxs-lookup"><span data-stu-id="fc063-129">-VolumeName</span></span>
<span data-ttu-id="fc063-130">A ANF-kötet neve</span><span class="sxs-lookup"><span data-stu-id="fc063-130">The name of the ANF volume</span></span>

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

### <span data-ttu-id="fc063-131">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="fc063-131">-VolumeObject</span></span>
<span data-ttu-id="fc063-132">Az új pillanatkép-objektum mennyisége</span><span class="sxs-lookup"><span data-stu-id="fc063-132">The volume for the new snapshot object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc063-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fc063-133">-Confirm</span></span>
<span data-ttu-id="fc063-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fc063-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc063-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc063-135">-WhatIf</span></span>
<span data-ttu-id="fc063-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fc063-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc063-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fc063-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc063-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc063-138">CommonParameters</span></span>
<span data-ttu-id="fc063-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fc063-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc063-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fc063-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc063-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc063-141">INPUTS</span></span>

### <span data-ttu-id="fc063-142">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="fc063-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="fc063-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc063-143">OUTPUTS</span></span>

### <span data-ttu-id="fc063-144">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="fc063-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="fc063-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fc063-145">NOTES</span></span>

## <span data-ttu-id="fc063-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fc063-146">RELATED LINKS</span></span>
