---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/save-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVMImage.md
ms.openlocfilehash: b663087437097b3e059f9d88c7720696222134e3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836690"
---
# <span data-ttu-id="a452c-101">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="a452c-101">Save-AzVMImage</span></span>

## <span data-ttu-id="a452c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a452c-102">SYNOPSIS</span></span>
<span data-ttu-id="a452c-103">Virtuális gép mentése VMImage.</span><span class="sxs-lookup"><span data-stu-id="a452c-103">Saves a virtual machine as a VMImage.</span></span>

## <span data-ttu-id="a452c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a452c-104">SYNTAX</span></span>

### <span data-ttu-id="a452c-105">ResourceGroupNameParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a452c-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Save-AzVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String> [-Overwrite]
 [[-Path] <String>] [-ResourceGroupName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a452c-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="a452c-106">IdParameterSetName</span></span>
```
Save-AzVMImage [[-Name] <String>] [-DestinationContainerName] <String> [-VHDNamePrefix] <String> [-Overwrite]
 [[-Path] <String>] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a452c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a452c-107">DESCRIPTION</span></span>
<span data-ttu-id="a452c-108">A **Save-AzVMImage** parancsmag a virtuális gépet VMImage menti.</span><span class="sxs-lookup"><span data-stu-id="a452c-108">The **Save-AzVMImage** cmdlet saves a virtual machine as a VMImage.</span></span>
<span data-ttu-id="a452c-109">A virtuálisgép-képek létrehozása előtt a Sysprep a virtuális gépet használja, és a Set-AzVM parancsmaggal jelölje meg.</span><span class="sxs-lookup"><span data-stu-id="a452c-109">Before you create a virtual machine image, sysprep the virtual machine, and then mark it as generalized by using the Set-AzVM cmdlet.</span></span>
<span data-ttu-id="a452c-110">Ennek a parancsmagnak a kimenete egy JavaScript-objektum típusú (JSON) sablon.</span><span class="sxs-lookup"><span data-stu-id="a452c-110">The output of this cmdlet is a JavaScript Object Notation (JSON) template.</span></span>
<span data-ttu-id="a452c-111">A virtuális gépeket a rögzített képből is telepítheti.</span><span class="sxs-lookup"><span data-stu-id="a452c-111">You can deploy virtual machines from your captured image.</span></span>

## <span data-ttu-id="a452c-112">Példák</span><span class="sxs-lookup"><span data-stu-id="a452c-112">EXAMPLES</span></span>

### <span data-ttu-id="a452c-113">Példa 1: virtuális gép rögzítése</span><span class="sxs-lookup"><span data-stu-id="a452c-113">Example 1: Capture a virtual machine</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

<span data-ttu-id="a452c-114">Az első parancs a VirtualMachine07 nevű virtuális gépet általánosként jelöli meg.</span><span class="sxs-lookup"><span data-stu-id="a452c-114">The first command marks the virtual machine named VirtualMachine07 as generalized.</span></span>
<span data-ttu-id="a452c-115">A második parancs rögzíti a VirtualMachine07 nevű virtuális gépet VMImage.</span><span class="sxs-lookup"><span data-stu-id="a452c-115">The second command captures a virtual machine named VirtualMachine07 as a VMImage.</span></span>
<span data-ttu-id="a452c-116">A **kimenet** tulajdonság egy JSON-sablont ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="a452c-116">The **Output** property returns a JSON template.</span></span>

## <span data-ttu-id="a452c-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a452c-117">PARAMETERS</span></span>

### <span data-ttu-id="a452c-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a452c-118">-AsJob</span></span>
<span data-ttu-id="a452c-119">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="a452c-119">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a452c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a452c-120">-DefaultProfile</span></span>
<span data-ttu-id="a452c-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a452c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a452c-122">-DestinationContainerName</span><span class="sxs-lookup"><span data-stu-id="a452c-122">-DestinationContainerName</span></span>
<span data-ttu-id="a452c-123">A "rendszer" tárolóban lévő tároló nevét adja meg, amelyre a képeket tárolni szeretné.</span><span class="sxs-lookup"><span data-stu-id="a452c-123">Specifies the name of a container inside the "system" container that you want to hold your images.</span></span>
<span data-ttu-id="a452c-124">Ha a tároló nem létezik, akkor létrejön Önnek.</span><span class="sxs-lookup"><span data-stu-id="a452c-124">If the container doesn't exist, it is created for you.</span></span>
<span data-ttu-id="a452c-125">A VMImage alkotó virtuális merevlemezek (VHD-EK) a paraméterben megadott tárolóban találhatók.</span><span class="sxs-lookup"><span data-stu-id="a452c-125">The virtual hard disks (VHDs) that constitute the VMImage reside in the container that this parameter specifies.</span></span>
<span data-ttu-id="a452c-126">Ha a VHD-es merevlemezek több tárolási fiók között oszlanak el, ez a parancsmag egy olyan tárolót hoz létre, amelynek a neve minden tárolási fiókban szerepel.</span><span class="sxs-lookup"><span data-stu-id="a452c-126">If the VHDs are spread across multiple storage accounts, this cmdlet creates one container that has this name in each storage account.</span></span>
<span data-ttu-id="a452c-127">A mentett kép URL-címe a következőhöz hasonló: https:// \< storageAccountName \> . blob.Core.Windows.net/System/Microsoft.Compute/images/ \< imagesContainer vhdPrefix. \> / \< \> osDisk. vhd.</span><span class="sxs-lookup"><span data-stu-id="a452c-127">The URL of the saved image is similar to: https://\<storageAccountName\>.blob.core.windows.net/system/Microsoft.Compute/Images/\<imagesContainer\>/\<vhdPrefix-osDisk\>.xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.vhd.</span></span>

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

### <span data-ttu-id="a452c-128">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="a452c-128">-Id</span></span>
<span data-ttu-id="a452c-129">A virtuális gép erőforrás-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a452c-129">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="a452c-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a452c-130">-Name</span></span>
<span data-ttu-id="a452c-131">Egy nevet ad meg.</span><span class="sxs-lookup"><span data-stu-id="a452c-131">Specifies a name.</span></span>

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

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases: VMName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a452c-132">-Átír</span><span class="sxs-lookup"><span data-stu-id="a452c-132">-Overwrite</span></span>
<span data-ttu-id="a452c-133">Azt jelzi, hogy ez a parancsmag felülírja azokat a VHD-ket, amelyek azonos előtaggal rendelkeznek a célhely tárolóban.</span><span class="sxs-lookup"><span data-stu-id="a452c-133">Indicates that this cmdlet overwrites any VHDs that have the same prefix in the destination container.</span></span>

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

### <span data-ttu-id="a452c-134">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="a452c-134">-Path</span></span>
<span data-ttu-id="a452c-135">Annak a fájlnak az elérési útvonala, amelyben a rögzített kép sablonja van tárolva.</span><span class="sxs-lookup"><span data-stu-id="a452c-135">The file path in which the template of the captured image is stored.</span></span>

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

### <span data-ttu-id="a452c-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a452c-136">-ResourceGroupName</span></span>
<span data-ttu-id="a452c-137">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a452c-137">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="a452c-138">-VHDNamePrefix</span><span class="sxs-lookup"><span data-stu-id="a452c-138">-VHDNamePrefix</span></span>
<span data-ttu-id="a452c-139">Annak az előtagnak a neve, amely a VMImage tárolási profilját képezi.</span><span class="sxs-lookup"><span data-stu-id="a452c-139">Specifies the prefix in the name of the blobs that constitute the storage profile of the VMImage.</span></span>
<span data-ttu-id="a452c-140">Egy operációs rendszerhez használt előtag vhdPrefix például a vhdPrefix-osdisk nevet adja eredményül. \< GUID \> . vhd.</span><span class="sxs-lookup"><span data-stu-id="a452c-140">For example, a prefix vhdPrefix for an operating system disk results in the name vhdPrefix-osdisk.\<guid\>.vhd.</span></span>

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

### <span data-ttu-id="a452c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a452c-141">CommonParameters</span></span>
<span data-ttu-id="a452c-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a452c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a452c-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a452c-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a452c-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a452c-144">INPUTS</span></span>

### <span data-ttu-id="a452c-145">System. String</span><span class="sxs-lookup"><span data-stu-id="a452c-145">System.String</span></span>

### <span data-ttu-id="a452c-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a452c-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a452c-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a452c-147">OUTPUTS</span></span>

### <span data-ttu-id="a452c-148">Microsoft. Azure. commands. kiszámítás. models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="a452c-148">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="a452c-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a452c-149">NOTES</span></span>

## <span data-ttu-id="a452c-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a452c-150">RELATED LINKS</span></span>

[<span data-ttu-id="a452c-151">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="a452c-151">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="a452c-152">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="a452c-152">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="a452c-153">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="a452c-153">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="a452c-154">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="a452c-154">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="a452c-155">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="a452c-155">Set-AzVM</span></span>](./Set-AzVM.md)


