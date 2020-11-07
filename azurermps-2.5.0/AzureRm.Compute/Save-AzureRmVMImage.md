---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/save-azurermvmimage
schema: 2.0.0
ms.openlocfilehash: b781023b424dd23d3d0874893b724744ecb33bda
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850909"
---
# <span data-ttu-id="8a4c7-101">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="8a4c7-101">Save-AzureRmVMImage</span></span>

## <span data-ttu-id="8a4c7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8a4c7-102">SYNOPSIS</span></span>
<span data-ttu-id="8a4c7-103">Virtuális gép mentése VMImage.</span><span class="sxs-lookup"><span data-stu-id="8a4c7-103">Saves a virtual machine as a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a4c7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8a4c7-104">SYNTAX</span></span>

### <span data-ttu-id="8a4c7-105">ResourceGroupNameParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8a4c7-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a4c7-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="8a4c7-106">IdParameterSetName</span></span>
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8a4c7-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8a4c7-107">DESCRIPTION</span></span>
<span data-ttu-id="8a4c7-108">A **Save-AzureRmVMImage** parancsmag a virtuális gépet VMImage menti.</span><span class="sxs-lookup"><span data-stu-id="8a4c7-108">The **Save-AzureRmVMImage** cmdlet saves a virtual machine as a VMImage.</span></span>
<span data-ttu-id="8a4c7-109">A virtuálisgép-képek létrehozása előtt a Sysprep a virtuális gépet használja, és a Set-AzureRmVM parancsmaggal jelölje meg.</span><span class="sxs-lookup"><span data-stu-id="8a4c7-109">Before you create a virtual machine image, sysprep the virtual machine, and then mark it as generalized by using the Set-AzureRmVM cmdlet.</span></span>

<span data-ttu-id="8a4c7-110">Ennek a parancsmagnak a kimenete egy JavaScript-objektum típusú (JSON) sablon.</span><span class="sxs-lookup"><span data-stu-id="8a4c7-110">The output of this cmdlet is a JavaScript Object Notation (JSON) template.</span></span>
<span data-ttu-id="8a4c7-111">A virtuális gépeket a rögzített képből is telepítheti.</span><span class="sxs-lookup"><span data-stu-id="8a4c7-111">You can deploy virtual machines from your captured image.</span></span>

## <span data-ttu-id="8a4c7-112">Példák</span><span class="sxs-lookup"><span data-stu-id="8a4c7-112">EXAMPLES</span></span>

