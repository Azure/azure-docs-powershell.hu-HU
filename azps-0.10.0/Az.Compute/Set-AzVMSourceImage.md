---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 91B2DE2F-442D-4428-8A6F-9C2CEC181CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsourceimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMSourceImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMSourceImage.md
ms.openlocfilehash: 88a6431d0a59c4dcd875abb0569a0280325cda18
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844197"
---
# <span data-ttu-id="496c0-101">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="496c0-101">Set-AzVMSourceImage</span></span>

## <span data-ttu-id="496c0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="496c0-102">SYNOPSIS</span></span>
<span data-ttu-id="496c0-103">A virtuális gép képét adja meg.</span><span class="sxs-lookup"><span data-stu-id="496c0-103">Specifies the image for a virtual machine.</span></span>

## <span data-ttu-id="496c0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="496c0-104">SYNTAX</span></span>

### <span data-ttu-id="496c0-105">ImageReferenceSkuParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="496c0-105">ImageReferenceSkuParameterSet (Default)</span></span>
```
Set-AzVMSourceImage [-VM] <PSVirtualMachine> [-PublisherName] <String> [-Offer] <String> [-Skus] <String>
 [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="496c0-106">ImageReferenceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="496c0-106">ImageReferenceIdParameterSet</span></span>
```
Set-AzVMSourceImage [-VM] <PSVirtualMachine> [-Id] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="496c0-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="496c0-107">DESCRIPTION</span></span>
<span data-ttu-id="496c0-108">A **set-AzVMSourceImage** parancsmag a virtuális gépekhez használni kívánt platform képét adja meg.</span><span class="sxs-lookup"><span data-stu-id="496c0-108">The **Set-AzVMSourceImage** cmdlet specifies the platform image to use for a virtual machine.</span></span>

## <span data-ttu-id="496c0-109">Példák</span><span class="sxs-lookup"><span data-stu-id="496c0-109">EXAMPLES</span></span>

### <span data-ttu-id="496c0-110">1. példa: a képek értékeinek beállítása</span><span class="sxs-lookup"><span data-stu-id="496c0-110">Example 1: Set values for an image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzVMSourceImage -VM $VirtualMachine -PublisherName "MicrosoftWindowsServer" -Offer "WindowsServer" -Skus "2012-R2-Datacenter" -Version "latest"
```

<span data-ttu-id="496c0-111">Az első parancs beolvassa a AvailablitySet03 nevű ResourceGroup11 nevű erőforráscsoport elérhetőségi készletét, majd a $AvailabilitySet változóban tárolja az objektumot.</span><span class="sxs-lookup"><span data-stu-id="496c0-111">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="496c0-112">A második parancs létrehoz egy Virtual Machine-objektumot, majd a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="496c0-112">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="496c0-113">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="496c0-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="496c0-114">A virtuális gép a $AvailabilitySetban tárolt elérhetőségi készlethez tartozik.</span><span class="sxs-lookup"><span data-stu-id="496c0-114">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="496c0-115">A végleges parancs a Publisher-név, az ajánlat, a SKU és a verzió értékeit állítja be.</span><span class="sxs-lookup"><span data-stu-id="496c0-115">The final command sets values for publisher name, offer, SKU, and version.</span></span>
<span data-ttu-id="496c0-116">A **Get-AzVMImagePublisher** , a **Get-AzVMImageOffer** , a Get- **AzVMImageSku** és a Get- **AzVMImage** parancsmagok felfedezhetik ezeket a beállításokat.</span><span class="sxs-lookup"><span data-stu-id="496c0-116">The **Get-AzVMImagePublisher** , **Get-AzVMImageOffer** , **Get-AzVMImageSku** , and **Get-AzVMImage** cmdlets can discover these settings.</span></span>

## <span data-ttu-id="496c0-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="496c0-117">PARAMETERS</span></span>

### <span data-ttu-id="496c0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="496c0-118">-DefaultProfile</span></span>
<span data-ttu-id="496c0-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="496c0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="496c0-120">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="496c0-120">-Id</span></span>
<span data-ttu-id="496c0-121">Az azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="496c0-121">Specifies the ID.</span></span>

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

### <span data-ttu-id="496c0-122">-Ajánlat</span><span class="sxs-lookup"><span data-stu-id="496c0-122">-Offer</span></span>
<span data-ttu-id="496c0-123">A VMImage-ajánlat típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="496c0-123">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="496c0-124">Képajánlat beolvasásához használja az Get-AzVMImageOffer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="496c0-124">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="496c0-125">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="496c0-125">-PublisherName</span></span>
<span data-ttu-id="496c0-126">A VMImage közzétevő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="496c0-126">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="496c0-127">Publisher beolvasásához használja az Get-AzVMImagePublisher parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="496c0-127">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="496c0-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="496c0-128">-Skus</span></span>
<span data-ttu-id="496c0-129">Egy VMImage SKU-ot ad meg.</span><span class="sxs-lookup"><span data-stu-id="496c0-129">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="496c0-130">A SKU beolvasásához használja az Get-AzVMImageSku parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="496c0-130">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="496c0-131">-Verzió</span><span class="sxs-lookup"><span data-stu-id="496c0-131">-Version</span></span>
<span data-ttu-id="496c0-132">A VMImage verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="496c0-132">Specifies a version of a VMImage.</span></span>
<span data-ttu-id="496c0-133">A legújabb verzió használatához adjon meg egy új értéket az adott verzió helyett.</span><span class="sxs-lookup"><span data-stu-id="496c0-133">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="496c0-134">-VM</span><span class="sxs-lookup"><span data-stu-id="496c0-134">-VM</span></span>
<span data-ttu-id="496c0-135">A konfigurálandó helyi virtuális gép objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="496c0-135">Specifies the local virtual machine object to configure.</span></span>

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

### <span data-ttu-id="496c0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="496c0-136">CommonParameters</span></span>
<span data-ttu-id="496c0-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="496c0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="496c0-138">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="496c0-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="496c0-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="496c0-139">INPUTS</span></span>

### <span data-ttu-id="496c0-140">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="496c0-140">PSVirtualMachine</span></span>
<span data-ttu-id="496c0-141">A ' VM ' paraméter elfogadja a "PSVirtualMachine" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="496c0-141">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="496c0-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="496c0-142">OUTPUTS</span></span>

### <span data-ttu-id="496c0-143">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="496c0-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="496c0-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="496c0-144">NOTES</span></span>

## <span data-ttu-id="496c0-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="496c0-145">RELATED LINKS</span></span>

[<span data-ttu-id="496c0-146">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="496c0-146">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="496c0-147">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="496c0-147">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="496c0-148">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="496c0-148">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="496c0-149">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="496c0-149">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="496c0-150">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="496c0-150">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="496c0-151">Új – AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="496c0-151">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


