---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Save-AzureRmVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Save-AzureRmVMImage.md
ms.openlocfilehash: cadcaccc2bb93dee5298ca92561c5bef36b5d9ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505147"
---
# <span data-ttu-id="45fe2-101">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="45fe2-101">Save-AzureRmVMImage</span></span>

## <span data-ttu-id="45fe2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="45fe2-102">SYNOPSIS</span></span>
<span data-ttu-id="45fe2-103">Virtuális gép mentése VMImage.</span><span class="sxs-lookup"><span data-stu-id="45fe2-103">Saves a virtual machine as a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45fe2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="45fe2-104">SYNTAX</span></span>

### <span data-ttu-id="45fe2-105">ResourceGroupNameParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="45fe2-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="45fe2-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="45fe2-106">IdParameterSetName</span></span>
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45fe2-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="45fe2-107">DESCRIPTION</span></span>
<span data-ttu-id="45fe2-108">A **Save-AzureRmVMImage** parancsmag a virtuális gépet VMImage menti.</span><span class="sxs-lookup"><span data-stu-id="45fe2-108">The **Save-AzureRmVMImage** cmdlet saves a virtual machine as a VMImage.</span></span>
<span data-ttu-id="45fe2-109">A virtuálisgép-képek létrehozása előtt a Sysprep a virtuális gépet használja, és a Set-AzureRmVM parancsmaggal jelölje meg.</span><span class="sxs-lookup"><span data-stu-id="45fe2-109">Before you create a virtual machine image, sysprep the virtual machine, and then mark it as generalized by using the Set-AzureRmVM cmdlet.</span></span>

<span data-ttu-id="45fe2-110">Ennek a parancsmagnak a kimenete egy JavaScript-objektum típusú (JSON) sablon.</span><span class="sxs-lookup"><span data-stu-id="45fe2-110">The output of this cmdlet is a JavaScript Object Notation (JSON) template.</span></span>
<span data-ttu-id="45fe2-111">A virtuális gépeket a rögzített képből is telepítheti.</span><span class="sxs-lookup"><span data-stu-id="45fe2-111">You can deploy virtual machines from your captured image.</span></span>

## <span data-ttu-id="45fe2-112">Példák</span><span class="sxs-lookup"><span data-stu-id="45fe2-112">EXAMPLES</span></span>

