---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/save-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVMImage.md
ms.openlocfilehash: 0d2a4ade662ec23a4a139460bce8fe5387683120
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480729"
---
# <span data-ttu-id="c4c5c-101">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="c4c5c-101">Save-AzVMImage</span></span>

## <span data-ttu-id="c4c5c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4c5c-102">SYNOPSIS</span></span>
<span data-ttu-id="c4c5c-103">Virtuális gépet ment VMImage-fájlként.</span><span class="sxs-lookup"><span data-stu-id="c4c5c-103">Saves a virtual machine as a VMImage.</span></span>

## <span data-ttu-id="c4c5c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c4c5c-104">SYNTAX</span></span>

### <span data-ttu-id="c4c5c-105">ResourceGroupNameParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c4c5c-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Save-AzVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String> [-Overwrite]
 [[-Path] <String>] [-ResourceGroupName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c4c5c-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="c4c5c-106">IdParameterSetName</span></span>
```
Save-AzVMImage [-DestinationContainerName] <String> [-VHDNamePrefix] <String> [-Overwrite] [[-Path] <String>]
 [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4c5c-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c4c5c-107">DESCRIPTION</span></span>
<span data-ttu-id="c4c5c-108">A **Save-AzVMImage** parancsmag virtuális gépet ment VMImage-fájlként.</span><span class="sxs-lookup"><span data-stu-id="c4c5c-108">The **Save-AzVMImage** cmdlet saves a virtual machine as a VMImage.</span></span>
<span data-ttu-id="c4c5c-109">Mielőtt létrehoz egy virtuális gépi képet, készítse elő a virtuális gépet, majd jelölje meg általánosítottként a Set-AzVM parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="c4c5c-109">Before you create a virtual machine image, sysprep the virtual machine, and then mark it as generalized by using the Set-AzVM cmdlet.</span></span>
<span data-ttu-id="c4c5c-110">A parancsmag kimenete egy JavaScript-objektum-notation (JSON) sablon.</span><span class="sxs-lookup"><span data-stu-id="c4c5c-110">The output of this cmdlet is a JavaScript Object Notation (JSON) template.</span></span>
<span data-ttu-id="c4c5c-111">Virtuális gépeket telepíthet a rögzített képből.</span><span class="sxs-lookup"><span data-stu-id="c4c5c-111">You can deploy virtual machines from your captured image.</span></span>

## <span data-ttu-id="c4c5c-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c4c5c-112">EXAMPLES</span></span>

### <span data-ttu-id="c4c5c-113">1. példa: Virtuális gép rögzítése</span><span class="sxs-lookup"><span data-stu-id="c4c5c-113">Example 1: Capture a virtual machine</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

<span data-ttu-id="c4c5c-114">Az első parancs általánosítottként jelöli meg a VirtualMachine07 nevű virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="c4c5c-114">The first command marks the virtual machine named VirtualMachine07 as generalized.</span></span>
<span data-ttu-id="c4c5c-115">A második parancs egy VirtualMachine07 nevű virtuális gépet rögzít VMImage-ként.</span><span class="sxs-lookup"><span data-stu-id="c4c5c-115">The second command captures a virtual machine named VirtualMachine07 as a VMImage.</span></span>
<span data-ttu-id="c4c5c-116">A **Kimeneti tulajdonság** egy JSON-sablont ad vissza.</span><span class="sxs-lookup"><span data-stu-id="c4c5c-116">The **Output** property returns a JSON template.</span></span>

## <span data-ttu-id="c4c5c-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4c5c-117">PARAMETERS</span></span>

### <span data-ttu-id="c4c5c-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c4c5c-118">-AsJob</span></span>
<span data-ttu-id="c4c5c-119">Futtasa a parancsmagot a háttérben, és adja vissza a feladatot az előrehaladás nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="c4c5c-119">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4c5c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4c5c-120">-DefaultProfile</span></span>
<span data-ttu-id="c4c5c-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c4c5c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4c5c-122">-DestinationContainerName</span><span class="sxs-lookup"><span data-stu-id="c4c5c-122">-DestinationContainerName</span></span>
<span data-ttu-id="c4c5c-123">Annak a tárolónak a nevét adja meg a "rendszer" tárolón belül, amelybe a képeket helyezni szeretné.</span><span class="sxs-lookup"><span data-stu-id="c4c5c-123">Specifies the name of a container inside the "system" container that you want to hold your images.</span></span>
<span data-ttu-id="c4c5c-124">Ha a tároló nem létezik, akkor az Ön számára jön létre.</span><span class="sxs-lookup"><span data-stu-id="c4c5c-124">If the container doesn't exist, it is created for you.</span></span>
<span data-ttu-id="c4c5c-125">A VMImage-tárolót alkotó virtuális merevlemezek (VHD-k) a paraméter által megadott tárolóban találhatók.</span><span class="sxs-lookup"><span data-stu-id="c4c5c-125">The virtual hard disks (VHDs) that constitute the VMImage reside in the container that this parameter specifies.</span></span>
<span data-ttu-id="c4c5c-126">Ha a VHD-eket több tárfiókban is elterjed, ez a parancsmag létrehoz egy tárolót, amely mindegyik tárfiókban ezt a nevet tárolja.</span><span class="sxs-lookup"><span data-stu-id="c4c5c-126">If the VHDs are spread across multiple storage accounts, this cmdlet creates one container that has this name in each storage account.</span></span>
<span data-ttu-id="c4c5c-127">A mentett kép URL-címe a következő: https:// \<storageAccountName\> .blob.core.windows.net/system/Microsoft.Compute/Images/ \<imagesContainer\> / \<vhdPrefix-osDisk\> .xxxxxxxx-xxxx-xxxxxx.vhd.</span><span class="sxs-lookup"><span data-stu-id="c4c5c-127">The URL of the saved image is similar to: https://\<storageAccountName\>.blob.core.windows.net/system/Microsoft.Compute/Images/\<imagesContainer\>/\<vhdPrefix-osDisk\>.xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.vhd.</span></span>

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

### <span data-ttu-id="c4c5c-128">-Id</span><span class="sxs-lookup"><span data-stu-id="c4c5c-128">-Id</span></span>
<span data-ttu-id="c4c5c-129">A virtuális gép erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c4c5c-129">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="c4c5c-130">-Name</span><span class="sxs-lookup"><span data-stu-id="c4c5c-130">-Name</span></span>
<span data-ttu-id="c4c5c-131">Egy nevet ad meg.</span><span class="sxs-lookup"><span data-stu-id="c4c5c-131">Specifies a name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4c5c-132">-Felülírás</span><span class="sxs-lookup"><span data-stu-id="c4c5c-132">-Overwrite</span></span>
<span data-ttu-id="c4c5c-133">Azt jelzi, hogy ez a parancsmag felülír minden olyan VHD-t, amely a céltárolóban azonos előtaggal van megrendelve.</span><span class="sxs-lookup"><span data-stu-id="c4c5c-133">Indicates that this cmdlet overwrites any VHDs that have the same prefix in the destination container.</span></span>

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

### <span data-ttu-id="c4c5c-134">-Path</span><span class="sxs-lookup"><span data-stu-id="c4c5c-134">-Path</span></span>
<span data-ttu-id="c4c5c-135">Az a fájl elérési útja, amelyben a rögzített kép sablonja található.</span><span class="sxs-lookup"><span data-stu-id="c4c5c-135">The file path in which the template of the captured image is stored.</span></span>

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

### <span data-ttu-id="c4c5c-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4c5c-136">-ResourceGroupName</span></span>
<span data-ttu-id="c4c5c-137">A virtuális gép erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c4c5c-137">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="c4c5c-138">-VHDNamePrefix</span><span class="sxs-lookup"><span data-stu-id="c4c5c-138">-VHDNamePrefix</span></span>
<span data-ttu-id="c4c5c-139">A VMImage tárolóprofilját megfedő blobok nevében megadja az előtagot.</span><span class="sxs-lookup"><span data-stu-id="c4c5c-139">Specifies the prefix in the name of the blobs that constitute the storage profile of the VMImage.</span></span>
<span data-ttu-id="c4c5c-140">Egy operációs rendszer lemezének előtagja például a vhdPrefix-osdisk. nevet ad. \<guid\> vhd.</span><span class="sxs-lookup"><span data-stu-id="c4c5c-140">For example, a prefix vhdPrefix for an operating system disk results in the name vhdPrefix-osdisk.\<guid\>.vhd.</span></span>

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

### <span data-ttu-id="c4c5c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4c5c-141">CommonParameters</span></span>
<span data-ttu-id="c4c5c-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4c5c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4c5c-143">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c4c5c-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4c5c-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c4c5c-144">INPUTS</span></span>

### <span data-ttu-id="c4c5c-145">System.String</span><span class="sxs-lookup"><span data-stu-id="c4c5c-145">System.String</span></span>

### <span data-ttu-id="c4c5c-146">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c4c5c-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c4c5c-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4c5c-147">OUTPUTS</span></span>

### <span data-ttu-id="c4c5c-148">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="c4c5c-148">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="c4c5c-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c4c5c-149">NOTES</span></span>

## <span data-ttu-id="c4c5c-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c4c5c-150">RELATED LINKS</span></span>

[<span data-ttu-id="c4c5c-151">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="c4c5c-151">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="c4c5c-152">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="c4c5c-152">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="c4c5c-153">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="c4c5c-153">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="c4c5c-154">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="c4c5c-154">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="c4c5c-155">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="c4c5c-155">Set-AzVM</span></span>](./Set-AzVM.md)