### <span data-ttu-id="8a4c7-113">Példa 1: virtuális gép rögzítése</span><span class="sxs-lookup"><span data-stu-id="8a4c7-113">Example 1: Capture a virtual machine</span></span>
```
PS C:\> Set-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzureRmVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

<span data-ttu-id="8a4c7-114">Az első parancs a VirtualMachine07 nevű virtuális gépet általánosként jelöli meg.</span><span class="sxs-lookup"><span data-stu-id="8a4c7-114">The first command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

<span data-ttu-id="8a4c7-115">A második parancs rögzíti a VirtualMachine07 nevű virtuális gépet VMImage.</span><span class="sxs-lookup"><span data-stu-id="8a4c7-115">The second command captures a virtual machine named VirtualMachine07 as a VMImage.</span></span>
<span data-ttu-id="8a4c7-116">A **kimenet** tulajdonság egy JSON-sablont ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="8a4c7-116">The **Output** property returns a JSON template.</span></span>

## <span data-ttu-id="8a4c7-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8a4c7-117">PARAMETERS</span></span>

### <span data-ttu-id="8a4c7-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8a4c7-118">-AsJob</span></span>
<span data-ttu-id="8a4c7-119">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="8a4c7-119">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a4c7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a4c7-120">-DefaultProfile</span></span>
<span data-ttu-id="8a4c7-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8a4c7-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a4c7-122">-DestinationContainerName</span><span class="sxs-lookup"><span data-stu-id="8a4c7-122">-DestinationContainerName</span></span>
<span data-ttu-id="8a4c7-123">A "rendszer" tárolóban lévő tároló nevét adja meg, amelyre a képeket tárolni szeretné.</span><span class="sxs-lookup"><span data-stu-id="8a4c7-123">Specifies the name of a container inside the "system" container that you want to hold your images.</span></span>

<span data-ttu-id="8a4c7-124">Ha a tároló nem létezik, akkor létrejön Önnek.</span><span class="sxs-lookup"><span data-stu-id="8a4c7-124">If the container doesn't exist, it is created for you.</span></span>
<span data-ttu-id="8a4c7-125">A VMImage alkotó virtuális merevlemezek (VHD-EK) a paraméterben megadott tárolóban találhatók.</span><span class="sxs-lookup"><span data-stu-id="8a4c7-125">The virtual hard disks (VHDs) that constitute the VMImage reside in the container that this parameter specifies.</span></span>
<span data-ttu-id="8a4c7-126">Ha a VHD-es merevlemezek több tárolási fiók között oszlanak el, ez a parancsmag egy olyan tárolót hoz létre, amelynek a neve minden tárolási fiókban szerepel.</span><span class="sxs-lookup"><span data-stu-id="8a4c7-126">If the VHDs are spread across multiple storage accounts, this cmdlet creates one container that has this name in each storage account.</span></span>
<span data-ttu-id="8a4c7-127">A mentett kép URL-címe a következőhöz hasonló:</span><span class="sxs-lookup"><span data-stu-id="8a4c7-127">The URL of the saved image is similar to:</span></span> 

<span data-ttu-id="8a4c7-128"> https:// \<storageAccountName\> . blob.Core.Windows.net/System/Microsoft.Compute/images/ \<imagesContainer\> / \<vhdPrefix-osDisk\> . XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX. vhd.</span><span class="sxs-lookup"><span data-stu-id="8a4c7-128">https://\<storageAccountName\>.blob.core.windows.net/system/Microsoft.Compute/Images/\<imagesContainer\>/\<vhdPrefix-osDisk\>.xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.vhd.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a4c7-129">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="8a4c7-129">-Id</span></span>
<span data-ttu-id="8a4c7-130">A virtuális gép erőforrás-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8a4c7-130">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a4c7-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8a4c7-131">-Name</span></span>
<span data-ttu-id="8a4c7-132">Egy nevet ad meg.</span><span class="sxs-lookup"><span data-stu-id="8a4c7-132">Specifies a name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a4c7-133">-Átír</span><span class="sxs-lookup"><span data-stu-id="8a4c7-133">-Overwrite</span></span>
<span data-ttu-id="8a4c7-134">Azt jelzi, hogy ez a parancsmag felülírja azokat a VHD-ket, amelyek azonos előtaggal rendelkeznek a célhely tárolóban.</span><span class="sxs-lookup"><span data-stu-id="8a4c7-134">Indicates that this cmdlet overwrites any VHDs that have the same prefix in the destination container.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a4c7-135">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="8a4c7-135">-Path</span></span>
<span data-ttu-id="8a4c7-136">A virtuális merevlemez elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8a4c7-136">Specifies the path of the VHD.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a4c7-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a4c7-137">-ResourceGroupName</span></span>
<span data-ttu-id="8a4c7-138">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8a4c7-138">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a4c7-139">-VHDNamePrefix</span><span class="sxs-lookup"><span data-stu-id="8a4c7-139">-VHDNamePrefix</span></span>
<span data-ttu-id="8a4c7-140">Annak az előtagnak a neve, amely a VMImage tárolási profilját képezi.</span><span class="sxs-lookup"><span data-stu-id="8a4c7-140">Specifies the prefix in the name of the blobs that constitute the storage profile of the VMImage.</span></span>

<span data-ttu-id="8a4c7-141">Egy operációs rendszerhez használt előtag vhdPrefix például a vhdPrefix- \<guid\> osdisk. VHD.</span><span class="sxs-lookup"><span data-stu-id="8a4c7-141">For example, a prefix vhdPrefix for an operating system disk results in the name vhdPrefix-osdisk.\<guid\>.vhd.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: VirtualHardDiskNamePrefix

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a4c7-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a4c7-142">CommonParameters</span></span>
<span data-ttu-id="8a4c7-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8a4c7-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a4c7-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a4c7-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a4c7-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8a4c7-145">INPUTS</span></span>

### <span data-ttu-id="8a4c7-146">Nincs</span><span class="sxs-lookup"><span data-stu-id="8a4c7-146">None</span></span>
<span data-ttu-id="8a4c7-147">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="8a4c7-147">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8a4c7-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8a4c7-148">OUTPUTS</span></span>

### <span data-ttu-id="8a4c7-149">Microsoft. Azure. commands. kiszámítás. models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="8a4c7-149">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="8a4c7-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8a4c7-150">NOTES</span></span>

## <span data-ttu-id="8a4c7-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8a4c7-151">RELATED LINKS</span></span>

[<span data-ttu-id="8a4c7-152">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="8a4c7-152">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="8a4c7-153">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="8a4c7-153">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="8a4c7-154">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="8a4c7-154">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="8a4c7-155">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="8a4c7-155">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="8a4c7-156">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8a4c7-156">Set-AzureRmVM</span></span>](./Set-AzureRmVM.md)


