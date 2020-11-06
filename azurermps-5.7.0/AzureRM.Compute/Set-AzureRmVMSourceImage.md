---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 91B2DE2F-442D-4428-8A6F-9C2CEC181CA7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMSourceImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMSourceImage.md
ms.openlocfilehash: d96d583f871e0d037c72018339d44952562bac35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493173"
---
# <span data-ttu-id="eb484-101">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="eb484-101">Set-AzureRmVMSourceImage</span></span>

## <span data-ttu-id="eb484-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eb484-102">SYNOPSIS</span></span>
<span data-ttu-id="eb484-103">A virtuális gép képét adja meg.</span><span class="sxs-lookup"><span data-stu-id="eb484-103">Specifies the image for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb484-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eb484-104">SYNTAX</span></span>

### <span data-ttu-id="eb484-105">ImageReferenceSkuParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="eb484-105">ImageReferenceSkuParameterSet (Default)</span></span>
```
Set-AzureRmVMSourceImage [-VM] <PSVirtualMachine> [-PublisherName] <String> [-Offer] <String> [-Skus] <String>
 [-Version] <String> [<CommonParameters>]
```

### <span data-ttu-id="eb484-106">ImageReferenceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb484-106">ImageReferenceIdParameterSet</span></span>
```
Set-AzureRmVMSourceImage [-VM] <PSVirtualMachine> [-Id] <String> [<CommonParameters>]
```

## <span data-ttu-id="eb484-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="eb484-107">DESCRIPTION</span></span>
<span data-ttu-id="eb484-108">A **set-AzureRmVMSourceImage** parancsmag a virtuális gépekhez használni kívánt platform képét adja meg.</span><span class="sxs-lookup"><span data-stu-id="eb484-108">The **Set-AzureRmVMSourceImage** cmdlet specifies the platform image to use for a virtual machine.</span></span>

## <span data-ttu-id="eb484-109">Példák</span><span class="sxs-lookup"><span data-stu-id="eb484-109">EXAMPLES</span></span>

### <span data-ttu-id="eb484-110">1. példa: a képek értékeinek beállítása</span><span class="sxs-lookup"><span data-stu-id="eb484-110">Example 1: Set values for an image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzureRmVMSourceImage -VM $VirtualMachine -PublisherName "MicrosoftWindowsServer" -Offer "WindowsServer" -Skus "2012-R2-Datacenter" -Version "latest"
```

<span data-ttu-id="eb484-111">Az első parancs beolvassa a AvailablitySet03 nevű ResourceGroup11 nevű erőforráscsoport elérhetőségi készletét, majd a $AvailabilitySet változóban tárolja az objektumot.</span><span class="sxs-lookup"><span data-stu-id="eb484-111">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="eb484-112">A második parancs létrehoz egy Virtual Machine-objektumot, majd a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="eb484-112">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="eb484-113">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="eb484-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="eb484-114">A virtuális gép a $AvailabilitySetban tárolt elérhetőségi készlethez tartozik.</span><span class="sxs-lookup"><span data-stu-id="eb484-114">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="eb484-115">A végleges parancs a Publisher-név, az ajánlat, a SKU és a verzió értékeit állítja be.</span><span class="sxs-lookup"><span data-stu-id="eb484-115">The final command sets values for publisher name, offer, SKU, and version.</span></span>
<span data-ttu-id="eb484-116">A **Get-AzureRmVMImagePublisher** , a **Get-AzureRmVMImageOffer** , a Get- **AzureRmVMImageSku** és a Get- **AzureRmVMImage** parancsmagok felfedezhetik ezeket a beállításokat.</span><span class="sxs-lookup"><span data-stu-id="eb484-116">The **Get-AzureRmVMImagePublisher** , **Get-AzureRmVMImageOffer** , **Get-AzureRmVMImageSku** , and **Get-AzureRmVMImage** cmdlets can discover these settings.</span></span>

## <span data-ttu-id="eb484-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eb484-117">PARAMETERS</span></span>

### <span data-ttu-id="eb484-118">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="eb484-118">-Id</span></span>
<span data-ttu-id="eb484-119">Az azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="eb484-119">Specifies the ID.</span></span>

```yaml
Type: String
Parameter Sets: ImageReferenceIdParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb484-120">-Ajánlat</span><span class="sxs-lookup"><span data-stu-id="eb484-120">-Offer</span></span>
<span data-ttu-id="eb484-121">A VMImage-ajánlat típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="eb484-121">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="eb484-122">Képajánlat beolvasásához használja az Get-AzureRmVMImageOffer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="eb484-122">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb484-123">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="eb484-123">-PublisherName</span></span>
<span data-ttu-id="eb484-124">A VMImage közzétevő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="eb484-124">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="eb484-125">Publisher beolvasásához használja az Get-AzureRmVMImagePublisher parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="eb484-125">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb484-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="eb484-126">-Skus</span></span>
<span data-ttu-id="eb484-127">Egy VMImage SKU-ot ad meg.</span><span class="sxs-lookup"><span data-stu-id="eb484-127">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="eb484-128">A SKU beolvasásához használja az Get-AzureRmVMImageSku parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="eb484-128">To obtain SKUs, use the Get-AzureRmVMImageSku cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb484-129">-Verzió</span><span class="sxs-lookup"><span data-stu-id="eb484-129">-Version</span></span>
<span data-ttu-id="eb484-130">A VMImage verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="eb484-130">Specifies a version of a VMImage.</span></span>
<span data-ttu-id="eb484-131">A legújabb verzió használatához adjon meg egy új értéket az adott verzió helyett.</span><span class="sxs-lookup"><span data-stu-id="eb484-131">To use the latest version, specify a value of latest instead of a particular version.</span></span>

```yaml
Type: String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb484-132">-VM</span><span class="sxs-lookup"><span data-stu-id="eb484-132">-VM</span></span>
<span data-ttu-id="eb484-133">A konfigurálandó helyi virtuális gép objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="eb484-133">Specifies the local virtual machine object to configure.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb484-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb484-134">CommonParameters</span></span>
<span data-ttu-id="eb484-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eb484-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb484-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb484-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb484-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb484-137">INPUTS</span></span>

### <span data-ttu-id="eb484-138">Nincs</span><span class="sxs-lookup"><span data-stu-id="eb484-138">None</span></span>
<span data-ttu-id="eb484-139">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="eb484-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="eb484-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb484-140">OUTPUTS</span></span>

## <span data-ttu-id="eb484-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eb484-141">NOTES</span></span>

## <span data-ttu-id="eb484-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eb484-142">RELATED LINKS</span></span>

[<span data-ttu-id="eb484-143">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="eb484-143">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="eb484-144">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="eb484-144">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="eb484-145">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="eb484-145">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="eb484-146">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="eb484-146">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="eb484-147">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="eb484-147">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="eb484-148">Új – AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="eb484-148">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


