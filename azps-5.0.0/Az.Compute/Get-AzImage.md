---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzImage.md
ms.openlocfilehash: 4d1de6553a07cf58fdc109dc5703e37392a27a02
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194792"
---
# <span data-ttu-id="59b35-101">Get-AzImage</span><span class="sxs-lookup"><span data-stu-id="59b35-101">Get-AzImage</span></span>

## <span data-ttu-id="59b35-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="59b35-102">SYNOPSIS</span></span>
<span data-ttu-id="59b35-103">A kép tulajdonságainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="59b35-103">Gets the properties of an image.</span></span>

## <span data-ttu-id="59b35-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="59b35-104">SYNTAX</span></span>

```
Get-AzImage [[-ResourceGroupName] <String>] [[-ImageName] <String>] [[-Expand] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59b35-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="59b35-105">DESCRIPTION</span></span>
<span data-ttu-id="59b35-106">A **Get-AzImage** parancsmag a kép tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="59b35-106">The **Get-AzImage** cmdlet gets the properties of an image.</span></span>

## <span data-ttu-id="59b35-107">Példák</span><span class="sxs-lookup"><span data-stu-id="59b35-107">EXAMPLES</span></span>

### <span data-ttu-id="59b35-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="59b35-108">Example 1</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01'

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image01
Name                 : Image01
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}
```

<span data-ttu-id="59b35-109">Ez a parancs a ' Image01 ' nevű kép tulajdonságait kapja meg a "ResourceGroup01" erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="59b35-109">This command gets the properties of the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="59b35-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="59b35-110">Example 2</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01'

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image01
Name                 : Image01
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image02
Name                 : Image02
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}
```

<span data-ttu-id="59b35-111">Ez a parancs a "ResourceGroup01" erőforráscsoport összes képének tulajdonságait adja meg.</span><span class="sxs-lookup"><span data-stu-id="59b35-111">This command gets the properties of all images in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="59b35-112">3. példa</span><span class="sxs-lookup"><span data-stu-id="59b35-112">Example 3</span></span>
```
PS C:\> Get-AzImage

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image01
Name                 : Image01
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image02
Name                 : Image02
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}

ResourceGroupName    : ResourceGroup02
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup02/prov
                       iders/Microsoft.Compute/images/Image03
Name                 : Image03
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}
```

<span data-ttu-id="59b35-113">Ez a parancs az előfizetés alatti képek tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="59b35-113">This command gets the properties of all images under the subscription.</span></span>

### <span data-ttu-id="59b35-114">4. példa</span><span class="sxs-lookup"><span data-stu-id="59b35-114">Example 4</span></span>
```
PS C:\> Get-AzImage -Name "Image*"

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image01
Name                 : Image01
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image02
Name                 : Image02
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}

ResourceGroupName    : ResourceGroup02
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup02/prov
                       iders/Microsoft.Compute/images/Image03
Name                 : Image03
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}
```

<span data-ttu-id="59b35-115">Ez a parancs a "képpel" kezdetű előfizetés alatti képek tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="59b35-115">This command gets the properties of all images under the subscription that start with "Image".</span></span>

## <span data-ttu-id="59b35-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="59b35-116">PARAMETERS</span></span>

### <span data-ttu-id="59b35-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59b35-117">-DefaultProfile</span></span>
<span data-ttu-id="59b35-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="59b35-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59b35-119">– Kibontás</span><span class="sxs-lookup"><span data-stu-id="59b35-119">-Expand</span></span>
<span data-ttu-id="59b35-120">A kifejezés kibontása lekérdezést adja meg.</span><span class="sxs-lookup"><span data-stu-id="59b35-120">Specifies the expand expression query.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59b35-121">-ImageName</span><span class="sxs-lookup"><span data-stu-id="59b35-121">-ImageName</span></span>
<span data-ttu-id="59b35-122">A kép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="59b35-122">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="59b35-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59b35-123">-ResourceGroupName</span></span>
<span data-ttu-id="59b35-124">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="59b35-124">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="59b35-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59b35-125">CommonParameters</span></span>
<span data-ttu-id="59b35-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="59b35-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59b35-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="59b35-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59b35-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="59b35-128">INPUTS</span></span>

### <span data-ttu-id="59b35-129">System. String</span><span class="sxs-lookup"><span data-stu-id="59b35-129">System.String</span></span>

## <span data-ttu-id="59b35-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="59b35-130">OUTPUTS</span></span>

### <span data-ttu-id="59b35-131">Microsoft. Azure. commands. számítási. Automation. models. PSImage</span><span class="sxs-lookup"><span data-stu-id="59b35-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="59b35-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="59b35-132">NOTES</span></span>

## <span data-ttu-id="59b35-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="59b35-133">RELATED LINKS</span></span>