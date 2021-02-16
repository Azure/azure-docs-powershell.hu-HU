---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImage.md
ms.openlocfilehash: 33446cf9e14175c67e3f2fd2fa5dead33b88f526
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148930"
---
# <span data-ttu-id="2e566-101">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="2e566-101">Get-AzVMImage</span></span>

## <span data-ttu-id="2e566-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e566-102">SYNOPSIS</span></span>
<span data-ttu-id="2e566-103">A VMImage összes verzióját beveszi.</span><span class="sxs-lookup"><span data-stu-id="2e566-103">Gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="2e566-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2e566-104">SYNTAX</span></span>

### <span data-ttu-id="2e566-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="2e566-105">ListVMImage</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> [-Top <Int32>]
 [-OrderBy <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e566-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="2e566-106">GetVMImageDetail</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e566-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2e566-107">DESCRIPTION</span></span>
<span data-ttu-id="2e566-108">A **Get-AzVMImage** parancsmag begyűjte a VMImage összes verzióját.</span><span class="sxs-lookup"><span data-stu-id="2e566-108">The **Get-AzVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="2e566-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2e566-109">EXAMPLES</span></span>

### <span data-ttu-id="2e566-110">1. példa: VMImage-objektumok lekérte</span><span class="sxs-lookup"><span data-stu-id="2e566-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "MicrosoftWindowsServer" -Offer "windowsserver" -Skus "2012-R2-Datacenter"

Version        Skus               Offer         PublisherName          Location  Id
-------        ----               -----         -------------          --------  --
4.127.20180315 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180510 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180815 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180912 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181010 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181125 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190104 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190115 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190204 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190218 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
```

<span data-ttu-id="2e566-111">Ez a parancs a VMImage összes olyan verzióját beveszi, amely megfelel a megadott értékeknek.</span><span class="sxs-lookup"><span data-stu-id="2e566-111">This command gets all the versions of VMImage that match the specified values.</span></span>

### <span data-ttu-id="2e566-112">2. példa: A VMImage objektum lekérte</span><span class="sxs-lookup"><span data-stu-id="2e566-112">Example 2: Get VMImage object</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "MicrosoftWindowsServer" -Offer "windowsserver" -Skus "2012-R2-Datacenter" -Version 4.127.20180315

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/centralus/
                   Publishers/MicrosoftWindowsServer/ArtifactTypes/VMImage/Offers/windowsserver/Skus/2012-R2-Datacenter
                   /Versions/4.127.20180315
Location         : centralus
PublisherName    : MicrosoftWindowsServer
Offer            : windowsserver
Skus             : 2012-R2-Datacenter
Version          : 4.127.20180315
Name             : 4.127.20180315
OSDiskImage      : {
                     "operatingSystem": "Windows"
                   }
PurchasePlan     : null
DataDiskImages   : []
```

<span data-ttu-id="2e566-113">Ez a parancs a VMImage egy adott verzióját kapja meg, amely megfelel a megadott értékeknek.</span><span class="sxs-lookup"><span data-stu-id="2e566-113">This command gets a specific version of VMImage that matches the specified values.</span></span>

### <span data-ttu-id="2e566-114">3. példa: VMImage-objektumok lekérte</span><span class="sxs-lookup"><span data-stu-id="2e566-114">Example 3: Get VMImage objects</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "MicrosoftWindowsServer" -Offer "windowsserver" -Skus "2012-R2-Datacenter" -Version 4.127.2018*

Version        Skus               Offer         PublisherName          Location  Id
-------        ----               -----         -------------          --------  --
4.127.20180315 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180510 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180815 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180912 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181010 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181125 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
```

<span data-ttu-id="2e566-115">Ez a parancs a VMImage minden olyan verzióját beveszi, amely megfelel a megadott értékeknek a verzión keresztüli szűréssel.</span><span class="sxs-lookup"><span data-stu-id="2e566-115">This command gets all the versions of VMImage that match the specified values with filtering over version.</span></span>

## <span data-ttu-id="2e566-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e566-116">PARAMETERS</span></span>

### <span data-ttu-id="2e566-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e566-117">-DefaultProfile</span></span>
<span data-ttu-id="2e566-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2e566-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e566-119">-Location</span><span class="sxs-lookup"><span data-stu-id="2e566-119">-Location</span></span>
<span data-ttu-id="2e566-120">A VMImage-fájl helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2e566-120">Specifies the location of a VMImage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e566-121">-Offer</span><span class="sxs-lookup"><span data-stu-id="2e566-121">-Offer</span></span>
<span data-ttu-id="2e566-122">A VMImage-ajánlat típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="2e566-122">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="2e566-123">Képajánlat beszerzéséhez használja a Get-AzVMImageOffer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="2e566-123">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e566-124">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="2e566-124">-OrderBy</span></span>
<span data-ttu-id="2e566-125">A visszaadott eredmények sorrendjét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="2e566-125">Specifies the order of the results returned.</span></span> <span data-ttu-id="2e566-126">OData-lekérdezésként formázva.</span><span class="sxs-lookup"><span data-stu-id="2e566-126">Formatted as an OData query.</span></span>

```yaml
Type: System.String
Parameter Sets: ListVMImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e566-127">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="2e566-127">-PublisherName</span></span>
<span data-ttu-id="2e566-128">A VMImage-fájl közzétevője.</span><span class="sxs-lookup"><span data-stu-id="2e566-128">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="2e566-129">Képkiadó beszerzéséhez használja a Get-AzVMImagePublisher parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="2e566-129">To obtain an image publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e566-130">-Skus</span><span class="sxs-lookup"><span data-stu-id="2e566-130">-Skus</span></span>
<span data-ttu-id="2e566-131">Egy VMImage-termékváltozatot ad meg.</span><span class="sxs-lookup"><span data-stu-id="2e566-131">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="2e566-132">Termékváltozat beszerzéséhez használja a Get-AzVMImageSku parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="2e566-132">To obtain an SKU, use the Get-AzVMImageSku cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e566-133">-Top</span><span class="sxs-lookup"><span data-stu-id="2e566-133">-Top</span></span>
<span data-ttu-id="2e566-134">A visszaadott virtuális gépi képek maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2e566-134">Specifies the maximum number of virtual machine images returned.</span></span> 

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ListVMImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e566-135">-Version</span><span class="sxs-lookup"><span data-stu-id="2e566-135">-Version</span></span>
<span data-ttu-id="2e566-136">A VMImage verziójának megadása.</span><span class="sxs-lookup"><span data-stu-id="2e566-136">Specifies the version of the VMImage.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVMImageDetail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e566-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e566-137">CommonParameters</span></span>
<span data-ttu-id="2e566-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e566-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e566-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2e566-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e566-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2e566-140">INPUTS</span></span>

### <span data-ttu-id="2e566-141">System.String</span><span class="sxs-lookup"><span data-stu-id="2e566-141">System.String</span></span>

## <span data-ttu-id="2e566-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e566-142">OUTPUTS</span></span>

### <span data-ttu-id="2e566-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span><span class="sxs-lookup"><span data-stu-id="2e566-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span></span>

### <span data-ttu-id="2e566-144">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span><span class="sxs-lookup"><span data-stu-id="2e566-144">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span></span>

## <span data-ttu-id="2e566-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2e566-145">NOTES</span></span>

## <span data-ttu-id="2e566-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2e566-146">RELATED LINKS</span></span>

[<span data-ttu-id="2e566-147">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="2e566-147">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="2e566-148">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="2e566-148">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="2e566-149">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="2e566-149">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="2e566-150">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="2e566-150">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