### <span data-ttu-id="45fe2-113">Példa 1: virtuális gép rögzítése</span><span class="sxs-lookup"><span data-stu-id="45fe2-113">Example 1: Capture a virtual machine</span></span>
```
PS C:\> Set-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzureRmVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

<span data-ttu-id="45fe2-114">Az első parancs a VirtualMachine07 nevű virtuális gépet általánosként jelöli meg.</span><span class="sxs-lookup"><span data-stu-id="45fe2-114">The first command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

<span data-ttu-id="45fe2-115">A második parancs rögzíti a VirtualMachine07 nevű virtuális gépet VMImage.</span><span class="sxs-lookup"><span data-stu-id="45fe2-115">The second command captures a virtual machine named VirtualMachine07 as a VMImage.</span></span>
<span data-ttu-id="45fe2-116">A **kimenet** tulajdonság egy JSON-sablont ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="45fe2-116">The **Output** property returns a JSON template.</span></span>

## <span data-ttu-id="45fe2-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="45fe2-117">PARAMETERS</span></span>

### <span data-ttu-id="45fe2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45fe2-118">-DefaultProfile</span></span>
<span data-ttu-id="45fe2-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="45fe2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45fe2-120">-DestinationContainerName</span><span class="sxs-lookup"><span data-stu-id="45fe2-120">-DestinationContainerName</span></span>
<span data-ttu-id="45fe2-121">A "rendszer" tárolóban lévő tároló nevét adja meg, amelyre a képeket tárolni szeretné.</span><span class="sxs-lookup"><span data-stu-id="45fe2-121">Specifies the name of a container inside the "system" container that you want to hold your images.</span></span>

<span data-ttu-id="45fe2-122">Ha a tároló nem létezik, akkor létrejön Önnek.</span><span class="sxs-lookup"><span data-stu-id="45fe2-122">If the container doesn't exist, it is created for you.</span></span>
<span data-ttu-id="45fe2-123">A VMImage alkotó virtuális merevlemezek (VHD-EK) a paraméterben megadott tárolóban találhatók.</span><span class="sxs-lookup"><span data-stu-id="45fe2-123">The virtual hard disks (VHDs) that constitute the VMImage reside in the container that this parameter specifies.</span></span>
<span data-ttu-id="45fe2-124">Ha a VHD-es merevlemezek több tárolási fiók között oszlanak el, ez a parancsmag egy olyan tárolót hoz létre, amelynek a neve minden tárolási fiókban szerepel.</span><span class="sxs-lookup"><span data-stu-id="45fe2-124">If the VHDs are spread across multiple storage accounts, this cmdlet creates one container that has this name in each storage account.</span></span>
<span data-ttu-id="45fe2-125">A mentett kép URL-címe a következőhöz hasonló:</span><span class="sxs-lookup"><span data-stu-id="45fe2-125">The URL of the saved image is similar to:</span></span> 

<span data-ttu-id="45fe2-126"> https:// \<storageAccountName\> . blob.Core.Windows.net/System/Microsoft.Compute/images/ \<imagesContainer\> / \<vhdPrefix-osDisk\> . XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX. vhd.</span><span class="sxs-lookup"><span data-stu-id="45fe2-126">https://\<storageAccountName\>.blob.core.windows.net/system/Microsoft.Compute/Images/\<imagesContainer\>/\<vhdPrefix-osDisk\>.xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.vhd.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45fe2-127">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="45fe2-127">-Id</span></span>
<span data-ttu-id="45fe2-128">A virtuális gép erőforrás-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="45fe2-128">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45fe2-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="45fe2-129">-Name</span></span>
<span data-ttu-id="45fe2-130">Egy nevet ad meg.</span><span class="sxs-lookup"><span data-stu-id="45fe2-130">Specifies a name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45fe2-131">-Átír</span><span class="sxs-lookup"><span data-stu-id="45fe2-131">-Overwrite</span></span>
<span data-ttu-id="45fe2-132">Azt jelzi, hogy ez a parancsmag felülírja azokat a VHD-ket, amelyek azonos előtaggal rendelkeznek a célhely tárolóban.</span><span class="sxs-lookup"><span data-stu-id="45fe2-132">Indicates that this cmdlet overwrites any VHDs that have the same prefix in the destination container.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45fe2-133">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="45fe2-133">-Path</span></span>
<span data-ttu-id="45fe2-134">A virtuális merevlemez elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="45fe2-134">Specifies the path of the VHD.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45fe2-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45fe2-135">-ResourceGroupName</span></span>
<span data-ttu-id="45fe2-136">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="45fe2-136">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45fe2-137">-VHDNamePrefix</span><span class="sxs-lookup"><span data-stu-id="45fe2-137">-VHDNamePrefix</span></span>
<span data-ttu-id="45fe2-138">Annak az előtagnak a neve, amely a VMImage tárolási profilját képezi.</span><span class="sxs-lookup"><span data-stu-id="45fe2-138">Specifies the prefix in the name of the blobs that constitute the storage profile of the VMImage.</span></span>

<span data-ttu-id="45fe2-139">Egy operációs rendszerhez használt előtag vhdPrefix például a vhdPrefix- \<guid\> osdisk. VHD.</span><span class="sxs-lookup"><span data-stu-id="45fe2-139">For example, a prefix vhdPrefix for an operating system disk results in the name vhdPrefix-osdisk.\<guid\>.vhd.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VirtualHardDiskNamePrefix

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45fe2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45fe2-140">CommonParameters</span></span>
<span data-ttu-id="45fe2-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="45fe2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45fe2-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45fe2-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45fe2-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="45fe2-143">INPUTS</span></span>

## <span data-ttu-id="45fe2-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="45fe2-144">OUTPUTS</span></span>

## <span data-ttu-id="45fe2-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="45fe2-145">NOTES</span></span>

## <span data-ttu-id="45fe2-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="45fe2-146">RELATED LINKS</span></span>

[<span data-ttu-id="45fe2-147">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="45fe2-147">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="45fe2-148">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="45fe2-148">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="45fe2-149">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="45fe2-149">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="45fe2-150">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="45fe2-150">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="45fe2-151">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="45fe2-151">Set-AzureRmVM</span></span>](./Set-AzureRmVM.md)

