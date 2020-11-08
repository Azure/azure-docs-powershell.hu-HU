---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImage.md
ms.openlocfilehash: d5fd6e6dea5af9ed3d8bc02e69f155e74a4bb3f5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012885"
---
# <span data-ttu-id="056e3-101">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="056e3-101">Get-AzVMImage</span></span>

## <span data-ttu-id="056e3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="056e3-102">SYNOPSIS</span></span>
<span data-ttu-id="056e3-103">Beolvassa a VMImage összes verzióját.</span><span class="sxs-lookup"><span data-stu-id="056e3-103">Gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="056e3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="056e3-104">SYNTAX</span></span>

### <span data-ttu-id="056e3-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="056e3-105">ListVMImage</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="056e3-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="056e3-106">GetVMImageDetail</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="056e3-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="056e3-107">DESCRIPTION</span></span>
<span data-ttu-id="056e3-108">A **Get-AzVMImage** parancsmag a VMImage összes verzióját kapja.</span><span class="sxs-lookup"><span data-stu-id="056e3-108">The **Get-AzVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="056e3-109">Példák</span><span class="sxs-lookup"><span data-stu-id="056e3-109">EXAMPLES</span></span>

### <span data-ttu-id="056e3-110">1. példa: VMImage-objektumok beolvasása</span><span class="sxs-lookup"><span data-stu-id="056e3-110">Example 1: Get VMImage objects</span></span>
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

<span data-ttu-id="056e3-111">Ez a parancs a megadott értékeknek megfelelő VMImage-verziókat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="056e3-111">This command gets all the versions of VMImage that match the specified values.</span></span>

### <span data-ttu-id="056e3-112">2. példa: VMImage objektum beolvasása</span><span class="sxs-lookup"><span data-stu-id="056e3-112">Example 2: Get VMImage object</span></span>
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

<span data-ttu-id="056e3-113">Ez a parancs beolvassa a VMImage egy olyan verzióját, amely megfelel a megadott értékeknek.</span><span class="sxs-lookup"><span data-stu-id="056e3-113">This command gets a specific version of VMImage that matches the specified values.</span></span>

### <span data-ttu-id="056e3-114">3. példa: VMImage-objektumok beolvasása</span><span class="sxs-lookup"><span data-stu-id="056e3-114">Example 3: Get VMImage objects</span></span>
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

<span data-ttu-id="056e3-115">Ez a parancs beolvassa a VMImage összes olyan verzióját, amely megfelel a megadott értékeknek a verzió szerinti szűréssel.</span><span class="sxs-lookup"><span data-stu-id="056e3-115">This command gets all the versions of VMImage that match the specified values with filtering over version.</span></span>

## <span data-ttu-id="056e3-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="056e3-116">PARAMETERS</span></span>

### <span data-ttu-id="056e3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="056e3-117">-DefaultProfile</span></span>
<span data-ttu-id="056e3-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="056e3-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="056e3-119">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="056e3-119">-FilterExpression</span></span>
<span data-ttu-id="056e3-120">A szűrő kifejezését adja meg.</span><span class="sxs-lookup"><span data-stu-id="056e3-120">Specifies a filter expression.</span></span>

```yaml
Type: System.String
Parameter Sets: ListVMImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="056e3-121">-Hely</span><span class="sxs-lookup"><span data-stu-id="056e3-121">-Location</span></span>
<span data-ttu-id="056e3-122">A VMImage helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="056e3-122">Specifies the location of a VMImage.</span></span>

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

### <span data-ttu-id="056e3-123">-Ajánlat</span><span class="sxs-lookup"><span data-stu-id="056e3-123">-Offer</span></span>
<span data-ttu-id="056e3-124">A VMImage-ajánlat típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="056e3-124">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="056e3-125">Képajánlat beolvasásához használja az Get-AzVMImageOffer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="056e3-125">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="056e3-126">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="056e3-126">-PublisherName</span></span>
<span data-ttu-id="056e3-127">A VMImage közzétevőjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="056e3-127">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="056e3-128">Képközzétevő beolvasásához használja az Get-AzVMImagePublisher parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="056e3-128">To obtain an image publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="056e3-129">-SKU</span><span class="sxs-lookup"><span data-stu-id="056e3-129">-Skus</span></span>
<span data-ttu-id="056e3-130">Egy VMImage SKU-ot ad meg.</span><span class="sxs-lookup"><span data-stu-id="056e3-130">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="056e3-131">SKU beolvasásához használja az Get-AzVMImageSku parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="056e3-131">To obtain an SKU, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="056e3-132">-Verzió</span><span class="sxs-lookup"><span data-stu-id="056e3-132">-Version</span></span>
<span data-ttu-id="056e3-133">A VMImage verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="056e3-133">Specifies the version of the VMImage.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVMImageDetail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="056e3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="056e3-134">CommonParameters</span></span>
<span data-ttu-id="056e3-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="056e3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="056e3-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="056e3-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="056e3-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="056e3-137">INPUTS</span></span>

### <span data-ttu-id="056e3-138">System. String</span><span class="sxs-lookup"><span data-stu-id="056e3-138">System.String</span></span>

## <span data-ttu-id="056e3-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="056e3-139">OUTPUTS</span></span>

### <span data-ttu-id="056e3-140">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineImage</span><span class="sxs-lookup"><span data-stu-id="056e3-140">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span></span>

### <span data-ttu-id="056e3-141">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineImageDetail</span><span class="sxs-lookup"><span data-stu-id="056e3-141">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span></span>

## <span data-ttu-id="056e3-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="056e3-142">NOTES</span></span>

## <span data-ttu-id="056e3-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="056e3-143">RELATED LINKS</span></span>

[<span data-ttu-id="056e3-144">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="056e3-144">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="056e3-145">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="056e3-145">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="056e3-146">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="056e3-146">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="056e3-147">Mentés-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="056e3-147">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


