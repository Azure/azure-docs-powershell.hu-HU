---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskAccess.md
ms.openlocfilehash: 69f83b7c98850ba74476e6d81803e748f48bea6a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94018149"
---
# <span data-ttu-id="f2bb4-101">Get-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="f2bb4-101">Get-AzDiskAccess</span></span>

## <span data-ttu-id="f2bb4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f2bb4-102">SYNOPSIS</span></span>
<span data-ttu-id="f2bb4-103">A lemezek elérésének tulajdonságai</span><span class="sxs-lookup"><span data-stu-id="f2bb4-103">Gets the properties of Disk Accesses</span></span>

## <span data-ttu-id="f2bb4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f2bb4-104">SYNTAX</span></span>

### <span data-ttu-id="f2bb4-105">DefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f2bb4-105">DefaultParameterSet (Default)</span></span>
```
Get-AzDiskAccess [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f2bb4-106">ResourceIDParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2bb4-106">ResourceIDParameterSet</span></span>
```
Get-AzDiskAccess [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2bb4-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f2bb4-107">DESCRIPTION</span></span>
<span data-ttu-id="f2bb4-108">A **Get-AzDiskAccess** parancsmag a Disk-hozzáférések tulajdonságait kapja meg</span><span class="sxs-lookup"><span data-stu-id="f2bb4-108">The **Get-AzDiskAccess** cmdlet gets the properties of Disk Accesses</span></span>

## <span data-ttu-id="f2bb4-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f2bb4-109">EXAMPLES</span></span>

### <span data-ttu-id="f2bb4-110">1. példa: alapértelmezett paraméterérték használata</span><span class="sxs-lookup"><span data-stu-id="f2bb4-110">Example 1: Using Default Parameter Set</span></span> 
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

<span data-ttu-id="f2bb4-111">Ez a parancs a "ResourceGroup01" erőforráscsoport "DiskAccess01" nevű Disk Access-erőforrásának tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f2bb4-111">This command gets the properties of a Disk Access resource named 'DiskAccess01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="f2bb4-112">2. példa: erőforráscsoport szerint Get-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="f2bb4-112">Example 2: Get-AzDiskAccess by Resource Group</span></span>
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

<span data-ttu-id="f2bb4-113">Ez a parancs a "ResourceGroup01" erőforráscsoport erőforrás-elérési területének tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f2bb4-113">This command gets the properties of all disk accesses in the resource group 'ResourceGroup01'.</span></span>


### <span data-ttu-id="f2bb4-114">3. példa: az összes lemez elérésének beszerzése</span><span class="sxs-lookup"><span data-stu-id="f2bb4-114">Example 3: Getting all Disk Access</span></span>
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

<span data-ttu-id="f2bb4-115">Ez a parancs beolvassa az előfizetés alatti minden lemez tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="f2bb4-115">This command gets the properties of all disk accesses under the subscription.</span></span>

### <span data-ttu-id="f2bb4-116">Példa 4: az összes lemez elérésének beolvasása helyettesítő karakter használatával</span><span class="sxs-lookup"><span data-stu-id="f2bb4-116">Example 4: Get all Disk Access using Wildcard Character</span></span>
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

<span data-ttu-id="f2bb4-117">Ez a parancs a "DiskAccessMicrosoft" karakterrel kezdődően az előfizetéses név alatti összes lemezen elérhető tulajdonságot kapja.</span><span class="sxs-lookup"><span data-stu-id="f2bb4-117">This command gets the properties of all disk accesses under the subscription name starting with 'DiskAccessMicrosoft'.</span></span>

### <span data-ttu-id="f2bb4-118">Példa 5: a ResourceId használatával beolvashatja a Disk Accesst.</span><span class="sxs-lookup"><span data-stu-id="f2bb4-118">Example 5: Get Disk Access using ResourceId.</span></span>
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

<span data-ttu-id="f2bb4-119">Ez a parancs beolvassa a lemez elérésének tulajdonságait a megadott ResourceId.</span><span class="sxs-lookup"><span data-stu-id="f2bb4-119">This command gets the properties of a Disk Access with the given ResourceId.</span></span>


## <span data-ttu-id="f2bb4-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f2bb4-120">PARAMETERS</span></span>

### <span data-ttu-id="f2bb4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2bb4-121">-DefaultProfile</span></span>
<span data-ttu-id="f2bb4-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f2bb4-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2bb4-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f2bb4-123">-Name</span></span>
<span data-ttu-id="f2bb4-124">A lemez elérési útjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f2bb4-124">Specifies the name of a disk access.</span></span>

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

### <span data-ttu-id="f2bb4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2bb4-125">-ResourceGroupName</span></span>
<span data-ttu-id="f2bb4-126">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f2bb4-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f2bb4-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2bb4-127">-ResourceId</span></span>
<span data-ttu-id="f2bb4-128">A lemez eléréséhez szükséges erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="f2bb4-128">Resource ID for your disk access.</span></span>

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

### <span data-ttu-id="f2bb4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2bb4-129">CommonParameters</span></span>
<span data-ttu-id="f2bb4-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f2bb4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2bb4-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f2bb4-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2bb4-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2bb4-132">INPUTS</span></span>

### <span data-ttu-id="f2bb4-133">System. String</span><span class="sxs-lookup"><span data-stu-id="f2bb4-133">System.String</span></span>

## <span data-ttu-id="f2bb4-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2bb4-134">OUTPUTS</span></span>

### <span data-ttu-id="f2bb4-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span><span class="sxs-lookup"><span data-stu-id="f2bb4-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="f2bb4-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f2bb4-136">NOTES</span></span>

## <span data-ttu-id="f2bb4-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f2bb4-137">RELATED LINKS</span></span>
