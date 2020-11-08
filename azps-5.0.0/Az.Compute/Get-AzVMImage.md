---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImage.md
ms.openlocfilehash: 350e03d6e238eb0cf1aa6b27da6b9a321603a664
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187634"
---
# <span data-ttu-id="2c553-101">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="2c553-101">Get-AzVMImage</span></span>

## <span data-ttu-id="2c553-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2c553-102">SYNOPSIS</span></span>
<span data-ttu-id="2c553-103">Beolvassa a VMImage összes verzióját.</span><span class="sxs-lookup"><span data-stu-id="2c553-103">Gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="2c553-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2c553-104">SYNTAX</span></span>

### <span data-ttu-id="2c553-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="2c553-105">ListVMImage</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> [-Top <Int32>]
 [-OrderBy <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c553-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="2c553-106">GetVMImageDetail</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c553-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2c553-107">DESCRIPTION</span></span>
<span data-ttu-id="2c553-108">A **Get-AzVMImage** parancsmag a VMImage összes verzióját kapja.</span><span class="sxs-lookup"><span data-stu-id="2c553-108">The **Get-AzVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="2c553-109">Példák</span><span class="sxs-lookup"><span data-stu-id="2c553-109">EXAMPLES</span></span>

### <span data-ttu-id="2c553-110">1. példa: VMImage-objektumok beolvasása</span><span class="sxs-lookup"><span data-stu-id="2c553-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "MicrosoftWindowsServer" -Offer "windowsserver" -Skus "2012-R2-Datacenter"

Version        FilterExpression Skus               Offer         PublisherName          Location  Id
-------        ---------------- ----               -----         -------------          --------  --
4.127.20180315                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180510                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180815                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180912                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181010                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181125                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190104                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190115                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190204                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190218                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
```

<span data-ttu-id="2c553-111">Ez a parancs a megadott értékeknek megfelelő VMImage-verziókat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2c553-111">This command gets all the versions of VMImage that match the specified values.</span></span>

### <span data-ttu-id="2c553-112">2. példa: VMImage objektum beolvasása</span><span class="sxs-lookup"><span data-stu-id="2c553-112">Example 2: Get VMImage object</span></span>
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
FilterExpression :
Name             : 4.127.20180315
OSDiskImage      : {
                     "operatingSystem": "Windows"
                   }
PurchasePlan     : null
DataDiskImages   : []
```

<span data-ttu-id="2c553-113">Ez a parancs beolvassa a VMImage egy olyan verzióját, amely megfelel a megadott értékeknek.</span><span class="sxs-lookup"><span data-stu-id="2c553-113">This command gets a specific version of VMImage that matches the specified values.</span></span>

### <span data-ttu-id="2c553-114">3. példa: VMImage-objektumok beolvasása</span><span class="sxs-lookup"><span data-stu-id="2c553-114">Example 3: Get VMImage objects</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "MicrosoftWindowsServer" -Offer "windowsserver" -Skus "2012-R2-Datacenter" -Version 4.127.2018*

Version        FilterExpression Skus               Offer         PublisherName          Location  Id
-------        ---------------- ----               -----         -------------          --------  --
4.127.20180315                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180510                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180815                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180912                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181010                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181125                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
```

<span data-ttu-id="2c553-115">Ez a parancs beolvassa a VMImage összes olyan verzióját, amely megfelel a megadott értékeknek a verzió szerinti szűréssel.</span><span class="sxs-lookup"><span data-stu-id="2c553-115">This command gets all the versions of VMImage that match the specified values with filtering over version.</span></span>

## <span data-ttu-id="2c553-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2c553-116">PARAMETERS</span></span>

### <span data-ttu-id="2c553-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c553-117">-DefaultProfile</span></span>
<span data-ttu-id="2c553-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2c553-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c553-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="2c553-119">-Location</span></span>
<span data-ttu-id="2c553-120">A VMImage helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2c553-120">Specifies the location of a VMImage.</span></span>

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

### <span data-ttu-id="2c553-121">-Ajánlat</span><span class="sxs-lookup"><span data-stu-id="2c553-121">-Offer</span></span>
<span data-ttu-id="2c553-122">A VMImage-ajánlat típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2c553-122">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="2c553-123">Képajánlat beolvasásához használja az Get-AzVMImageOffer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="2c553-123">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="2c553-124">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="2c553-124">-OrderBy</span></span>
<span data-ttu-id="2c553-125">A visszaadott eredmény sorrendjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2c553-125">Specifies the order of the results returned.</span></span> <span data-ttu-id="2c553-126">OData-lekérdezésként van formázva.</span><span class="sxs-lookup"><span data-stu-id="2c553-126">Formatted as an OData query.</span></span>

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

### <span data-ttu-id="2c553-127">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="2c553-127">-PublisherName</span></span>
<span data-ttu-id="2c553-128">A VMImage közzétevőjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2c553-128">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="2c553-129">Képközzétevő beolvasásához használja az Get-AzVMImagePublisher parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="2c553-129">To obtain an image publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="2c553-130">-SKU</span><span class="sxs-lookup"><span data-stu-id="2c553-130">-Skus</span></span>
<span data-ttu-id="2c553-131">Egy VMImage SKU-ot ad meg.</span><span class="sxs-lookup"><span data-stu-id="2c553-131">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="2c553-132">SKU beolvasásához használja az Get-AzVMImageSku parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="2c553-132">To obtain an SKU, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="2c553-133">-Top</span><span class="sxs-lookup"><span data-stu-id="2c553-133">-Top</span></span>
<span data-ttu-id="2c553-134">A virtuális gép által visszaadott képek maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2c553-134">Specifies the maximum number of virtual machine images returned.</span></span> 

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

### <span data-ttu-id="2c553-135">-Verzió</span><span class="sxs-lookup"><span data-stu-id="2c553-135">-Version</span></span>
<span data-ttu-id="2c553-136">A VMImage verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2c553-136">Specifies the version of the VMImage.</span></span>

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

### <span data-ttu-id="2c553-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c553-137">CommonParameters</span></span>
<span data-ttu-id="2c553-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2c553-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c553-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2c553-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c553-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c553-140">INPUTS</span></span>

### <span data-ttu-id="2c553-141">System. String</span><span class="sxs-lookup"><span data-stu-id="2c553-141">System.String</span></span>

## <span data-ttu-id="2c553-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c553-142">OUTPUTS</span></span>

### <span data-ttu-id="2c553-143">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineImage</span><span class="sxs-lookup"><span data-stu-id="2c553-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span></span>

### <span data-ttu-id="2c553-144">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineImageDetail</span><span class="sxs-lookup"><span data-stu-id="2c553-144">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span></span>

## <span data-ttu-id="2c553-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2c553-145">NOTES</span></span>

## <span data-ttu-id="2c553-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2c553-146">RELATED LINKS</span></span>

[<span data-ttu-id="2c553-147">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="2c553-147">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="2c553-148">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="2c553-148">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="2c553-149">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="2c553-149">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="2c553-150">Mentés-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="2c553-150">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


