---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 91B2DE2F-442D-4428-8A6F-9C2CEC181CA7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMSourceImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMSourceImage.md
ms.openlocfilehash: 88b8af8cd16ab4868a10c5ff1aa3759a6d771a6e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492503"
---
# <span data-ttu-id="09901-101">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="09901-101">Set-AzureRmVMSourceImage</span></span>

## <span data-ttu-id="09901-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="09901-102">SYNOPSIS</span></span>
<span data-ttu-id="09901-103">A virtuális gép képét adja meg.</span><span class="sxs-lookup"><span data-stu-id="09901-103">Specifies the image for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09901-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="09901-104">SYNTAX</span></span>

### <span data-ttu-id="09901-105">ImageReferenceSkuParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="09901-105">ImageReferenceSkuParameterSet (Default)</span></span>
```
Set-AzureRmVMSourceImage [-VM] <PSVirtualMachine> [-PublisherName] <String> [-Offer] <String> [-Skus] <String>
 [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09901-106">ImageReferenceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="09901-106">ImageReferenceIdParameterSet</span></span>
```
Set-AzureRmVMSourceImage [-VM] <PSVirtualMachine> [-Id] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="09901-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="09901-107">DESCRIPTION</span></span>
<span data-ttu-id="09901-108">A **set-AzureRmVMSourceImage** parancsmag a virtuális gépekhez használni kívánt platform képét adja meg.</span><span class="sxs-lookup"><span data-stu-id="09901-108">The **Set-AzureRmVMSourceImage** cmdlet specifies the platform image to use for a virtual machine.</span></span>

## <span data-ttu-id="09901-109">Példák</span><span class="sxs-lookup"><span data-stu-id="09901-109">EXAMPLES</span></span>

### <span data-ttu-id="09901-110">1. példa: a képek értékeinek beállítása</span><span class="sxs-lookup"><span data-stu-id="09901-110">Example 1: Set values for an image</span></span>
```
PS C:\> AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzureRmVMSourceImage -VM $VirtualMachine -PublisherName "MicrosoftWindowsServer" -Offer "WindowsServer" -Skus "2012-R2-Datacenter" -Version "latest"
```

<span data-ttu-id="09901-111">Az első parancs beolvassa a AvailablitySet03 nevű ResourceGroup11 nevű erőforráscsoport elérhetőségi készletét, majd a $AvailabilitySet változóban tárolja az objektumot.</span><span class="sxs-lookup"><span data-stu-id="09901-111">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="09901-112">A második parancs létrehoz egy Virtual Machine-objektumot, majd a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="09901-112">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="09901-113">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="09901-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="09901-114">A virtuális gép a $AvailabilitySetban tárolt elérhetőségi készlethez tartozik.</span><span class="sxs-lookup"><span data-stu-id="09901-114">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="09901-115">A végleges parancs a Publisher-név, az ajánlat, a SKU és a verzió értékeit állítja be.</span><span class="sxs-lookup"><span data-stu-id="09901-115">The final command sets values for publisher name, offer, SKU, and version.</span></span>
<span data-ttu-id="09901-116">A **Get-AzureRmVMImagePublisher** , a **Get-AzureRmVMImageOffer** , a Get- **AzureRmVMImageSku** és a Get- **AzureRmVMImage** parancsmagok felfedezhetik ezeket a beállításokat.</span><span class="sxs-lookup"><span data-stu-id="09901-116">The **Get-AzureRmVMImagePublisher** , **Get-AzureRmVMImageOffer** , **Get-AzureRmVMImageSku** , and **Get-AzureRmVMImage** cmdlets can discover these settings.</span></span>

## <span data-ttu-id="09901-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="09901-117">PARAMETERS</span></span>

### <span data-ttu-id="09901-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09901-118">-DefaultProfile</span></span>
<span data-ttu-id="09901-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="09901-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09901-120">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="09901-120">-Id</span></span>
<span data-ttu-id="09901-121">Az azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="09901-121">Specifies the ID.</span></span>

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

### <span data-ttu-id="09901-122">-Ajánlat</span><span class="sxs-lookup"><span data-stu-id="09901-122">-Offer</span></span>
<span data-ttu-id="09901-123">A VMImage-ajánlat típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="09901-123">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="09901-124">Képajánlat beolvasásához használja az Get-AzureRmVMImageOffer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="09901-124">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="09901-125">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="09901-125">-PublisherName</span></span>
<span data-ttu-id="09901-126">A VMImage közzétevő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="09901-126">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="09901-127">Publisher beolvasásához használja az Get-AzureRmVMImagePublisher parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="09901-127">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="09901-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="09901-128">-Skus</span></span>
<span data-ttu-id="09901-129">Egy VMImage SKU-ot ad meg.</span><span class="sxs-lookup"><span data-stu-id="09901-129">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="09901-130">A SKU beolvasásához használja az Get-AzureRmVMImageSku parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="09901-130">To obtain SKUs, use the Get-AzureRmVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="09901-131">-Verzió</span><span class="sxs-lookup"><span data-stu-id="09901-131">-Version</span></span>
<span data-ttu-id="09901-132">A VMImage verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="09901-132">Specifies a version of a VMImage.</span></span>
<span data-ttu-id="09901-133">A legújabb verzió használatához adjon meg egy új értéket az adott verzió helyett.</span><span class="sxs-lookup"><span data-stu-id="09901-133">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="09901-134">-VM</span><span class="sxs-lookup"><span data-stu-id="09901-134">-VM</span></span>
<span data-ttu-id="09901-135">A konfigurálandó helyi virtuális gép objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="09901-135">Specifies the local virtual machine object to configure.</span></span>

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

### <span data-ttu-id="09901-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09901-136">CommonParameters</span></span>
<span data-ttu-id="09901-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="09901-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09901-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09901-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09901-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="09901-139">INPUTS</span></span>

## <span data-ttu-id="09901-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="09901-140">OUTPUTS</span></span>

## <span data-ttu-id="09901-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="09901-141">NOTES</span></span>

## <span data-ttu-id="09901-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="09901-142">RELATED LINKS</span></span>

[<span data-ttu-id="09901-143">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="09901-143">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="09901-144">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="09901-144">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="09901-145">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="09901-145">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="09901-146">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="09901-146">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="09901-147">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="09901-147">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="09901-148">Új – AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="09901-148">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


