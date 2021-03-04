---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 91B2DE2F-442D-4428-8A6F-9C2CEC181CA7
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmsourceimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSourceImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSourceImage.md
ms.openlocfilehash: ac02e3c54500e1ba104c4deb323bb7257fa3e71b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935282"
---
# <span data-ttu-id="f6f30-101">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="f6f30-101">Set-AzVMSourceImage</span></span>

## <span data-ttu-id="f6f30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6f30-102">SYNOPSIS</span></span>
<span data-ttu-id="f6f30-103">Egy virtuális gép képét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f6f30-103">Specifies the image for a virtual machine.</span></span>

## <span data-ttu-id="f6f30-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f6f30-104">SYNTAX</span></span>

### <span data-ttu-id="f6f30-105">ImageReferenceSkuParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f6f30-105">ImageReferenceSkuParameterSet (Default)</span></span>
```
Set-AzVMSourceImage [-VM] <PSVirtualMachine> [-PublisherName] <String> [-Offer] <String> [-Skus] <String>
 [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6f30-106">ImageReferenceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6f30-106">ImageReferenceIdParameterSet</span></span>
```
Set-AzVMSourceImage [-VM] <PSVirtualMachine> [-Id] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f6f30-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f6f30-107">DESCRIPTION</span></span>
<span data-ttu-id="f6f30-108">A **Set-AzVMSourceImage parancsmag** megadja a virtuális géphez használt platformképet.</span><span class="sxs-lookup"><span data-stu-id="f6f30-108">The **Set-AzVMSourceImage** cmdlet specifies the platform image to use for a virtual machine.</span></span>

## <span data-ttu-id="f6f30-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f6f30-109">EXAMPLES</span></span>

### <span data-ttu-id="f6f30-110">1. példa: Kép értékeinek beállítása</span><span class="sxs-lookup"><span data-stu-id="f6f30-110">Example 1: Set values for an image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzVMSourceImage -VM $VirtualMachine -PublisherName "MicrosoftWindowsServer" -Offer "WindowsServer" -Skus "2012-R2-Datacenter" -Version "latest"
```

<span data-ttu-id="f6f30-111">Az első parancs az Erőforráscsoport11 erőforráscsoportBan az AvailabilitySet03 nevű elérhetőségi halmazt kapja, majd az objektumot a $AvailabilitySet tárolja.</span><span class="sxs-lookup"><span data-stu-id="f6f30-111">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="f6f30-112">A második parancs létrehoz egy virtuális gépobjektumot, majd a $VirtualMachine tárolja.</span><span class="sxs-lookup"><span data-stu-id="f6f30-112">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="f6f30-113">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="f6f30-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="f6f30-114">A virtuális gép a 2016-ban tárolt rendelkezésre állási $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="f6f30-114">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="f6f30-115">A végleges parancs beállítja a közzétevő nevét, ajánlatát, termékváltozatát és verzióját.</span><span class="sxs-lookup"><span data-stu-id="f6f30-115">The final command sets values for publisher name, offer, SKU, and version.</span></span>
<span data-ttu-id="f6f30-116">Ezeket a beállításokat a **Get-AzVMImagePublisher,** **a Get-AzVMImageOffer,** a **Get-AzVMImageSku** és a **Get-AzVMImage** parancsmagok is felfedezhetik.</span><span class="sxs-lookup"><span data-stu-id="f6f30-116">The **Get-AzVMImagePublisher**, **Get-AzVMImageOffer**, **Get-AzVMImageSku**, and **Get-AzVMImage** cmdlets can discover these settings.</span></span>

## <span data-ttu-id="f6f30-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f6f30-117">PARAMETERS</span></span>

### <span data-ttu-id="f6f30-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6f30-118">-DefaultProfile</span></span>
<span data-ttu-id="f6f30-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f6f30-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6f30-120">-Id</span><span class="sxs-lookup"><span data-stu-id="f6f30-120">-Id</span></span>
<span data-ttu-id="f6f30-121">Az azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="f6f30-121">Specifies the ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ImageReferenceIdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6f30-122">-Offer</span><span class="sxs-lookup"><span data-stu-id="f6f30-122">-Offer</span></span>
<span data-ttu-id="f6f30-123">A VMImage-ajánlat típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="f6f30-123">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="f6f30-124">Képajánlat beszerzéséhez használja a Get-AzVMImageOffer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="f6f30-124">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6f30-125">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="f6f30-125">-PublisherName</span></span>
<span data-ttu-id="f6f30-126">Egy VMImage-közzétevő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f6f30-126">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="f6f30-127">Közzétevő beszerzéséhez használja a Get-AzVMImagePublisher parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="f6f30-127">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6f30-128">-Skus</span><span class="sxs-lookup"><span data-stu-id="f6f30-128">-Skus</span></span>
<span data-ttu-id="f6f30-129">Egy VMImage-termékváltozatot ad meg.</span><span class="sxs-lookup"><span data-stu-id="f6f30-129">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="f6f30-130">Az SKUs-k beszerzéséhez használja a Get-AzVMImageSku parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="f6f30-130">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6f30-131">-Version</span><span class="sxs-lookup"><span data-stu-id="f6f30-131">-Version</span></span>
<span data-ttu-id="f6f30-132">Egy VMImage-verzió megadása.</span><span class="sxs-lookup"><span data-stu-id="f6f30-132">Specifies a version of a VMImage.</span></span>
<span data-ttu-id="f6f30-133">A legújabb verzió csak akkor használható, ha az adott verzió helyett a legújabb értéket adja meg.</span><span class="sxs-lookup"><span data-stu-id="f6f30-133">To use the latest version, specify a value of latest instead of a particular version.</span></span>

```yaml
Type: System.String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6f30-134">-VM</span><span class="sxs-lookup"><span data-stu-id="f6f30-134">-VM</span></span>
<span data-ttu-id="f6f30-135">A konfigurálni megfelelő helyi virtuális gépobjektum.</span><span class="sxs-lookup"><span data-stu-id="f6f30-135">Specifies the local virtual machine object to configure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6f30-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6f30-136">CommonParameters</span></span>
<span data-ttu-id="f6f30-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6f30-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6f30-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f6f30-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6f30-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f6f30-139">INPUTS</span></span>

### <span data-ttu-id="f6f30-140">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="f6f30-140">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="f6f30-141">System.String</span><span class="sxs-lookup"><span data-stu-id="f6f30-141">System.String</span></span>

## <span data-ttu-id="f6f30-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6f30-142">OUTPUTS</span></span>

### <span data-ttu-id="f6f30-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="f6f30-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="f6f30-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f6f30-144">NOTES</span></span>

## <span data-ttu-id="f6f30-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f6f30-145">RELATED LINKS</span></span>

[<span data-ttu-id="f6f30-146">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f6f30-146">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="f6f30-147">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="f6f30-147">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="f6f30-148">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="f6f30-148">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="f6f30-149">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="f6f30-149">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="f6f30-150">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="f6f30-150">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="f6f30-151">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="f6f30-151">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


