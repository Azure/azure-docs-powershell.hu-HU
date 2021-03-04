---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/get-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 80d8a27aaf0d2aa27f9924d93669548c1d0dda93
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926913"
---
# <span data-ttu-id="7ad6c-101">Get-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="7ad6c-101">Get-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="7ad6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ad6c-102">SYNOPSIS</span></span>
<span data-ttu-id="7ad6c-103">Az Azure NetApp-fájlok (ANF) pillanatkép részleteinek lekérte.</span><span class="sxs-lookup"><span data-stu-id="7ad6c-103">Gets details of an Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="7ad6c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7ad6c-104">SYNTAX</span></span>

### <span data-ttu-id="7ad6c-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7ad6c-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesSnapshot -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ad6c-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ad6c-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesSnapshot [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7ad6c-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ad6c-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesSnapshot [-Name <String>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ad6c-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7ad6c-108">DESCRIPTION</span></span>
<span data-ttu-id="7ad6c-109">A **Get-AzNetAppFilesSnapshot** parancsmag egy ANF-pillanatfelvétel részleteit tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="7ad6c-109">The **Get-AzNetAppFilesSnapshot** cmdlet gets details of an ANF snapshot.</span></span>

## <span data-ttu-id="7ad6c-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7ad6c-110">EXAMPLES</span></span>

### <span data-ttu-id="7ad6c-111">1. példa: ANF-pillanatkép készítése</span><span class="sxs-lookup"><span data-stu-id="7ad6c-111">Example 1: Get an ANF snapshot</span></span>
```
PS C:\>Get-AzNetAppFilesSnapshot -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -Name "MyAnfSnapshot"

Output:

ResourceGroupName : MyRG
Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume/snapshots/MyAnfSnapshot
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume/MyAnfSnapshot
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes/snapshots
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
SnapshotId        : ca7c4ebd-91cb-0e30-91f5-9154050033df
Created           :
ProvisioningState : Succeeded
```

<span data-ttu-id="7ad6c-112">Ez a parancs a MyAnfSnapshot nevű pillanatképet a MyAnfVolume kötetből kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7ad6c-112">This command gets the snapshot named MyAnfSnapshot from the volume "MyAnfVolume".</span></span>

## <span data-ttu-id="7ad6c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ad6c-113">PARAMETERS</span></span>

### <span data-ttu-id="7ad6c-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7ad6c-114">-AccountName</span></span>
<span data-ttu-id="7ad6c-115">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="7ad6c-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="7ad6c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ad6c-116">-DefaultProfile</span></span>
<span data-ttu-id="7ad6c-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7ad6c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ad6c-118">-Name</span><span class="sxs-lookup"><span data-stu-id="7ad6c-118">-Name</span></span>
<span data-ttu-id="7ad6c-119">Az ANF-pillanatkép neve</span><span class="sxs-lookup"><span data-stu-id="7ad6c-119">The name of the ANF snapshot</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SnapshotName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ad6c-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="7ad6c-120">-PoolName</span></span>
<span data-ttu-id="7ad6c-121">Az ANF-készlet neve</span><span class="sxs-lookup"><span data-stu-id="7ad6c-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="7ad6c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ad6c-122">-ResourceGroupName</span></span>
<span data-ttu-id="7ad6c-123">Az ANF-mennyiség erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="7ad6c-123">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="7ad6c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7ad6c-124">-ResourceId</span></span>
<span data-ttu-id="7ad6c-125">Az ANF-pillanatfelvétel erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="7ad6c-125">The resource id of the ANF snapshot</span></span>

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

### <span data-ttu-id="7ad6c-126">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="7ad6c-126">-VolumeName</span></span>
<span data-ttu-id="7ad6c-127">Az ANF-kötet neve</span><span class="sxs-lookup"><span data-stu-id="7ad6c-127">The name of the ANF volume</span></span>

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

### <span data-ttu-id="7ad6c-128">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="7ad6c-128">-VolumeObject</span></span>
<span data-ttu-id="7ad6c-129">A visszaadott pillanatképet tartalmazó kötetobjektum</span><span class="sxs-lookup"><span data-stu-id="7ad6c-129">The volume object containing the snapshot to return</span></span>

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

### <span data-ttu-id="7ad6c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ad6c-130">CommonParameters</span></span>
<span data-ttu-id="7ad6c-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ad6c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ad6c-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7ad6c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ad6c-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7ad6c-133">INPUTS</span></span>

### <span data-ttu-id="7ad6c-134">System.String</span><span class="sxs-lookup"><span data-stu-id="7ad6c-134">System.String</span></span>

### <span data-ttu-id="7ad6c-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="7ad6c-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="7ad6c-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ad6c-136">OUTPUTS</span></span>

### <span data-ttu-id="7ad6c-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="7ad6c-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="7ad6c-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7ad6c-138">NOTES</span></span>

## <span data-ttu-id="7ad6c-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7ad6c-139">RELATED LINKS</span></span>
