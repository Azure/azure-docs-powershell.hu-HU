---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/new-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 47d1aeb2868e8f104791527636a67a31b1e42c1a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926834"
---
# <span data-ttu-id="f187a-101">New-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="f187a-101">New-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="f187a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f187a-102">SYNOPSIS</span></span>
<span data-ttu-id="f187a-103">Létrehoz egy új Azure NetApp-fájlok (ANF) pillanatképet.</span><span class="sxs-lookup"><span data-stu-id="f187a-103">Creates a new Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="f187a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f187a-104">SYNTAX</span></span>

### <span data-ttu-id="f187a-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f187a-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesSnapshot -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -VolumeName <String> -Name <String> [-FileSystemId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f187a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f187a-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesSnapshot -Name <String> [-Tag <Hashtable>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f187a-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f187a-107">DESCRIPTION</span></span>
<span data-ttu-id="f187a-108">A **New-AzNetAppFilesSnapshot** parancsmag ANF-pillanatképet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f187a-108">The **New-AzNetAppFilesSnapshot** cmdlet creates an ANF snapshot.</span></span>

## <span data-ttu-id="f187a-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f187a-109">EXAMPLES</span></span>

### <span data-ttu-id="f187a-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="f187a-110">Example 1</span></span>
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

<span data-ttu-id="f187a-111">Ez a parancs létrehozza az új ANF-pillanatképet (MyAnfSnapshot) a "MyAnfVolume" köteten belül.</span><span class="sxs-lookup"><span data-stu-id="f187a-111">This command creates the new ANF snapshot "MyAnfSnapshot" within the volume "MyAnfVolume".</span></span>

## <span data-ttu-id="f187a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f187a-112">PARAMETERS</span></span>

### <span data-ttu-id="f187a-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f187a-113">-AccountName</span></span>
<span data-ttu-id="f187a-114">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="f187a-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="f187a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f187a-115">-DefaultProfile</span></span>
<span data-ttu-id="f187a-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f187a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f187a-117">-FileSystemId</span><span class="sxs-lookup"><span data-stu-id="f187a-117">-FileSystemId</span></span>
<span data-ttu-id="f187a-118">A fájlrendszer azonosítója</span><span class="sxs-lookup"><span data-stu-id="f187a-118">The file system id</span></span>

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

### <span data-ttu-id="f187a-119">-Location</span><span class="sxs-lookup"><span data-stu-id="f187a-119">-Location</span></span>
<span data-ttu-id="f187a-120">Az erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="f187a-120">The location of the resource</span></span>

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

### <span data-ttu-id="f187a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f187a-121">-Name</span></span>
<span data-ttu-id="f187a-122">Az ANF-pillanatkép neve</span><span class="sxs-lookup"><span data-stu-id="f187a-122">The name of the ANF snapshot</span></span>

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

### <span data-ttu-id="f187a-123">-PoolName</span><span class="sxs-lookup"><span data-stu-id="f187a-123">-PoolName</span></span>
<span data-ttu-id="f187a-124">Az ANF-készlet neve</span><span class="sxs-lookup"><span data-stu-id="f187a-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="f187a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f187a-125">-ResourceGroupName</span></span>
<span data-ttu-id="f187a-126">Az ANF-fiók erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="f187a-126">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="f187a-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="f187a-127">-Tag</span></span>
<span data-ttu-id="f187a-128">Erőforráscímkéket képviselő hashtable</span><span class="sxs-lookup"><span data-stu-id="f187a-128">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="f187a-129">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="f187a-129">-VolumeName</span></span>
<span data-ttu-id="f187a-130">Az ANF-kötet neve</span><span class="sxs-lookup"><span data-stu-id="f187a-130">The name of the ANF volume</span></span>

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

### <span data-ttu-id="f187a-131">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="f187a-131">-VolumeObject</span></span>
<span data-ttu-id="f187a-132">Az új pillanatkép-objektum hangereje</span><span class="sxs-lookup"><span data-stu-id="f187a-132">The volume for the new snapshot object</span></span>

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

### <span data-ttu-id="f187a-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f187a-133">-Confirm</span></span>
<span data-ttu-id="f187a-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f187a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f187a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f187a-135">-WhatIf</span></span>
<span data-ttu-id="f187a-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f187a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f187a-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f187a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f187a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f187a-138">CommonParameters</span></span>
<span data-ttu-id="f187a-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f187a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f187a-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f187a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f187a-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f187a-141">INPUTS</span></span>

### <span data-ttu-id="f187a-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="f187a-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="f187a-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f187a-143">OUTPUTS</span></span>

### <span data-ttu-id="f187a-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="f187a-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="f187a-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f187a-145">NOTES</span></span>

## <span data-ttu-id="f187a-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f187a-146">RELATED LINKS</span></span>
