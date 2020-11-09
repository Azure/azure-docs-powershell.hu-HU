---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageVersion.md
ms.openlocfilehash: 1385d4fe93157715ffdd521cfb62ed963b86e1ef
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302832"
---
# <span data-ttu-id="510a3-101">Get-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="510a3-101">Get-AzGalleryImageVersion</span></span>

## <span data-ttu-id="510a3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="510a3-102">SYNOPSIS</span></span>
<span data-ttu-id="510a3-103">Beolvashatja vagy listázhatja a Képtár képverzióit.</span><span class="sxs-lookup"><span data-stu-id="510a3-103">Get or list gallery image versions.</span></span>

## <span data-ttu-id="510a3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="510a3-104">SYNTAX</span></span>

### <span data-ttu-id="510a3-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="510a3-105">DefaultParameter (Default)</span></span>
```
Get-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [[-Name] <String>] [-ExpandReplicationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="510a3-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="510a3-106">ResourceIdParameter</span></span>
```
Get-AzGalleryImageVersion [-ResourceId] <String> [-ExpandReplicationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="510a3-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="510a3-107">DESCRIPTION</span></span>
<span data-ttu-id="510a3-108">Beolvashatja vagy listázhatja a Képtár képverzióit.</span><span class="sxs-lookup"><span data-stu-id="510a3-108">Get or list gallery image versions.</span></span>

## <span data-ttu-id="510a3-109">Példák</span><span class="sxs-lookup"><span data-stu-id="510a3-109">EXAMPLES</span></span>

### <span data-ttu-id="510a3-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="510a3-110">Example 1</span></span>
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

<span data-ttu-id="510a3-111">Beolvassa a gyűjtemény képének verzióját.</span><span class="sxs-lookup"><span data-stu-id="510a3-111">Get the gallery image version.</span></span>

### <span data-ttu-id="510a3-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="510a3-112">Example 2</span></span>
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

<span data-ttu-id="510a3-113">Az "1" kezdetű gyűjteményes képverziók beszerzése</span><span class="sxs-lookup"><span data-stu-id="510a3-113">Get the gallery image versions that starts with "1".</span></span>

### <span data-ttu-id="510a3-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="510a3-114">Example 3</span></span>
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

<span data-ttu-id="510a3-115">Az összes gyűjtemény képének beolvasása</span><span class="sxs-lookup"><span data-stu-id="510a3-115">Get all gallery image versions.</span></span>

## <span data-ttu-id="510a3-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="510a3-116">PARAMETERS</span></span>

### <span data-ttu-id="510a3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="510a3-117">-DefaultProfile</span></span>
<span data-ttu-id="510a3-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="510a3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="510a3-119">-ExpandReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="510a3-119">-ExpandReplicationStatus</span></span>
<span data-ttu-id="510a3-120">Replikációs állapot megjelenítése</span><span class="sxs-lookup"><span data-stu-id="510a3-120">Show replication status.</span></span>

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

### <span data-ttu-id="510a3-121">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="510a3-121">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="510a3-122">A gyűjtemény képének definíciójának neve.</span><span class="sxs-lookup"><span data-stu-id="510a3-122">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="510a3-123">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="510a3-123">-GalleryName</span></span>
<span data-ttu-id="510a3-124">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="510a3-124">The name of the gallery.</span></span>

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

### <span data-ttu-id="510a3-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="510a3-125">-Name</span></span>
<span data-ttu-id="510a3-126">A gyűjtemény képének neve.</span><span class="sxs-lookup"><span data-stu-id="510a3-126">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="510a3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="510a3-127">-ResourceGroupName</span></span>
<span data-ttu-id="510a3-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="510a3-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="510a3-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="510a3-129">-ResourceId</span></span>
<span data-ttu-id="510a3-130">A gyűjtemény képének-verziójához tartozó erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="510a3-130">The resource ID for the gallery image version</span></span>

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

### <span data-ttu-id="510a3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="510a3-131">CommonParameters</span></span>
<span data-ttu-id="510a3-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="510a3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="510a3-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="510a3-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="510a3-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="510a3-134">INPUTS</span></span>

### <span data-ttu-id="510a3-135">System. String</span><span class="sxs-lookup"><span data-stu-id="510a3-135">System.String</span></span>

### <span data-ttu-id="510a3-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="510a3-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="510a3-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="510a3-137">OUTPUTS</span></span>

### <span data-ttu-id="510a3-138">Microsoft. Azure. commands. számítási. Automation. models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="510a3-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="510a3-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="510a3-139">NOTES</span></span>

## <span data-ttu-id="510a3-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="510a3-140">RELATED LINKS</span></span>
