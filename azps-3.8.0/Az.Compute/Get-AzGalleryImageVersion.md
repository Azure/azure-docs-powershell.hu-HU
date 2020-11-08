---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageVersion.md
ms.openlocfilehash: 1385d4fe93157715ffdd521cfb62ed963b86e1ef
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013688"
---
# <span data-ttu-id="0d61d-101">Get-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="0d61d-101">Get-AzGalleryImageVersion</span></span>

## <span data-ttu-id="0d61d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0d61d-102">SYNOPSIS</span></span>
<span data-ttu-id="0d61d-103">Beolvashatja vagy listázhatja a Képtár képverzióit.</span><span class="sxs-lookup"><span data-stu-id="0d61d-103">Get or list gallery image versions.</span></span>

## <span data-ttu-id="0d61d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0d61d-104">SYNTAX</span></span>

### <span data-ttu-id="0d61d-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0d61d-105">DefaultParameter (Default)</span></span>
```
Get-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [[-Name] <String>] [-ExpandReplicationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d61d-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="0d61d-106">ResourceIdParameter</span></span>
```
Get-AzGalleryImageVersion [-ResourceId] <String> [-ExpandReplicationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d61d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0d61d-107">DESCRIPTION</span></span>
<span data-ttu-id="0d61d-108">Beolvashatja vagy listázhatja a Képtár képverzióit.</span><span class="sxs-lookup"><span data-stu-id="0d61d-108">Get or list gallery image versions.</span></span>

## <span data-ttu-id="0d61d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="0d61d-109">EXAMPLES</span></span>

### <span data-ttu-id="0d61d-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0d61d-110">Example 1</span></span>
```powershell
PS C:\> Get-AzGalleryImageVersion -ResourceGroupName rg1 -GalleryName gallery1 -GalleryImageDefinitionName image1 -GalleryImageVersionName 1.0.0

ResourceGroupName        : rg1
PublishingProfile        :
  TargetRegions[0]       :
    Name                 : South Central US
    RegionalReplicaCount : 1
  TargetRegions[1]       :
    Name                 : East US 2
    RegionalReplicaCount : 2
  TargetRegions[2]       :
    Name                 : Central US
    RegionalReplicaCount : 1
  Source                 :
    ManagedImage         :
      Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/images/test1
  ReplicaCount           : 1
  ExcludeFromLatest      : False
  PublishedDate          : 11/14/2018 12:00:00 AM
  EndOfLifeDate          : 2/18/2025 12:07:00 PM
ProvisioningState        : Succeeded
StorageProfile           :
  OsDiskImage            :
    SizeInGB             : 127
    HostCaching          : ReadWrite
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/galleries/gallery1/images/image1/versions/1.0.0
Name                     : 1.0.0
Type                     : Microsoft.Compute/galleries/images/versions
Location                 : eastus2
Tags                     : {}
```

<span data-ttu-id="0d61d-111">Beolvassa a gyűjtemény képének verzióját.</span><span class="sxs-lookup"><span data-stu-id="0d61d-111">Get the gallery image version.</span></span>

### <span data-ttu-id="0d61d-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="0d61d-112">Example 2</span></span>
```powershell
PS C:\> Get-AzGalleryImageVersion -ResourceGroupName rg1 -GalleryName gallery1 -GalleryImageDefinitionName image1 -GalleryImageVersionName 1*

ResourceGroupName        : rg1
PublishingProfile        :
  TargetRegions[0]       :
    Name                 : South Central US
    RegionalReplicaCount : 1
  TargetRegions[1]       :
    Name                 : East US 2
    RegionalReplicaCount : 2
  TargetRegions[2]       :
    Name                 : Central US
    RegionalReplicaCount : 1
  Source                 :
    ManagedImage         :
      Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/images/test1
  ReplicaCount           : 1
  ExcludeFromLatest      : False
  PublishedDate          : 11/14/2018 12:00:00 AM
  EndOfLifeDate          : 2/18/2025 12:07:00 PM
ProvisioningState        : Succeeded
StorageProfile           :
  OsDiskImage            :
    SizeInGB             : 127
    HostCaching          : ReadWrite
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/galleries/gallery1/images/image1/versions/1.0.0
Name                     : 1.0.0
Type                     : Microsoft.Compute/galleries/images/versions
Location                 : eastus2
Tags                     : {}

ResourceGroupName        : rg1
PublishingProfile        :
  TargetRegions[0]       :
    Name                 : South Central US
    RegionalReplicaCount : 1
  TargetRegions[1]       :
    Name                 : East US 2
    RegionalReplicaCount : 2
  TargetRegions[2]       :
    Name                 : Central US
    RegionalReplicaCount : 1
  Source                 :
    ManagedImage         :
      Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/images/test1
  ReplicaCount           : 1
  ExcludeFromLatest      : False
  PublishedDate          : 11/14/2018 12:00:00 AM
  EndOfLifeDate          : 2/18/2025 12:07:00 PM
ProvisioningState        : Succeeded
StorageProfile           :
  OsDiskImage            :
    SizeInGB             : 127
    HostCaching          : ReadWrite
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/galleries/gallery1/images/image1/versions/1.1.0
Name                     : 1.1.0
Type                     : Microsoft.Compute/galleries/images/versions
Location                 : eastus2
Tags                     : {}
```

<span data-ttu-id="0d61d-113">Az "1" kezdetű gyűjteményes képverziók beszerzése</span><span class="sxs-lookup"><span data-stu-id="0d61d-113">Get the gallery image versions that starts with "1".</span></span>

### <span data-ttu-id="0d61d-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="0d61d-114">Example 3</span></span>
```powershell
PS C:\> Get-AzGalleryImageVersion -ResourceGroupName rg1 -GalleryName gallery1 -GalleryImageDefinitionName image1

ResourceGroupName        : rg1
PublishingProfile        :
  TargetRegions[0]       :
    Name                 : South Central US
    RegionalReplicaCount : 1
  TargetRegions[1]       :
    Name                 : East US 2
    RegionalReplicaCount : 2
  TargetRegions[2]       :
    Name                 : Central US
    RegionalReplicaCount : 1
  Source                 :
    ManagedImage         :
      Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/images/test1
  ReplicaCount           : 1
  ExcludeFromLatest      : False
  PublishedDate          : 11/14/2018 12:00:00 AM
  EndOfLifeDate          : 2/18/2025 12:07:00 PM
ProvisioningState        : Succeeded
StorageProfile           :
  OsDiskImage            :
    SizeInGB             : 127
    HostCaching          : ReadWrite
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/galleries/gallery1/images/image1/versions/1.0.0
Name                     : 1.0.0
Type                     : Microsoft.Compute/galleries/images/versions
Location                 : eastus2
Tags                     : {}

ResourceGroupName        : rg1
PublishingProfile        :
  TargetRegions[0]       :
    Name                 : South Central US
    RegionalReplicaCount : 1
  TargetRegions[1]       :
    Name                 : East US 2
    RegionalReplicaCount : 2
  TargetRegions[2]       :
    Name                 : Central US
    RegionalReplicaCount : 1
  Source                 :
    ManagedImage         :
      Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/images/test1
  ReplicaCount           : 1
  ExcludeFromLatest      : False
  PublishedDate          : 11/14/2018 12:00:00 AM
  EndOfLifeDate          : 2/18/2025 12:07:00 PM
ProvisioningState        : Succeeded
StorageProfile           :
  OsDiskImage            :
    SizeInGB             : 127
    HostCaching          : ReadWrite
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/galleries/gallery1/images/image1/versions/1.1.0
Name                     : 1.1.0
Type                     : Microsoft.Compute/galleries/images/versions
Location                 : eastus2
Tags                     : {}
```

<span data-ttu-id="0d61d-115">Az összes gyűjtemény képének beolvasása</span><span class="sxs-lookup"><span data-stu-id="0d61d-115">Get all gallery image versions.</span></span>

## <span data-ttu-id="0d61d-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0d61d-116">PARAMETERS</span></span>

### <span data-ttu-id="0d61d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d61d-117">-DefaultProfile</span></span>
<span data-ttu-id="0d61d-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0d61d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d61d-119">-ExpandReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="0d61d-119">-ExpandReplicationStatus</span></span>
<span data-ttu-id="0d61d-120">Replikációs állapot megjelenítése</span><span class="sxs-lookup"><span data-stu-id="0d61d-120">Show replication status.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d61d-121">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="0d61d-121">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="0d61d-122">A gyűjtemény képének definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="0d61d-122">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d61d-123">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="0d61d-123">-GalleryName</span></span>
<span data-ttu-id="0d61d-124">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="0d61d-124">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d61d-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0d61d-125">-Name</span></span>
<span data-ttu-id="0d61d-126">A gyűjtemény képének neve.</span><span class="sxs-lookup"><span data-stu-id="0d61d-126">The name of the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageVersionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="0d61d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d61d-127">-ResourceGroupName</span></span>
<span data-ttu-id="0d61d-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0d61d-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d61d-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d61d-129">-ResourceId</span></span>
<span data-ttu-id="0d61d-130">A gyűjtemény képének-verziójához tartozó erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="0d61d-130">The resource ID for the gallery image version</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d61d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d61d-131">CommonParameters</span></span>
<span data-ttu-id="0d61d-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0d61d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d61d-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0d61d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d61d-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0d61d-134">INPUTS</span></span>

### <span data-ttu-id="0d61d-135">System. String</span><span class="sxs-lookup"><span data-stu-id="0d61d-135">System.String</span></span>

### <span data-ttu-id="0d61d-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0d61d-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0d61d-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0d61d-137">OUTPUTS</span></span>

### <span data-ttu-id="0d61d-138">Microsoft. Azure. commands. számítási. Automation. models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="0d61d-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="0d61d-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0d61d-139">NOTES</span></span>

## <span data-ttu-id="0d61d-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0d61d-140">RELATED LINKS</span></span>
