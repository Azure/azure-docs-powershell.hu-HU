---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskAccess.md
ms.openlocfilehash: 69f83b7c98850ba74476e6d81803e748f48bea6a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927290"
---
# <span data-ttu-id="a884a-101">Get-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="a884a-101">Get-AzDiskAccess</span></span>

## <span data-ttu-id="a884a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a884a-102">SYNOPSIS</span></span>
<span data-ttu-id="a884a-103">A lemezelérések tulajdonságainak lekérte</span><span class="sxs-lookup"><span data-stu-id="a884a-103">Gets the properties of Disk Accesses</span></span>

## <span data-ttu-id="a884a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a884a-104">SYNTAX</span></span>

### <span data-ttu-id="a884a-105">DefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a884a-105">DefaultParameterSet (Default)</span></span>
```
Get-AzDiskAccess [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a884a-106">ResourceIDParameterSet</span><span class="sxs-lookup"><span data-stu-id="a884a-106">ResourceIDParameterSet</span></span>
```
Get-AzDiskAccess [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a884a-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a884a-107">DESCRIPTION</span></span>
<span data-ttu-id="a884a-108">A **Get-AzDiskAccess** parancsmag beveszi a lemezelérések tulajdonságait</span><span class="sxs-lookup"><span data-stu-id="a884a-108">The **Get-AzDiskAccess** cmdlet gets the properties of Disk Accesses</span></span>

## <span data-ttu-id="a884a-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a884a-109">EXAMPLES</span></span>

### <span data-ttu-id="a884a-110">1. példa: Alapértelmezett paraméterkészlet használata</span><span class="sxs-lookup"><span data-stu-id="a884a-110">Example 1: Using Default Parameter Set</span></span> 
```
PS C:\> Get-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -Name 'DiskAccess01'

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:02:50 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess01
Name                       : DiskAccess01
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}
```

<span data-ttu-id="a884a-111">Ez a parancs a "ResourceGroup01" erőforráscsoport "DiskAccess01" nevű lemezelérési erőforrásának tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a884a-111">This command gets the properties of a Disk Access resource named 'DiskAccess01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="a884a-112">2. példa: Get-AzDiskAccess erőforráscsoport szerint</span><span class="sxs-lookup"><span data-stu-id="a884a-112">Example 2: Get-AzDiskAccess by Resource Group</span></span>
```
PS C:\> Get-AzDiskAccess -ResourceGroupName 'ResourceGroup01'

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:02:50 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess01
Name                       : DiskAccess01
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:05:19 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess02
Name                       : DiskAccess02
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}
```

<span data-ttu-id="a884a-113">Ez a parancs az "ResourceGroup01" erőforráscsoport összes lemez-hozzáférésének tulajdonságait beveszi.</span><span class="sxs-lookup"><span data-stu-id="a884a-113">This command gets the properties of all disk accesses in the resource group 'ResourceGroup01'.</span></span>


### <span data-ttu-id="a884a-114">3. példa: Az összes lemezelérés elérése</span><span class="sxs-lookup"><span data-stu-id="a884a-114">Example 3: Getting all Disk Access</span></span>
```
PS C:\> Get-AzDiskAccess

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:02:50 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess01
Name                       : DiskAccess01
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:05:19 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup21/providers/Microsoft.Compute/diskAccesses/DiskAccess02
Name                       : DiskAccess02
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:05:19 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup08/providers/Microsoft.Compute/diskAccesses/DiskAccess03
Name                       : DiskAccess03
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}
```

<span data-ttu-id="a884a-115">Ez a parancs az előfizetés alatt lévő összes lemez-hozzáférés tulajdonságait beveszi.</span><span class="sxs-lookup"><span data-stu-id="a884a-115">This command gets the properties of all disk accesses under the subscription.</span></span>

### <span data-ttu-id="a884a-116">4. példa: Az összes lemezelérés lekérte helyettesítő karakter használatával</span><span class="sxs-lookup"><span data-stu-id="a884a-116">Example 4: Get all Disk Access using Wildcard Character</span></span>
```
PS C:\> Get-AzDiskAccess -Name DiskAccessMicrosoft*

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:02:50 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccessMicrosoftAzure
Name                       : DiskAccessMicrosoftAzure
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:05:19 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccessMicrosoftTeams
Name                       : DiskAccessMicrosoftTeams
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}
```

<span data-ttu-id="a884a-117">Ez a parancs az előfizetés neve alatt lévő összes lemez-hozzáférés tulajdonságait a "DiskAccessMicrosoft" névvel kezdődően kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a884a-117">This command gets the properties of all disk accesses under the subscription name starting with 'DiskAccessMicrosoft'.</span></span>

### <span data-ttu-id="a884a-118">5. példa: Lemezelérés a ResourceId használatával.</span><span class="sxs-lookup"><span data-stu-id="a884a-118">Example 5: Get Disk Access using ResourceId.</span></span>
```
PS C:\> Get-AzDiskAccess -ResourceId '/subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess01'

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:02:50 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess01
Name                       : DiskAccess01
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}
```

<span data-ttu-id="a884a-119">Ez a parancs a lemezelérés tulajdonságait kapja meg a megadott ResourceId-val.</span><span class="sxs-lookup"><span data-stu-id="a884a-119">This command gets the properties of a Disk Access with the given ResourceId.</span></span>


## <span data-ttu-id="a884a-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a884a-120">PARAMETERS</span></span>

### <span data-ttu-id="a884a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a884a-121">-DefaultProfile</span></span>
<span data-ttu-id="a884a-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a884a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a884a-123">-Name</span><span class="sxs-lookup"><span data-stu-id="a884a-123">-Name</span></span>
<span data-ttu-id="a884a-124">A lemezelérés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a884a-124">Specifies the name of a disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases: diskAccessName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="a884a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a884a-125">-ResourceGroupName</span></span>
<span data-ttu-id="a884a-126">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a884a-126">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="a884a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a884a-127">-ResourceId</span></span>
<span data-ttu-id="a884a-128">A lemezelérés erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a884a-128">Resource ID for your disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIDParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a884a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a884a-129">CommonParameters</span></span>
<span data-ttu-id="a884a-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a884a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a884a-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a884a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a884a-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a884a-132">INPUTS</span></span>

### <span data-ttu-id="a884a-133">System.String</span><span class="sxs-lookup"><span data-stu-id="a884a-133">System.String</span></span>

## <span data-ttu-id="a884a-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a884a-134">OUTPUTS</span></span>

### <span data-ttu-id="a884a-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span><span class="sxs-lookup"><span data-stu-id="a884a-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="a884a-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a884a-136">NOTES</span></span>

## <span data-ttu-id="a884a-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a884a-137">RELATED LINKS</span></span>
